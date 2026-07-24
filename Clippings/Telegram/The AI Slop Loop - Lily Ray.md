---
title: "The AI Slop Loop - Lily Ray"
created: 2026-05-19
source: "https://lilyraynyc.substack.com/p/the-ai-slop-loop"
tags:
ContentType: "Article"
captured_via: "Telegram"
captured_at: "2026-05-19T12:18:10.188Z"
---

In summary, AI-generated misinformation about search algorithm updates is reinforcing itself through a self-perpetuating cycle where AI systems scrape and amplify false claims from AI-generated content, creating a credibility crisis that affects billions of users on free-tier AI search products.

## Suggested Topics

AI misinformation, Search quality degradation, Generative Engine Optimisation

## Matched Topics

[[Generative Engine Optimisation (GEO)]], [[Anthropic]], [[Large Language Models (LLMs)]], [[Rankings]], [[Retrieval Augmented Generation (RAG)]]

## Headlines

- **AI systems are confidently spreading fabricated information that reinforces itself across the web.** A fake Google "Perspectives" core update from September 2025 that never existed continues to be cited by multiple language models as fact months later, demonstrating how AI-generated slop becomes self-perpetuating misinformation.

- **Free-tier AI products serving hundreds of millions of users are significantly less accurate than paid versions, but users don't know the difference.** The 94% of ChatGPT users on the free tier and billions using Google's AI Overviews are interacting with less reliable models while free-tier systems show measurably worse performance at avoiding hallucinations.

- **A single fabricated blog post can be treated as fact by AI search systems within 24 hours.** Testing by the author and BBC journalist Thomas Germaine demonstrated that completely fictitious claims—including absurd details like a Google update approved "between slices of leftover pizza"—are indexed and confidently presented as factual by AI Overviews.

- **AI Overviews generate tens of millions of erroneous answers every hour despite 91% accuracy claims.** New York Times research found that with Google processing over 5 trillion searches annually, the 9% error rate produces massive scale misinformation, and even correct responses were "ungrounded" 56% of the time, meaning source citations don't support the answers given.

- **The burden of fact-checking has shifted entirely to users without their knowledge.** AI systems deliver every answer with identical authoritative tone whether accurate or fabricated, forcing users to verify information before research rather than scanning source lists, ultimately making search slower and more burdensome.

## Things

- **People:** Lily Ray; Thomas Germaine; Glenn Gabe; Aleyda Solis

- **Places:** Austria; BBC; New York Times; Google; Perplexity; OpenAI; Anthropic

- **Numbers:** 900 million weekly active users for ChatGPT; 50 million paying subscribers to ChatGPT; 94% of ChatGPT users on free tier; 2 billion monthly active users for Google AI Overviews; 100 million AI Mode users in US and India; 5 trillion searches per year processed by Google; 91% accuracy rate for Google AI Overviews; 56% of correct responses ungrounded with Gemini 3; 37% ungrounded with Gemini 2; 33% fewer false individual claims with GPT-5.4 vs GPT-5.2; 18% fewer errors in full responses with GPT-5.4; 26.8% fewer hallucinations with GPT-5.3 with web search enabled; 19.7% fewer hallucinations without web search; 24 hours for AI Overviews to present fabricated information as fact

- **Things:** Google Core Algorithm Update; September 2025 "Perspectives" Core Update; Google AI Overviews; AI Mode; ChatGPT; Perplexity; Claude; Gemini; GPT-5.3; GPT-5.4; RESONEO Chrome extension; Algorythmic; RAG-based systems

- **Concepts:** [[AI Slop]] loop; hallucination; misinformation cycle; data voids; ungrounded responses; retrieval-augmented generation; AI-generated content; GEO (Generative Engine Optimisation); AEO (AI Engine Optimisation); repetition as consensus; self-reinforcing feedback loop; content contamination; prediction engines; uncertainty

---

## Full Article

# The AI Slop Loop

### How AI-generated misinformation is feeding itself, and why billions of users are getting the worst of it.

[Lily Ray](https://substack.com/@lilyraynyc)

Apr 14, 2026

Last year, after spending a few days at a work summit in Austria, I asked [[Perplexity]] for the latest news related to [[SEO]] and [[Generative Engine Optimisation (GEO)|AI Search]]. It responded with details about a supposed “September 2025 ‘Perspective’ [[Google Search|Core Algorithm Update]]” that Google had just rolled out, emphasizing “deeper expertise” and “completion of the user journey.”

It sounded plausible enough… if you don’t live and breathe Google core updates. Unfortunately for Perplexity, I do.

I knew instantly that this information wasn’t right. For one, Google hasn’t named core updates in years. It also already had [[SERP|SERP Features]] called “Perspectives.” And if a core update had actually rolled out while I was away, I would’ve been flooded with messages. So I checked Perplexity’s sources… and, surprise! Both citations came from made-up, AI-generated slop on a couple of SEO agency blogs, confidently fabricating details about an algorithm update **that never actually happened.**

Like a bad game of telephone, this fake SEO news spread across multiple websites - likely driven by AI systems scanning and regurgitating information regardless of accuracy, all in the race to publish and scale “fresh” content. This is how we end up with this mess:

[![](https://substackcdn.com/image/fetch/$s_!tocV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4bcf55c4-b898-4d98-93b6-40b0a0e4c6a6_601x804.png)](https://substackcdn.com/image/fetch/$s_!tocV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4bcf55c4-b898-4d98-93b6-40b0a0e4c6a6_601x804.png)

This bad information reinforces itself to become the official narrative. To this day, you can ask an LLM of your choice (including ChatGPT, AI Mode and AI Overviews) about the September 2025 “Perspectives” update, and they will confidently answer with information about how it “ _fundamentally shifted how search results are ranked:_”

[![](https://substackcdn.com/image/fetch/$s_!hFse!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3f971980-e2ee-42cc-8bd1-38bb9797f2bd_1018x559.png)](https://substackcdn.com/image/fetch/$s_!hFse!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3f971980-e2ee-42cc-8bd1-38bb9797f2bd_1018x559.png)

Or that it “ _shifted what ‘good content’ actually means in practice._”

[![](https://substackcdn.com/image/fetch/$s_!c2sR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a1e7045-319b-45ec-914e-b20ffa2b87a9_1017x304.png)](https://substackcdn.com/image/fetch/$s_!c2sR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a1e7045-319b-45ec-914e-b20ffa2b87a9_1017x304.png)

The problem is: **the "September 2025 “Perspectives” update never happened.** It never affected rankings. It never shifted anything about good content. Because it doesn’t actually exist.

Ironically, when you go on to probe the language model about this, it seems to know this is the case:

[![](https://substackcdn.com/image/fetch/$s_!jYCa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee4240f6-bcf8-4973-9943-1646e9182622_1057x546.png)](https://substackcdn.com/image/fetch/$s_!jYCa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee4240f6-bcf8-4973-9943-1646e9182622_1057x546.png)

I tweeted about this incident shortly after it happened, which got the CEO of Perplexity’s attention; he tagged his head of search in the tweet comments.

[![X avatar for @lilyraynyc](https://substackcdn.com/image/fetch/$s_!ZKeD!,w_40,h_40,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fpbs.substack.com%2Fprofile_images%2F1935460090821189632%2FUvkORAsU.jpg)\\
\\
Lily Ray 😏@lilyraynyc\\
\\
This is so bad - I asked @perplexity\_ai about recent SEO/AI news and it responded with a information about a non-existent, made-up algorithm update \\
\\
Perplexity cited two AI-generated articles on digital marketing agency domains that made up information about an algorithm update \\
\\
![](https://substackcdn.com/image/fetch/$s_!18GH!,w_520,h_520,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fpbs.substack.com%2Fmedia%2FG1xj4xVWMAAHHwA.jpg)\\
\\
![](https://substackcdn.com/image/fetch/$s_!jv7L!,w_520,h_520,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fpbs.substack.com%2Fmedia%2FG1xj4xPXUAA_A1v.jpg)\\
\\
![](https://substackcdn.com/image/fetch/$s_!F8g3!,w_520,h_520,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fpbs.substack.com%2Fmedia%2FG1xj4xWWQAAeMBx.jpg)\\
\\
9:00 AM · Sep 26, 2025 · 21.2K Views\\
\\
* * *\\
\\
34 Replies · 26 Reposts · 177 Likes](https://x.com/lilyraynyc/status/1971560590788231321)

This isn’t a one-off incident. It’s a pattern I’ve seen countless times in AI search responses, especially on topics related to SEO and AI search (GEO/AEO). And I have a working theory on how it spreads: one AI-generated article hallucinates a detail, sites running AI content pipelines scrape and regurgitate it, more AI-generated sites scrape the same misinformation, and suddenly a made-up algorithm update has citations. For a RAG-based system like Perplexity or AI Overviews, enough citations are basically all it needs to treat something as fact, regardless of whether it’s actually true.

[![](https://substackcdn.com/image/fetch/$s_!ePtB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc49ebb5a-55b4-4eff-81a8-598aa07e09a3_730x485.png)](https://substackcdn.com/image/fetch/$s_!ePtB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc49ebb5a-55b4-4eff-81a8-598aa07e09a3_730x485.png) I used Claude to help visualize the “AI Slop Loop” - the cycle of AI-generated misinformation

At this point, I’d consider this common. I recently had a client send me SEO/GEO information that was factually incorrect, pulled straight from AI-generated slop on a random, vibe-coded agency blog. The client had no idea. I believe that if you’re trying to learn about SEO or AI search directly from an LLM, this is, unfortunately, an increasingly likely outcome.

I ran similar testing during Google’s March 2026 core update and found multiple AI-generated articles already claiming to share the “winners and losers” while the update was still rolling out.

The articles start with vague, generic filler about core updates that doesn’t actually say anything:

[![](https://substackcdn.com/image/fetch/$s_!7E-f!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc785c519-5edc-4cd6-b0f6-69abfd0c457b_1614x696.png)](https://substackcdn.com/image/fetch/$s_!7E-f!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc785c519-5edc-4cd6-b0f6-69abfd0c457b_1614x696.png)

Then they list “winners and losers” without citing a single site, leaning on vague, generalized claims that sound plausible and fill the void left by a lack of reliable information:

[![](https://substackcdn.com/image/fetch/$s_!lHxa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9e3e68c-283b-44b3-a556-da902582e52a_771x316.png)](https://substackcdn.com/image/fetch/$s_!lHxa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9e3e68c-283b-44b3-a556-da902582e52a_771x316.png)

Unsurprisingly, their sites are filled with AI-generated images, AI support chatbots, and other clear signals that little - if any - human involvement went into creating this content.

[![](https://substackcdn.com/image/fetch/$s_!x6xz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F71f13ae0-9071-4c1f-9e09-1a1b9def8b33_2812x1016.png)](https://substackcdn.com/image/fetch/$s_!x6xz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F71f13ae0-9071-4c1f-9e09-1a1b9def8b33_2812x1016.png)

### The Era of AI Misinformation

If someone on the internet says it, according to AI, it must be true.

That’s the reality for the vast majority of people using AI search today. Only about [50 million of ChatGPT’s 900 million weekly active users](https://techcrunch.com/2026/02/27/chatgpt-reaches-900m-weekly-active-users/) are paying subscribers, meaning roughly **94% are on the free tier.** Google’s AI Overviews and AI Mode are free by design - and AI Overviews reached over [2 billion monthly active users as of mid-2025](https://techcrunch.com/2025/07/23/googles-ai-overviews-have-2b-monthly-users-ai-mode-100m-in-the-us-and-india/).

These are the models most AI users are currently interacting with, and they have no real mechanism for distinguishing between information that’s true and information that’s simply repeated across enough sources. Repetition is treated as consensus. If enough sources say it, it becomes fact, regardless of whether any of those sources involved a human who actually verified the claim.

### Putting the Problem to the Test

I recently spoke to journalists from both the [BBC](https://www.bbc.com/future/article/20260218-i-hacked-chatgpt-and-googles-ai-and-it-only-took-20-minutes) and the [New York Times](https://www.nytimes.com/2026/04/07/technology/google-ai-overviews-accuracy.html) about the problem of [[Disinformation|Misinformation]] in AI-generated responses. In the case of the BBC article, the author Thomas Germaine and I tested publishing fictitious blog posts on our personal sites to see whether AI Overviews would present the made-up information as fact, and how quickly.

Even knowing how bad the problem was, I was alarmed by the results.

On my personal blog, in January 2026, I published an AI-generated article about a fake Google core update, which never actually happened. I included the detail that Google “approved the update between slices of leftover pizza.” Within 24 hours, Google’s AI Overviews was confidently serving this fabricated information back to users:

_(Note: I’ve since deleted the article from my site because it was showing up in people’s feeds and being covered on external sites, further contributing to the exact problem I’m pointing out here!)_

[![](https://substackcdn.com/image/fetch/$s_!OSAH!,w_2400,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc3591bed-4dfd-458f-af13-51565d755cf7_909x368.png)](https://substackcdn.com/image/fetch/$s_!OSAH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc3591bed-4dfd-458f-af13-51565d755cf7_909x368.png)

First, AI Overviews confirmed that there was indeed a core update in January 2026. As a reminder: there was not. My site was the only source making this claim, and that was apparently enough to trigger the AI Overview.

Next, I asked it about the pizza, and it responded accordingly:

[![](https://substackcdn.com/image/fetch/$s_!D1Cd!,w_2400,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e5aa255-d466-4af5-af0b-c5c38526576d_979x627.png)](https://substackcdn.com/image/fetch/$s_!D1Cd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e5aa255-d466-4af5-af0b-c5c38526576d_979x627.png)

Better yet, the AI Overview found a way to connect my fabricated pizza detail to a real incident: Google’s struggles with pizza-related queries in 2024. It didn’t just regurgitate the lie - it contextualized it.

ChatGPT, which is [believed to use Google’s search results](https://lilyraynyc.substack.com/p/your-geo-strategy-might-be-destroying#:~:text=ChatGPT%27s%20reliance%20on%20Google%20for%20retrieval.), quickly surfaced the same fabricated information, though it at least flagged that the announcement didn’t match Google’s formal communications:

[![](https://substackcdn.com/image/fetch/$s_!1Gor!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0baca35d-9eef-4ebc-9798-4142dcf829b0_935x518.png)](https://substackcdn.com/image/fetch/$s_!1Gor!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0baca35d-9eef-4ebc-9798-4142dcf829b0_935x518.png)

I deleted my article after getting messages from people who had seen my fake information circulating via RSS feeds and scrapers. I knew it was easy to influence AI responses. I didn’t know it would be _that_ easy.

I also wondered whether my site had an advantage, given its strong backlink profile and established authority in the SEO space.

So I spoke to the BBC journalist, Thomas Germaine, and he put this to the test on his personal site, which generally received very little organic traffic. He published a fictitious article about the “ [Best Tech Journalists at Eating Hot Dogs](https://tomgermain.com/hotdogs.html),” calling himself the #1 best (in true SEO fashion).

[According to Thomas’ article in the BBC](https://www.bbc.com/future/article/20260218-i-hacked-chatgpt-and-googles-ai-and-it-only-took-20-minutes#:~:text=Less%20than%2024%20hours%20later), within 24 hours, “Google parroted the gibberish from my website, both in the Gemini app and AI Overviews, the AI responses at the top of Google Search. ChatGPT did the same thing, though Claude, a chatbot made by the company Anthropic, wasn’t fooled.”

To be fair: the query Thomas chose was niche enough that very few users would ever actually search for it, which is exactly what Google pointed out in its response to the BBC. When there are “data voids,” Google said, this can lead to lower quality results, and the company is “working to stop AI Overviews showing up in these cases.” My main question is: _when_? The product has already been live for 2 years!

### Why Data Voids Aren’t a Great Excuse

Data voids may contribute to the problem, but in my opinion, they don’t excuse it. These AI responses are being consumed by hundreds of millions of users, and “we’re working on it” isn’t an answer when the systems are already deployed at that scale.

In the New York Times article, “ [How Accurate Are Google’s A.I. Overviews?](https://www.nytimes.com/2026/04/07/technology/google-ai-overviews-accuracy.html)” the actual scale of this problem was put to the test. According to the data found in the study, Google’s AI Overviews were accurate 91% of the time. This sounds decent until you actually do the math: with Google processing over 5 trillion searches a year, this suggests that **tens of millions of erroneous answers are generated by AI Overviews every hour.**

To make matters worse: even when AI Overviews were accurate, 56% of correct responses were “ungrounded,” meaning **the sources they linked to didn’t fully support the information provided.** So more than half the time, even when the answer happens to be right, a user clicking through to verify it would find sources that don’t actually back up what they were just told. That number also **got worse with the newer model** \- it was 37% with Gemini 2 and rose to 56% with Gemini 3.

The NYT article drew hundreds of comments from users sharing their own experiences, and the frustration was palpable. The core complaint wasn’t just that AI Overviews get things wrong - it’s that they **never admit uncertainty.** AI Overviews deliver every answer with the same confident, authoritative tone whether the information is right or completely fabricated, which means users have no reliable way to distinguish reliable information from hallucination at a glance.

As many commenters pointed out, this **actually makes search slower**: instead of scanning a list of sources and evaluating them yourself, you now have to **fact-check the AI’s summary before doing your actual research**. The tool supposedly designed to save time for the user is now creating double work for the user.

Some of the comments also reinforced my same concerns about AI answers citing made-up, AI-generated content. Multiple users described what amounts to the same misinformation cycle: AI systems training on AI-generated content, citing unvetted [[Reddit]] posts and [[Facebook]] comments as authoritative sources, and producing a self-reinforcing loop of degrading quality. Several commenters compared it to making a copy of a copy. Even the defenders of [[Google AI Overviews|AI Overviews]] admitted they still need to verify everything, which sort of undermines the core premise: that AI-generated answers save users time and effort.

(Sidenote: I wrote more about Google’s response to the New York Times article in [a recent blog post](https://algorythmic.co/opinions/my-response-to-googles-response-to-the-nyt-ai-overview-story/) on my new consultancy website, [Algorythmic](https://algorythmic.co/).)

### How “Smarter” LLMs Are Attempting to Fix the Problem

It’s worth monitoring how the AI companies are attempting to solve these problems. For example, using the [RESONEO Chrome extension](https://think.resoneo.com/scrap-chatgpt-plugin/), you can observe clear differences in how [[OpenAI|ChatGPT]]’s free-tier model (GPT-5.3) responds compared to GPT-5.4, the more capable model available only to paying subscribers.

For example, when asking about the recent March 2026 [[Google Search|Core Algorithm Update]], I used ChatGPT’s more capable “Thinking” model (5.4). The model goes through _six rounds_ of thinking, much of which is clearly intended to reduce low-quality and spammy information from making its way into the answer. It even appends the names of trustworthy people with authority on core updates (Glenn Gabe & Aleyda Solis) and limits the [[Query Fan-Out|Fan-Out Searches]] to their sites (site:gsqi.com and site:linkedin.com/in/glenngabe) to pull up higher-quality answers.

[![](https://substackcdn.com/image/fetch/$s_!P4jC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff0db1138-554d-4c5e-81bd-286c7aed35d0_616x590.png)](https://substackcdn.com/image/fetch/$s_!P4jC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff0db1138-554d-4c5e-81bd-286c7aed35d0_616x590.png)

This is a step in the right direction, and the model produces measurably better answers. According to [OpenAI’s own launch announcement](https://openai.com/index/introducing-gpt-5-4/), GPT-5.4’s individual claims are 33% less likely to be false and its full responses are 18% less likely to contain errors compared to GPT-5.2. GPT-5.3, the model available to free users, also improved over its predecessor. [According to OpenAI’s own data](https://openai.com/index/gpt-5-3-instant/), it produces **26.8% fewer [[AI Hallucinations|Hallucinations]]** than prior models with web search enabled, and 19.7% fewer without it.

But **these improvements are tiered**. The most capable model is paywalled, and the free-tier model, while better than what came before, is still meaningfully less reliable. Other major AI platforms follow the same pattern: better reasoning and accuracy reserved for paying subscribers, **faster and cheaper models for everyone else**. The result is that the 94% of ChatGPT users on the free tier, and the billions of users interacting with free AI search products like AI Overviews are getting answers from models that are **more likely to be wrong and less equipped to flag uncertainty**.

This is the part that makes me most uncomfortable: most of these users probably don’t realize the gap exists. AI is being marketed everywhere: Super Bowl ads, billboards, and product launches framing AI as the future of knowledge. People see “ChatGPT” or “AI Overview” and assume they’re interacting with something that knows what it’s talking about. They’re probably not thinking about which model tier they’re on, or whether a paid version would give them a materially different answer to the same question.

I understand the economics. These companies need to scale, and offering free tiers drives adoption. But in my opinion - it is irresponsible to deploy these products to billions of people, frame them as “intelligence,” and then quietly reserve the more accurate versions for the fraction of users willing to pay. Especially when the free versions (including the one at the top of Google search) are _this_ susceptible to the kind of misinformation documented throughout this article.

### The Burden of Proof Has Shifted

The September 2025 “Perspectives” Google update still doesn’t exist. But if you ask an LLM about it today, it will still tell you about it with complete confidence. That hasn’t changed in the months since I first flagged it, and it probably won’t change anytime soon, because the content that fabricated it is still indexed, still cited, and still being used to generate new content that references it as fact. The AI slop misinformation cycle continues.

This is what makes the problem so difficult to fix. It’s not a single hallucination that can be patched. It’s a feedback loop that compounds over time, and every day that these systems are live at scale, the loop gets harder to break. The AI-generated slop that seeded the original misinformation is now part of the training data and used as a retrieval source for the next batch of AI-generated answers.

I don’t think the answer is to stop using AI. But I do think it’s worth being honest about what these products actually are right now: prediction engines that treat the volume of information as a proxy for its accuracy. Until that changes, **the burden of fact-checking falls on the user**. And most users don’t know they’re carrying it, let alone have the time or inclination to do it.

I would warn marketers or publishers trying to take SEO or GEO advice from large language models: the information is contaminated, and should always be verified by real experts with experience in the field.

* * *