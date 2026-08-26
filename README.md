## Diffport

**Know who wrote your code.**

Diffport tags every pull request with its true authorship — which agent, which model,
which session, or a person — then scores the risk and shows what it does to your
database schema.

---

### Why it exists

Most of the code shipping today is at least partly machine-written, and git was not
designed to record that. An agent commits under the identity of whoever was at the
keyboard, so `git log` says a person wrote something a model actually wrote. That gap
is fine until an auditor, a customer, or an incident review asks who is accountable
for a specific line.

### How it works

Diffport reads **git**, not any vendor's API. Commit trailers, app actors, co-author
lines, branch patterns, diff shape — each is a signal carrying its own confidence, and
a resolver collapses them into an answer with the evidence attached.

That choice matters twice over: every coding tool that leaves a trace is supported
without asking permission, and no vendor can withdraw support.

### The part most tools get wrong

A commit with no provenance signal is marked **untraced** — never guessed as human.

"We know a person wrote this" and "we don't know who wrote this" are different claims,
and collapsing them manufactures exactly the attestation the product exists to provide
honestly. A repository at 71% coverage says so, on every screen and in every report.

### Read-only, by construction

Diffport never pushes and never asks for write access. Its GitHub App requests three
read-only permissions and nothing else.

---

<sub>

[diffport.com](https://diffport.com) · [changelog](https://changelog.diffport.com)

</sub>
