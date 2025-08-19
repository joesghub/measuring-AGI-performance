# How do we determine the intelligence of an AGI?

## Breaking News! Grok 4 beats GPT-5

I was reading AI Breakfast, a weekly analysis of the latest AI projects, products, and news, when I learned that Grok 4 outperformed the newly relesed GPT-5!

> In the new ARC-AGI-2 benchmark report, Grok 4 (Thinking) still outperformed GPT-5 (High), scoring ~16% versus 9.9%, albeit at a significantly higher cost per task ($2–$4 vs. $0.73).
> - AI Breakfast, August 8, 2025 [1]

![ARC AGI Report](https://github.com/user-attachments/assets/c18d2b1b-0ea7-41aa-adb7-ed9be408aaa3)

At first I was surprised as I thought the newer LLM would perform better. Then it led to me to ask, what do these scores mean?



## What is the ARC-AGI Benchmark Report?

> The ARC (Abstract and Reasoning Corpus) Prize is a non-profit dedicated to accelerating the development of AGI (Artificial General Intelligence). They achieve this by creating and curating human-calibrated benchmarks that serve as a clear and objective measure of progress towards AGI. The benchmarks incentivize researchers to explore approaches that go beyond pattern matching and memorization. [2]

How can they be objective I wondered and what did that objectivity mean?

Well, in 2019 François Chollet published the influential paper "On the Measure of Intelligence" where he introduced the "Abstract and Reasoning Corpus" for Artificial General Intelligence (ARC-AGI) benchmark to measure fluid intelligence. 

A principle underlying ARC-AGI's design is the need to create a **fair and meaningful** comparison between artificial intelligence and human intelligence. 

To achieve this, ARC-AGI focuses on **fluid intelligence** (the ability to reason, solve novel problems, and adapt to new situations) rather than **crystallized intelligence**, which relies on accumulated knowledge and skills. [3]

This distinction between intelligence's highlights the different ways humans think. Although they are both valuable in our daily lives, its more valuable that we have fluidly intelligent AGI. 



## What is Intelligence?

> Intelligence is what you use when you don't know what to do: when neither innateness nor learning has prepared you for the particular situation.
> - Jean Piaget, Psychologist

Is it time to break out the thinking caps again? Apparently yes according to Jean!

And in the case of AGI, we have to define what intelligence is through the tests it is given. 

"AGI is a system that can efficiently acquire new skills outside of its training data. This means that a system is able to adapt to new problems it has not seen before and that its creators (developers) did not anticipate." [3]



## Testing Intelligence in AGI

ARC tasks look like small grid-based puzzles. Here's a quick example:

> Input: A grid with a red square on the left.
> 
> Output: The same grid, but the red square is mirrored to the right side.
> 
> Task: Given a new grid, apply the same transformation (Abstract rule = mirroring).

<img width="1600" height="915" alt="arc-agi-task-c6e1b8da" src="https://github.com/user-attachments/assets/80d9cd97-1d22-46f9-96f6-dcd699b2a443" /> [4]

This way instead of memorization, the AI must infer the abstract rule, then apply it to new situations.

After seeing a test problem, it struck me that I've answered problems like that before: on IQ tests!

> **Prompt**: Is it fair to say the arc-agi benchmark is similar to an IQ test for humans?
>
>**Output**: Yes that’s actually a fair analogy! Here’s why:
>
>- IQ tests for humans are designed to measure fluid intelligence (the ability to reason, abstract, and solve novel problems) without relying only on learned knowledge.
>
>- ARC-AGI is explicitly built to measure fluid intelligence in AI: Can it learn a new transformation rule from a handful of examples and generalize to new cases?

Now that we understand the testing, lets unravel the mechanics of scoring!



## Scoring Intelligence in AI

For context, all the tasks in the benchmark are human solveable. Each task was solved in 2 attempts or less. 

This sets the baseline at 100% for humans! 

Similarly, the AIs were allowed up to two attempts at each task. They also needed to have the exact output, to the pixel. 

From 2019 - 2024 most AI's scored in the 20% - 35% range ont he ARC-AGI 1. Until late last year when OpenAI's o3-preview scored an 87%!

However, the ARC prize recently released the ARC-AGI 2 Benchmark and it has reduced AI success rates back into the single digits range.

With all this hype about AI, knowing the limitations and capabilities of these tools sets us up for success. 

It also helps quell natural fears about replacement and underscores the value of human thinking!



## Understanding AI "Thinking"

Not all models are created the same. While we have been exposed to LLMs (Large Language Models), they are not the only models capable of solving these problems. 

Program-Synthesis models are equipped with a library of basic functions that it searches through to generate candidate programs capable of explaining the input-output examples.

LLMs are pretrained on vast internet text and code. They treat the grid as a kind of structured input (code). Then use pattern completion to guess transformations, applying few-shot reasoning on the provided examples.

<img width="527" height="835" alt="simple-testing-agi" src="https://github.com/user-attachments/assets/fd7a922f-4b57-4d78-b90b-d07fb105e663" />

Program-Synthesis systems struggle when there isn't an exact matching function in its library. Say if “shift_diagonal” isn’t in the library, it has to compose two functions (shift_down + shift_right), which increases search complexity.

Whereas an LLM might latch onto the wrong heuristic. Instead of “shift one step diagonally”, it may infer “always move to bottom-right corner”.




## Food for Thought

It’s tempting to compare Grok 4’s 16% and GPT-5’s 9.9% as if they were final report cards. But in reality, these scores highlight how far AI still has to go. 

Humans effortlessly achieve near-100% on these tasks, not because we’ve memorized solutions, but because we can adapt to the unknown.

That is the essence of intelligence and why benchmarks like ARC-AGI remind us that while AI may assist, human reasoning is still the gold standard!


### 🤝🏾  Connect with Me

[Joe's LinkedIn](https://www.linkedin.com/in/joeslnkdin/)

[1]: https://aibreakfast.beehiiv.com/p/gpt-5-released-f255?_bhlid=38b2364114aa3f9d07c0f213eb2b9704f71e8e29&utm_campaign=gpt-5-released&utm_medium=newsletter&utm_source=aibreakfast.beehiiv.com 
[2]: https://arcprize.org/about
[3]: https://arcprize.org/arc-agi
[4]: https://arcprize.org/blog/oai-o3-pub-breakthrough

