# Access Modifiers (public, private, protected, and readonly) in TypeScript OOP with examples.

## Introduction

Access modifiers are important features of Object-Oriented Programming (OOP) in TypeScript.They can be used to control the access to class properties and methods in various parts of a program. To control access and protect the data, TypeScript offers public, private, protected and readonly properties.

## Detailed Explanation

1. Public

The public modifier allows properties and methods to be accessed from anywhere. This is the default access modifier of TypeScript.

```class Person {
  public name: string = "Nusrat";
}

const person = new Person();
console.log(person.name);
```
2. Private

The private modifier allows a property or method to be accessed only inside its own class. It is not directly accessible from subclass or outside subclass.

```
class Employee {
  private salary: number = 50000;
}
```

3. Protected

The protected modifier allows access inside the class and its subclasses, but not directly from outside the class.

```
class Animal {
  protected name: string = "Cat";
}

class Cat extends Animal {
  showName(): string {
    return this.name;
  }
}
```
4. Readonly

The readonly modifier allows a property to be assigned only during its declaration or inside the constructor. After that, its value cannot be changed.

```
class Student {
  readonly id: number;

  constructor(id: number) {
    this.id = id;
  }
}
```
## Conclusion

Access modifiers are used to control access to data and enhance the security and organization of code: public – can be accessed from anywhere; private – can be accessed only within the class; protected – can be accessed within subclasses; readonly – can only be assigned during initialization. With proper usage, TypeScript will be maintainable.