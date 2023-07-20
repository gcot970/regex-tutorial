# Tutorial for using Regular Expressions with Email Addresses

  

Introductory paragraph (replace this with your text)

  

## Summary

  

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

I have chosen to break apart the regular expression for email validation.
>/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/



Code example:

    function  isValidEmail(input) { 
	    const mailformat = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
	    if(input.value.match(mailformat)) {
		    alert("This is a valid email address");
		    return true;}
		else {
		    alert("Please put in a valid email address"); 
			return  false; } }

  
  

## Table of Contents

  

- [Anchors](#anchors)

- [Quantifiers](#quantifiers)

- [Grouping Constructs](#grouping-constructs)

- [Bracket Expressions](#bracket-expressions)

- [Character Classes](#character-classes)

- [Character Escapes](#character-escapes)

  

## Regex Components

  

### Anchors
There is one anchor in this selected regex.
> /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})**$**/

The '$' is located at the end of the line to make sure the string matches with the pattern as expressed in the regex.

  

### Quantifiers
There is one group of quantifiers.
  > /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]**{2,6}**)$/

The {2,6} specifies that the third group should be at minimum two characters, and at maximum six characters.

### Grouping Constructs
The regular expression starts and ends with a '/' to denote a regular expression. Then, it has a '^' carrot key to denote the beginning of the string. 

For the first group, [a-z0-9_\.-], represents the username. It allows for characters a through z, numbers 0 through 9, and allows the characters ' . ', ' - ', and ' _ '. The '+' allows for the characters to repeat.

The '@' sign is the @ separating the domain and the username.

For the second group, ([\da-z\.-]+), represents the domain. '\d' allows for single digits (for example 0-9). Then, 'a-z' allows for characters a through z, and the characters ' . ' and ' - '. The '+' allows for the characters to repeat.

The '\.' matches a dot, which is required to denote the domain and the top-level-domain.

The last group, [a-z\.]{2,6}, represents the top-level-domain (com, net, org, biz, ...).  'a-z' allows for characters between a through z appear and a dot. The {2,6} specifies that it should have a minimum of two characters and a maximum of six characters.
  

### Bracket Expressions
There are three bracket expressions:

 - [a-z0-9_\.-] - This represents the 'username' of an email.
 - [\da-z\.-] - This represents the 'second level domain' of an email 
 - [a-z\.] - This represents the 'top level domain' of an email

  

### Character Classes

 - a-z - Allows for characters a through z to be used
 - 0-9 - Allows for digits 0 through 9 to be used
 - \d - Allows for digits 0 through 9 to be used

  

### Character Escapes

 - \. - Allows for a ' . ' period to be matched

  

## Author

  

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
