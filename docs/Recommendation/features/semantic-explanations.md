---
title: Semantic Explanations
excerpt: >-
  Explain why any title is recommended to the end user, either through similar
  titles they’ve already watched or through semantic pairs of keywords they
  usually interact with.
deprecated: false
hidden: false
metadata:
  robots: index
---
**Semantic Explanations** is a feature which can show the reasoning behind any single recommendation. It can be displayed in 2 ways:

1. The name of the most relevant content related to the current title, e.g. _The Hobbit_  is being recommended to you because you watched _The Lord of the Rings_
2. A pair of keywords which is most accurate regarding the user’s recent interactions, e.g. _The Hobbit_ is recommended to you because you like “fantasy and quests”.

“Recommendations explained” can be displayed on content files when a user consults them (if the personalized recommendation would be relevant to the user), or even underneath every content in a list of titles in a “Recommended for you” line. In the latter example, this does not mean every title would have the same argument. Therefore, a personalized recommendations line could be composed of: _The Hobbit_, because you like “fantasy and quests”, _Matrix_, because you like science fiction and martial arts, _The Lion King_, because you like Disney cartoons, etc

### Endpoint

```
GET /contents/{contentId}/guarantees?user={userid}
```

More details on the [API documentation](/dev/null)

this will be a conflict
