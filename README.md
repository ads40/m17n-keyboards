# Custom input sources for `ibus-m17n`

Classical Greek input source is from:

- https://github.com/marczuo/grc-beta-code/blob/master/grc-beta-code.mim

For Sanskrit devanāgarī, just use the built-in sa-itrans.mim input source. There
are a couple of rough edges (ITRANS has <R> -> ऋ instead of <.r> -> ऋ) but
these are minor

Sanskrit transliteration input source has been built from tutorials:

- https://ubuntuforums.org/showthread.php?t=646207
- https://wikis.swarthmore.edu/ling073/Making_a_keyboard_layout_using_IBus

The second set of instructions are important to avoid playing with system-level
files but instead just adding per user features.

Latin input source is based on the Sanskrit transliteration input source, for
consistency across input methods when working directly with Roman text.

## Installing

Make sure that the `ibus-m17n` library is installed.

Copy these `.mim` files to `~/.m17n.d/` (create it if needed) and then log out
and back in again to restart `ibus`.

Make the input sources active via Settings > Keyboard > "+ Add Input Source".

## Modifying

The `.mim` file appears to be Lisp.

For details of the format and features:

- https://www.nongnu.org/m17n/manual-en/index.html
- https://www.nongnu.org/m17n/manual-en/m17nDBTutorial.html

