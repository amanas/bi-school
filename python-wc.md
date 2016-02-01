Map reduce with python 
----------------------

mapper.py

```python
#!/usr/bin/env python
import sys
 
#--- get all lines from stdin ---
for line in sys.stdin:
    #--- remove leading and trailing whitespace---
    line = line.strip()

    #--- split the line into words ---
    words = line.split()

    #--- output tuples [word, 1] in tab-delimited format---
    for word in words: 
        print '%s\t%s' % (word, "1")
```

reducer.py

```python
#!/usr/bin/env python
import sys
 
# maps words to their counts
word2count = {}
 
# input comes from STDIN
for line in sys.stdin:
    # remove leading and trailing whitespace
    line = line.strip()
 
    # parse the input we got from mapper.py
    word, count = line.split('\t', 1)
    # convert count (currently a string) to int
    try:
        count = int(count)
    except ValueError:
        continue

    try:
        word2count[word] = word2count[word]+count
    except:
        word2count[word] = count
 
# write the tuples to stdout
# Note: they are unsorted
for word in word2count.keys():
    print '%s\t%s'% ( word, word2count[word] )
```

and run it

```sh
hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-streaming-2.6.0-mr1-cdh5.5.1.jar \
-input el-quijote.txt \
-output el-quijote-wc-python \
-mapper mapper.py \
-reducer reducer.py \
-file mapper.py \
-file reducer.py
```