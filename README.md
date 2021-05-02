# Apache Avro.





## Contents at a Glance.
* [About.](#about)
* [Documentation.](#documentation)
* [Others useful topics.]()
  * [JavaScript Object Notation.](https://github.com/descriptions-of-it-technologies/json)
* [Help.](#help)





## About.





## Documentation.





## An evolution of data Avro.
* Avro is defined by a schema (schema is written in JSON)
* To get started, you can view Avro as JSON with a schema attached to it.





## 
* Avro has schema and has preloaded.




## Pros.
* Data is fully typed. 
* Data is compressed automatically (less CPU usage).
* Schema (defined useing JSON) comes along the data.
* Documentation is embedded in the schema.
* Data can be red across any languages.
* Schema can evolve over time, in a safe manner (schema evolution)





## Cons.
* Avro support from some languages may be lacking (but the main ones is fine)
* Can't print the data without using the Avro tools (because is compressed and serialized)





## Avro vs Protobuf vs Thrift vs Parquet vs ORC vs ...
* Overall, all of these data formats archive pretty much the same goal.
* At Kafka's level, what we care about is one message being self explicit and full described as we're dealing with streaming (so no RPC, Parquet, etc)
* Avro has good support from Hadoop based technologies like Hive
* Avro has ben chosen as the only supported data format from Confluent Schema Registry so well just go along with that.
* There is no need compare performance etc unless you can prove that Avro is indeed a performance roadblock in your programs
  (and that won't happen unless you reach insane volumes of one million messages per second)




## Help.



```
