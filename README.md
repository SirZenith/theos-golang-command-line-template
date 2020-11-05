# How to use

This repo is modified from [Thisrepo](https://github.com/cszichao/theos-golang).

As any other theos template, you can simple do

```
git clone https://github.com/SirZenith/theos-golang-command-line-template.git
$THEOS/bin/nicify.pl ./theos-golang-command-line-template golang_command_line
```

After getting the `.nic.tar` file, put it in `$THEOS/templates`. So that next
time when you use NIC, you will see this template in the list.

Put your golang code in the same directory with `main.go`. there is already some
code in `main.go`, adding your code into that file base on existing content to
get project running.

`gogo.sh` provide some shortcut

```
gogo.h <flag> <tool_name>

flags (all flags are bool type):
    -g | --go:      will generate go static lib.
    -p | --package: will run `make package` in ./theos_code drectory
    -i | --install: will run `make install` in ./theos_code drectory
    clean:          remove build results
```

You should proviede argument `tool_name` when `-g` flag appears, when multiple
flags come up at the same time, operation will be execute in order of `-g` then
`-p` finally `-i`.

`clean` will override all other flags. Do cleaning then exit.

