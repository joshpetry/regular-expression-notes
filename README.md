# regular-expression-notes

What is a regular expression?

  A regular expression is a way to describe a pattern in a string.

What is a Regex Parser?

  A Regex parser requires two things. A expression (pattern) and string to match.
  The parser walks through the expression character by character and compares it to the string.

What is Validation?

  The process of guarding against receiving bad or inaccurate data



REFERENCE

Basics

?       Makes preceding character optional

[]      Character Set
        Regular expressions are case sensitive by default. To bypass this use a character set []
        Wrap characters with [] and uppercase/lowercase variant to cover both (e.g. [Tt])
        No matter how many characters we put within the [] only one position will be matched.

[A-Z]   Ranges of characters.
        For upper and lowercase [A-Za-z], for numbers [0-9], you can do both [0-9A-Za-z]

\       Escaping. E.g. if i wanted to use a . (even though its a wildcard), I would use \.

^       beginning of string

$       end of a string


Flags

i       Case-insensitive

g       Global

m       Multiline


Using Wildcard Characters

[0-9]   =   \d

[A-Za-z0-9_]   =   \w     Match all alphanumeric characters and underscore

\s    whitespace

\D    not digit

\S    not whitespace


Finding Repeated Characters

*      0 or more word characters

+      match 1 or more word characters, matches previous expression 1 or more times

{3}    matching 3 characters

{3,}   matching 3 or more characters

{3,5}  matching 3 - 5 characters


Excluding characters

[^@]   match any character except @ character


Alternation

|     similar to or operator

()    used to group parts of expressions


Using regular expressions in javascript

/regExpression/       to create a regular expression (literal syntax shown)

regex.text(testString)    => true/false

string.replace(regex, replacementString)    => newString        
        Takes string, finds regex in string, and replaces regex with replacement
