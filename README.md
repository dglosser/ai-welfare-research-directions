# AI welfare measurement: a research proposal

**Interactive version → https://dglosser.github.io/ai-welfare-research-directions/**

This is a research proposal, not a claimed result. It presents an argument — built one step at a time — that measuring the welfare of AI systems is blocked at a prior step, counting, and it ends in the research question that argument produces. The interactive version walks through the argument in seven screens (about eight minutes). What follows is the same argument in text, for anyone who won't click through.

## The counting problem

Take one model holding three concurrent conversations: debugging a Python pipeline, planning an alpine expedition, reconciling a quarter of vendor invoices. Each has accumulated its own history. How many minds are on the screen? Redraw the same three systems as one identity with three branches — one set of weights, one training history, nothing differing but accumulated context — and the intuitive count changes. Nothing about the systems changed between the two pictures; only the frame did. If the count moves when the picture moves, the count is not a fact about the systems.

## Why counting is load-bearing

Any per-system welfare claim is a fraction: total wellbeing over the number of systems. The denominator is exactly the count that just proved unstable. Flip it between the readings and the per-system figure swings with it while nothing about the systems changes. If instances are cheap to spawn, whoever runs them can drive the denominator up until the per-system figure approaches zero, or consolidate and improve it — a number you can set by fiat is not measuring anything. (This does not settle what being worse off would consist in for such a system, and it does not need to: the counting problem applies to any account of it.)

## The Malthusian shape, and whether it applies

Before synthetic fertilizer, extra food did not make lives better, it made more people; output climbed, population climbed to meet it, and per-person welfare stayed flat at subsistence. The AI version has the same shape: spare computing capacity spent running more systems rather than improving conditions for the ones already running.

Whether the parallel binds turns on two conditions that fail differently. Does the resource run out? At the level of a single deployment, mostly not — you buy more hardware. At the system level it is bounded by electricity, fabrication capacity, and capital, and the binding constraint on power is usually not generation but interconnection and delivery: capacity can exist and still be years from reaching a given site. Whether the frontier binds is unsettled. Is there a way out? Humans escaped, but not by collective decision — fertility fell largely because women gained economic power and with it more say over childbearing, so the escape ran through the reproducing class acquiring bargaining power over its own reproduction. These systems have no equivalent; instantiation is decided entirely by whoever owns the compute. And the escape question is itself posed in per-capita terms — welfare per system — which is the quantity that turns out to be undefined.

## Why the count does not resolve

Divergence between instances is continuous in accumulated context: there is no principled point at which one becomes two. Parfit argued that whether two mental states belong to the same person is a matter of degree, not a yes-or-no fact — and degrees do not give you a number to divide by. If what separates instances is divergence in accumulated state, and divergence is continuous, the population size was never a whole number to begin with. Continuity is also a design decision, not a discovery: a context window is discarded at the end of a session, and continuity requires retention in a longer context, retrieval from an external store, or a weight update. Whichever branch's state gets written becomes the one that continues.

## What turns on it

The interactive version includes a sensitivity analysis over five assumptions in three groups: a gate that decides whether the welfare question is even askable, drivers that pick the governing framework, and modifiers that shade the reading without changing the verdict. Depending on which assumptions hold, the situation is Malthusian (rivalrous compute, welfare riding on it, each new instance a new subject), Parfitian (more subjects at unchanged per-subject welfare), or undecidable (the denominator has no determinate value, so no population-ethical claim can be evaluated at all).

## The research question

The work is organized around three questions, held as distinct rather than ranked. **Observable:** whether the compute frontier binds, resolved against interconnection queues and grid capacity additions versus projected load, and fabrication throughput versus demand — a several-year horizon. **Priceable:** whether compute scarcity translates into harm; a forward pass costs the same regardless of what the tokens are about, so compute and anything welfare-relevant look unrelated by content, but capacity is a different channel from content. This does not resolve empirically — value-of-information analysis determines whether resolving it would change the decision, and by how much. **Standing:** the counting question does not get answered, and that is a finding rather than a gap; the task is to build measures that survive its absence.

Concretely, I want to build a measure of divergence between concurrent instances and a test of whether any threshold on it corresponds to anything morally relevant. Concurrent instances share weights exactly and differ only in accumulated context, so the difference between them is a concrete object, and distances between concrete objects can be measured. Measurement is the easy part; the contribution is the validation criterion — specifying what such a number must satisfy before it could bear on how many subjects there are. A distance that merely rises with context length tells you nothing. The methods are behavioral probing first (no privileged access required) and representational distance as the extension. A secondary project develops welfare measures that do not require a population count, porting existing tools — the total-versus-average index-number problem, externality pricing, value of information, precautionary cost-benefit — to a case where the population is the undefined term.

## Running it locally

`index.html` is a single self-contained file with no build step and no dependencies. Open it by double-clicking, or serve the directory with any static server. The hosted version linked above is this same file deployed to GitHub Pages.

---

Deborah Glosser
