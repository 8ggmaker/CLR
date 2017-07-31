1. Base Type: System.Object

| Public Method |               Description                |
| :-----------: | :--------------------------------------: |
|    Equals     | Returns *true* if two objects have the same value. |
|  GetHashCode  | Returns a hash code for this object's value, override this method if this type objects are be used as a key in a hash table collection, like *Dictionary*, this method should provide a good distribution for its objects. |
|   ToString    | The default implementation returns the full name of the type, override this method to represent the object state with a string (e.g. for ebugging). |
|    GetType    | Returns an instance of a `Type`-derived object that identifies the type of the object used to call `GetType`. The returned `Type` object can be used with the reflection classes to obtain metadata information about the object’s type. |

| Protected Method |               Description                |
| :--------------: | :--------------------------------------: |
| MemberwiseClone  | This `nonvirtual` method creates a new instance of the type and sets the new object’s instance fields to be identical to the `this` object’s instance fields. A reference to the new instance is returned. |
|     Finalize     |       `virtural` method,Destructor       |



2. `new` Operator

   ``` c#
   Employee e = new Employee("ConstructorParam1");
   ```

   1. It calculates the number of bytes required by all the fields of `Employee` and all of its base type up to and including `System.Object` , and every object in managed heap requires two additional members: 1. *Type Object Pointer*, 2. *Sync Block Index* — used by CLR to manage the object. The bytes for these two additional members are add to the size of the object.
   2. It allocates memory for the object by the size, all these bytes are then set to zero.
   3. It initializes the object's type object pointer and sync block index.
   4. The type's instance constructor is called (`Employee("ConstructorParam1")`).

   After `new` has performed all of these operations, it returns a reference (or pointer) to the newly created object. In the preceding code example, this reference is saved in the variable `e`, which is of type `Employee`.