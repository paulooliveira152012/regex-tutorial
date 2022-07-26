# Regex, analyzing an email structure 

In this documentation you will be presented with a walkthrough of an email regex and its components followed by descriptive sections explaining how each character or set of characters come into play to validate the email format. The purpose of this documentation is to provide a basic understanding of how each portion of the regex functions so that the same logic may be implemented by users. 

The regex that we will be analyzing will be composed of a set of rules for letters, numbers, and special characters implemented in both literal and meta characters. The example is as follows:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
So what’s going on here? Generally speaking, we are specifying a set of rules that defines where a set of characters should be (/^), which type of characters is allowed to be used and where by grouping them in a specified location ([a-z0-9_\.-]+), limiting a set of characters to be allowed in a specific area ( _ \ . - ), what specific characters should be allowed and where (@), placeholders for any character the user might choose (.), ranges of up to how many times a character can be repeated in a specific delimited area {2,6}, and the end of rules to be applied in the validator.

Literal character → literally a specific character we want to find or use.
Meta character → a character that indicates a more generalized pattern


## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

I’ll be describing an email validator regex and explain how each character or set of characters promotes rules to be taken into consideration. I will be going over the following regex: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/



## Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Regex Components individual characters](#Regex-Components-individual-characters)

## Regex Components

### Anchors
Anchors are delimiters that either set the starting or the ending  position of the set of rules we  want to apply as the regex. The starting anchor is represented by /^ while the ending anchor is represented by $/. So as for an example of anchors in action we can use: /^abc&/ meaning that “abc” are the roles in action.

### Quantifiers
Quantifiers refer to the previous set of rules which allow users to utilize unlimited or limited but repetitively,  the previously represented characters. They are found at the end of a class and in our case, it is represented by the + sign on our example.:
[a-z0-9_\.-]+. Because we have the + sign there, any email containing indefinite numbers of letters ranging from A to Z, and an indefinite number of numbers ranging from 0 to 9, as well as the indefinite number of _, . and - characters.

### OR Operator
Or operators promotes a possibility between characters to be accounted for during a query. Although our example does not contain it, it could be used by using the | operator. As an example; abc|ABC would return abc or ABC and they both would be applied in the regex configuration.

### Character Classes
Character classes delimit a specific group of characters. In our example, we have three examples of  character classes, for they all contain characters in them to be possibly used. They are [a-z0-9_\.-], [\da-z\.-] and [a-z\.]. Character classes are delimited within an opening and closing bracket [ characters in here ], and we can specify the rules as for what we want to look for or validate. In our example, “any letter between a and z, any number between 0 and 9, and the following characters: _ . -”.

### Flags
Flags are letters that represent specific configurations that can modify the behavior of a given pattern. There are 6 tags, and each one has one functionality. They are g, i, m, u, s, and y. Therefore, because they are to enhance the search, their use is optional. 
i (Ignore casing) → nulls the expression’s search case-sensitivity
g (Global) → Makes the expression search for all occurrences.
s (Dot All) → makes the dot (.) match newlines as well.
m (multiline) → makes delimiting characters match the beginning and ending of each line.
y (Sticky) → starts the search from a specific indicated index.
u (unicode) → makes the expression assume individual characters as code points instead of code units. They can be applied in both // notation as well as RegExp() form. Example: /pattern/flags and new RegExp('pattern', 'flags'. → new RegExp('a', 'i'.

### Grouping and Capturing
Grouping and capturing are necessary to specify which rules apply to each area of the search, almost like “parameters”. And in order to apply them, we use parenthesis. For example, in our expression we have ([a-z0-9_\.-]+), the parenthesis allow us to group everything inside of it together so that we may utilize the quantifier + on the entire set of characters.

### Bracket Expressions
Bracket Expressions allow us to tell regex to choose only one out of several characters, being them within a range of 2 extremes or literal characters. We apply them through square brackets. From the example we have:  [a-z0-9_\.-], in this case, the search and\or replace will look for patterns that have either of the characters represented inside the square brackets.


## Regex Components individual characters
An individual breakdown of each character and how they affect the regex:
/ → delimiter indicating the beginning of the regex specifications
^ → stating that the rules to elements starts off from the beginning
( → opening grouping delimiter 
[ → opening character class delimiter
A → starting character from
- → “through” specifying the range of characters
Z → ending point at
0 → starting at number
- →“through” specifying the range of characters
9 → ending at number
_ → matches this character
\. → matches this character (.)
- → matches this character
] → closing character delimiter
+ → implicates that the previous token can be repeated many times ([content])
) → closing group delimiter
@ → matches this character
( → opening grouping delimiter 
[ → opening character class delimiter
\d → matches a digit, anything from 0-9
A-z → range between a through z
\. → matches this character (.)
- → matches this character (-)
] → closing character delimiter
+ → implicates that the previous token can be repeated many times ([content])
) → closing group delimiter
\. → matches this character (.)
( → opening grouping delimiter 
[ → opening character class delimiter
A-z → range between a through z
\. → matches this character (.)
] → closing character delimiter
{2,6} → implicates that the previous token can repeat from 2 to 6 times
) → closing group delimiter
$ → states the end of rules to be applied
/ → delimiter indicating the end of the regex specifications


## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

This gist was created by Paulo Oliveira, a soon to be full stack junior web developer. Currently attending Rutgers University full-stack web development bootcamp. Github profile: paulooliveira152012
