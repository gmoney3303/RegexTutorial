# Regex-Tutorial: Matching a Hex Value

## Introduction
Understanding regex will help in pattern matching within strings. This tutorial aims to help understand /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ regex,  used to detect a hex color code.
## Summary
The regular expression is used to judge if the string has a hexadecimal color code format. It can recognize both short and long hexadecimal color specifications (e.g., #0f9, or #00ff99).

## Table of Contents
1. [Anchors: (^ and $)](#anchors)
2. [Optional Character: (#?)](#optional-character)
3. [Hexadecimal Characters: ([a-f0-9])](#hexadecimal-characters)
4. [Quantifiers: ({6} and {3})](#quantifiers)
5. [Greedy and Lazy Match](#greedy-and-lazy-match)
5. [Examples](#examples)
6. [Author](#author)

### Anchors
The Anchors in a regex string are the ^ and $, the ^ will represent the start of the string and the $ represents the end of the string

-^#?([a-f0-9]{6}|[a-f0-9]{3})$ everything in between the ^ and $ will be representing what the regex is looking for.

### Optional Character
The optional character #? in the regex allows for an optional hash symbol at the beginning of the hexadecimal color code. This means it can match both color codes with and without the leading # symbol.

### Hexadecimal Characters
The [a-f0-9] segment within the regex represents the range of characters allowed in hexadecimal notation. It includes all characters from 'a' to 'f' and digits from 0 to 9.

### Quantifiers
Quantifiers ({6} and {3}) in the regex specify the length of the matched pattern. {6} requires a six-character match (e.g., #00FF99), while {3} allows for a three-character match (e.g., #0F9).

### Greedy and Lazy Match
Code Snipet: [a-f0-9]{6} Code Snipet: [a-f0-9]{3}

Quantifier: {}

Description: Greedy means match the longest possible string. Lazy means match the shortest possible string.

Example: w.+l matches well in well but the lazy w.+?l matches wel

### Examples
#0F9
This short format includes three characters representing RGB values. It matches the regex pattern.

#00FF99
A long-format hex color code comprising six characters for RGB values. It matches the regex pattern.

#G3E589
This does not conform to the regex pattern because 'G' is not a valid hexadecimal character.
## Author
Garrett sheppard 
I am a new web developer learning more about web development to get a job.
https://github.com/
