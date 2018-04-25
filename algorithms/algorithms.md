# Essential Algorithms

Algorithms are listed in the recommended order of introduction. Later algorithms depend on introduction of earlier ones.

Unless otherwise noted, examples are in Python language.

## Conditional

If:

    x = input()
    if has_some_property(x):
        print(x)
    print("done")

If - else:

    x = input()
    if has_some_property(x):
        print("yes")
    else
        print("no")
    print("done")


## Repetition

### Until an effect is observed

Indirect cause:

    while elapsed_seconds() < 1:
        print("Hi")
        time.sleep(0.1)

    while guess != secret:
        guess = input("Enter your guess: ")

Direct cause:

    while x < 10:
        x += 2

### Conditional effect

    while x != 0:
        direction = input()
        if direction == "left":
            x -= 1
        else if direction == "right":
            x += 1


### For each item

NOTE: Requires explanation of *collections*.

    for e in list:
        print(e)

### For a subset of items

    for e in list:
        if has_some_property(e):
            print(e)


### Predefined number of times

NOTE: In many languages, there is no special syntax for plain repetition without variation. Instead, such repetition must be implemented using other concepts like iterating a collection (Python), or updating a state (C++). Therefore, it may be better to introduce it after those concepts.

In Python, `range` behaves as a collection (of numbers):

    for i in range(N):
        print("*")

In C, we need to explicitly update a state:

    for(int i = 0; i < N; ++i)
        puts("*")

## Fold

### Sum of items

    y = 0
    for x in list:
        y += x

### Sum of a property of items

    y = 0
    for x in list:
        y += some_property(x)

### Counting a subset of items

    y = 0
    for x in list:
        if has_some_property(x):
            y += 1

### Maximum item

    y = 0
    for x in list:
        if x > y:
            y = x

### Item with maximum property

    max_p = 0;
    y = 0;
    for x in list:
        p = some_property(x)
        if p > max_p:
            max_p = p
            y = x

