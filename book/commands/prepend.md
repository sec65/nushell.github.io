---
title: prepend
version: 0.63.0
usage: |
  Prepend any number of rows to a table.
---

<script>
  import { usePageFrontmatter } from '@vuepress/client';
  export default { computed: { frontmatter() { return usePageFrontmatter().value; } } }
</script>

# <code>{{ frontmatter.title }}</code>

<div style='white-space: pre-wrap;'>{{ frontmatter.usage }}</div>

## Signature

```> prepend (row)```

## Parameters

 -  `row`: the row, list, or table to prepend

## Examples

Prepend one Int item
```shell
> [1,2,3,4] | prepend 0
```

Prepend two Int items
```shell
> [2,3,4] | prepend [0,1]
```

Prepend Ints and Strings
```shell
> [2,nu,4,shell] | prepend [0,1,rocks]
```
