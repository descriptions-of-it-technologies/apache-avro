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
* Don't store secrets in Avro.



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



## Avro primitive types.
* null
* boolean
* integer 
* long 
* bytes
* string 
* float
* double



## Avro complex types.
* Enums
  * Note: once an enum is set, changing the enum values is forbidden if you want to mantain compatibility.
* Arrays
* Maps
* Unions
  * Unions can allow a field value to take different types.
  * If defaults are defined, the default must be of the type of the first item in the union.
  * The most common use for unions is to define an optional value. 
  * Note: for the default don't write `"null"`, write `null` without quotes.
* Calling other schemas as type.



## Avro logical types.
* decimals
* date 
* time-millis
* timestamp-millis



## Help.
