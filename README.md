# Steganography

## Installation

This software requires the [NetPBM][1] tools.
Once those have been installed,
simply copy the `hide` and `unhide` scripts
to a location in your $PATH.
If you want the manpages (`hide.1` and `unhide.1`),
place them in a reasonable directory.

[1]: http://netpbm.sourceforge.net

## Usage

To hide the image `secret.png` inside `base.png`,
placing the output in `out.png`:

    hide "base.png" "secret.png" | pamtopng > "out.png"

Then to reverse this process and extract the hidden image
to `extracted.png`:

    unhide "out.png" > "extracted.png"

All output images are written to the standard output.
Either argument to `hide` (but not both)
may be `-` to represent the standard input.
With `unhide`, standard input is used when `-` is given as an argument
or when no arguments are given at all.
