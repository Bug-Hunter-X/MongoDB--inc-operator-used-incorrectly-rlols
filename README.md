# MongoDB $inc Operator Error
This example demonstrates an incorrect usage of the MongoDB $inc operator. The $inc operator is designed to increment a numeric field by a specified value. Attempting to use it with a string value will lead to an error or unexpected results.

## Bug
The following code snippet demonstrates the incorrect usage:
```javascript
db.collection('myCollection').updateOne({"_id": 1}, {"$inc": {"field": 'value' }});
```

## Solution
To solve this, ensure that the value being incremented is a number.  If necessary, convert the string to a number before updating.

The corrected code is shown in `bugSolution.js`.