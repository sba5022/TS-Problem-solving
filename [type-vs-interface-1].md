Type alias allows to create a custome name for any type including functions,tuples.
For example: 
type Status = "success" | "error" | "loading";
Interface is used to define the structure of an object.It has no types like union,intersecton,primitive.for example:
interface User {
  name: string;
  age: number;
}
I will use both, interface for object structure and alias for complex types .when i need to define tuples , union then i will use type .
