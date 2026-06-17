# Delimiter

Delimiter are those which give's a limit to anything

```js
/*This is first and last forward and star are the delimiter which limits the comment*/
```

# Literal Characters

Those characters which present in a string and have no special character in regex or not a meta characters those characters meanly knows Liters characters .

# Meta characters (special characters)

Those characters which have some meaning for regex those area known as meta characters  
ex:- `.`,`{}`,`\n`,`$`,`^`,`[]`,`?`,`|`,`*`,`+`,`()`,`\r`,`\`,etc...

# Making Meta characters as a literal character

We use back slace `\` to make any regex special characters as a literal characters

```js
/\\n \\*/;

//created a space character to literal character with the help of backslace special character.
```

# Flags

1. `Global Flag(g)`=> this flag help to select all the pattern globally like select all the character which match with pattern.
2. `case-insensitive(i)`=> this flag used for case insensitive if the character is written in uppercase or lower not a matter it just select it.
3. `single-line(s)`=>this flag works with . (dot special character) to select all the new line which were not selected as default.
4. `unicode(u)`=> this regex flag used for selecting the pattern which were of different language character by the help of unicode ex:-`\u0454` after u 0 is mandatory.
5. `multi-line(m)`=> this m flag used in anchors . If wanted to check the value after ending or starting of every new line then we use this flag. If we only wanted to view the ending and last character then we would't user this flag

# Character set (character class)

we create a set of character inside square bracket `[]`
ex:-`[abcd]` => only this set of character is selected not a single character will selected

1. `Range`=> with the help of range we can provide a range of character according to the unique code of character. ex:- `[a-zZ-a]`
2. `Inverter or not` => if caret is written initially then it denoted as a special character or meta character .This special character make the set not means if anything is written in the character class then that will be not selected accept that all set's other character will be selected. ex:- `[^a-z_A-Z]`. If we write the `^`caret symbol after some character then it lose it's special ability ex:- `[hd^3-9]` this now select all the given set present in the set.

# Quantify

Quantify is used for tell the regex that how many u have to select the character means the quantity

1. `?` => if character is present or not (1 or 0) then select that text.
2. `+` => at least one single similar character to select text (1 or more text's according to set or text).
3. `*` => character present or not no matter it will select that text (0 or more then 0 text will be selected).
4. `{n}` => we can set specific n number of character should be written the pattern.
5. `{n,}` => add at least n number or more then n number character in pattern.
6. `{n,m}` => add at lest n number and less then equal to last m numbers in pattern.

# Anchor

This anchor works when we want to check the word is that word is present in initially or in last of the word or in new line (only works when multi-line flag is on).

1. `^` => this flag check the initial value in the hole sentence or in new line.
2. `$` => this flag check the last value in hole sentence or in a new line.

example:-

```js
/^Mrs? [A-Z][a-z]{2,}/gim;
// selects Mr Prabhu
// select Mr Prakas
// not selects mr mohan
```

# ShortHand or predefined character (class or sets)

Short Hand for writing character class

1. `\d` => [0-9].
2. `\w` => [a-zA-Z0-9_].
3. `\s` =>[\n ] can select those which has space,tab space,new line(line break).
4. `\D` => [^0-9]
5. `\W` => [^A-Za-z0-9_]
6. `\S` => [^\n ] would't select space,tab space or new line (line break) other pattern will be selected

# Alternative or (OR operator)

This alternative named special character used for spurting the pattern differently if one pattern got correct then other pattern will not works
`symbol` => `|`
example

```js
/hello sir [A-Z][a-zA-Z]{2,}| what happen [A-Z][a-zA-Z]{2,} kumar/g;
```

# Groups

A group in regex is a way to bundle multiple pattern pieces together so they can be treated as one unit.

There is two typeof Group in regex

<details>
<summary>Capturing Group</summary>

- This group track the patten and also capture it for the feature use .
- We can backtrack it means reUse that captured patten again in regex using `\1,\2,\3 ... \\n` up to `n numbers` every number represent the different capturing group `()`.
- We can also provide a capturing name like this --> `(?<sirName>Mr|Mrs)? [A-Z][a-z]{2,}\.Hello \k<sirName>` or we can also use number for the capturing `\1` in the place of `\k<sirName>`.
- We needed then use this group if not then use non-capturing group . Because when it captures the pattern then it will store in memory so if there is no need then would not capture it.
</details>

<details>
<summary>Non-Capturing Group</summary>

This group would `not capture any thing just match the pattern` . We would `not able to backtrack` it.  
use => `(?:Hello)? [A-Z][a-z]{2,}`

</details>

```js
/(?:Mr|Mrs)? [A-Z][a-zA-Z]{2,}/g;
// Mr Prabhu
// Mrs Prakash
// Pramod
/(?:3[01]|0[1-9]|[12]\d)(?<split>\\|\-)(?:1[0-2]|0[1-9])\k<split>20\d{2}/g;
// 03-12-2000
// 12\01\2034
```

# Word Boundary and Non-Word Boundary

<details>
<summary>Word Boundary</summary>

This is denoted with `\b` this works which pattern match with this regex pattern [^a-zA-Z0-9_] `\W`

</details>

<details>
<summary>Non-Word Boundary</summary>

This is denoted with `\B` this works which pattern match with this regex pattern [a-zA-Z0-9_] or `\W`

</details>
