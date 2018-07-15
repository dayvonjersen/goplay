 - go playground-inspired repl for Go
    - goplay
    - opens a template file with vim -u NONE --no-plugin
        - potential for common boilerplates to choose from
    - :wq
    - runs goimports (why is that still not ticked by default??)
    - makes a tempdir
    - puts the file you just wrote there (ok it does it first w/e)
    - calls go run | less
    - prompt: [R]un again [S]hare [E]dit [Q]uit
        - edit re-opens the file you just made

I took 10 minutes to write this up instead of just finding out if
strconv.Atoi handles hexadecimal notation fml.
-tso 7/15/2018 9:55:25 AM
