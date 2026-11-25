# Article 4 – Chord: A Scalable Peer-to-Peer Lookup Protocol for Internet Applications

**Authors:** Stoica, Morris, Liben-Nowell, Karger, Kaashoek, Dabek, Balakrishnan
**Published:** IEEE/ACM Transactions on Networking, 2003

## Central idea
The article presents **Chord**, a protocol to find which node stores a key in a
peer-to-peer network, without a central server.

## Three important takeaways
1. **A ring:** Nodes and keys are placed on a circle; a key goes to the next node.
2. **Fast lookup:** A lookup needs about **log(N)** messages.
3. **Handles change:** Nodes can join, leave or fail, and Chord still works.

## Interesting observations
- Only one operation: given a key, find the node.
- Theorems prove the cost and the correctness.
- The evaluation is done by **simulation**. Tests on a real network are in another paper.

## Patterns identified
- Introduction → related work → system model → protocol and proofs → simulation → future work → conclusion.

## Practical applications
- File sharing, distributed storage.

## Critical thinking
- **Assumptions:** nodes behave correctly, IDs are random.
- **Limitations:**
  - Bad (malicious) nodes are left for future work, as the authors say.
  - Results come from simulation only.
  - A lookup can be slow in real network time; the paper only starts to improve this.
- **Do I agree?** Yes, the protocol is simple and proven.

## My feedback on the article
- **Worth reading?** Yes.
- **Structure:** Very good: abstract, introduction, related work, model,
  protocol, results, future work, conclusion, references.
- **Relevance:** High.
- **Weak point:** proofs are heavy to read.
- **Overall:** Professional and well done.
