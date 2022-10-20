The stack - the procedural approach vs. the object-oriented approach
The procedural stack is ready. Of course, there are some weaknesses, and the implementation could be improved in many ways (harnessing exceptions to work is a good idea), but in general the stack is fully implemented, and you can use it if you need to.

But the more often you use it, the more disadvantages you'll encounter. Here are some of them:

the essential variable (the stack list) is highly vulnerable; anyone can modify it in an uncontrollable way, destroying the stack, in effect; this doesn't mean that it's been done maliciously - on the contrary, it may happen as a result of carelessness, e.g., when somebody confuses variable names; imagine that you have accidentally written something like this:

stack[0] = 0


The functioning of the stack will be completely disorganized;

it may also happen that one day you need more than one stack; you'll have to create another list for the stack's storage, and probably other push and pop functions too;

it may also happen that you need not only push and pop functions, but also some other conveniences; you could certainly implement them, but try to imagine what would happen if you had dozens of separately implemented stacks.


The objective approach delivers solutions for each of the above problems. Let's name them first:

the ability to hide (protect) selected values against unauthorized access is called encapsulation; the encapsulated values can be neither accessed nor modified if you want to use them exclusively;

when you have a class implementing all the needed stack behaviors, you can produce as many stacks as you want; you needn't copy or replicate any part of the code;

the ability to enrich the stack with new functions comes from inheritance; you can create a new class (a subclass) which inherits all the existing traits from the superclass, and adds some new ones.
The stack - procedural vs. object approach
