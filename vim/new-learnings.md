# New things I learned with vim

## `gn`

Search forward for the last used search pattern, like with n, and start Visual mode to select the match. If the cursor is on the match, visually selects it. If an operator is pending, operates on the match.

dgn will delete the next match, cgn will do the same then switch to Insert mode, gUgn will convert the next match to uppercase characters. Look up :h operator for more ideas.

### Using gn with the dot command

Suppose that we have a document containing several occurrences of the word ‘Normal’ and we’d like to change each occurrence to ‘Visual’. We can run /Normal to search for the word ‘Normal’, then type cgnVisual\<Esc> to change the next match to the word ‘Visual’. You’re probably familiar with the technique of pressing n. to repeat the change for each subsequent match. In Practical Vim, I call this pattern of usage The Dot Formula. It lets us use two keystrokes per change.

In this context, we can do better. The dot command repeats the last change, which is equivalent to typing cgnVisual\<Esc>. We could translate that into plain English as: “change the next match”. We don’t have to press n. because . does the job by itself. That makes it just one keystroke per change!

## `gN`

like `gn` but searches backward

## `:norm`

Vim’s :norm command allows you to execute normal mode operations from the command line. By combining with %, we can run a sequence of operations on an entire file:

## `gv`

Start Visual mode with the same area as the previous area and the same mode. In Visual mode the current and the previous Visual area are exchanged. After using "p" or "P" in Visual mode the text that was put will be selected.

## `CTRL-A`

Add [count] to the number or alphabetic character at or after the cursor.

## `CTRL-X`

CTRL-X Subtract [count] from the number or alphabetic character at or after the cursor.
