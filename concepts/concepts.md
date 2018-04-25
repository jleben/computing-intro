# Concepts

This lists concepts in the imperative paradigm. Some of them do not apply to applicative paradigm, and there may be some concepts found in applicative paradigm that are missing.

Concepts are listed in recommended order of introduction. Later concepts depend on earlier ones.

Unless otherwise noted, examples are in Python language.

## Instruction (Command) and Sequencing

Languages like Scratch have a concept of instructions/commands with parameters that have external effects - draw something or change appearance of something already on screen, play a sound. This concept can be understood without introducing expressions, operators, types, functions.

In textual languages like Python, this concept corresponds to effectful functions, like `print`. Unfortunately, usually very few such functions are immediately available.

Processing.org is one exceptions, with a lot of readily available drawing functions.

Exercises:

- Modify instruction parameters.
- Copy and paste instructions.
- Add instructions.

Many Hour of Code exercise don't go beyond this.

## Expression, Value

NOTE: To make expressions really useful, one needs non-constants, e.g. program input or variables, ...

    1
    1 + 2
    "Hi!"
    "Hi " + "Alice!"

Exercise: Modify expressions
Exercise: Compose expressions

## Type

Type error:

    "Hi " + 2

## Function, Method

Parameters (arguments), return value:

    "Hi " + str(2)

    "Alice".lower()

Effect:

    print("something")

    print("Hi: " + input("Enter your name:"))

Exercise: Modify arguments to functions.
Exercise: Add function calls.

## Event

Essence: executing code when something external happens.

Events are mentioned as fundamental concept in Google's hour of code activity:
g.co/csfirst/logo

Events are part of Scratch (e.g. when mouse is clicked or key is pressed).

In Python, using `input` is a response to events.

## Repetition

In some graphical languages, like Scratch, there exists pure repetition without variation.

NOTE: In many professional languages, there is no special syntax for plain repetition without variation. Instead, such repetition must be implemented using other concepts like iterating a collection (Python), or updating a state (C++). Therefore, it may be better to introduce it after those concepts.

In Python, `range` behaves as a collection (of numbers):

    for i in range(N):
        print("*")

In C, we need to explicitly update a state:

    for(int i = 0; i < N; ++i)
        puts("*")

## Variable

Variable, its value, ...
Defining and updating (assignment), using, ...

http://code.globaloria.com/
"Variables control many things at once."

https://www.khanacademy.org/computing/computer-programming/programming/variables/p/intro-to-variables
"Variable is a *name* or a *placeholder* for something else. A big *bucket* with a name on it..."
Read `x = 1` as "x *gets* 1"

Variables can be introduced usefully before expressions, operators, for example in Processing:

    size = 50;
    ellipse(100, 100, size, size);

... and expressions added later, based on variables:

    x = 50;
    ellipse(x, 50, 100, 100)
    ellipse(x + 20, 60, 60)

Exercise: Modify a variable used in multiple places.
Exercise: Use a variable in expressions.
Exercise: Define new variable. (How to justify?)

## Collection

Arrays, ...

## Iteration

Iteration is similar to repetition, except that there is a context that changes (current item).

Range-based:

    for e in list:
        print(e)

Index-based:

- Python:
    for i in range(len(list)):
        list[i]

- C++:
    for(int i = 0; i < N; ++i)
        array[i]

## Truth

Comparison using `==`, `<`, etc.


## Conditional

NOTE: To justify the use of conditionals, we need a variable context, for example:

- some kind of input to the program.
- embedding "if" in a loop
- embedding "if" in a function

If:

    x = input()
    if has_some_property(x):
        print(x)
    print("done")

If - else:

    x = input()
    if has_some_property(x):
        print("yes")
    else:
        print("no")
    print("done")

In a loop:

    for x in list:
        if x < 5:
            print(x)

## Conditional repetition

    while guess != secret:
        guess = input("Enter your guess: ")

NOTE: To justify conditional repetition, the problem must be such that simple repetition or iteration is not useful.
For example, the condition must depend on an unpredictable output of the loop body.

NOTE: Traditional C for loop falls into this category and is also easily justified,
since an equivalent to Python's `for i in range(N)` is not in the standard library.


## Function definition

### Use already written function

Function is already written. Goal must be achieved by calling funcion and without modifying.

In practice:

- [Code.org's "Minecraft: Hero's Journey"](https://studio.code.org/s/hero)


### Write function already in use

Function is already called, but not written. Goal must be achieved by writting the function and without modifying other code.


### Recursion?
