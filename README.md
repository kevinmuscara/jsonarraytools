# JSON Tools
Easy to use functions for handling JSON objects and arrays. Documentation provided below.

## isArrayEqualToValue
Arguments: `(array, value)`

```js
require("jsonarraytools").isArrayEqualToValue(["foo", "foo"], "foo"); 
require("jsonarraytools").isArrayEqualToValue(["foo", "bar"], "bar");
```
Response
```js
true
false
```

## isArrayEqual
Arguments: `(arrays...)`
```js
require("jsonarraytools").isArrayEqual([1, 1, 1, 1]);
require("jsonarraytools").isArrayEqual([1, 2, 3, 4]);
```
Response
```js
true
false
```

## checkArrayByCriteria
Arguments: `(array, criteria)`
```js
require("jsonarraytools").checkArrayByCriteria([10, 20, 30], v => v > 25);
require("jsonarraytools").checkArrayByCriteria([10, 20, 30], v => v > 100);
```
Response
```js
true
false
```

## arrayIsNotEmpty
Arguments: `(arrays...)`
```js
require("jsonarraytools").arrayIsNotEmpty([1, 2, 3]);
require("jsonarraytools").arrayIsNotEmpty([]);
```
Response
```js
true
false
```

## isArraySubset
Arguments: `(arrays...)`
```js
require("jsonarraytools").isArraySubset([1, 2], [1, 3, 2]);
require("jsonarraytools").isArraySubset([1, 2, 5], [1, 2, 3 ,4]);
```
Response
```js
true
false
```

## isArray
Arguments: `(array)`
```js
require("jsonarraytools").isArray(["1"]);
require("jsonarraytools").isArray({ "1": "1" });
```
Response
```js
true
false
```

## compareArrays
Arguments: `(arrays...)`
```js
require("jsonarraytools").compareArrays([1, 2, 3], [3, 1, 2]);
require("jsonarraytools").compareArrays([1, 2, 3], [1, "2", 3]);
```
Response
```js
true
false
```

## convertArrayToObject
Arguments: `(array, key)`
```js
require("jsonarraytools").convertArrayToObject([{ name: "Michael", email: "michael.scott@dundermifflin.com", password: "ilovehollyflax"}, { name: "Toby", email: "toby.flenderson@dundermufflin.com", password: "whydoesnooneloveme"}], "email");
```
Response
```json
{
	"michael.scott@dundermufflin.com": {
		name: "Michael",
		email: "michael.scott@dundermifflin.com",
		password: "ilovehollyflax"
	},
	"toby.flenderson@dundermufflin.com": {
		name: "Toby",
		email: "toby.flenderson@dundermufflin.com",
		password: "whydoesnooneloveme"
	}
}
```

## convertArrayOfStringsToNumber
Arguments: `(array)`
```js
require("jsonarraytools").convertArrayOfStringsToNumber(["2", "3", "4"]);
```
Response
```json
[ 2, 3, 4 ]
```

## createCumulativeArray
Arguments: `(array)`
```js
require("jsonarraytools").createCumulativeArray([1, 2, 3]);
```
Response
```json
[ 1, 3, 6 ]
```

## createArrayInRange
Arguments: `(min, max)`
```js
require("jsonarraytools").createArrayInRange(0, 10);
```
Response
```json
[ 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 ]
```

## emptyArray
```js
let array = ["1", "2"];
console.log(array);
array = require("jsonarraytools").emptyArray(array);
console.log(array)
```
Response
```json
["1", "2"]
[]
```

## closetNumberToValue
Arguments: `(array, number)`
```js
require("jsonarraytools").closetNumberToValue([10, 20, 30], 12); 
```
Response
```json
10
```

## findLongestString
Arguments: `(array)`
```js
require("jsonarraytools").findLongestString(["find", "the", "longest", "string"]); 
```
Response
```json
7
```

## findMaxItemInArray
Arguments: `(array)`
```js
require("jsonarraytools").findMaxItemInArray([1, 100])
```
Response
```json
100
```

## findMinItemInArray
Arguments: `(array)`
```js
require("jsonarraytools").findMinItemInArray([1, 100])
```
Response
```json
1
```

## flattenArray
Arguments: `(array[array])`
```js
require("jsonarraytools").flattenArray(["Dwight", ["Jim", "Pam"]]);
```
Response
```json
["Dwight", "Jim", "Pam"]
```

## randomArrayInRange
Arguments: `(min, max, amount)`
```js
require("jsonarraytools").randomArrayInRange(0, 100, 2);
```
Response
```json
returns 2 random numbers in range 0-100
```

## randomItemFromArray
Arguments: `(array)`
```js
require("jsonarraytools").randomItemFromArray([1, 2, 3]);
```
Response
```json
1 || 2 || 3
```

## getAverageOfArray
Arguments: `(array)`
```js
require("jsonarraytools").getAverageOfArray([1, 2, 3]);
```
Response
```json
2
```

## getIntersectionOfArray
Arguments: `(arrays...)`
```js
require("jsonarraytools").getIntersectionOfArray([1, 3], [2, 3, 4], [3]);
```
Response
```json
3
```

## getSumOfArray
Arguments: `(array)`
```js
require("jsonarraytools").getSumOfArray([1, 2])
```
Response
```json
3
```

## getUniqueValuesOfArray
Arguments: `(array)`
```js
require("jsonarraytools").getUniqueValuesOfArray([1, 1, 2]);
```
Response
```json
1
```

## getUnionOfArrays
Arguments: `(arrays...)`
```js
require("jsonarraytools").getUnionOfArrays([1, 2], [2, 1]);
```
Response
```json
[1, 2]
```

## mergeArrays
Arguments: `(array...)`
```js
require("jsonarraytools").mergeArrays([1], [2]);
```
Response
```json
[ 1, 2 ]
```

## partitionArrayOnCondition
Arguments: `(array, condition)`
```js
require("jsonarraytools").partitionArrayOnCondition([1, 2, 3, 4, 5], n => n > 2);
```
Response
```json
[ [ 3, 4, 5 ], [ 1, 2] ]
```

## removeFalsyValues
Arguments: `(array)`
```js
require("jsonarraytools").removeFalsyValues([0, "string", NaN]);
```
Response
```json
[ "string" ]
```

## shuffleArray
Arguments: `(array)`
```js
require("jsonarraytools").shuffleArray([1, 2, 3, 4]);
```
Response
```json
[ 3, 2, 1, 4 ]
```

## sortArrayOfNumbers
Arguments: `(array)`
```js
require("jsonarraytools").sortArrayOfNumbers([1, 5, 10, 7, 3]);
```
Response
```json
[ 1, 3, 5, 7, 10 ]
```

## splitArrayIntoChunks
Arguments: `(array, chunks)`
```js
require("jsonarraytools").splitArrayIntoChunks([1, 2, 3, 4], 1));
```
Response
```json
[ [ 1 ], [ 2 ], [ 3 ], [ 4 ] ]
```

## tranposeMatrix
Arguments: `(arrays...)`
```js
require("jsonarraytools").tranposeMatrix([1, 2, 3], [4, 5, 6], [7, 8, 9]);
```
Response
```json
[ [1, 4, 7], [ 2, 5, 8 ], [ 3, 6, 9 ] ]
```

## unzipArrayOfArrays
Arguments: `(arrays...)`
```js
require("jsonarraytools").unzipArrayOfArrays([["a", 1], ["b", 2], ["c", 3]]);
```
Response
```json
[ [ "a", "b", "c"], [ 1, 2, 3 ] ]
```

## zipArrayOfArrays
Arguments: `(arrays...)`
```js
require("jsonarraytools").zipArrayOfArrays(["a", "b", "c"], [1, 2, 3]);
```
Response
```json
[ [ "a", 1 ], [ "b", 2 ], [ "c", 3 ] ]
```

## isPlainObject
Arguments: `(object)`
```js
require("jsonarraytools").isPlainObject({ a: "1"});
require("jsonarraytools").isPlainObject(null);
```
Response
```json
true
false
```

## isObject
Arguments: `(object)`
```js
require("jsonarraytools").isObject({});
require("jsonarraytools").isObject(null);
```
Response
```json
true
false
```

## isObjectEmpty
Arguments: `(object)`
```js
require("jsonarraytools").isObjectEmpty({});
require("jsonarraytools").isObjectEmpty({ "": "" });
```
Response
```json
true
false
```

## isObjectEqual
Arguments: `(object1, object2)`
```js
require("jsonarraytools").isObjectEqual({ foo: "bar"}, { foo: "bar" });
require("jsonarraytools").isObjectEqual({ foo: "bar"}, { bar: "foo" });
```
Response
```json
true
false
```

## arrayToObject
Arguments: `(arrays...)`
```js
require("jsonarraytools").arrayToObject([["a", 1], ["b", 2]]);
```
Response
```json
{ a: 1, b: 2 }
```

## ExtractValueFromObject
Arguments: `(array of objects)`
```js
require("jsonarraytools").ExtractValueFromObject([{ name: "Toby", loveable: false }, { name: "Michael", loveable: true }], "name");
```
Response
```json
[ "Toby", "Michael" ]
```

## getValueOfPath
Arguments: `(path, objects)`
```js
require("jsonarraytools").getValueOfPath("foo.bar", { foo: { bar: "hello world" } });
```
Response
```json
hello world
```

## invertKeysOfObject
Arguments: `(object)`
```js
require("jsonarraytools").invertKeysOfObject({ a: "1", b: "2" });
```
Response
```json
{ 1: "a", 2: "b" }
```

## OmitSubsetPropFromObject
Arguments: `(object, prop)`
```js
require("jsonarraytools").OmitSubsetPropFromObject({ a: "1", b: "2" }, ["a"]);
```
Response
```json
{ b: "2" }
```

## PickSubsetPropFromObject
Arguments: `(object, prop)`
```js
require("jsonarraytools").PickSubsetPropFromObject({ a: "1", b: "2" }, ["a"]);
```
Response
```json
{ a: "1" }
```
