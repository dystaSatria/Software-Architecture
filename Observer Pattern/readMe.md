# Observer Pattern

This chapter covers the observer pattern.

## GoF Definition

Define a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.

## Concept

The Observer Pattern establishes a one-to-many relationship between objects, where multiple observers (objects) monitor changes in a particular subject (also an object). Observers register themselves with a subject to receive notifications when changes occur. When observers lose interest in the subject, they can unregister themselves. This pattern is also known as the publish-subscribe pattern, enabling an object (subject) to send notifications to multiple observers simultaneously.

### Visualization Steps:

1. **Observers request notifications from a subject** (See Figure 14-1).
   ![Step 1](<ImageURL>)

2. **The subject grants the requests, establishing the connection** (See Figure 14-2).
   ![Step 2](<ImageURL>)

3. **Subject sends notifications to registered users** (See Figure 14-3).
   ![Step 3](<ImageURL>)

4. **Optionally, an observer unregisters itself** (See Figure 14-4).
   ![Step 4](<ImageURL>)

5. **Only remaining registered observers receive notifications** (See Figure 14-5).
   ![Step 5](<ImageURL>)

## Real-World Examples

- **Celebrity and Followers**: Think of a celebrity with followers on social media. Followers subscribe to receive updates but can unsubscribe when they lose interest.

- **Computer Science Example**: In a UI connected to a database, UI elements can receive notifications when the database changes.

## Implementation Example

- Illustrates a scenario with three observers and one subject. Observers receive notifications when a flag value changes in the subject.

### Class Diagram
![Class Diagram](<ImageURL>)

### Package Explorer View
![Package Explorer](https://github.com/dystaSatria/Software-Architecture/blob/main/Observer%20Pattern/package.png)

### Code Example (Java)

[See Example Code](https://github.com/dystaSatria/Software-Architecture/blob/main/Observer%20Pattern/observerPattern.java)

## Q&A Session

1. **Need for Interface**: Using interfaces is preferable for abstraction and following OOP principles.
2. **Multiple Observer Types**: Different types of observers can exist in the same application.
3. **Dynamic Observer Addition/Removal**: Observers can be added or removed at runtime.
4. **Comparison with Chain of Responsibility Pattern**: Observers receive notifications simultaneously; chain of responsibility handles notifications sequentially.
5. **Support for One-to-Many Relationship**: Yes, this pattern depicts a one-to-many relationship.
6. **Custom Implementation vs. Built-in Constructs**: Custom implementations can provide more flexibility and understanding than built-in constructs.
7. **Benefits of the Observer Pattern**: Loose coupling, dynamic addition/removal of observers, and no modifications needed in subjects for observer changes.
8. **Challenges of the Observer Pattern**: Concerns about memory leaks, undependable order of notification, and limitations in some language constructs.

## Resources

- [Java Observable Documentation](<JavaObservableURL>)
- [.NET System.IObservable<T> Documentation](<DotNetObservableURL>)

