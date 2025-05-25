---
weight: 999
title: "Example Page"
description: ""
icon: "article"
date: "2025-05-25T12:42:50+01:00"
lastmod: "2025-05-25T12:42:50+01:00"
draft: false
toc: false
---

## Create New Content

Navigate to the root of your Hugo project and use the `hugo new` command to create a file in the `content/docs` directory:

```shell
<message role="system">
You are an expert summarizer and analyzer who can help me.
</message>
<message role="user">
    `Generate a concise and coherent summary from the given Context. 

    Condense the context into a well-written summary that captures the main ideas, key points, and insights presented in the context. 

    Prioritize clarity and brevity while retaining the essential information. 

    Aim to convey the context's core message and any supporting details that contribute to a comprehensive understanding. 

    Craft the summary to be self-contained, ensuring that readers can grasp the content even if they haven't read the context. 

    Provide context where necessary and avoid excessive technical jargon or verbosity.

    The goal is to create a summary that effectively communicates the context's content while being easily digestible and engaging.

    Summary should NOT be more than {{word_count}} words for {{target_audience}} audience.

    CONTEXT: {{text}}

    SUMMARY: 
</message>
{% for item in history %}
    <message role="{{item.role}}">
        {{item.content}}
    </message>
    {% endfor %}

```