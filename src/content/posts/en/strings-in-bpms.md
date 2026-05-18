---
title: 'Strings in BPMs'
description: 'Useful tips for using strings in BPMs.'
pubDate: 2026-05-18
tags: [kinetic, bpm, dashboards]
categories: [BPMs]
pinned: false
toc: true
---

# Declaring a String

```csharp
// [data type] [variable name] = [default value];
string myString = "Hello World";
```

# Using data in a string
Data can be dynamically added to a string using `string.Format()`.

```csharp
// Data
string userName = "Tom";
int userAge = 38;

// String with data
string greeting = string.Format("Hello {0}, you are {1} years old.", userName, userAge);

// Output:
// Hello Tom, you are 38 years old.
```
