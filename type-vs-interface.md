# Type vs Interface in TypeScript

## Introduction

TypeScript has two ways of specifying data structures: `type` and `interface`. Both enable developers to define the form of the data and create more reliable applications.They are very similar, but there are some differences.

## Detailed Explanation

The main purpose of an interface is to specify the structure of objects. It describes the properties and methods an object should contain.

```
interface User {
  name: string;
  age: number;
}
```

A type alias can also define object structures, but it is more flexible. It can represent primitive types, unions, tuples, and other complex types.

```
type User = {
  name: string;
  age: number;
};

type ID = string | number;
```

The other big difference is in their extension of other types. An interface is extended with the keyword extends and type aliases can form type combinations with intersections (`&`).

```
interface Person {
  name: string;
}

interface Employee extends Person {
  salary: number;
}
```

Interfaces are helpful when you need to define the structure of objects, the contract of classes, or reusable properties of objects. Type aliases are preferable when dealing with union types, tuples, primitive types or more complex type combinations.

## Conclusion

The type and the interface are allowed in Typescript. They work similar to each other, come in a number of features but not the same. It is important to keep in mind these differences in the development world so that they can write clean, flexible and maintainable code.