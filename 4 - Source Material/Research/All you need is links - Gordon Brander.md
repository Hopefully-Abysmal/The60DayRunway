---
Date Created: 2025-05-06 22:29
Last Updated: 2025-05-06 22:29
tags:
  - Resource
Index: 
Topic: 
Link:
  - https://newsletter.squishy.computer/p/all-you-need-is-links
Status: Unweathered
Published: true
---
---
# Summary:


# Key Terms:
* 

# Reflection:

## Misc. Notes
- The aforementioned links are critical to a better reccomendation system, to a better web experience in my honest opinion. We have to start from something to grow a community though; so I believe the semantic webs current and past attempts at concept modeling acn be used as a baseline; from there we can allow users to link things at scale (see metagovs KOI on how this may be technically feasible) and interact with the content on a level deeper than currently possible.
## Curiosities
- 
## Ideas
- 
## Questions
- 

# GPT Refinement: 

# Transcript:


## All you need is links

[](https://substack.com/@gordonbrander)

[Gordon Brander](https://substack.com/@gordonbrander)

Jan 22, 2022

When Tim Berners Lee talks about how he designed the web, he uses an analogy from physics, describing his process as a quest to find “fundamental laws” which can generate a desired system:

> One of the beautiful things about physics is its ongoing quest to find simple rules that describe the behavior of very small, simple objects. Once found, these rules can often be scaled up to describe the behavior of monumental systems in the real world. […]
> 
> If the rules governing hypertext links between servers and browsers stayed simple, then our web of a few documents could grow to a global web. The art was to define the few basic, common rules of “protocol” that would allow one computer to talk to another, in such a way that when all computers everywhere did it, the system would thrive, not break down.
> 
> _Tim Berner’s Lee, 2000, “Weaving the Web”_

I like this description of design as a quest to discover a simple set of primitives, **[a small alphabet](https://subconscious.substack.com/p/provoking-emergence-with-alphabets)** for generating a system. To paraphrase [Gall’s Law](https://gordonbrander.com/pattern/galls-law/):

> Simple rules produce complex behavior. Complex rules produce stupid behavior.

What if we applied this lens to designing tools for thought? What are some examples of simple features with extremely broad ranges of motion? I’d like to put forward one candidate…

**Links**.

A surprising number of other features can be expressed in terms of links.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F792147ea-0a28-48a0-855b-bc11f98e893e_1024x576.png)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F792147ea-0a28-48a0-855b-bc11f98e893e_1024x576.png)

#### You don’t need tags, you just need links

What is a tag? What is its structure? What is its function?

When you tag something, it gets added to a collection of other things with the same tag. So, this is a one-to-many relationship, where one tag points to many pages.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Feb93fee8-489e-4551-bc86-94c9ac638753_576x678.png)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Feb93fee8-489e-4551-bc86-94c9ac638753_576x678.png)

Let’s think about a link. Many pages can point to a single page. Many-to-one. One-to-many. So, we could achieve tagging with links by listing all backlinks to a given page. **Tags are just backlinks to pages that don’t exist**.

#### You don’t need folders, you just need links

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F17fafc93-fcf0-47ef-a9dc-549e9eb80237_1600x1194.png)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F17fafc93-fcf0-47ef-a9dc-549e9eb80237_1600x1194.png)

Folders are a place to put things. Like most of the desktop paradigm, folders use a familiar object borrowed from the office as a metaphor to communicate an abstract relationship. You put multiple documents into a paper folder for filing, you put multiple documents into a digital folder for filing. Object metaphors are powerful, both because they leverage something familiar to introduce something new, and because they lean into our natural cognitive strengths for spatial reasoning and object manipulation.

Hmm, many documents, one folder. It seems that underneath this object metaphor is another one-to-many relationship. So, **a folder could be expressed in terms of a page full of links**.

#### You don’t need stars, hearts, upvotes, downvotes, you just need links

> What information consumes is rather obvious: it consumes the attention of its recipients. Hence a wealth of information creates a poverty of attention, and a need to allocate that attention efficiently among the overabundance of information sources that might consume it.  
> _Herbert Simon_

Social media, search, spam, recommendations — when faced with an abundance of information, we often find ourselves needing to separate wheat from the chaff. Many systems reach for stars, hearts, upvotes, and downvotes as quick fixes for user-generated quality signals. But what if we just used links?

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F85c89e69-28ce-4034-9487-4fc02e9b9b8e_769x872.png)



](https://en.wikipedia.org/wiki/PageRank)

**Inbound links can be used as a signal of quality**. People are more likely to link to things that matter, and less likely to link to things that don’t. Sum up the backlinks to a page and you have a quality signal. This is the key insight behind [Google Pagerank](https://en.wikipedia.org/wiki/PageRank).

#### You don’t need comments, you just need links

Comments are one of the core interaction primitives of today’s web. I can comment on your Facebook post, your Google Doc, your blog.

What is a comment? What is its structure? What is its function? It’s a bit of content that is conceptually related to a parent post. We could say that the comment _points to_ the post, or something in the post. That’s a directional relationship.

Links also _point to_ something. They describe a directional relationship. It’s not much of a leap to consider an inbound link a comment on the thing it links to. **If we implement some form of [transclusion](https://en.wikipedia.org/wiki/Transclusion), we can express comments in terms of links**. In fact, WordPress already does this with [Pingbacks](https://wordpress.org/support/article/trackbacks-and-pingbacks/).

#### You don’t need outliners, you just need links

[Outliners](http://outliners.scripting.com/) are tools for thought that conceive of documents as a hierarchy, or tree, or nested bulleted list. They’re one of those simple ideas, like spreadsheets that have an almost inexhaustible range of applications.

Outliners have a rich and interesting history, from [Dave Winer’s outliner programs for command line and Mac Classic](http://outliners.scripting.com/), through to today’s [Roam Research](https://roamresearch.com/).

[

![Twitter avatar for @davewiner](https://substackcdn.com/image/twitter_name/w_96/davewiner.jpg)

Dave The Outliner @davewiner

Screen shot of ThinkTank outliner on character-based IBM PC, circa 1987.

![Image](https://substackcdn.com/image/fetch/w_600,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fpbs.substack.com%2Fmedia%2FE40C6CtWQAgi8QI.png)



](https://twitter.com/davewiner/status/1408785536651776003?s=20)[

1:53 PM ∙ Jun 26, 2021

---

10Likes1Retweet



](https://twitter.com/davewiner/status/1408785536651776003?s=20)

So, but what is an outliner? What is its structure? What is its function? An outliner lets you break a document up into discrete nodes, nest those nodes under other nodes, hide branches, focus in on branches. The structure formed by an outliner is a tree, with parent and child nodes.

In an outliner, one parent may have many children. One-to-many. Links again. **We can express an outliner in terms of links by nesting inbound links underneath the document they point to**. So an outliner could be thought of as one view over a network of linked documents.

#### You don’t need semantic triples, you just need links

[Semantic triples](https://en.wikipedia.org/wiki/Semantic_triple) are one of those ideas you run into if you poke around the “tools for thought” space long enough. A semantic triple is a simple idea with some powerful properties. The basic idea is to construct a network made up of:

```
Subject - Predicate - Object
```

For example, “Xerxes is the parent of Brook” can be expressed as a triple:

```
Xerxes - Parent - Brook
```

Objects can themselves be subject-predicate-object triples, so you can build up complex networks of relationships this way.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc975d9f-6db5-4b71-b5a7-7d500e13edfd_1100x861.png)



](https://neo4j.com/blog/buzzfeed-trumpworld-dataset-neo4j/)

Triples allow computers to do complex automated reasoning. You can even use them to derive relationships that aren’t explicitly stated. You know those answer cards that appear in Google searches? Those are largely constructed from Google Knowledge Graph, [a giant network of semantic triples](https://inlinks.net/p/knowledge-graph-explained/).

Triples are often expressed in terms of special formal languages like [TURTLE](https://en.wikipedia.org/wiki/Turtle_\(syntax\)) or [Datalog](https://en.wikipedia.org/wiki/Datalog). Here’s how I might jot down that Xerces is a parent of Brooke and Brooke is a parent of Damocles using Datalog:

```
parent(xerces, brooke).
parent(brooke, damocles).
```

This can get old fast. Writing formal relationships by hand is ok for narrow domains, but it’s not exactly the most natural thing to reach for when trying to express ideas.

So, knowledge graphs are tremendously useful for computers, but not so fun to write by hand. If you ask me, [Semantic Web](https://en.wikipedia.org/wiki/Semantic_Web) efforts have repeatedly stubbed their toe on this mismatch between symbolic alignment and the messy, emergent, imprecise, _human_ process of knowledge construction.

But wait. What is a triple? What is its structure? What is its function?

[

![Making New Connections with MarkLogic Semantics - MarkLogic](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F3e14b5a6-55ef-477f-9506-575c13bff6a4_804x229.png "Making New Connections with MarkLogic Semantics - MarkLogic")



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F3e14b5a6-55ef-477f-9506-575c13bff6a4_804x229.png)

It seems a triple is a **link** between two things, _through_ a predicate. Here is yet another thing we can reimagine through the mechanism of links.

**A hyperlink is a triple where the subject is the page, the predicate is the link text, and the object is the thing being linked to**.

Better yet, it’s organic. This knowledge graph is constructed from things I would do anyway. I create a link because it solves my problem as an author of pointing you, the reader, to a concept. This good-enough alignment between user goals and computer goals is one reason the regular web succeeded where the [semantic web](https://en.wikipedia.org/wiki/Semantic_Web) failed.

#### You don’t need topic modeling, you just need links

[Topic modeling](https://en.wikipedia.org/wiki/Topic_model) is a range of machine learning techniques for deriving abstract topics from a collection of documents using statistical analysis. I put in a collection of Subconscious newsletters, and topic modeling tells me they’re about tools for thought, cybernetics, the web, computing, distributed systems, etc. Pretty cool.

So, ok, you might still want topic analysis, but following on from our observation that we can use links as knowledge graphs, we can also use links as quick-and-dirty topic models.

**If we consider each page to be a topic, then then links offer a pretty good map of topics within a page**. Pull out a list of links from a page, and you approximately have the topics for the page. Collect all the links across pages, rank them by frequency, and you have a sense of the most frequently addressed topics within the collection.

#### Links are a good idea

> It is my belief that this new ability to represent ideas in the fullness of their interconnections will lead to easier and better writing, easier and better learning, and a far greater ability to share and communicate the interconnections among tomorrows ideas and problems. Hypertext can represent all the interconnections an author can think of, and compound hypertext can represent all the interconnections _many_ authors can think of, as we shall see.  
> _Ted Nelson, 1982, “Literary Machines”_

Links aren’t the only way—I don’t want to be totalizing here—but they are something special. It’s rare to discover a simple mechanism with such broad and expressive range of motion.

I hope to keep **[Subconscious](https://subconscious.substack.com/p/subconscious-alpha)** simple. Few features, **[a small alphabet with wide expressive range of motion](https://subconscious.substack.com/p/provoking-emergence-with-alphabets)**. Before reaching for features, my goal is to explore, to the fullest extent, the creative potential of plain old links.