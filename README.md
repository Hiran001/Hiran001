## Hiran

I work on computational science across structural biology and drug discovery, and
I build the tooling that research needs but rarely has.

Two things run through most of what I do. **Workflows**: turning a method that
works once on someone's laptop into a pipeline that runs reproducibly at scale.
**Access**: the results of publicly funded research should be readable and usable
by anyone, and a surprising amount of the friction is tooling rather than
principle.

---

### What I work on

**Structural biology.** Cryo-EM and X-ray crystallography. Particular interest in
**GPCRs and membrane proteins**, where the structural problem and the
computational one are hard in the same places: conformational ensembles, lipid
environment, and states that a single static model does not capture.

**Drug design.** Structure-based design, covalent inhibitors, virtual screening
at scale, and the scoring problem underneath all of it. I spend as much effort
evaluating scoring functions as using them, because a benchmark that lies is
worse than no benchmark.

**Simulation and biophysics.** Molecular dynamics, coarse-grained models,
biomolecular condensates and phase behaviour.

**Scientific computing generally.** GPU pipelines, distributed screening
campaigns, cheminformatics databases, ML for molecular property prediction. I run
a small multi-node GPU cluster for this work, which keeps me honest about what
things actually cost.

### On combining work across labs

Most research software is written to solve one group's problem, and it solves it
well. The same problem is usually being worked on in parallel in a dozen other
groups, each solution strong in a different direction and none of them quite
usable by anyone outside the lab that wrote it. The field ends up with many
partial tools rather than one good one, and the same ground gets covered
repeatedly.

The work I find most worthwhile is in the join: taking several approaches that
each work somewhere and building the version that works generally. That is not a
lesser contribution than writing something new, though it tends to be valued as
though it were, because it does not look like novelty. It is usually where the
largest gain in usability sits, and it is nearly always faster than starting
over.

So if you have built something and it does most of what I need, I would rather
extend it, contribute upstream, or integrate it than write a second one. If
something here is useful to you, take it, and tell me what it got wrong.

### Open source

**[scilib-mcp](https://github.com/Hiran001/scilib-mcp)** — an MCP server for
open-access scientific literature.

Federated search across the open scholarly record (OpenAlex, Europe PMC,
Semantic Scholar, arXiv, DOAJ, OpenAIRE, CORE), full-text retrieval through legal
open-access routes with per-file provenance, and full-text search over the papers
already on your own disk.

It exists because two different problems get confused with one another.
*Acquisition*, finding a legal free copy, is largely solved and widely underused:
most of the open corpus is invisible to a search that only checks the publisher's
page. *Retrieval*, knowing what is inside the papers you already hold, is not
solved at all, and that is where the expensive mistakes happen, because a keyword
search can only return answers to questions you already thought to ask.

Runs entirely locally. No server component, no telemetry, documented public APIs
only.

More to follow. Most of my tooling starts as something I needed for a specific
problem, and the parts that generalise get released.

### On how I work

Much of what I publish is written with AI assistance, and I say so plainly rather
than leaving it to be inferred. I set the scope and the constraints, I review and
test what comes back, and I am responsible for every number that leaves my hands.
Being precise about where work came from is the same discipline as being precise
about where a measurement came from.

A result is not real until it exists as a file that regenerates it. A metric
quoted without a path to the code that made it is a rumour. Negative results are
kept rather than discarded, because they are the ones most easily lost and often
the most valuable.

I care about the difference between a number that is correct and a number that is
*trustworthy*: whether the trivial null was run, whether the comparison groups
were matched on everything except the variable of interest, and whether a good
result was audited as hard as a bad one.
