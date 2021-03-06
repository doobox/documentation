**super**: **[BaseDataSet](BaseDataSet.md)**

This class is reserved and cannot be directly instantiated.

A RecordSet is a data structure that consists of a group of database records, and can either come from a base table or as the result of a query to the table. At any time, the RecordSet object refers to only a single record within the set as the current record, use the MoveTo method to change current record position.
Rows and columns are 0-based indexed.

### Events

* **DidStart**()
Event raised when DataSet started retrieving data.

* **NewValue**(**value**: **[Object](../gravity/types.md)**)
Event raised when a new value becomes available.

* **DidFinish**()
Event raised when DataSet finished retrieving data.

* **DidFail**()
Event raised in case of DataSet error.



### Properties

* **var** **sql**: **[String](../gravity/types.md)**
Use to this property to retrieve or set current sql statement.

* **var** **hasRow**: **[Bool](../gravity/types.md)**
Check if RecordSet has a row ready to be read. \(read-only\)

* **var** **rowCount**: **[Int](../gravity/types.md)**
Number of rows in the RecordSet. \(read-only\)

* **var** **columnCount**: **[Int](../gravity/types.md)**
Number of columns in the RecordSet. \(read-only\)

* **var** **objectName**: **[String](../gravity/types.md)**
The name of the object.



### Methods

* **func** **run**()
Perform the query specified in the current RecordSet (specified by the sql property). Each control which uses this RecordSet for it <code>dataSet</code> property is notified when new rows are available and when the run is completed, and updates itself to show the new data. This method automatically connects the parent <a href="Database.html">Database</a> instance if needed.

* **func** **columnType**(**index**: **[Int](../gravity/types.md)**): <strong><a href="#_enum_DatabaseFieldType">DatabaseFieldType</a></strong> 
Returns column type specified by the index parameter.

* **func** **columnName**(**index**: **[Int](../gravity/types.md)**): <strong>[String](../gravity/types.md)</strong> 
Returns column name specified by the index parameter.

* **func** **stringValue**(**index**: **[Int](../gravity/types.md)**): <strong>[String](../gravity/types.md)</strong> 
Returns column value converted to String specified by the index parameter.

* **func** **intValue**(**index**: **[Int](../gravity/types.md)**): <strong>[Int](../gravity/types.md)</strong> 
Returns column value converted to Int32 specified by the index parameter.

* **func** **int64Value**(**index**: **[Int](../gravity/types.md)**): <strong>[Int](../gravity/types.md)</strong> 
Returns column value converted to Int64 specified by the index parameter.

* **func** **floatValue**(**index**: **[Int](../gravity/types.md)**): <strong>[Float](../gravity/types.md)</strong> 
Returns column value converted to Float specified by the index parameter.

* **func** **doubleValue**(**index**: **[Int](../gravity/types.md)**): <strong>[Float](../gravity/types.md)</strong> 
Returns column value converted to Double specified by the index parameter.

* **func** **boolValue**(**index**: **[Int](../gravity/types.md)**): <strong>[Bool](../gravity/types.md)</strong> 
Returns column value converted to Boolean specified by the index parameter.

* **func** **blobValue**(**index**: **[Int](../gravity/types.md)**): <strong>[Data](Data.md)</strong> 
Returns column value (not converted) specified by the index parameter.

* **func** **isCached**(): <strong>[Bool](../gravity/types.md)</strong> 
Check if RecordSet is actually in cache (and moveTo method can be used).

* **func** **moveTo**(**index**: **[Int](../gravity/types.md)**): <strong>[Bool](../gravity/types.md)</strong> 
Move current record pointer specified by the index parameter. Returns true is operation succedd.

* **func** **moveNext**(): <strong>[Bool](../gravity/types.md)</strong> 
Move to the next record. Returns false is no more records are availables.

* **func** **moveFirst**(): <strong>[Bool](../gravity/types.md)</strong> 
Move to the first record.

* **func** **moveLast**(): <strong>[Bool](../gravity/types.md)</strong> 
Move to the latest record.

* **func** **movePrevious**(): <strong>[Bool](../gravity/types.md)</strong> 
Move to the previous record. Returns false is no more records are availables.





### Enumeration

#### DatabaseFieldType
 * .Blob
 * .DateTime
 * .Decimal
 * .Double
 * .Integer
 * .Null
 * .Text



