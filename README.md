# ansible-issues

## Issues

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
