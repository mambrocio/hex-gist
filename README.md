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

Code Structure In Order 

- [What Is A Regex](#what-is-a-regex)
- [Starter Fields](#starter-fields)
- [Hex Starter](#grouping-constructs)
- [Quantifiers](#quantifiers)
- [Groups](#groups)
- [Six Code Color](#six-code-color)
- [Pipe Symbol](#pipe-symbol)
- [Three Color Code](#three-code-Color)
- [Additional Codes](#additonal-codes)
- [Regex Playground](#regex-playground)
- [Contact](#contacts)



## What Is A Regex 

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

Its much like a opening and closing element tags that HTML elements need to hold content. <br> Like `<div></div>`.



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


## Six Code Color
```
[a-f0-9]{6}
```

Here in this snippet the brackets are given a range asking the regex to parse through a-f earlier I mentioned before of a hex color of white but through the combination of 0-9 you get different shades of white like alice blue, whose hex color is F0F8FF. This part seeks out the for color combinations of a six character combination of letters and numbers. With the brackets {} seeking a strict number character requirement.


## Pipe Symbol

```
|
```
 Although it looks like an uppercase "I", it is actually the seperator character |. This differs from the Quantifier mentioned earlier wheres is that it chooses to be a part of the range and can be included or ignored. Whereas this one is can be used and applied for two or more situations.

## Three Code Color

```
[a-f0-9]{3}
```

Works like the six color code range, but this one functions as a shortener for six color codes that you would be chosen to be needed. For example hex color CC00aa is shortened to C0a. This one is a strict 3 color code.

## Additional Notes 

This does need to be expanded upon. If you were to input hex codes that is possibly out of range or possibly missing some characters and you wanted to get the nearest color code, as a suggestion for nearest color combination you would need to write some new regex for it.

Possible structures you need to put in to a new regex.

#### Color Library

Import a color library from an npm or make your own custom library or array.

#### Quantifiers

```
{min, max}
```

You can start here setting a character code of mimnimum and maximum characters.

#### Assertions and Look Arounds

Positive Lookaheads
```
?=
```

Will find mathches ahead of a characters combinations. 

For example, f(?=0) will try to match to f0f or f0A, but the outside character and the character inside the paranthesis will need to be followed up. Characters will not be matched if it is 0fb or bf0.

Negative look ahead
```
?!
```
Negative look arounds will ty to look to see if the positive lookahead to see if the pattern does not follow the match. Similar to the positive look aheads but the character inside the paranthesis is prioritized followed by the character outisde.


Positive Look Behind
```
?<=
```
This will seek out charatcters towards the end of a string but must still be followed up in order.
For example the (?<=2>)3 codes need to match with f23 or a23 but not 23f.

```
?<!
```

This will seek out characters in between but not together.

(?<!yc)5 will match with 55c or 5fc but not f5c.

## Regex PlayGround 

[Regex Tester](https://regexr.com/) - Use this to play around with your hex color regex and other regex here it allows you to sign in and have your patterns and WIP to be saved along with a cheat sheet and community made patterns.

## Contacts

[Github](https://github.com/mambrocio)
