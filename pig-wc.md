Map reduce with Pig 
----------------------

<!-- ```pig
<!-- 
a = load 'el-quijote.txt' AS (line:chararray);
b = foreach a generate flatten(TOKENIZE(line)) as word;
c = group b by word;
d = foreach c generate group, COUNT(b);
store d into 'el-quijote-wc-pig';
```

Remember to use the illustrate function