# Typescript

### What is Typescript 
    Typescript is a statically typed superset of javascript developed by microsoft.

    Statically Typed - The data types of variables are checked and enforced before the code 
    runs(compile time), rather than while executing (at runtime).

    JavaScript + a static type system + additional developer tooling = TypeScript



### Example in javascript:

      function add(a,b){
        return a+b;
      }

    There is no information telling what a and b should be 

### Typescript

      function (a:number, b:number): number {
        return a+b;
      }

      So:
        add(10,20)   //This is valid
        add("10", 20)   //This gives typescript error



## Why Typescript is created ??

    Javascript is a dynamically typed  - means data types are associated with values not with variable
    themselves and typechecking happens at runtime.

    In a dynamically typed language like JavaScript, you do not declare what kind of data (like a string, 
    number, or boolean) a variable will hold. The engine figures it out automatically based on the value
    currently assigned.
    
    javascript os dynamically typed, that gives javascript flexibility, but large applications can become
    diffcult maintain.

    In typescript - Static typing means types are checked before the program runs.


##  Is TypeScript a programming language?
    Yes, Typescript is a programming language, but technically it is a superset of javascript.


## Does the borswer understand Typescript ??

    Broswer understands javascript, 

    They dont directly execute typescript.

    So: 
      const age:number = 25;

      needs to eventually become javascript.

    The type annotation :number is removed and eventually its like const age = 25;

## What happens when we write typescript ??

    You write TypeScript -> TypeScript compiler / build tool  ->  Type checking  -> Javascript output -> browser / nodejs  -> execution
      
##  Important: TypeScript types don't exist at runtime


    Consider:

        function greet(name: string) {
          return `Hello ${name}`;
        }

      At runtime javascript doesn't know that name was supposed  to be string.

      Typescript's type information is primarily a compile time/development-time construct.



##  TypeScript doesn't provide runtime validation automatically

    This is very important when we are working with APIs.

    Suppose your backend says:

      {
      "id": 1,
      "name": John,
      }

      you write:

      interface User{
      id: number;
      name: string;
      }

      Const user: User = response.data

      The interface doesn't validate server reponse at runtime.

      This is why real applications sometimes use runtime validation libraries such as Zod.

## Type inference

    you dont need to write types explicitly always.

    let num  = 10;

    Its automatically then number type will get assign to its variable based on the value you provided.

    so typescript infer num: number automatically. 

    This is called type inference.

##  Explicit typing vs inference

    let age : number = 25;

    This is explicit typing.

    let age = 25;

    Here typescript will give type automatically based on the value that you provided here.

## Why inference is useful

    example:

    const user = [
       {
          id: 1,
          name: "Srikanth",
       }
       {
         id: 2,
         name: "Gopi"
       }
    ]


    here typescript give type 

  {
    id: number,
    name: string,
  }[]


     if you access users[0].name 
     here typescript knows its a string

     And your editor can provide autocomplete.
   improves developer experience

    This is one of the biggest reasons TypeScript improves developer experience.

      
        
