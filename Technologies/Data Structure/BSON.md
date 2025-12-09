**BSON** stands for **Binary JSON**, it is a binary-encoded serialization of [[JSON]]-like documents.

**BSON** is designed to be lightweight, traversable and efficient. It supports additional data types beyond what [[JSON]] offers, such as `int32`, ``int64``, ``double``, ``decimal128``, ``date``, ``objectId`` and more. This mas BSON suitable for complex data structures and specialized applications like financial systems.

#### Example
Consider the following [[JSON]] document:
```JSON
{
   "hello": "world"
}
```

Its BSON equivalent would be:
```BSON
\x16\x00\x00\x00 // Size of the Document
\x02 // 0x02 = type String
hello\x00 // field name
\x06\x00\x00\x00world\x00 // field value
\x00 // End of object
```
This example illustrates how BSON encodes type and length information, making it easier for machines to parse

#### Differences Between BSON and JSON
- **Encoding**: **[[JSON]]** is plain text, while **BSON** is binary-encoded
- **Data Types**: **BSON** supports additional data types like _Date_, _Binary_, _ObjectId_, and _Decimal128_
- **Size**: **BSON** is typically smaller due to binary encoding, but it may be slightly larger than **[[JSON]]** due to length prefixes
- **Efficiency**: **BSON** is more efficient for storage and transmission
- **Human Readability**: **[[JSON]]** is more human-readable compared to **BSON**

#### Conclusion
BSON is a powerful and efficient format for storing and transmitting data, especially in applications that require complex data structures and high precision. Its binary encoding and support for additional data types make it a preferred choice for databases like [[MongoDB]]