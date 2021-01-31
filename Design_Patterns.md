## 1. Creational Patterns

### 1.1 Singleton
- Singleton is a creational pattern which describes a way to create an object.
- The Singleton pattern refers to having only one object of a class.
- **Goals of Singleton pattern:**
- Enforces one and only one object of a Singleton class
- Has the Singleton object globally accessible
  
### 1.2 Factory Method Pattern
- **Benefits of Factory Object:** If there are multiple clients that want to instantiate the same set of classes, then by using a Factory object, you have cut out redundant code and made the software easier to modify.
- The act of object creation, usually with the new keyword in Java is called **concrete instantiation**.
- "This allows the developer to make changes to the concrete instantiation without touching the client method. The client method does not need to name a concrete knife classes and now deals with a knife generalization. This is called coding to an interface, not an implementation."
- Factories allow client code to operate on generalizations. This is called **coding to an interface, not an implementation**. 
- The factory method design intent is to define an interface for creating objects, but let the sub-classes decide which class to instantiate.
  
### 1.3 Facade Pattern
- The facade design pattern provides a single simplified interface for client classes to interact with the subsystem.
- A facade does not actually add more functionality, a facade simply acts as a point of entry into your subsystem. 
- In software, the facade design pattern does exactly what a waiter or salesperson would do in real life. A facade is a wrapper class that encapsulate the subsystem in order to hide the subsystem's complexity. This wrapper class will allow a client class to interact with the subsystem through a facade. 
- **What are the two conditions required for you to use the facade design pattern?** 
  * 1.You need a class to act as an interface between your subsystem and a client class. (The client will only interact with the Facade but in fact the Facade draws on the subsystem to do most of its work.) 
  * 2.You need to simplify the interaction with your subsystem for client classes. (Facade provides a simpler interface so that clients can use a subsystem with ease.)
- A facade class can be used to wrap all the interfaces and classes for a subsystem.
- Since the entire point of the facade design pattern is to hide complexity, we use the information hiding design principle to prevent all client classes from seeing the account objects and how these accounts behave. 
- The key design principles are used to implement the facade design pattern: 
**Encapsulation, information hiding, separation of concerns**.
- While the facade design pattern uses a number of different design principles, it purpose is to provide ease of access to a complex subsystem. This is done by encapsulating the subsystem classes into a Facade class, and then hiding them from the client classes so that the clients do not know about the details of the subsystem. 
- **Summarize what characterizes the facade design pattern:**
  * Is a means to hide the complexity of a subsystem by encapsulating it behind a unifying wrapper called a facade class.
  * Removes the need for client classes to manage a subsystem on their own, resulting in less coupling between the subsystem and the client classes.
  * Handles instantiation and redirection of tasks to the appropriate class within the subsystem.S
  * Provides client classes with a simplified interface for the subsystem.
  * Acts simply as a point of entry to a subsystem and does not add more functionality to the subsystem.

### 1.4 Adapter Pattern
- The adapter design pattern will help facilitate communication between two existing systems by providing a compatible interface.
- The adaptee is hidden from the client by the wrapping adapter class.
- **Remember that an adapter is meant to:**
  * Wrap the adaptee and expose a target interface to the client.
  * Indirectly change the adaptee's interface into one that the client is expecting by implementing a target interface
  * Indirectly translate the client's request into one the adaptee is expecting.
  * Reuse an existing adaptee with an incompatible interface.

###  1.5 Composite Pattern
- **Composite Design Pattern achieves two goals:**
  * To compose nested structures of objects.
  * To deal with the classes for these objects uniformly. 
- **The composite design pattern is used to solve the issues of:**
  * How to build a tree-like structure of objects.
  * How to treat the individual types of those objects uniformly. 
- **This is achieved by:**
  * Enforcing polymorphism across each class through implementing an interface or inheriting from a superclass.
  * Using a technique called recursive composition, which allows objects to be composed of other objects that are of a common type. 

### 1.6 Proxy Pattern
- The proxy acts as a simplified or lightweight version of the original object. 
- A proxy object is still able to accomplish the same tasks, but may delegate requests to the original object to achieve them.
- **Why do we want to use a proxy class? The three most common scenarios for them are:** 
  1. To act as a virtual proxy where the proxy class is used in place of a real subject class, that is resource intensive to instantiate. This is commonly used on images, and web pages, or graphics editors, because a single high definition image can be extremely large. If you were to load all of these images at once, it could put a strain on your system's resources. 
  2. To act as a protection proxy in order to control access to the real subject class. A protection proxy can be used in a learning management system that checks the credentials of a user. So the different users, like students and instructors, can only access the appropriate functions permitted by their role. And three, 
  3. To act as a remote proxy, where the proxy class is local and the real subject class exists remotely. 
- **To summarize, the main features of the proxy design pattern are:**
  * To use the proxy class to wrap the real subject class.
  * To have a polymorphic design so that the client class can expect the same interface for the proxy and real subject classes.
  * To use a lightweight proxy in place of a resource intensive object until it is actually needed.
  * To implement some form of intelligent verification of requests from client code in order to determine if, how, and to whom the requests should be forwarded to.
  * To present a local representation of a system that is not in the same physical or virtual space. 

### 1.7 Decorator Pattern

## 2. Behavioural Patterns

### 2.1 Template Method Pattern
- The template method defines an algorithm's steps generally, deferring the implementation of some steps to subclasses. It is a behavioral design pattern and is concerned with the assignment of responsibilities.
- The template method can be helpful if you have two classes with similar functionality. When you notice two classes with a very similar order of operations, you can choose to use a template method. The template method pattern is a practical application of generalization and inheritance.

### 2.2 Chain of Responsibility Pattern
- A chain of objects that are responsible for handling requests.
- In software design, the Chain of Responsibility is a series of handler objects that are linked together.
- You can also think of this pattern as similar to Exception handling in Java. 

### 2.3 State Pattern
- **When should you use the state pattern?** 
  * The state pattern is primarily used when you need to change the behavior of an object based upon the state that it's in at run-time.

### 2.4 Command Pattern
- Instead of having these objects directly communicating with each other, the command pattern creates a command object in between the sender and receiver. 
- The command pattern has another object that invokes the command objects to complete whatever task it is supposed to do, called the invoker.
- A command manager can also be used which basically keeps track of the commands, manipulates them and invokes them. 
- **Where can you implement the command pattern in your software?**
  1. One purpose of using the command pattern is to store and schedule different requests. You can store these command objects into lists, you can manipulate them before they are completed, or you can put them onto a queue so that you can schedule different commands to be completed at different times. 
  2. Another important purpose of the command pattern is allowing commands to be undone or redone.
- **There are many benefits that come from using the command pattern.**
  * It allows you to manipulate the commands as objects the way you could not do with method calls. 
  * Working with command objects allows you to add the functionalities I mentioned earlier, like putting commands into queues and adding an undo/redo function. 
  * Another main benefit of the command pattern is that it decouples the objects of your software program. 