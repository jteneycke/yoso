# "You Only Script Once" 🎩
Instead of digging into the arcane incantations of bash or fish syntax,
just make a portable script that works across both, and lets you use
all the goodies that Ruby has to provide!

![script-writing-a-script](https://github.com/jteneycke/yoso/blob/master/escher.jpg)

## Installation
If you copy-pasta and clone it into this dir in your home folder...
```
git clone https://github.com/jteneycke/yoso.git ~/scripts
```

...the first time you run it, it will add itself to the PATH in your shell!
```
cd ~/scripts
./yoso
```

## Usage
Then you can call it from anywhere...
```
/anywhere/in_your/filesystem $ yoso get-cats
```

... and it will automatically open up a fresh script template in your favorite `EDITOR`.
```ruby
#!/usr/bin/env ruby

require "pry"
require "fileutils"

# A multi-line string area to call bash
BASH = <<-SH

echo "YOSO - You Only Script Once."

SH
system(BASH)
```
And it's already `chmod +x`'d, in your PATH and ready to run!

I recommend opening up another terminal in a split, keeping your freshly baked script open in your editor, and liberally noodling back and forth between the two as you experiment REPL-styles. (Take that Emacs!)

```lisp
(just-kidding
  (its-actually
    (my (favorite))))
```

P.S. - It's also great for copying sketchy-one-off-gists-for-mass-renaming-files-with-bash and having that indecipherable kludge executable on your system as fast as you can say it's "fresh OS install time anyway".
