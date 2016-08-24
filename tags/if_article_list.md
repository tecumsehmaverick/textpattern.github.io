---
layout: document
category: tags
published: true
title: "If article list"
Description: The if_article_list tag will execute the contained statement if an article list is being displayed.
tags:
  - Article tags
  - Conditional tags
---

# If article list

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)

## Syntax

~~~ html
<txp:if_article_list>
~~~

The **if_article_list** tag is a *conditional* tag and always used as an opening and closing pair, like this...

~~~ html
<txp:if_article_list>
    ...conditional statement...
</txp:if_article_list>
~~~

The tag will execute the contained statement if an article list is being displayed (i.e.,not showing an individual article).

## Attributes

This tag has no attributes.

## Examples

### Example 1: Article/article list navigation

~~~ html
<txp:article />

<txp:if_individual_article>
    <p>
        <txp:link_to_prev>
            <txp:prev_title />
        </txp:link_to_prev>
        <txp:link_to_next>
            <txp:next_title />
        </txp:link_to_next>
    </p>
</txp:if_individual_article>
~~~

&lt;txp:if_article_list&gt;
    <p>
        <txp:older>Previous</txp:older>
        <txp:newer>Next</txp:newer>
    </p>
</txp:if_article_list>
~~~

This example shows how to setup article navigation so that [link_to_prev](link-to-prev) and [link_to_next](link-to-next) are used at the individual article level *or* [older](older) and [newer](newer) with article lists.

Other tags used: [link_to_prev](link-to-prev), [link_to_next](link-to-next), [prev_title](prev-title), [next_title](next-title), [if_individual_article](if-individual-article), [older](older).texrtile, [newer](newer).texrtile.

### Example 2: In combination with the 'else' tag

~~~ html
<txp:if_article_list>
    <p>
        <txp:site_name />
    </p>
<txp:else />
    <p>
        <img src="http://example.com/logo.png" alt="Logo">
    </p>
</txp:if_article_list>
~~~

This example shows the if_article_list in combination with [else](else) to display a site's [site_name](site-name) or logo when an article list is displayed or not, respectively.

Other tags used: [else](else), [site_name](site-name).