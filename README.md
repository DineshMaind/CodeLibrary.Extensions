# How to use
```
string jsonString = @"[{ firstName : 'FirstName01', lastName : 'LastName01' }, { firstName : 'FirstName02', lastName : 'LastName02', subjects : { Maths : 87, Science : 60 } } ]";
dynamic obj = jsonString.AsExpandoObject();
// Accessing array elements use (item0, item1, item2, ...).
var subjects = obj.item1.subjects; // Accessing 2nd element of array and then pointing to subjects element.
int mathsMarks = subjects.Maths;
int scienceMarks = subjects.Science;
Console.WriteLine("Maths : {0}, Science : {1}", mathsMarks, scienceMarks);
```
