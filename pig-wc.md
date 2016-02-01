Map reduce with Pig 
----------------------

```pig
a = load 'el-quijote.txt';
b = foreach a generate flatten(TOKENIZE((chararray)$0)) as word;
c = group b by word;
d = foreach c generate group, COUNT(b);
store d into 'el-quijote-wc-pig';
```