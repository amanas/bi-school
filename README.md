BigData and hadoop module of escuela-bi
=======================================
An introduction to BigData with hadoop - cloudera suite focused

Example's dataset
-----------------
[here](https://github.com/gclaramunt/el-quijote-spark/blob/master/el-quijote.txt)

Requirements
------------
A running instance of [cloudera QuickStart VM](http://www.cloudera.com/downloads/quickstart_vms/5-4.html)

Index
-----
1. Intro to BigData 
    * data vs big data
    * [intro](http://www.slideshare.net/hemapani/introduction-to-big-data)
    * [intro 2](http://www.slideshare.net/nasrinhussain1/big-data-ppt-31616290)
    * [quotes](http://www.slideshare.net/BernardMarr/big-data-best-quotes/7-You_can_have_datawithout_information)
2. Map/reduce
    * [intro/pseudoc�digo/python](http://www.slideshare.net/JeffPatti/map-reducebeyondwordcount)
    * [ex: discuss together a minimal wc ex]
3. Hadoop - YARN
    * [home](http://hadoop.apache.org/) and [doc](http://hadoop.apache.org/docs/current/)
    * [intro](todo)
    * [hdfs commands](http://hadoop.apache.org/docs/current/hadoop-project-dist/hadoop-hdfs/HDFSCommands.html)
    * ex: copy dataset to hdfs
4. Suites hadoop  	
    * [cloudera](http://cloudera.com/)
    	* look at [QuickStart VM](http://www.cloudera.com/get-started/cloudera-live.html) and [install it](http://www.cloudera.com/downloads/quickstart_vms/5-4.html)
    	* live HUE demo [registering](http://go.cloudera.com/hue-demo) or [without registration](http://demo.gethue.com/) - quite limited and slow 
    * [BigInsights](http://www.ibm.com/analytics/us/en/technology/hadoop/)
    * [hortonworks](http://hortonworks.com/)
5. Virtualizaci�n hadoop 
    * [AWS - EMR](https://aws.amazon.com/elasticmapreduce/)
    * [Bluemix] - virtualizaci�n de BigInsights
    * [Google Cloud Platform](https://cloud.google.com/hadoop/)
6. Suite Cloudera 
    * [home]
    * [intro]
    * [virtual box]
7. Frameworks map/reduce 
    1. Mapreduce - java api 
        * [home](http://hadoop.apache.org/docs/current2/hadoop-mapreduce-client/hadoop-mapreduce-client-core/MapReduceTutorial.html)
        * [ex: word count +/- histogram] 
        * [package and submit] 
        * On top of it
        	[cascading]
        	[cascalog]        
    2. Mapreduce - python api 
        * [home](http://hadoop.apache.org/docs/current2/hadoop-streaming/HadoopStreaming.html)
        * ex:  word count - the first in the document (no python) 
    3. Pig
		* [home]
		* [intro]
		* [sintaxis]
		* [ex: word count +/- histogram]
	4. Hive
		* [home]
		* [intro]
		* [sintaxis]
		* [ex: external table +/- histogram]
	5. Spark
		* [home]
		* [intro]
		* [python api + python repl]
		* [ex: python repl wordcount]
		    Optional - scala repl
8. Databases for Hadoop
	1. Impala - MPP
		* [home]
		* [ex: externa table +/- histograma]
	2. Bigsql	
		* [home]
9. Key/value stores
	1. Hbase
		* [home]
		* [intro]
		* [shell commands]
	2. Cassandra
		* [home]
10. Others  
	1. Phoenix
		* [home]
		* [intro]
	2. Kafka 
		* [home]
		* [intro]
	3. Sqoop
		* [home]
		* [cloudera example link]

  
TODOs
-----  
* seleccionar las mejores diapositivas
* preparar los scripts
* preparar proyecto maven para hadoop mapreduce java api
* probar la m�quina virtual y comprobar que trae todos los servicio necesarios
* seguir de principio a fin todos los ejemplos comprobando que funcionan  