* Event raiser method: Initiates the event, announcing that something has happened.
* Event handler method: Reacts to the event, performing actions in response to the notification.
* Naming: "On" + EventName is the convention for event-raising methods
* The class that sends (or raises) the event is called the publisher
* classes that receive (or handle) the event are called subscribers.

Create an event declaration , given the access level is public. The EventHandler is of type string and name is EnrollmentFull

```c#
public event EventHandler<string> EnrollmentFull;
```
Given a class history with event EnrollmentFull, subscribe the History_EnrollmentFull event handler method to the EnrollmentFull event :
```c#
history.EnrollmentFull += History_EnrollmentFull;
```
What is History_EnrollmentFull called in this context? What does that mean?
What is sender?
What is e?
What does the following code do?
```c#
private static void History_EnrollmentFull(object sender, string e)
{
  Console.WriteLine($" EVENT: {e}");
}
```
History_EnrollmentFull is the event handler, it runs when EnrollmentFull event fires and defines what happens when the event occurs
sender is the object that raised the event
e is the message that is passed from the event
its write to console

What is OnEnrollmentFull?
What is EnrollmentFull?.Invoke(this.message)?
What does the following code do?
```c#
 protected virtual void OnEnrollmentFull(string message)
 {
     EnrollmentFull?.Invoke(this, message);
 }
```
OnEnrollmentFull is event raiser method
Checks if EnrollmentFull is null before trying to invoke it, where this is the instance raising the event.
Notifies all subscribers that something happened
