[Back to the homepage](../README.md)

# Strings

Contents:
- [1. String constants](#1-string-constants)
- [2. Searching for a characters](#2-searching-for-a-characters)
- [3. Counting characters](#3-counting-characters)

## 1. String constants

> A string constant, or string literal, is a sequence of zero or more characters surrounded by double quotes:
>
> ```c
> "I am string";
> ```
>
> or empty string:
>
> ```c
> "";
> ```
>
> The quotes are not part of the string, but serve only to delimit it. String constants can be concatenated at compile time:
>
> ```c
> "hello," " world";
> ```
>
> is equivalent to:
>
> ```c
> "hello, world";
> ```
>
> Technically, a string constant is an array of characters. The internal representation of a string has a null character `'\0'` at the end, so the physical storage required is one more than the number of characters written between the double quotes.
>
> Hence, to declare a string one should use an array of characters:
>
> ```c
> char message[] = "hello";
> ```
>
> is equivalent to:
>
> ```c
> char message[] = { 'h', 'e', 'l', 'l', 'o', '\0' };
> ```
>
> Here is an example of writing string to a standard output:
>
> ```c
> char message[] = "hello, world";
> printf("%s", message);
> ```
>
> Here is an example of reading string from a standard input:
>
> ```c
> char message[20];
> scanf("%s", message);
> ```

Ask for user's name, surname, and age. After receiving all the data, print a greeting.

All the messages should be declared as a characters array, for example:

```c
char name_question[] = "What is your name?";
```


Sample output:

```
What is your name?
Nick

What is your surname?
Smith

What is your age?
19

Long time no see you, Nick Smith. You already 19 years old!
```

## 2. Searching for a characters

Read a string from a standard input. Determine whether there is at least one character in the string ...

| Variant | Description              |
| ------- | ------------------------ |
| 1       | ... from `'a'` to `'d'`. |
| 2       | ... from `'e'` to `'h'`. |
| 3       | ... from `'i'` to `'l'`. |
| 4       | ... from `'m'` to `'q'`. |
| 5       | ... from `'r'` to `'u'`. |
| 6       | ... from `'v'` to `'z'`. |

If the required character was found, display it. Otherwise, display a message saying that the no one characters was found.

## 3. Counting characters

Read a string from a standard input. Determine how many in the string of characters ...

| Variant | Description                                      |
| ------- | ------------------------------------------------ |
| 1       | ... from `'a'` to `'d'` and from `'e'` to `'h'`. |
| 2       | ... from `'e'` to `'h'` and from `'i'` to `'l'`. |
| 3       | ... from `'i'` to `'l'` and from `'m'` to `'q'`. |
| 4       | ... from `'m'` to `'q'` and from `'r'` to `'u'`. |
| 5       | ... from `'r'` to `'u'` and from `'v'` to `'z'`. |
| 6       | ... from `'v'` to `'z'` and from `'a'` to `'d'`. |