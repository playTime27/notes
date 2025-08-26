protected means Access is limited to the containing class and any derived classes
internal means Access is limited to the current assembly
protected internal: Only code in the same assembly or in a derived class in another assembly can access this type or member.
private protected: Only code in the same assembly and in the same class or a derived class can access the type or member.
file: Only code in the same file can access the type or member.
The base keyword is used to access members of the base class from within a derived class.
The override keyword is used to provide a new implementation for a property inherited from a base class
The virtual keyword is used to modify a property and allow for it to be overridden in a derived class

