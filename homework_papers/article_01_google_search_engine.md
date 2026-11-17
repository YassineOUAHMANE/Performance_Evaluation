# Article 1 – The Anatomy of a Large-Scale Hypertextual Web Search Engine

**Authors:** Sergey Brin, Lawrence Page (Stanford University)
**Published:** Computer Networks and ISDN Systems, 1998

## Central idea
The article presents Google, a prototype search engine made at Stanford.
The main goal is to give **better quality** results and to **scale** to a very
big web. The authors explain the architecture, the data structures and some first results.

## Three important takeaways
1. **Links help ranking:** Google uses links between pages (PageRank) and the text
   of links (anchor text) to find good pages, not only keywords.
2. **Built to scale:** The system is designed for millions of pages and many queries.
3. **Open research:** Most search engines are commercial and closed; the authors
   want an academic one that others can study.

## Interesting observations
- Search engines that only match keywords often return low quality results.
- Google uses the structure of hypertext (links, anchor text) to give better results.
- The web and the number of users grow very fast, so scale and quality are both important.
- The index can be huge, so it must be processed fast and stored efficiently.
- PageRank is a simple formula: a page is important if important pages link to it.
- The prototype has at least 24 million pages.

## Patterns identified
- Problem → system features → related work → architecture → results → conclusion.

## Practical applications
- Web search, and ranking things in any network of links.

## Critical thinking
- **Assumptions:** a link to a page is like a "vote" for this page.
- **Limitations:**
  - The authors say themselves that a user evaluation is "beyond the scope of this paper".
    Results are shown with an example query, not with measures.
  - People could create fake links to push their pages up.
- **Do I agree?** Yes, the main idea is strong. But the results part is weak.

## My feedback on the article
- **Worth reading?** Yes. It is clear and easy to follow.
- **Structure:** Good: abstract, introduction, related work, system, results,
  conclusion, acknowledgments, references.
- **Relevance:** Yes, the problem was real and the idea is still used.
- **Weak point:** the evaluation is short and not measured.
- **Overall:** A strong paper, more a system description than a tested study.
