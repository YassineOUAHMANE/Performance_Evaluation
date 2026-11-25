# Article 3 – A Relational Model of Data for Large Shared Data Banks

**Author:** E. F. Codd (IBM Research, San Jose)
**Published:** Communications of the ACM, 1970

## Central idea
The article proposes to store data as **relations (tables)**. Users should not
need to know how data is stored in the machine. The goal is that programs keep
working when the storage changes.

## Three important takeaways
1. **Independence:** Programs should not depend on order, indexes or access paths.
2. **Relations:** Data is described with simple math relations, better than the
   tree (hierarchical) and network models used at that time.
3. **Keys and normal form:** The paper defines primary key, foreign key and a
   normal form, and talks about redundancy and consistency.

## Interesting observations
- The paper shows three problems of old systems: ordering, indexing and access path dependence.
- Operations on relations: permutation, projection, join, composition.
- It is a theory paper: no program, no experiments.

## Patterns identified
- Problems of current systems → new model → operations → redundancy and consistency → summary.

## Practical applications
- Relational databases (MySQL, PostgreSQL, Oracle).

## Critical thinking
- **Assumptions:** a clean math model can be made fast in practice.
- **Limitations:**
  - No performance results, no implementation.
  - The data language is only introduced briefly.
  - Hard to read: old style and a lot of math.
- **Do I agree?** Yes, the idea is clear and useful.

## My feedback on the article
- **Worth reading?** Yes, it is the base of databases.
- **Structure:** Good for a theory paper: abstract, keywords, numbered sections,
  summary, references. No experiments, which fits the type of paper.
- **Relevance:** Very high, still used today.
- **Weak point:** hard to read for a student.
- **Overall:** Professional and very important.
