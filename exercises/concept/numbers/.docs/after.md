One of the key aspects of working with numbers in C# is the distinction between integers (numbers with no digits after the decimal separator) and floating-point numbers (numbers with zero or more digits after the decimal separator).

The two most commonly used numeric types in C# are `int` (a 32-bit integer) and `double` (a 64-bit floating-point number).

```csharp
int i = 123;
double d = 54.29;
```

Arithmetic is done using the standard [arithmetic operators][arithmetic-operators] (`+`, `-`, `*`, etc.). Numbers can be compared using the standard [comparison operators][comparison-operators] (`<`, `>=`, etc.) and the [equality-][equality-operators] operator (`==`) and [inequality][equality-operators] operator (`!=`).

```csharp
5 * 6;
// => 30

1.2 > 0.8
// => true

2 != 4
// => true
```

When converting between numeric types, there are two types of numeric conversions:

1. Implicit conversions: no data will be lost and no additional syntax is required.
2. Explicit conversions: data could be lost and additional syntax in the form of a _cast_ is required.

As an `int` has less precision than a `double`, converting from an `int` to a `double` is safe and is thus an implicit conversion. However, converting from a `double` to an `int` could mean losing data, so that requires an explicit conversion.

```csharp
int i = 9;
double d = 2.66;

// Safe conversion, thus implicit conversion
double fromInt = i;

// Potentially unsafe conversion, thus explicit conversion
int fromDouble = (int)d;
```

An `if` statement can be used to conditionally execute code. The condition of an `if` statement must be of type `bool`. C# has no concept of _truthy_ values.

```csharp
int x = 6;

if (x == 5)
{
    // Execute logic if x equals 5
}
else if (x > 7)
{
    // Execute logic if x greater than 7
}
else
{
    // Execute logic in all other cases
}
```

[arithmetic-operators]: https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/arithmetic-operators
[equality-operators]: https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/equality-operators
[comparison-operators]: https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/comparison-operators