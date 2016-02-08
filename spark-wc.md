Python word count 
----------------------

```python
el_quijote = sc.textFile("el-quijote.txt")
counts = el_quijote.flatMap(lambda line: line.split(" ")).map(lambda word: (word, 1)).reduceByKey(lambda a, b: a + b)
counts.saveAsTextFile("spark-wc")
```