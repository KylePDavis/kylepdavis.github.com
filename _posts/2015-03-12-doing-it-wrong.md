---
tags: apple iphone techtalk programming doingitwrong gimme protip bash shell
---


### projects

- pushed `gimme` to GitHub ~~*late* last night~~ early this morning -- https://github.com/KylePDavis/gimme


### personal

- taking vacation Friday and Monday so I will probably get more done on my pet projects


### random

I just realized that I've been using my earbuds (from Apple, came with my iPhone 6 Plus) all wrong.

Maybe you have too -- find out:

1. push them all the way in
2. then pull them back out just slightly
3. rotate them until the sound is at it's peak quality and volume
4. figure out how to do this every time


### protips

- `bash`:
    - open the current line in your `$EDITOR` by pressing `Ctrl-X` then `Ctrl-E`
    - string manipulation (faster though admittedly a bit cryptic)
        - `${FILE##*/}` - like `basename`; removes longest leading `*/`
        - `${FILE%/*}` - like `dirname`; removes longest trailing `/*`
    - the `for` loop defaults to iterating over the `"$@"` list so you can simply say `for ARG; do` to loop over all args
    - use the `[[` rather than the `[` -- it has more features and fewer edge cases
    - `shellcheck` yo self before you shell wreck yo self
    - `read`ing is _fun_ ~~da~~ _mental_

        ```bash
        X $  find . -type f | while read F     # wrong: splits on IFS (whitespaces)
        √ $  find . -type f | while read -r F  # CORRECT! DO THIS!! ONLY!!!
        ```
