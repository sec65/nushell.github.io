---
title: wrap
version: 0.63.0
usage: |
  Wrap the value into a column.
---

<script>
  import { usePageFrontmatter } from '@vuepress/client';
  export default { computed: { frontmatter() { return usePageFrontmatter().value; } } }
</script>

# <code>{{ frontmatter.title }}</code>

<div style='white-space: pre-wrap;'>{{ frontmatter.usage }}</div>

## Signature

```> wrap (name)```

## Parameters

 -  `name`: the name of the column

## Examples

Wrap a list into a table with a given column name
```shell
> echo [1 2 3] | wrap num
```
