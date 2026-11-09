# TypeScript Practice – Functions, Generics, Interfaces & OOP

##  About This Project

This repository contains practical TypeScript exercises designed to strengthen my understanding of TypeScript fundamentals and advanced concepts. Through these examples, I practiced writing type-safe functions, working with generics, using interfaces, implementing object-oriented programming, and handling asynchronous operations.

## Topics Covered

### 1. Optional and Nullish Coalescing Parameters
- Created a function with an optional parameter.
- Used the nullish coalescing operator (`??`) to provide a default value.
- Practiced handling `0` as a valid input.

### 2. Union Types and Type Narrowing
- Used union types (`string | number | boolean`).
- Applied `typeof` to identify different data types.
- Processed different values based on their types.

### 3. Readonly Tuples
- Used readonly tuples to define fixed-length coordinate data.
- Practiced array destructuring.
- Formatted geographic coordinates into readable strings.

### 4. Generics and Rest Parameters
- Created a reusable generic function using `<T>`.
- Used rest parameters to accept multiple arrays.
- Combined multiple arrays into a single array using `flat()`.

### 5. Interfaces and Array Filtering
- Defined a `Course` interface to describe course objects.
- Used the `filter()` method to find published courses.
- Applied conditions based on student enrollment.

### 6. Generic Constraints and Keyof
- Used generic types (`T` and `K`).
- Applied `K extends keyof T` to restrict property keys.
- Used indexed access types (`T[K]`) to return selected object properties.

### 7. Classes and Inheritance
- Created an `Employee` class and a `Manager` subclass.
- Practiced constructors and the `super()` keyword.
- Used access modifiers: `public`, `protected`, and `private`.
- Implemented inheritance and class methods.

### 8. Promises and Asynchronous Programming
- Created an asynchronous age validation function.
- Used `Promise<string>` with `resolve` and `reject`.
- Handled successful and failed promises using `.then()` and `.catch()`.

##  Technologies Used

- TypeScript
- JavaScript
- Node.js




##  Learning Goals

The main goal of this practice is to improve my TypeScript skills by understanding type safety, reusable functions, generic programming, object-oriented programming, and asynchronous JavaScript.


This document covers some important TypeScript concepts, including special types (any, unknown, and never), type aliases, and interfaces. These concepts help us understand type safety, define data structures, and write reusable and maintainable code.

1. Any, Unknown, and Never

In TypeScript, any, unknown, and never work differently in the type system.

Any

The any type allows us to assign any value to a variable.

We can perform different operations without TypeScript checking whether they are safe.

It disables type checking and can lead to runtime errors.

Unknown

The unknown type can also store any type of value.

However, TypeScript requires us to check the type before performing operations.

It provides better type safety than any.

Never

The never type represents a value that never occurs.

It is commonly used for functions that never return normally, such as functions that always throw an error or run indefinitely.

Why is Unknown Preferred Over Any?

unknown is preferred over any because it provides better type safety. Before performing operations, we must check the value's type. This helps prevent unsafe operations and potential runtime errors.

2. Type Alias

A type alias allows us to create a custom name for any type, including objects, primitive types, functions, tuples, union types, and intersection types.

Example:

type Status = "success" | "error" | "loading";

Here, Status is a union type that allows only three possible values: "success", "error", or "loading".

3. Interface

An interface is mainly used to define the structure or shape of an object. It specifies which properties and their types an object should contain.

Example:

interface User {
  name: string;
  age: number;
}

Here, the User interface defines an object with two properties: name and age.

Interfaces do not directly define union types, intersection types, or primitive type aliases.

4. When Should We Use Type Alias and Interface?

I would use both depending on the requirements:

Interface: When I need to define the structure of an object or extend object structures.

Type Alias: When I need to define union types, intersection types, tuples, primitive types, or more complex type combinations.

Example:

interface User {
  name: string;
  age: number;
}

type Status = "success" | "error" | "loading";

Conclusion

Both type aliases and interfaces are useful in TypeScript. I prefer using interfaces for defining object structures and type aliases for more complex or flexible type definitions. Similarly, I prefer unknown over any because it helps maintain type safety and reduces potential errors.
