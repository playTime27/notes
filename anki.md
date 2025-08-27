protected means Access is limited to the containing class and any derived classes
internal means Access is limited to the current assembly
protected internal: Only code in the same assembly or in a derived class in another assembly can access this type or member.
private protected: Only code in the same assembly and in the same class or a derived class can access the type or member.
file: Only code in the same file can access the type or member.
The base keyword is used to access members of the base class from within a derived class.
The override keyword is used to provide a new implementation for a property inherited from a base class
The virtual keyword is used to modify a property and allow for it to be overridden in a derived class
To implement custom extension methods for method chaining, you must :
  define a static class to contain the method extension
  extension method is static with at least same visibility as containing class
  the first parameter of the method is preceded by this and specifies the type that the method operates on

Write an extension method StringLength in class StringExtension that takes a string input and returns the length of it

public static class StringExtension
{
    public static int StringLength(this string str)
        {
            return str.Length;
        }
}

Generics make it possible to design classes and methods that defer the specification of one or more type parameters until you use the class or method in your code

Define a generic class named Student

public class Student<T> {}


Events allow us to signal that state has changed

public event EventHandler<string> EnrollmentFull;
