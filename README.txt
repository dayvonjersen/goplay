 - go playground-inspired repl for Go
    - goplay
    - opens a template file with vim -u NONE --no-plugin
        - potential for common boilerplates to choose from e.g.
            - networking examples
            - concurrency examples
            - interfaces
            - whatever else is hard to remember sometimes
    - :wq
    - runs goimports (why is that still not ticked by default??)
    - makes a tempdir
    - puts the file you just wrote there (ok it does it first w/e)
    - calls go run | less
    - prompt: [R]un again [S]hare [E]dit [Q]uit
        - edit re-opens the file you just made

I took 10 minutes to write this up instead of just finding out if
strconv.Atoi handles hexadecimal notation (it doesn't btw)
-tso 7/15/2018 9:55:25 AM

PREREQ:
 - go
 - vim
 - bash and friends
 - goimports

INSTALL:

put goplay in your $PATH somewhere, $GOPATH/bin is a suggestion
don't forget to chmod +x

NOTE(tso):

The official "The Go Playground" (not associated btw) is a much __safer__ way
for newcomers to Go to play with the language because it does things like
limit execution time, doesn't do networking, and obviously it prevents you
from accidentally running malicious or destructive code.

They explain this on their blog here read this:
https://blog.golang.org/playground

But I always find myself making files like, well take a look at this directory:
tso@wok goplay (master) $ ls ~/Desktop/go
badidea.go      channels/                    fields/    net/      throw.go
c++/            embeded_struct_inheritance/  filepath/  numbers/  time/
can_i_do_that/  external/                    iface/     regex/    timetest/

and using go run 

but I was just using psysh again and I forgot how nice it is to just type it
and get a result right away so I thought I'd make something I can't believe no
one else has done yet but now that I made this they're all gonna come out of
the woodwork...

-tso 7/15/2018 11:26:07 AM

TODO(tso):

DRY variables
colors (maybe)
option -t more minified go templates to choose from
    - *very* excited to have an excuse to write minified go :D
