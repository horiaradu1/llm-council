# LLM Council

A multi-model AI agora for structured debate, critique, and synthesis.

An MCP server for discussing complex topics across multiple LLMs — Claude, GPT, Gemini, Grok, and local models.

## Idea

This project explores a way to let multiple AI models discuss the same complex prompt, question, or idea.

Instead of relying on a single model response, the goal is to experiment with workflows where models such as GPT, Claude, Gemini, Grok, and local models can answer, challenge assumptions, expose disagreements, and help synthesize a better final response.

Single-model answers can miss perspectives, overfit to the user's framing, or present uncertain claims too confidently. `llm-council` aims to let multiple models discuss, debate, and critique each other on the same question, instead of answering in isolation.

Single-model answers can sometimes be overly agreeable, insufficiently critical, or confident about assumptions that were not independently checked.

The project could support two complementary council modes:

### Multi-provider council

A council made of different models from different providers, for example GPT, Claude, Gemini, Grok, and local models.

Each model answers independently, then the system compares their reasoning, highlights agreements and disagreements, and synthesizes a final response.

### Peer-review council

A council made of multiple independent agents, which may use the same underlying model or different models.

This mode is useful when the goal is not only to compare providers, but also to reduce single-answer bias. Several advisors can analyze the same question independently, review each other's outputs anonymously, and then produce a final verdict through a chairman/synthesizer step.

The intended flow is:

1. The user submits a question, idea, decision, or piece of work.
2. Multiple advisors analyze it independently, each from a different angle.
3. Advisors peer-review each other's responses without knowing who wrote them.
4. A chairman/synthesizer combines the results into a final answer.
5. The final output explains where the advisors agree, where they disagree, what assumptions were challenged, and what recommendation follows.

This direction is inspired by Andrej Karpathy's "LLM Council" methodology and by projects such as `claude-skills-llm-council`, which explore council-style workflows using multiple agents.

## Possible Direction

The project may evolve into an MCP server or orchestration layer for multi-model and multi-agent discussions.

Potential areas to explore:

- independent answers from multiple models
- councils across different providers
- same-model peer-review councils
- anonymous cross-review between advisors
- debate and refinement flows
- chairman/synthesizer final verdicts
- agreement/disagreement summaries
- confidence and uncertainty tracking
- storing discussion transcripts
- reusable council templates for different tasks

### Important concept to explore - LLM WIKI:

Store all the data in vaults/wikis, some sort of sorted "brain" for the information to better tailor to your needs

[llm-wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)

## References and Inspiration

- [karpathy/llm-council](https://github.com/karpathy/llm-council)  
  Inspiration for the multi-model council flow: independent model answers, anonymous cross-review, and final chairman synthesis.

- [aiwithremy/claude-skills-llm-council](https://github.com/aiwithremy/claude-skills-llm-council/blob/main/SKILL.md)  
  Inspiration for a same-model peer-review council using multiple agents with different thinking lenses.

`llm-council` aims to explore these ideas as an MCP server or orchestration layer, with support for both multi-provider councils and same-model peer-review councils.
