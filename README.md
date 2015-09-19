# sse_taxonomy

Drupal Moduel that fix taxonomy links for SSE website.

## TL;DR

Replace `taxonomy/term/TERMID` with `notice/filter/target/TERMID` or `notice/filter/category/TERMID` for `target` or `category` taxonomy.

## Background

We have `taxonomy-target`(通知面向群体) and `taxonomy-category`(通知内容分类).

To query multiple terms, we have created following view pages:

- `notice/filter/target/TERMID`

- `notice/filter/category/TERMID`

- `notice/filter/target/TERMID/category/TERMID`

However, when rendering nodes, the taxonomy link is still `taxonomy/term/TERMID` (although user will be redirected to `notice/target/filter` or `notice/target/category` using Rabbit Hole plugin). This module will solve the output link issue.