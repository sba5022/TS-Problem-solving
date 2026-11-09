Introduction
type and interface have some differences in how they define and extend types. Understanding these differences helps us choose the right one for different situations.

Type:
Type alias allows to create a custome name for any type including functions,tuples.
For example: 
type Status = "success" | "error" | "loading";

type Coordinate = [number, number];

type UserId = string;

Here, Status represents three possible values, Coordinate represents a tuple, and UserId is an alias for the string type.

Interface:
Interface is used to define the structure of an object.It has no types like union,intersecton,primitive.for example:
interface User {
  name: string;
  age: number;
}
Interfaces support extension using extends and declaration merging, which makes them useful for defining and extending object structures.

interface Admin extends User {
  role: string;
}
I will use both, interface for object structure and alias for complex types .when i need to define tuples , union then i will use type .

conclusion

Both type aliases and interface are important features of TypeScript. Although they have overlapping capabilities, choosing the appropriate one makes code easier to understand, organize, and maintain.
