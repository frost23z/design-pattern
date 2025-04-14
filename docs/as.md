Suggestions for Object Oriented Design
Whenever writing code in an object oriented language, sticking to the following list of suggestions will make your code amenable to changes with the least effort.

Separate out parts of code that vary or change from those that remain the same.

Always code to an interface and not against a concrete implementation.

Encapsulate behaviors as much as possible.

Favor composition over inheritance. Inheritance can result in explosion of classes and also sometimes the base class is fitted with new functionality that isn't applicable to some of its derived classes.

Interacting components within a system should be as loosely coupled as possible.

Ideally, class design should inhibit modification and encourage extension.

Using patterns in your day to day work, allows exchanging entire implementation concepts with other developers via shared pattern vocabulary.

❌ God Object / God Class
Problem: One class does everything, making it huge, complex, and hard to maintain.

✅ Solution:
Apply Single Responsibility Principle (SRP) and break it into multiple cohesive classes.
Use patterns like:

Facade (for simplifying interfaces)

Strategy (for varying behavior)

Observer (for communication between components)

❌ Spaghetti Code
Problem: Code with tangled logic and poor structure, making it hard to follow or debug.

✅ Solution:
Use MVC (Model-View-Controller) or MVVM to separate concerns.
Introduce State or Command patterns to isolate complex logic.

❌ Hard-Coded Values (Magic Numbers/Strings)
Problem: Embedding values directly in code makes it fragile and error-prone.

✅ Solution:
Use Constants, Enums, or external Configuration Files.
Abstract using Factory or Builder patterns for complex object creation.

❌ Copy-Paste Programming
Problem: Repeating similar code across the codebase, leading to duplication and maintenance nightmares.

✅ Solution:
Refactor repeated logic into reusable functions or classes.
Use Template Method or Decorator pattern to avoid duplication while allowing variations.

❌ Tight Coupling
Problem: Classes are heavily dependent on each other, making changes risky and testing difficult.

✅ Solution:
Apply Dependency Injection and Inversion of Control.
Use Observer, Mediator, or Adapter to decouple components.

❌ Premature Optimization
Problem: Overengineering for performance before it’s actually needed, leading to complex and unreadable code.

✅ Solution:
Focus on clean, readable design first. Profile bottlenecks and apply patterns like:

Flyweight (to reduce memory)

Caching strategies

Prototype (for object cloning)

❌ Lava Flow
Problem: Legacy code that's still running but no one understands or dares to touch it.

✅ Solution:
Gradually refactor using Strangler Fig Pattern – replace parts incrementally.
Add tests, apply Facade to simplify interaction, and use Adapter to bridge old and new code.