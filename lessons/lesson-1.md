# Lesson 1 - Variables and If Statements

At this point, you should be able to run write dart programs in VSCode and run them on your computer. You should have a basic _Hello World_ program.

## Variables
Variables are places we can store information on the computer. We can store all sorts of information in variables: numbers, text, lists, ect. They look like this:

```dart
var variableName = 4;
var variable2 = 'Hello world';
var variableThatsTrue = true;
```

Variables can also be reassigned, which means we're changing them later instead of creating an new variable. Because of that, we don't use the `var` keyword.

```dart
// Since we've already specified `variableName` as a variable up above, we shouldn't use `var` again.
variableName = 2;
variable2 = 'Hi mom';
```

### Variable Names
Variables can be named almost anything. They just need to be letters (upper or lowercase) or digits 0-9 (although they can't **start** with a digit), and underscores (`_`). You'll notice that you can't put any special characters in a variable, and you cannot put a space.

While variables _can_ be anything, the common convention is to use camel case, where the first word in a name is lowercase, and subsequent words start with an uppercase:
- `thisIsALongVariableName`
- `shortVar1`

### Types

Each variable has one type of data and keeps that type forever.

- booleans (a value that's either `true` or `false`, called `bool` in dart)
- integers (whole numbers, called `int` in dart)
- decimal numbers (called floating point numbers or `double` in dart)
- `String`s (just a list of characters like a word or sentence)
- `List`s of elements (sometimes called arrays)
- Complex `Object`s that represent more complex data like an address, user, ect

This example shows what happens when you try to assign a value of a different type to your variable.

```dart
var myString = 'a new String';
myString = 4; // ERROR - cannot assign a int to a variable of type String
```

You can create a new variable (called _declaring_ a variable) without giving it a value (called _assigning_ the variable) by specifying their type instead of using `var`:

```dart
int? myNumber;
String? aNewString;

// This is also valid
String tmpVar = 'Hi there';
```

### Final variables
If you don't want a variable to ever change it's value once it's set, you can replace `var` with `final`

```dart
final myVar = 5;
myVar = 10; // ERROR - Cannot reassign a final variable
```

## If Statements
Sometimes, we want to change what code is executed depending on the value of a variable. For example, if we have a R-rated movie on our streaming service, we'll ask the viewer for their age and store that in a variable. Then, if they are underage, we'll show them a message that they can't see the movie; otherwise, we'll show them the movie.

In programming, these are accomplisehd by _if statements_ (also called _conditionals_). They look like this:

```dart
var viewerAge = 15

if (viewerAge < 17) {
  print('Youre too young for this movie');
} else {
  print('Enjoy the show');
}
```

Let's break that down:
1. `if (condition)`: this first line start the statment. the _condition_ is a piece of code that evaluates to a boolean (`true` or `false`). In the above example, our condition is `viewerAge < 17`, which returns true if the `viewerAge` variable contains a values less than `17`. 

2. `{` and `}`: these curly braces are called a _code block_. They specify a chunk of code that is grouped together in those braces. The first code block will be executed if they expression is true.

3. `else`: this keyword means that if the condition is false, do this code block instead.

### Operators
In the above example, we use the `<` character to mean "less than". We call these operators, and there are several you can use to compare variables and other values.
- `<` less than
- `<=` less than or equal to
- `>` greater than
- `>=` greater than or equal to
- `==` exactly equal to (NOTE: not `=`, that's used for assigning values)
- `!=` not equal to (anything but)

### Else if
Sometimes, it is helpful to chain together if statements to match multiple conditions. For example, in a video game, if you press the `w` key, you should move forward, but if you press the `d` key, you should move right. We can achieve this using the `else if` statement.

```dart
var key = 'a';

if (key == 'w') {
  print('moving forward');
} else if (key == 's') {
  print('moving backward');
} else if (key == 'a') {
  print('moving backward');
} else if (key == 'd') {
  print('moving backward');
} else {
  print('unknown key');
}
```

### Examples
Here are some examples to get you're brain thinking about them. Try to predict what they will print, then run them to see if you're right.

```dart
var myVar = 2;

if (myVar == 2) {
  print('1');
}
```

```dart
var myVar = 2;

if (myVar == 2) {
  print('1');
}
print('2');
```

```dart
var myVar = 2;

if (myVar > 2) {
  print('1');
}
print('2');
```

```dart
var myVar = 2;

if (myVar > 2) {
  print('1');
} else {
  print('3');
}
print('2');
```

```dart
var myVar = 2;

if (myVar > 2) {
  print('1');
} else if (myVar <= 2) {
  print('2');
} else {
  print('3');
}
```

```dart
var myVar = 2;

if (myVar > 2) {
  print('1');
} else if (myVar <= 2) {
  print('2');
} else if (myVar == 2) {
  print('3');
} else {
  print('4');
}
```