---
title: Regular Expression to find a string included between two characters while EXCLUDING the delimiters
toc: true
branch: master
categories: [regex, regex-between-two-characters]
badges: true
comments: true
layout: post
---

Easy done:

```
(?<=\[)(.*?)(?=\])
```

Technically that's using lookaheads and lookbehinds. See Lookahead and Lookbehind Zero-Width Assertions. The pattern consists of:

 - is preceded by a [ that is not captured (lookbehind);
 - a non-greedy captured group. It's non-greedy to stop at the first ]; and
 - is followed by a ] that is not captured (lookahead).

Alternatively you can just capture what's between the square brackets:

```
\[(.*?)\]
```

and return the first captured group instead of the entire match.

Example for <b>Dart language</b>

```
RegExp(r'@<.*?>') 
```

Ref: 
 - [Regex tutorial](https://www.regular-expressions.info/lookaround.html)
