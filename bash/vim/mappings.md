# About

`*` mappings are my custom mappings.

My nvim configuration can be found in https://github.com/jordisantamaria/nvcode


Basics
===============================================================================

```
nvim {filename}    # Enter nvim
:e [filename]      # Open or create a file if not exist
:f [filename]      # Find and open file relative to :set path?

:q                 # Quit window, If last window then quit nvim
:qa                # Quit all windows
:q{a}!             # Force quit window/s, even If not saved
:w                 # Save buffer
:wq                # Save buffer and quit window

u                  # Undo
C-r                # Revert Undo
```

Change vim modes
===============================================================================

## To normal mode

```
ESC            # Normal mode
C-c            # Normal mode
jk or kj       # Normal mode*

C-o            # Normal mode 1 command
```

## To Edit mode

```
i              # Before cursor
I              # Start of line
a              # After cursor
A              # End of line
o              # New line after current
O              # New line before current
c              # Delete motion
C              # Delete until end line
```

## To Visual mode

```
v               # Visual mode
V               # Visual line mode
C-v             # Visual block mode
```

Move with Motions
===============================================================================

## Basic

```
{n} h               # Left n times
{n} l               # Right n times
{n} j               # Down n times
{n} k               # Up n times

```

## Word

```
w                   # Next word (word like  It_s-a_word1 )
W                   # Next WORD (WORD ends in white space)
e                   # End of word
b                   # Back to last word
\w                  # Next part of a word when camelCase or snake-case or like-that
\e
\b
```

## Line

```
0                   # Start of line
$                   # End of line
^                   # First letter of line

H                   # Start of line*
L                   # End of line*

f [letter]          # Find and go to next letter in line
F [letter]          # Find and go to letter in left direction
t [letter]          # Find and go to next letter - 1
T [letter]          # Find and go to letter -1 in left direction
;                   # Next letter found in line
,                   # Last letter found in line
```

## Jumps

```
%                   # Go to pairing of <>{}[]()
{                   # Go to last empty line
}                   # Go to next empty line
(                   # Go to last paragraph border (line before empty line or empty line)
)                   # Go to next paragraph border (line before empty line or empty line)
M                   # Middle of screen

[n]g                # Go to line n
gg                  # Go to start file
G                   # Go to end file
[n]%                # Go to n % of file
```

Editing Text
===============================================================================

[operator][motion | object]

## Operators

```
d                             # Delete text and yank to noname register
dd                            # Delete line
D                             # Delete line
c                             # Change, same as delete but change to insert mode
cc                            # Change line
C                             # Change line
{"[register]}y                # Yank (copy text)
gu                            # To lowercase
gU                            # To Uppercase
=                             # Fix identation

R                             # Replace with yank text*
cs[curent][new]               # Change surround*
ys[motion][surround]          # Include surround*
ds[surround]                  # Remove surround*
```

## Objects

```
iw          # Word
i(          # Content inside ()
i)          # Content inside ()
a(          # Same, including ()
a)          # Same, including ()
i{          # Content inside {}
i}          # Content inside {}
a{          # Same, including {}
a}          # Same, including {}
i[
i]
a[
a]
i"
i'
a"
a'

i/          # Text founded by / or ?*
ii          # Identation text*
il          # Line*
ie          # All File content*
iv          # Word part when camelCase, snake_case...*
av          # Same but remove - or _ also*

```


Edit
===============================================================================

```
leader-/           # Comment line*
crs                # Word to snake_case*
crc                # Word to camelCase*
crm                # Word to capitalize*
cr<space>          # Separate word parts with space*
<                  # Tabulate left*
>                  # Tabulate right*
```

Changes
===============================================================================

```
.                  # Repeat change

[n]C-a             # Increase number n times
[n]C-x             # Decrease number n times

r                  # Replace character
x                  # Remove character
```

## Insert mode
```
C-u          # Remove until line start
C-w          # Remove last word
C-r          # Paste register
```

Command Line
===============================================================================

```
C-b          # Start of line
C-e          # End of line
C-u          # Remove until line start
C-w          # Remove last word
C-r          # Paste register
!            # Run external program
```


Scrolling
===============================================================================

```
C-F         # Bottom 100% screen
C-B         # Top 100% screen

C-d         # Bottom 50% screen
C-u         # Top 50% screen

C-e         # Bottom 1 line
C-y         # Top 1 line

zz          # Center to cursor
zt          # Cursor in top
zb          # Cursor in bottom
```

Quicklist
===============================================================================

-R means read only, to prevent changes

```
:vimgrep -R [regex] [glob file]  # Find regex in files and put in quicklist
:grep -R [regex] [glob file]     # Same but with OS grep instead of vim grep
```

Git
===============================================================================

```
:G               # Git status
leader-gb        # Git blame
leader-gB        # Open file in remote repo
leader-gd        # File diff
leader-gR        # Revert buffer changes
leader-go        # Open remote repo

leader-g1        # DiffGet left in merge
leader-g3        # DiffGet right in merge


leader-qg        # Quickfix git commits changes

leader-sb        # Search and jump to branch by telescope
leader-sc        # Search and jump to commit by telescope
leader-sC        # Search and jump to current branch commits by telescope
leader-ss        # Search and jump to changed files by telescope
```