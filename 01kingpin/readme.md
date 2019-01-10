```console
$ vgo run main.go foo
main: error: !expected command but got "foo"
usage: main [<flags>] <command> [<args> ...]

Flags:
  --help  Show context-sensitive help (also try --help-long and --help-man).

Commands:
  help [<command>...]
    Show help.

  add [<ns>...]
    add numbers

  hello [<flags>] [<name>]
    hello message

$ vgo run main.go hello
hello
$ vgo run main.go hello -v
(john doe) Hello
$ vgo run main.go hello -v foo
(foo) Hello

$ vgo run main.go add 1000 100
{false [1100]} = 1000 + 100
$ vgo run main.go add 1000000000000000000 1000000000000000000 1000000000000000000 1000000000000000000 1000000000000000000 1000000000000000000 1000000000000000000 1000000000000000000 1000000000000000000 1000000000000000000
{false [10000000000000000000]} = 1000000000000000000 + 1000000000000000000 + 1000000000000000000 + 1000000000000000000 + 1000000000000000000 + 1000000000000000000 + 1000000000000000000 + 1000000000000000000 + 1000000000000000000 + 1000000000000000000
```
