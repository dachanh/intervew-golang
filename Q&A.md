1. Difference between array and slice?

    - ARRAY : An array is a fixed collection of data. The emphasis here is on fixed, because once you set the length of an array, it cannot be changed.

    - SLICE : Slices are much more flexible, powerful, and convenient than arrays. Unlike arrays, slices can be resized using the built-in append function .

What is pointer?

    Those variables that hold the address of any variables
    Pointers are used for the following purposes:
        
        - Allowing function to directly mutate value passed to it. That is achieving pass by reference functionality.

        - For increasing the performance in the edge cases in the presence of a large data structure. Using pointers help to copy large data efficiently
        - Helps in signifying the lack of values. For instance, while unmarshalling JSON data into a struct, it is useful to know if the key is present or absent then the key is present with 0 value.

Normal variable vs pointer variable?
    
So sánh Concurrency và parallelism hoặc Concurrency là gì?

Buffer channel và unbuffered channel khác nhau như thế nào ?

- different buffer channel and unbuffer channel is declare capacity of channel 
- channel use get and pop element the same as FIFO 
- buffer channel will block the goroutine if the len equal the capacity of channel 
every 

Goroutine là gì?

Channels là gì?
    Channels are the pipes that connect concurrent goroutines. You can send values into channels from one goroutine and receive those values into another goroutine.

Interface là gì? Empty interface là gì, dùng như thế nào?
    The interface is a collection of methods as well as it is a custom type.
    ```
    package main

    import "fmt"
      
    // Creating an interface
    type tank interface {
      
        // Methods
        Tarea() float64
        Volume() float64
    }
      
    type myvalue struct {
        radius float64
        height float64
    }
      
    // Implementing methods of
    // the tank interface
    func (m myvalue) Tarea() float64 {
      
        return 2*m.radius*m.height +
            2*3.14*m.radius*m.radius
    }
      
    func (m myvalue) Volume() float64 {
      
        return 3.14 * m.radius * m.radius * m.height
    }
      
    // Main Method
    func main() {
      
        // Accessing elements of
        // the tank interface
        var t tank
        t = myvalue{10, 14}
        fmt.Println("Area of tank :", t.Tarea())
        fmt.Println("Volume of tank:", t.Volume())
    }
    ```
    Interfaces can make code clearer, shorter, more readable, and they can provide a good API between packages, or clients (users) and servers (providers).
- Empty Interface 
Panic và recover ?

What are the difference between goroutines and threads

    Threads : A thread is just a sequence of instructions that can be executed independently by a processor. Threads use a lot of memory due to their large stack and requires call to OS for resources (such as memory) which is slow. so doesn’t always guarantee a better performance than processes in this multi-core processor world.

    Goroutines:Goroutines exists only in the virtual space of go runtime and not in the OS. and A goroutine is created with initial only 2KB of stack size. Each function in go already has a check if more stack is needed or not and the stack can be copied to another region in memory with twice the original size. This makes goroutine very light on resources.

Why are goroutines light-weight?

    A goroutine is created with initial only 2KB of stack size. Each function in go already has a check if more stack is needed or not and the stack can be copied to another region in memory with twice the original size. This makes goroutine very light

(OOP) solid là gì? apply oop trong golang như thế nào?

    Golang has types and methods and allows an object-oriented style of programming, there is no type hierarchy.Golang has some properties of object oriented programming like Encapsulation , Composition , but it doesn't have inheritance , classes , function overloading .
    Có biết API ko? Kể tên 1 vài http method? Phân biệt get vs post?


SQL vs NOSQL ?

Method

Closure?
    A closure is a function value that references variables from outside its body. The function may access and assign to the referenced variables.

unit test vs integration test?

Khac nhau giua RUN, CMD, ENTRYPOINT trong Dockerfile?

1 số lệnh trong docker

Monolithic vs Microservices

variadic function?
    The function that takes a variable number of arguments is called a variadic function. We can pass zero or more parameters in the variadic function. The best example of a variadic function is fmt.Printf which requires one fixed argument as the first parameter and it can accept any arguments.

    The syntax for the variadic function isHere, we see that the type of the last parameter is preceded by the ellipsis symbol (...) which indicates that the function can take any number of parameters if the type is specified.
    Inside the variadic function, the ... type can be visualised as a slice. We can also pass the existing slice (or multiple slices) of the mentioned type to the function as a second parameter. When no values are passed in variadic function, the slice is treated as nil.
    These functions are generally used for string formatting.
    Variadic parameter can not be specified as return value, but we can return the variable of type slice from the function.
    Consider an example code below:

        func function_name(arg1, arg2...type)type{
            // Some statements
        }
        package main
        
        import(
            "fmt"
            "strings"
        )
        
        // Variadic function to join strings and separate them with hyphen
        func joinstring(element...string)string{
            return strings.Join(element, "-")
        }
        
        func main() {
        
        // To demonstrate zero argument
        fmt.Println(joinstring())
            
        // To demonstrate multiple arguments
        fmt.Println(joinstring("Interview", "Bit"))
        fmt.Println(joinstring("Golang", "Interview", "Questions"))
            
        }
            Here, we have a variadic function called joinstring that takes a variable number of arguments of a type string. We are trying to join the arguments separated by the hyphen symbol. We are demonstrating the variadic function behaviour by first passing 0 arguments and then passing multiple arguments to the function. The output of this code is:
Data type Golang:

    Method
    Boolean
    Numeric
    String
    Array
    Slice
    Struct
    Pointer
    Function
    Interface
    Map
    Channel

Package in Golang:

    A package is a collection of source files in the same directory that are compiled together.
    
    ```
        Interview-Bit
        Golang-Interview-Questions
    ```

How do we perform inheritance with Golang?
User reciver function golang