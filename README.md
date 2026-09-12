# n8n workflows

Seventy-six n8n workflows, exported from a working instance and published as
they are. Import a JSON file, connect your own credentials, keep whatever is
useful.

These are backups, not polished templates. Some are rough, several were built
against one specific account, and a few are experiments that never grew up.
They are here because a workflow you can read beats a description of one.

**Counted on 12 September 2026:** 76 workflows · 1,061 nodes (14 apiece on
average) · 57 call a language model · 39 contain an agent · 24 query a vector
store · 19 third-party services wired.

---

## Importing one

1. In n8n: **Workflows → ⋯ → Import from File**, and pick the `.json`.
2. Open each red node and attach **your own** credential. Exports carry the
   *name* of a credential, never the secret, so every connection has to be
   made again on your side.
3. Read the sticky notes before running anything. Some workflows write to
   Postgres, send mail, or post to a channel on the first run.
4. Check node versions. This is a December 2025 snapshot; n8n may ask you to
   upgrade a node before it will run.

### What most of them expect

- **A Postgres database with `pgvector`** for anything labelled RAG — the
  vector store, and in several workflows the chat memory as well.
- **An OpenAI key**, used for chat models, embeddings and Whisper.
- **A Telegram bot** for the workflows that use chat as their front end.
- **Google credentials** (Gmail, Drive, Sheets, Calendar) for the assistants.

## A word on cost

Nothing here is throttled or budgeted. A scraper pointed at a large list, or
an agent left on a webhook, will spend real money on API calls without
mentioning it. Run one against a small input first and watch what it does.

---

## What is in here

Grouped by what a workflow is for. The file names are n8n's own ids, so the
table is the index.

### Assistants and agents

| Workflow | Nodes | Uses | File |
| --- | --: | --- | --- |
| Agentic RAG | 42 | Drive, Postgres, Supabase · LLM, agent, vector store | [`I1eepaQ8D85KCFUQ.json`](./workflows/I1eepaQ8D85KCFUQ.json) |
| ai business advisor | 7 | Postgres · LLM | [`wXwL2dKG7KHuVwWh.json`](./workflows/Simple%20test/wXwL2dKG7KHuVwWh.json) |
| Budget Assistant | 14 | Notion, Sheets, Telegram · LLM, agent | [`IgZkPjNenspE8CYN.json`](./workflows/IgZkPjNenspE8CYN.json) |
| Calendar Agent | 10 | Calendar · LLM, agent | [`QmglT6aW30bIb7IA.json`](./workflows/AI%20Agent/QmglT6aW30bIb7IA.json) |
| Calendar Agent | 7 | Calendar · LLM, agent | [`Voz1mEMidV5zdJEI.json`](./workflows/Voz1mEMidV5zdJEI.json) |
| Contact Agent | 7 | Airtable · LLM, agent | [`2MUt3s2rG4Ab3VbH.json`](./workflows/AI%20Agent/2MUt3s2rG4Ab3VbH.json) |
| Content Creator | 6 | LLM, agent | [`kC59f6oV7xOzABvK.json`](./workflows/AI%20Agent/kC59f6oV7xOzABvK.json) |
| Content Creator | 11 | LLM, agent | [`CAPlbSjVku4S2hdC.json`](./workflows/content/CAPlbSjVku4S2hdC.json) |
| Conversational Agent RAG | 8 | LLM, agent, vector store | [`ny9QUuODxM2wmZak.json`](./workflows/AI%20Agent/ny9QUuODxM2wmZak.json) |
| Conversational Agent RAG | 8 | Slack · LLM, agent, vector store | [`F21Kh7B6tFD2Q4ac.json`](./workflows/F21Kh7B6tFD2Q4ac.json) |
| Email Agent | 12 | Gmail · LLM, agent | [`mmL0LFEhjvkjshZZ.json`](./workflows/AI%20Agent/mmL0LFEhjvkjshZZ.json) |
| Graphic Design AI Agent | 7 | Drive | [`5Rbq4ZYKNGuefB9s.json`](./workflows/5Rbq4ZYKNGuefB9s.json) |
| Health Assistant | 17 | Telegram · LLM, agent | [`F5X2j7HPG48IEc9t.json`](./workflows/trainings/F5X2j7HPG48IEc9t.json) |
| Image Analyze Agent | 10 | Telegram · LLM, agent | [`57nEyJdSuN3gRQNh.json`](./workflows/AI%20Agent/57nEyJdSuN3gRQNh.json) |
| Inbox Agent | 14 | Gmail · LLM | [`feNZcgvZvReq3EnQ.json`](./workflows/feNZcgvZvReq3EnQ.json) |
| Invoice Agent | 12 | Drive, Sheets, Telegram · LLM, agent | [`xSaUzKoqyHWF2b3M.json`](./workflows/xSaUzKoqyHWF2b3M.json) |
| Mails AI Agent | 18 | Gmail, Sheets · LLM | [`8L5dHVecY8G49Wx6.json`](./workflows/8L5dHVecY8G49Wx6.json) |
| Newsletter Agent | 20 | Gmail · LLM, agent | [`3nlXmaMxeNNbKZzJ.json`](./workflows/3nlXmaMxeNNbKZzJ.json) |
| Newsletter Research Agent | 20 | Gmail · LLM, agent | [`ciUfKA2V3O0CtLJN.json`](./workflows/ciUfKA2V3O0CtLJN.json) |
| Newsletter writing style to knowledgebase | 11 | Gmail · LLM, vector store | [`RRAwojTXB8iF5wGE.json`](./workflows/RRAwojTXB8iF5wGE.json) |
| POST question - personal trainer | 11 | LLM, agent, vector store | [`8C7VXqm5VkMDN6vS.json`](./workflows/personal%20trainer/8C7VXqm5VkMDN6vS.json) |
| POST resource - personal trainer | 11 | vector store | [`Ji2dDmHdrGfg8lw2.json`](./workflows/personal%20trainer/Ji2dDmHdrGfg8lw2.json) |
| RAG knowledgebase (Newsletters) | 11 | Gmail · LLM, vector store | [`kpgCsnaNfqcxYtft.json`](./workflows/newsletter%20collector/kpgCsnaNfqcxYtft.json) |
| Research Agent | 7 | Hacker News · LLM, agent | [`g7SG66agQBsDeKjK.json`](./workflows/AI%20Agent/g7SG66agQBsDeKjK.json) |
| SEO Agents team | 54 | Discord, Notion, Postgres, Slack, Telegram, X · LLM, agent, vector store | [`WJD00jF2lRFeZbfC.json`](./workflows/SEO/WJD00jF2lRFeZbfC.json) |
| Travel Agent | 14 | Gmail · LLM, agent | [`9O0siNkd8LNqtpqB.json`](./workflows/webhook/9O0siNkd8LNqtpqB.json) |
| Travel Agent AI | 13 | Gmail · LLM, agent | [`3CNZz5AxsPwVCuGK.json`](./workflows/AI%20Agent/3CNZz5AxsPwVCuGK.json) |
| upwork proposal assistant | 28 | Postgres, Telegram · LLM, agent, vector store | [`3GswtaIjYdoh05CF.json`](./workflows/upwork/3GswtaIjYdoh05CF.json) |
| Voice Email Agent | 6 | Gmail, Sheets · LLM, agent | [`rvid3fWHc4wgtP9Q.json`](./workflows/rvid3fWHc4wgtP9Q.json) |
| WIP personal trainer | 8 | Telegram · LLM, agent | [`F5X2j7HPG48IEc9t.json`](./workflows/personal%20trainer/F5X2j7HPG48IEc9t.json) |

### Knowledge bases and RAG

| Workflow | Nodes | Uses | File |
| --- | --: | --- | --- |
| Notion - RAG | 12 | Notion · LLM, agent | [`KXMlAbrpKfEZ1XBr.json`](./workflows/test%20training/KXMlAbrpKfEZ1XBr.json) |
| POST resource | 6 | Notion · vector store | [`PFFT1YSRE0SDYvFw.json`](./workflows/saas/PFFT1YSRE0SDYvFw.json) |
| POST training data | 5 | vector store | [`D2WNRVB9UZ7azFyu.json`](./workflows/personal%20trainer/D2WNRVB9UZ7azFyu.json) |
| RAG | 8 | LLM, agent, vector store | [`UZrulkJW8Zdg7T50.json`](./workflows/saas/UZrulkJW8Zdg7T50.json) |
| RAG Knowledgebase | 40 | Drive, Gmail, Notion · LLM, agent, vector store | [`C76bdtACUqxapmoI.json`](./workflows/C76bdtACUqxapmoI.json) |
| RagFLOW | 9 | LLM, agent, vector store | [`uxgXYZqhiwtk6Vtx.json`](./workflows/aiadaptiv%20landing%20page/uxgXYZqhiwtk6Vtx.json) |
| Supabase RAG Template | 29 | Drive, Supabase · LLM, agent, vector store | [`APd9AhKO9twWBmdV.json`](./workflows/APd9AhKO9twWBmdV.json) |
| YouTube Transcripts RAG | 9 | Notion · vector store | [`ZP04RnUIFFytiQRZ.json`](./workflows/ZP04RnUIFFytiQRZ.json) |
| YouTube video summarizer RAG | 31 | Notion, Telegram · LLM, agent, vector store | [`XjuzY0nFCYP3aDg0.json`](./workflows/saas/XjuzY0nFCYP3aDg0.json) |

### Collectors and scrapers

| Workflow | Nodes | Uses | File |
| --- | --: | --- | --- |
| FB Ad Spy Tool | 25 | Drive, Sheets · LLM | [`KN2fw1nZGZcrMmlP.json`](./workflows/KN2fw1nZGZcrMmlP.json) |
| firecrawl | 6 | — | [`MhuX7N7mkU3mityY.json`](./workflows/MhuX7N7mkU3mityY.json) |
| Get Brand Beef | 4 | Notion | [`wRllp1LNTKlLIQOL.json`](./workflows/content/wRllp1LNTKlLIQOL.json) |
| Get Content Feedback | 4 | LLM | [`qozfiKB96LWAQaZ3.json`](./workflows/content/qozfiKB96LWAQaZ3.json) |
| Get Content Ideas | 4 | LLM | [`ZyNKCIiWvxz7IMPi.json`](./workflows/content/ZyNKCIiWvxz7IMPi.json) |
| Google Maps Scraper | 15 | Sheets | [`uXuhne7tDwq90Iw8.json`](./workflows/google%20maps/uXuhne7tDwq90Iw8.json) |
| SaaS - checker | 22 | Puppeteer | [`CBNLmDkepgyRnS7S.json`](./workflows/CBNLmDkepgyRnS7S.json) |
| Scrape and summarize webpages with AI | 16 | LLM | [`iUg3mWgh0he1tCU2.json`](./workflows/iUg3mWgh0he1tCU2.json) |
| Tweets Scraper | 8 | Notion · vector store | [`SHIH7xcRVnjri5oZ.json`](./workflows/AI%20Agent/SHIH7xcRVnjri5oZ.json) |
| Tweets Scraper X | 8 | Notion · vector store | [`Im4uPg4uFZzZR9YA.json`](./workflows/saas/Im4uPg4uFZzZR9YA.json) |
| X scraper | 15 | Sheets | [`8hlJkYuyYCQBhqrd.json`](./workflows/8hlJkYuyYCQBhqrd.json) |
| YouTube Transcripts | 9 | Notion · vector store | [`edb8K2M5Jfxy5Q71.json`](./workflows/saas/edb8K2M5Jfxy5Q71.json) |

### Images and video

| Workflow | Nodes | Uses | File |
| --- | --: | --- | --- |
| ai fashion bot - v2 | 16 | Drive, Telegram | [`RR56oMYfMj7nADhS.json`](./workflows/RR56oMYfMj7nADhS.json) |
| AI Video Analysis | 22 | — | [`LZi4RzoSKnULaW5q.json`](./workflows/LZi4RzoSKnULaW5q.json) |
| Auto-Generate Virtual AI Try-On Images for WooCommerce with Gemini Nano Banana | 20 | Drive, Sheets, WooCommerce | [`RF7zy0hJumq55k78.json`](./workflows/RF7zy0hJumq55k78.json) |
| Automated AI image analysis and response via Telegram | 7 | Telegram | [`PYzIrbK6yQGDg4ok.json`](./workflows/PYzIrbK6yQGDg4ok.json) |
| Faceless YouTube | 42 | Drive, Gmail, Sheets, YouTube · LLM, agent | [`8KskG8izaeHzc0Tr.json`](./workflows/8KskG8izaeHzc0Tr.json) |
| Generate Fashion Model Product Ads with Gemini AI via OpenRouter | 10 | — | [`arxaRBhvnXviSTN6.json`](./workflows/arxaRBhvnXviSTN6.json) |
| Nano Banana AI Fashion Bot | 14 | Drive, Telegram | [`mjnoCkhtIWfkr2sI.json`](./workflows/mjnoCkhtIWfkr2sI.json) |
| Nano Banana AI Image Editor via Telegram | 9 | Telegram | [`qlnm8bQfPugEeEzZ.json`](./workflows/qlnm8bQfPugEeEzZ.json) |
| Viral AI Videos | 11 | Sheets · LLM, agent | [`bPnMroBHANusnBNE.json`](./workflows/bPnMroBHANusnBNE.json) |
| YouTube video summarizer copy | 7 | Telegram · LLM | [`aJ4uekDN3rozh7F6.json`](./workflows/saas/aJ4uekDN3rozh7F6.json) |

### Chat front ends

| Workflow | Nodes | Uses | File |
| --- | --: | --- | --- |
| AI Voice Chatbot with ElevenLabs & OpenAI for Customer Service and Restaurants | 11 | LLM, agent, vector store | [`LHuAWXTs3LwgigtM.json`](./workflows/voice/LHuAWXTs3LwgigtM.json) |
| aiAdaptiv landing page chatbot | 13 | LLM, agent, vector store | [`k9li7JZFX7aeffKz.json`](./workflows/aiadaptiv%20landing%20page/k9li7JZFX7aeffKz.json) |
| aiAdaptiv landing page chatbot - external trigger | 12 | LLM, agent, vector store | [`8bNShJx5AZOU0OFB.json`](./workflows/aiadaptiv%20landing%20page/8bNShJx5AZOU0OFB.json) |
| Telegram AI bot with LangChain nodes | 18 | Notion, Telegram, Todoist · LLM, agent, vector store | [`WtcmKVqPvNCbboRR.json`](./workflows/WtcmKVqPvNCbboRR.json) |
| Transcribe Voice Messages from Telegram using OpenAI Whisper-1 | 10 | Notion, Telegram · LLM, agent | [`3nWbgtsUJibXIk3C.json`](./workflows/3nWbgtsUJibXIk3C.json) |

### Site, ops and glue

| Workflow | Nodes | Uses | File |
| --- | --: | --- | --- |
| aiResearcher SaaS DEMO | 32 | Postgres, Telegram · LLM, agent | [`7Q1C2mJG62EGam1b.json`](./workflows/saas/7Q1C2mJG62EGam1b.json) |
| All workflows - github backup | 25 | GitHub | [`gJZJjIBCuwUKa4M5.json`](./workflows/backup/gJZJjIBCuwUKa4M5.json) |
| asana workflow | 2 | Asana | [`Uk1JO572JPF6BfFb.json`](./workflows/Uk1JO572JPF6BfFb.json) |
| Basic Automatic Gmail Email Labelling with OpenAI and Gmail API | 13 | Gmail · LLM, agent | [`nB7Uq7tAuAQDcQqk.json`](./workflows/nB7Uq7tAuAQDcQqk.json) |
| inform about new user | 2 | Gmail | [`65jrlPY9eTRuu0wI.json`](./workflows/saas/65jrlPY9eTRuu0wI.json) |
| My workflow | 18 | Drive, Telegram | [`829S0vU8NHEb8IqV.json`](./workflows/829S0vU8NHEb8IqV.json) |
| Ultimate Personal Assitant | 24 | Telegram · LLM, agent | [`IiLZPCXYmwe0Y2oR.json`](./workflows/AI%20Agent%20Main/IiLZPCXYmwe0Y2oR.json) |
| update script in DO | 1 | — | [`HNY1TBldikHaviKY.json`](./workflows/HNY1TBldikHaviKY.json) |
| Waitlist Backend | 9 | Postgres | [`9PuonPwJdXMAnSGQ.json`](./workflows/waitlist/9PuonPwJdXMAnSGQ.json) |
| Waitlist Confirmation Logic | 4 | Postgres | [`83CJf15FmOLyKGEx.json`](./workflows/waitlist/83CJf15FmOLyKGEx.json) |

---

## Caveats

- **A snapshot, not a product.** Last exported December 2025. Nothing here is
  maintained, and a provider that changed an endpoint since then will have
  broken something.
- **Built for one instance.** Workflow-to-workflow calls point at ids from the
  instance they came from; expect to re-link a few.
- **Some contain sample addresses and test data** left over from development.
  Read a workflow before you run it, rather than after.
- **No support, no warranty.** Open an issue if something is broken and it may
  get looked at, but that is a favour, not a commitment.

## Licence

MIT — see [`LICENSE`](./LICENSE). Use them commercially, modify them, ship
them inside your own product. Attribution is welcome and not required.

---

Built and published by [aiAdaptiv](https://www.aiadaptiv.com). We build
automations, agents and private AI systems for companies that would rather own
theirs than rent them.
