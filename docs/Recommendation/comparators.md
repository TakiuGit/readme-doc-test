---
title: Comparators
excerpt: >-
  This page describes information about operators that are used for advanced
  searching.
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

A comparator is one word which compares the value of a field on its left with one or more values on its right.

### IN

**Syntax** : `IN`, `=`

The `IN` comparator is used to search for metadata containing one of the match for the specified field.

When passing multiple values, any of the value quested are searched in order to find a match.
Meaning that `catalog IN ("foo","bar")` can be expressed as `catalog = foo OR catalog = bar`.

<Callout icon="📘" theme="info">
  This filter do not apply any additional filter on the content type.
  This mean that requesting for `$lineups NIN "channel"` can also return VOD contents.
</Callout>

**Examples**

```sql Content in the catalog foo
"catalog" IN "foo"
```

```sql Content the catalog foo or bar
"catalog" IN ("foo","bar")
```

### NIN

**Syntax** : `NIN`, `!=`

The `NIN` comparator is used to search for metadata not containing any of the match for the specified field.
This includes content that do not contain the specified field.

When passing multiple values, any of the value quested are searched in order to reject a match
`catalog NIN ("foo","bar")` can be expressed as `catalog != foo OR catalog != bar`.

**Examples**

```SQL Content without the catalog foo
catalog NIN "foo"
```

```SQL Content outside catalog foo or bar
catalog NIN ("foo","bar")
```

***

### ALL

**Syntax** : `ALL`

The `ALL` comparator is used to search for all metadata value in the specified field.
A content with the specified field containing more than the requested elements will match the request.

**Examples**

```SQL Content outside the catalog foo
catalog ALL "foo"
```

```SQL Content in catalog foo and bar
catalog ALL ("foo","bar")
```
