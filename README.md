# ocaml-pf

An [Angstrom-based](https://github.com/inhabitedtype/angstrom) parser for the
[FreeBSD pf](https://www.unix.com/man-page/freebsd/5/pf.conf/) firewall configuration format.

## compiling the example

First, install the dependencies:
```shell
opam pin add -n pf .
opam install --deps-only pf

# build test executable, self-test rules from 'man pf.conf':
jbuilder runtest
```

This will give you the `parse_conf.exe` utility that you can use to parse
firewall configuration files:
```
./_build/default/test/parse_conf.exe /home/me/my-pf-file.conf
Reading "/home/me/my-pf-file.conf"
Line 0: ext_bridge = "external"
Read 1 lines!
```

## contributing

- I would be very grateful for examples of rules that trip the parser - please
[file an issue ticket on GitHub](https://github.com/cfcs/ocaml-pf/issues/new).

- Ideas regarding the AST, the API, or other suggestions are also very welcome.

- It is always nice with improvements to the pretty-printers! :-)

- Before taking on larger rewrites, please get in touch so we can avoid merge conflicts.
