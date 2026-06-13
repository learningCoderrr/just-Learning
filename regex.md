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
