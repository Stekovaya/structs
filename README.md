# structs
Add extended structs for C#.

## Namespaces
```
StructCollection━┳━Array
		 ┃ 　┗(ListArray)
		 ┗━Template
		　   ┗(Array)
```

### Array
Namespace `Array` is containing struct for array.

Structs: ListArray

### Template
Namespace `Template` is containing struct templates.

Structs: Array

## Structs

### StructCollection.Array.ListArray
Make array-like list.

#### Constructors
----
 - `ListArray<T>()`

Make empty ListArray.

---

 - `ListArray<T>(T0,T1,T2...Tn)`

Make ListArray with T0 - Tn.

#### Properties
----
(\* = Readonly)

 - \*`Count`

Return length of ListArray.

---

 - \*`Length`

Return length of ListArray.

---

 - `Item[Int32]`

Return content of ListArray.

#### Methods
----
 - `Add(T)`
 - Void

Add data to ListArray.

---

 - `Remove(Int32)`
 - Void

Delete data from ListArray.

---

 - `ToArray()`
 - `T[]`

Convert ListArray to Array.

---

 - `ToList()`
 - `List<T>`

Convert ListArray to List.

#### Sample

----

```cs
using System;
using StructCollection.Array;

class MainClass {
  public static void Main(string[] args){
    var la = new ListArray<ListArray<decimal>>();
    for(int i = 0; i < 10; i++){
      la.Add(new ListArray<decimal>());
      for(int j = 0; j < 10; j++){
        la[i].Add(i * j);
      }
    }
  }
}
```
