# Tag Expressions

Tag expressions let you select a subset of scenarios, based on tags. They can be used for two purposes:

* [Running a subset of scenarios](https://docs.cucumber.io/cucumber/api#running-a-subset-of-scenarios)
* [Scoping hooks to a subset of scenarios](https://docs.cucumber.io/cucumber/api#tagged-hooks)

A tag expression is simply an _infix boolean expression_. Below are some examples:

| Expression | Description |
| :--- | ---: |
| `@fast` | Scenarios tagged with `@fast` |
| `@wip and not @slow` | Scenarios tagged with `@wip` that aren't also tagged with `@slow` |
| `@smoke and @fast` | Scenarios tagged with both `@smoke` and `@fast` |
| `@gui or @database` | Scenarios tagged with either `@gui` or `@database` |

For even more advanced tag expressions you can use parenthesis for clarity, or to change operator precedence:

```text
(@smoke or @ui) and (not @slow)
```

