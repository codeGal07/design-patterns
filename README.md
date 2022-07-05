# design-patterns
Some notes of "Dive into DESIGN PATTERNS" by Alexander Shvets

Google doscs notes with comments: https://docs.google.com/document/d/1jzzAfMacZmmW6TYcvSzUS-aZ164vVVyr7HqNvP-6ggk/edit?usp=sharing


----------------

## Single Responsibility Principle
> A class should have just one reason to change.

If you feel that it’s becoming hard to focus on specific aspects of the program one at a time, remember the single responsibility principle and check whether it’s time to divide some classes into parts. 



## Open/Closed Principle
> Classes should be open for extension but closed for modification.

The main idea of this principle is to keep existing code from breaking when you implement new features. Instead of changing the code of the class directly, you can create a subclass and override parts of the original class that you want to behave differently. Start by extracting shipping methods into separate classes with a common interface. You’ll achieve your goal but also won’t break any existing clients of the original class.


## Liskov Substitution Principle
> When extending a class, remember that you should be able to pass objects of the subclass in place of objects of the parent class without breaking the client code.

This means that the subclass should remain compatible with the behavior of the superclass. When overriding a method, extend the base behavior rather than replacing it with something else entirely.

- Parameter types in a method of a subclass should match or be more abstract than parameter types in the method of the superclass.
- The return type in a method of a subclass should match or be a subtype of the return type in the method of the superclass.
- A method in a subclass shouldn’t throw types of exceptions which the base method isn’t expected to throw.



## Interface Segregation Principle

> Clients shouldn’t be forced to depend on methods they do not use.
Don't put too much into an interface; Split into separate interfaces.

Try to make your interfaces narrow enough that client classes don’t have to implement behaviors they don’t need.
Class inheritance lets a class have just one superclass, but it doesn’t limit the number of interfaces that the class can implement at the same time. Hence, there’s no need to cram tons of unrelated methods to a single interface. Break it down into several more refined interfaces—you can implement them all in a single class if needed. However, some classes may be fine with implementing just one of them. 



## Dependency Inversion Principle

> High-level classes shouldn’t depend on low-level classes. Both should depend on abstractions. Abstractions shouldn’t depend on details. Details should depend on abstractions.

Once low-level classes implement these interfaces, they become dependent on the business logic level, reversing the direction of the original dependency.





