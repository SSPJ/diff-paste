## Diff Paste Readme

Diff Paste is an interactive Bash script to call a diff tool with pasted (or typed) content.

I wrote it because I have frequently found myself wanting to paste two short (or not so short) snippets of text into a Bash shell and see whether they are different.

### Usage


```
$ ./diffp
Paste or type the first text now (press Enter, Ctrl-d when done):
this is a 
short story
about a bat and a dog
who go on 
adventures
Paste or type the second text now (press Enter, Ctrl-d when done):
this is a 
short story
about a cat and a dog
who go on 
adventures
-----------------------------------------------------
| Your diff taken at 10:27 (1573662472) starts here |
-----------------------------------------------------
3c3
< about a bat and a dog
---
> about a cat and a dog
-----------------------------------------------------
| < this line came from your first input            |
| > this line came from your second input           |
-----------------------------------------------------
```

Or when the snippets are identical:

```
$ ./diffp
Paste or type the first text now (press Enter, Ctrl-d when done):
a cat
Paste or type the second text now (press Enter, Ctrl-d when done):
a cat
-----------------------------------------------------
| Your diff taken at 10:33 (1573662793) starts here |
-----------------------------------------------------
|                                                   |
| No diff. Inputs were identical.                   |
-----------------------------------------------------
```

### Installation

Download the `diffp` file and put it somewhere.

You may need to make it executable with `chmod +x diffp`.

I recommend putting it somewhere on your path, like in `/usr/local/sbin/`, so that you do not have to be in the same directory to call it.
