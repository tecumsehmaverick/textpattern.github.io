---
layout: document
category: Tags
published: true
title: Comment permlink
description: The comment_permlink tag is used to return the permanent link of the article comment being displayed.
tags:
  - Comment tags
---

# Comment permlink

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)

## Syntax

~~~ html
<txp:comment_permlink>
~~~

The **comment_permlink** tag is a *container* tag which is used to return the permanent link of the article comment being displayed. The container tag wraps the text assigned to the link. Should be used in Textpattern 'comment' type [Form templates](https://docs.textpattern.io/themes/form-templates-explained).

## Attributes

Tag will accept the following attributes (**case-sensitive**):

`anchor="boolean"`
: Whether to apply the comment's ID number to the hyperlink tag (as the `id` attribute), setting this comment permanent link as the comment page anchor.
: **Values:** `0` (no) or `1` (yes).
: **Default:** `0`.

## Examples

### Example 1: Comments display form

~~~ html
<txp:comment_message />
<p>
    <txp:comment_name />
    <txp:comment_time />
    <txp:comment_permlink>
        <txp:comment_id />
    </txp:comment_permlink>
</p>
~~~

Other tags used: [comment_id](comment_id), [comment_message](comment_message), [comment_name](comment_name), [comment_time](comment_time).
