# What's new in Robot Framework 5?

[Robot Framework 5](https://robotframework.org/) is fresh out of the oven!

Whether you are implementing tests or automating processes, this powerful Python-based open-source automation framework provides a lot of flexibility and power in your daily development.

## Error handling: `TRY` / `EXCEPT` / `FINALLY`

Robot Framework 5 introduces native error-handling support with the `TRY` / `EXCEPT` / `FINALLY` statements.

Python, the programming language powering Robot Framework, already supported [try-catch error-handling](https://docs.python.org/3/tutorial/errors.html#handling-exceptions). Now the human-readable Robot Framework syntax supports the same!

```robot
*** Tasks ***
TRY / EXCEPT / FINALLY
    TRY
        Fail    Catastrophic failure! 💥
    EXCEPT
        Log    Catches any exception.
    FINALLY
        Log    FINALLY is always executed.
    END
```

## `WHILE` loop

It's `FINALLY` here! The native `WHILE` loop keeps looping as long as the given condition is true:

```robot
*** Tasks ***
WHILE: The infamous infinite loop
    WHILE    True
        Log    Oh no. This is an infinite loop! 😱
        Log    Do not try this at home.
    END
```

## Inline `IF` statement

Short and simple conditional statements can now be written on one line thanks to the inline `IF` support:

```robot
*** Tasks ***
Inline IF: No need for IF / END construct
    IF    True    Log    Inline IF is nice!
```

Less lines is not _always_ better - common sense recommended! 😅

```robot
*** Tasks ***
Inline IF / ELSE IF / ELSE: Not pretty but works!
    IF    False    Log    False    ELSE IF    False    Log    False    ELSE    Log    True
```

## `BREAK` and `CONTINUE` constructs

Use `CONTINUE` to skip a loop iteration or `BREAK` to exit the loop.

## Learn more

- [TRY / EXCEPT / FINALLY exception catching and handling in Robot Framework](https://robocorp.com/docs/languages-and-frameworks/robot-framework/try-except-finally-exception-catching-and-handling)
- [While loops in Robot Framework](https://robocorp.com/docs/languages-and-frameworks/robot-framework/while-loops)
- [Conditional IF / ELSE IF / ELSE execution in Robot Framework](https://robocorp.com/docs/languages-and-frameworks/robot-framework/conditional-execution)
