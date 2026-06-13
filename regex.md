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

# Character set (character class)

we create a set of character inside square bracket `[]`
ex:-`[abcd]` => only this set of character is selected not a single character will selected

1. `Range`=> with the help of range we can provide a range of character according to the unique code of character. ex:- `[a-zZ-a]`
2. `Inverter or not` => if caret is written initially then it denoted as a special character or meta character .This special character make the set not means if anything is written in the character class then that will be not selected accept that all set's other character will be selected. ex:- `[^a-z_A-Z]`. If we write the `^`caret symbol after some character then it lose it's special ability ex:- `[hd^3-9]` this now select all the given set present in the set.
