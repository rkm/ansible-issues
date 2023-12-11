# ansible-issues

## Issues

### Overriding boolean variables

When overriding a bool from the CLI e.g. `-e"foo=false"`, `false` will be parsed
as a string. When this is used in a conditional on its own, it will not be
interpreted as a boolean, so results may be surprising.

A few solutions:

- `-eFOO=`
- `-e{FOO: false}`
- Be paranoid and put `| bool` at the end of all your conditionals

## Tips

### Debug

Print debug information without requiring `-v` (which will print debug info for
every task).

```yaml
- debug: var=foo
```

OR

```yaml
- debug:
    msg: foo is {{ foo }}
```

### Pause

Stop task execution here.

```yaml
- pause:
```

## TODO

- Note on system dnf/selinux libs for RHEL
- Note on controller vs remote sources
