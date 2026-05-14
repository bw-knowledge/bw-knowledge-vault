---
title: "Stop Treating AI Visibility as One Problem. It’s Actually Three, on Three Different Layers."
created: 2026-05-14
source: "https://duaneforresterdecodes.substack.com/p/stop-treating-ai-visibility-as-one"
tags:
ContentType: "Article"
captured_via: "Telegram"
captured_at: "2026-05-14T14:02:14.339Z"
---

In summary, AI visibility for brands operates across three distinct structural layers—retrieval, knowledge graphs, and context graphs—each requiring different strategies and organizational ownership, and most marketing teams are concentrating effort on the wrong layer while neglecting the entity definition and governance work that will determine enterprise AI agent decisions.

## Suggested Topics

AI visibility strategy, Knowledge graph optimization, Enterprise AI agents

## Matched Topics

[[Generative Engine Optimisation (GEO)]]

## Headlines

- **AI visibility requires fixing three different layers, not just writing more content.** Retrieval, knowledge graphs, and context graphs each have distinct failure modes, organizational owners, and solutions; most teams are optimizing content retrieval while losing ground on entity definition where the real leverage exists.

- **Entity definition in knowledge graphs determines how AI systems represent your brand.** Brands that exist as clean, well-defined entities in knowledge graphs like Google's Knowledge Graph, Microsoft's Satori, and Wikidata get cited consistently, while fuzzy entity definitions lead to pattern-matching against competing candidates regardless of content volume.

- **Context graphs inside enterprise systems are becoming the new visibility battleground.** Google's Knowledge Catalog and the rise of task-specific AI agents mean your brand must arrive at customers' internal context graphs in a consistent, well-structured state to influence agent reasoning about your business.

- **Governed visibility requires cross-functional work across retrieval, knowledge graph, and context graph layers.** Marketing owns the knowledge graph layer directly but must influence retrieval infrastructure (shared with web and IT) and ensure clean ingestion into enterprise context graphs controlled by customer IT departments.

- **The brands building governed visibility now will appear prepared in eighteen months while those relying solely on content volume will lose visibility ground.** The discipline requires clean entity definition, consistent third-party representation, reliable structured data, and category positioning that withstands agent traversal across relationship networks.

## Things

- **People:** Duane Forrester

- **Places:** ChatGPT, Perplexity, Google Cloud Next '26, Google, Microsoft Research, Wikidata, schema.org

- **Numbers:** 40 percent of enterprise applications will feature task-specific AI agents by end of 2026; less than 5 percent in 2025

- **Things:** Retrieval-augmented generation (RAG), Knowledge Catalog, Google Knowledge Graph, Microsoft Satori, context graph, knowledge graph, schema markup, AI agents, AI Overviews

- **Concepts:** Governed retrieval, governed visibility, entity recognition, entity definition, retrieval layer, relationship layer, context layer, pattern-matching, hallucination, knowledge graph architecture, operational context, business semantics, third-party signal

---

## Full Article

# [Duane Forrester Decodes](https://duaneforresterdecodes.substack.com/)

SubscribeSign in

[![Duane Forrester Decodes](https://substackcdn.com/image/fetch/$s_!Qx76!,w_144,h_144,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F613e8843-2ee4-4396-81a4-11c6ff18a1d8_1400x1400.png)](https://duaneforresterdecodes.substack.com/)

Duane Forrester Decodes

Stop Treating AI Visibility as One Problem. It’s Actually Three, on Three Different Layers.

6

7

1

1×

0:00

Current time: 0:00 / Total time: -16:35

-16:35

Audio playback is not supported on your browser. Please upgrade.

## Stop Treating AI Visibility as One Problem. It’s Actually Three, on Three Different Layers.

Each layer has different failure modes, different fixes, and different organizational owners. Most marketing teams are working hard on the wrong one.

[![Duane Forrester Decodes's avatar](https://substackcdn.com/image/fetch/$s_!dJ0A!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9350c9af-d0be-4715-b265-1176132ba113_1024x1024.png)](https://substack.com/@duaneforresterdecodes)

[Duane Forrester Decodes](https://substack.com/@duaneforresterdecodes)

May 10, 2026

6

7

1

Share

Transcript

When a brand stops appearing in ChatGPT, or when its share of voice in Perplexity drops by half over a quarter, the typical response from the marketing org is to write more content. Sometimes a lot more. The thinking goes that if AI systems aren’t surfacing the brand, the fix is to feed them more material to work with. That instinct is a misdiagnosis. It’s a retrieval-layer fix being applied to what is increasingly a different kind of problem entirely, and the cost shows up as wasted budget, missed quarters, and a creeping sense that the work isn’t connecting to the outcomes anymore.

The mistake is treating AI visibility as a single problem when it isn’t. There are three structurally different layers between your brand and the answer a user receives, each with its own failure modes, its own fixes, and increasingly its own organizational owner. Diagnose the wrong layer and the fix doesn’t land.

#### Where most of the conversation has been living

The first layer is retrieval. This is where the AI search optimization conversation has spent most of the last two years. The mechanics are familiar in shape if not in detail. When a model needs to answer a question grounded in real-world content, it pulls relevant material from external sources and uses that material to construct the response. The technical name is retrieval-augmented generation, or RAG, and the layer it operates on is the gateway between your content and the model’s output.

This is where crawlability, parseability, and chunk-friendliness do their work. If your content can’t be retrieved cleanly, nothing downstream matters. The visibility tracking platforms most marketing teams have evaluated this year measure outcomes that depend on this layer functioning, which is why they tend to reward the same disciplines that produced good results in classical search: structured content, schema markup, self-contained answers, clean technical implementation.

But retrieval has a structural limit, and Microsoft Research has been [unusually direct about it](https://www.microsoft.com/en-us/research/blog/graphrag-unlocking-llm-discovery-on-narrative-private-data/). Plain RAG, in their words, struggles to connect the dots. It retrieves chunks of text that look relevant to the question, but it cannot reason about how those chunks relate to each other. When the answer requires synthesizing information across multiple sources, or when the question is broad enough that the right answer depends on understanding patterns across an entire dataset, retrieval alone breaks down. The model gets the chunks and has to guess at the relationships, and guessing is where hallucinations enter.

The discipline question this layer asks is straightforward. Can the model retrieve our content at all, and is it retrieving the right content for the right query? Most marketing teams have some version of this work in flight already, even if the specific tactics have shifted from classical SEO. But retrieval is only the gateway. Even when a model retrieves your content correctly, what it does with it depends on whether you exist as a recognized thing in the layer above.

#### Where entity recognition does the real work

The second layer is the relationship layer, and the dominant structure on it is the knowledge graph. The major search infrastructures all maintain one. Google’s Knowledge Graph, Microsoft’s Satori, and the open knowledge graph built on Wikidata and schema.org collectively define how your brand is represented as an entity, what category you sit in, and which other entities you’re connected to.

This is the layer that decides whether AI Overviews and large language model responses treat you as a recognized member of your category, or as one fuzzy candidate string among many. Brands that exist as clean, well-defined entities get cited consistently. Brands that exist as undifferentiated tokens scattered across the open web get pattern-matched against fifty other candidates and lose more often than they win.

Knowledge graphs have been around long enough that the discipline is reasonably mature. Schema markup on owned properties, consistent naming and identifiers across the open web, structured presence on the high-trust nodes like Wikidata entries and review platforms, and the slow accumulation of brand mentions in contexts that the graph treats as authoritative. This is where the unlinked brand mentions conversation lives, because consistent contextual mentions strengthen the entity even without a hyperlink attached. The fix at this layer is structural rather than volume-based. Writing more content does almost nothing if the entity definition underneath it is fuzzy.

The discipline question here is harder than the retrieval-layer question. Are we a clean, defensible entity in our category, or are we still being pattern-matched against fifty other candidate strings? A brand that can’t answer that question affirmatively is going to lose ground in AI search regardless of how much content it produces, because the second layer is where the model decides what your content is actually about.

The knowledge graph tells the model what your brand is. But increasingly, your brand has to function inside a third layer that most marketing teams haven’t met yet, where the model isn’t just understanding you, it’s being asked to reason about you on behalf of someone making a decision.

#### The layer enterprise companies are quietly building right now

The third layer is the context graph, and this one needs a careful introduction because most of the marketing conversation hasn’t reached it yet.

A context graph has the same structural shape as a knowledge graph, with entities, relationships, and typed connections, but it’s grounded differently. A knowledge graph models the world. It tells you what things are and how they relate in general. A context graph models a specific organization’s data, decisions, policies, and operational reality. [The cleanest framing I’ve seen](https://www.tekst.com/blogs/context-graph-vs-knowledge-graph-the-enterprise-ai-distinction-that-actually-matters) calls a knowledge graph the library and a context graph the operating manual written by the people who actually run the place. The library tells you what exists. The operating manual tells you what’s relevant, what’s authorized, and what to do about it right now. The library is read-only semantic infrastructure. The operating manual is a living operational layer that grows every time a business process executes.

What separates a context graph from anything that came before it is that governance lives inside the graph rather than alongside it. Policies, permissions, validity windows, and authorization rules are nodes the graph itself queries, not external documentation applied at the edges. When an agent retrieves something from a context graph, the result has already been filtered through what’s currently authorized, currently valid, and currently applicable. The graph is also continuously evolving, so what it knows about you this week is not necessarily what it knew last quarter. That’s where the word “governed” comes from when people in this space talk about governed retrieval. It isn’t a frame, but rather the architecture.

That architecture used to be invisible to anyone outside the organization that built it, which is why marketers haven’t had to think about it. That changed at Google Cloud Next ‘26, when Google [introduced the Knowledge Catalog](https://cloud.google.com/blog/topics/google-cloud-next/next26-day-1-recap) inside its new Agentic Data Cloud. Google’s own description of the product, written in their own first-party blog content, says the Knowledge Catalog constructs a unified, dynamic context graph of your entire business, enabling you to ground agents in all of your business data and semantics. That sentence is the moment the term left the data-engineering blogs and entered enterprise procurement vocabulary.

The reason this matters for marketing is that context graphs are what’s going to power the next generation of agents inside your enterprise customers. Gartner [projects](https://www.gartner.com/en/newsroom/press-releases/2025-08-26-gartner-predicts-40-percent-of-enterprise-apps-will-feature-task-specific-ai-agents-by-2026-up-from-less-than-5-percent-in-2025) that 40 percent of enterprise applications will be integrated with task-specific AI agents by the end of 2026, up from less than 5 percent in 2025. Procurement agents, competitive intelligence agents, content strategy agents, vendor evaluation agents. These agents won’t be reasoning about your brand from the open web. They’ll be reasoning about your brand from inside their company’s context graph, and what that graph says about you depends on what got ingested into it.

That ingestion is where the work for marketing lives. The brand that arrives at the context graph fragmented arrives weak. If your category positioning is inconsistent across owned and earned media, the graph picks up the contradictions and represents you ambiguously. If your entity data is fuzzy on the second layer, it stays fuzzy when it gets pulled into the third. If your third-party signal is thin or contradictory, the graph has nothing solid to anchor to. The work is upstream of the graph, but the consequences land downstream of it, inside an agent’s reasoning process that you’ll never see directly.

I think of this discipline as _governed visibility_. The practice of making sure your brand arrives at the context graph in a state that holds up under governed retrieval. Clean entity definition, consistent third-party representation, reliable structured data, and a category position that doesn’t fall apart when an agent traverses the relationships around it. _Governed visibility_ isn’t a new tactic stack. It’s the result of doing the second-layer work well enough that the third layer has something solid to ingest.

The discipline question at this layer is the one most marketing teams haven’t started asking yet. When an agent inside our customer’s company is reasoning about us, what does it find, and is the version of us it finds the version we’d want it to act on?

Three layers, three different problems, three different fixes. But also three different responsibility zones, and that’s where most teams are quietly losing ground.

#### The reason most teams will lose this even though they’re working hard

Each layer maps to a different organizational responsibility, and most marketing teams only own one of the three cleanly.

• The retrieval layer is shared with web, dev, and sometimes IT. Marketing influences what gets published, but the infrastructure that makes content retrievable sits in someone else’s domain.

• The knowledge graph layer is genuinely marketing’s territory. Schema discipline, entity definition, third-party signal, brand consistency, the slow structural work that compounds over years.

• The context graph layer is where IT owns the infrastructure inside the customer’s organization, but marketing has to influence what gets ingested. The work is upstream and the consequences land downstream, often invisibly.

The teams that win in 2026 are the ones that figured out how to operate across all three responsibility zones rather than perfecting their work on just one. Most teams I see are still optimizing their owned content, which is the retrieval layer, while losing ground on entity definition, which is the knowledge graph layer, and remaining completely absent from the context graph conversation, which is the layer where some enterprise businesses are quietly standing up right now.

The work isn’t writing more content. The work is figuring out which layer the problem actually lives on, and building the disciplines to operate on all three. _Governed visibility_ is the third-layer discipline that marketing is going to have to develop whether or not the term sticks. The brands that build it now will look prepared in eighteen months. The brands that don’t will be wondering why their content investments stopped producing the visibility they used to.

* * *

If any of this lands or contradicts what you’re seeing inside your own teams, I want to hear about it. Drop a comment about which layer your work has been concentrated on, where you’re seeing the gaps, or where the responsibility zones break down inside your organization. The patterns are still forming, and the conversations in the comments tend to be fresher than anything else.

A lot of the measurement frameworks for this kind of work sit in [The Machine Layer](https://www.amazon.com/Machine-Layer-Visible-Trusted-Search/dp/B0G2WZKM59/ref=sr_1_1), which expands the original twelve KPIs for the GenAI era into something teams can actually run against.

Thanks for reading! This post is public so feel free to share it.

[Share](https://duaneforresterdecodes.substack.com/p/stop-treating-ai-visibility-as-one?utm_source=substack&utm_medium=email&utm_content=share&action=share)

[![Ali Van Straten's avatar](https://substackcdn.com/image/fetch/$s_!n7Iv!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack.com%2Fimg%2Favatars%2Fblack.png)](https://substack.com/profile/314584019-ali-van-straten)[![Recardo's avatar](https://substackcdn.com/image/fetch/$s_!Tfxb!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack.com%2Fimg%2Favatars%2Forange.png)](https://substack.com/profile/186782812-recardo)[![Dasean's avatar](https://substackcdn.com/image/fetch/$s_!s-s3!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76613fd6-0041-4298-b5c8-6ed89d54ba50_1280x1282.jpeg)](https://substack.com/profile/1323851-dasean)[![David Iwanow's avatar](https://substackcdn.com/image/fetch/$s_!-B02!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5fbc09c7-c2e3-40f6-a7ad-ac1a819d6477_150x150.jpeg)](https://substack.com/profile/25674140-david-iwanow)[![Samuel Lavoie's avatar](https://substackcdn.com/image/fetch/$s_!P4Ir!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fb766cfa7-f356-4286-bf66-a7d34803fa60_779x1171.jpeg)](https://substack.com/profile/4467505-samuel-lavoie)

6 Likes∙

[1 Restack](https://substack.com/note/p-197026879/restacks?utm_source=substack&utm_content=facepile-restacks)

#### Discussion about this episode

CommentsRestacks

![User's avatar](https://substackcdn.com/image/fetch/$s_!TnFC!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack.com%2Fimg%2Favatars%2Fdefault-light.png)

[![David Iwanow's avatar](https://substackcdn.com/image/fetch/$s_!-B02!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5fbc09c7-c2e3-40f6-a7ad-ac1a819d6477_150x150.jpeg)](https://substack.com/profile/25674140-david-iwanow?utm_source=comment)

[David Iwanow](https://substack.com/profile/25674140-david-iwanow?utm_source=substack-feed-item)

[3d](https://duaneforresterdecodes.substack.com/p/stop-treating-ai-visibility-as-one/comment/257094579 "May 11, 2026, 2:41 AM")

Liked by Duane Forrester Decodes

But if the SEO tools aren't driving us to feed the beast as we have traditionally done do they still have as much value going forward?

Like (1)

Reply (1)

Share

[![Duane Forrester Decodes's avatar](https://substackcdn.com/image/fetch/$s_!dJ0A!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9350c9af-d0be-4715-b265-1176132ba113_1024x1024.png)](https://substack.com/profile/31440955-duane-forrester-decodes?utm_source=comment)

[Duane Forrester Decodes](https://substack.com/profile/31440955-duane-forrester-decodes?utm_source=substack-feed-item)

[3d](https://duaneforresterdecodes.substack.com/p/stop-treating-ai-visibility-as-one/comment/257176171 "May 11, 2026, 7:50 AM")

Author

Right now, yes, because we exist in a hybrid space where traditional search and LLM search are both providing value - ke established, one growing. In the future, those tools better adapt, or they will become outdated and their value slips.

Like (1)

Reply (1)

Share

[![David Iwanow's avatar](https://substackcdn.com/image/fetch/$s_!-B02!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5fbc09c7-c2e3-40f6-a7ad-ac1a819d6477_150x150.jpeg)](https://substack.com/profile/25674140-david-iwanow?utm_source=comment)

[David Iwanow](https://substack.com/profile/25674140-david-iwanow?utm_source=substack-feed-item)

[3d](https://duaneforresterdecodes.substack.com/p/stop-treating-ai-visibility-as-one/comment/257407095 "May 11, 2026, 3:18 PM")

Liked by Duane Forrester Decodes

I think the value has slipped on many leagcy platforms but the costs of tracking the new AI isn't sustainable so there will be a consolidation as their revenue fails to maintain

Like (1)

Reply

Share

[![David Iwanow's avatar](https://substackcdn.com/image/fetch/$s_!-B02!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5fbc09c7-c2e3-40f6-a7ad-ac1a819d6477_150x150.jpeg)](https://substack.com/profile/25674140-david-iwanow?utm_source=comment)

[David Iwanow](https://substack.com/profile/25674140-david-iwanow?utm_source=substack-feed-item)

[4d](https://duaneforresterdecodes.substack.com/p/stop-treating-ai-visibility-as-one/comment/256826296 "May 10, 2026, 1:22 PM")

Liked by Duane Forrester Decodes

Love the audio version

Like (1)

Reply (1)

Share

[![Duane Forrester Decodes's avatar](https://substackcdn.com/image/fetch/$s_!dJ0A!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9350c9af-d0be-4715-b265-1176132ba113_1024x1024.png)](https://substack.com/profile/31440955-duane-forrester-decodes?utm_source=comment)

[Duane Forrester Decodes](https://substack.com/profile/31440955-duane-forrester-decodes?utm_source=substack-feed-item)

[4d](https://duaneforresterdecodes.substack.com/p/stop-treating-ai-visibility-as-one/comment/256897725 "May 10, 2026, 4:07 PM")

Author

Thanks man! And at 2X it’s only 7.6 minutes of listening to me! 😂🤣

Like (1)

Reply (1)

Share

[![David Iwanow's avatar](https://substackcdn.com/image/fetch/$s_!-B02!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5fbc09c7-c2e3-40f6-a7ad-ac1a819d6477_150x150.jpeg)](https://substack.com/profile/25674140-david-iwanow?utm_source=comment)

[David Iwanow](https://substack.com/profile/25674140-david-iwanow?utm_source=substack-feed-item)

[4d](https://duaneforresterdecodes.substack.com/p/stop-treating-ai-visibility-as-one/comment/256913051 "May 10, 2026, 4:44 PM")

Liked by Duane Forrester Decodes

Can manage that over breakfast

Like (1)

Reply (1)

Share

[![Duane Forrester Decodes's avatar](https://substackcdn.com/image/fetch/$s_!dJ0A!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9350c9af-d0be-4715-b265-1176132ba113_1024x1024.png)](https://substack.com/profile/31440955-duane-forrester-decodes?utm_source=comment)

[Duane Forrester Decodes](https://substack.com/profile/31440955-duane-forrester-decodes?utm_source=substack-feed-item)

[4d](https://duaneforresterdecodes.substack.com/p/stop-treating-ai-visibility-as-one/comment/256918520 "May 10, 2026, 4:57 PM")

Author

Exactly! Gotta make the time count!

Like (1)

Reply

Share

[![Duane Forrester Decodes](https://substackcdn.com/image/fetch/$s_!Qx76!,w_96,h_96,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F613e8843-2ee4-4396-81a4-11c6ff18a1d8_1400x1400.png)](https://duaneforresterdecodes.substack.com/)

Duane Forrester Decodes

AI is rewriting how brands get found, cited, and trusted. Duane Forrester breaks down what that means for practitioners and marketing leaders who can't afford to get it wrong.

AI is rewriting how brands get found, cited, and trusted. Duane Forrester breaks down what that means for practitioners and marketing leaders who can't afford to get it wrong.

Subscribe

Listen on

Substack App

Apple Podcasts

Spotify

RSS Feed

Appears in episode

[![Duane Forrester Decodes's avatar](https://substackcdn.com/image/fetch/$s_!dJ0A!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9350c9af-d0be-4715-b265-1176132ba113_1024x1024.png)](https://substack.com/@duaneforresterdecodes?utm_source=author-byline-face-podcast)

[Duane Forrester Decodes](https://substack.com/@duaneforresterdecodes)

Recent Episodes

![](https://substackcdn.com/image/fetch/$s_!Qx76!,w_150,h_150,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_center/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F613e8843-2ee4-4396-81a4-11c6ff18a1d8_1400x1400.png)

[Search Engines Were Built to Send Traffic Out. LLMs Were Built to Answer You, keep you in.](https://duaneforresterdecodes.substack.com/p/search-engines-were-built-to-send)

May 3•[Duane Forrester Decodes](https://substack.com/@duaneforresterdecodes)

![](https://substackcdn.com/image/fetch/$s_!Qx76!,w_150,h_150,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_center/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F613e8843-2ee4-4396-81a4-11c6ff18a1d8_1400x1400.png)

[AI Gives You the Vocabulary. It Doesn’t Give You the Expertise.](https://duaneforresterdecodes.substack.com/p/ai-gives-you-the-vocabulary-it-doesnt)

Apr 26•[Duane Forrester Decodes](https://substack.com/@duaneforresterdecodes)

### Ready for more?

Subscribe