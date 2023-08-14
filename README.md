# HEXCODE Matcher

## Welcome To The HEX GIST

Now if you have stumbled upon this page, the algorithim has brought you upon this repository to look at. You came here to find ways to use a hex matcher or at least get an idea on how to use one.

Whether that project pertains to e-commerce where you need the system to parse and send out information for product description for user and business side, a way develop/implement an eyedropper tool for your software, or maybe you want to start your own adult-coloring book website/app for your own coding hobby. 

I am here to help. So where to start.

Well you're gonna need this in your code.

```
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/ 
```

What's this you ask? It's called a regex or a regular expression, even though it kinda looks a little funky.

## Table of Contents

- [What Is A Regex](#What-Is-A-Regex)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

### What Is A Regex 

Regexes are sequences like the one above, are sequential patterns of characters of text, numbers, and metacharacters that are meant to serve as a way to parse through  values to attain a match on a certain and/or range of an input.

You may use these regexes for form validations for certain characterisitics that are required.

For Example, if you were to sign up/log in for a website but need users to have them end in a certain domain whether for public or certain organizational domain names like @gmail or @workemail, which is followed by another verifier where they need to end the email address with a .com, .co, .gov, and other entities of a domain. They can also set up values that are invalid to the field of certain characters 

Right now we are working with a color matcher regex. There are more like it, but this one is fine.


## Starter Fields
```
/^ and $/
```

Are openers and closer for the regex. In the middle is where the filter values and parsers are applied, i.e the code snippet:

```
#?([a-f0-9]{6}|[a-f0-9]{3})
```

Its much like a opening and closing element tags that HTML elements need to hold content. <br> Like `<div></div>`



## Hex Starter
```
#
```

For this part of the code it acts as a start of the filter that the hex needs to start with.

## Quantifier
```
?
```

This a quantifier or more specifically a Zero Or One Quantifier. Here it can be read through the pattern as a one or the other. In this instance the hex can normally start with a #ffffff or just plainly a ffffff;

## Groups

```
()
```
The purpose of this allows you to effectively create different sections of the regex and defining the range specifier and parser.


## Six Code Color Range
```
[a-f0-9]{6}
```

Here in this snippet the brackets are given a range asking the regex to parse through a-f earlier I mentioned before of a hex color of white but through the combination of 0-9 you get different shades of white like alice blue, whose hex color is F0F8FF;'
'

## Pipe Symbol

```
|
```
 Although it looks like an uppercase "I", it is actually the seperator character |. This differs from the Quantifier mentioned earlier wheres is that it chooses to be a part of the range and can be included or ignored. Whereas this one is can be used and applied for two or more situations.

## Three Code Color Range 

```
[a-f0-9]{3}
```

Works like the three color code range, bu this one functions as a shortener for six color codes that 