Hive word count 
----------------------
```sql
 
DROP TABLE IF EXISTS el_quijote;

CREATE EXTERNAL TABLE IF NOT EXISTS el_quijote (line string)
ROW FORMAT DELIMITED FIELDS TERMINATED BY '\n'
STORED AS TEXTFILE                                              
LOCATION '/user/amanas/el-quijote-hive';

DROP TABLE IF EXISTS tmp_words;
CREATE TABLE tmp_words
AS SELECT explode(split(line, ' ')) AS word FROM el_quijote;

INSERT OVERWRITE DIRECTORY '/user/amanas/hive-wc' 
SELECT word,count(1) AS count FROM tmp_words GROUP BY word;
```