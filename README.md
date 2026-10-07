### Hi, I'm Mirdula 👋

I build **LLM agents that are allowed to touch real things**: money, code, citizens' questions. So I put the rules in code, not in the prompt.

Final-year Integrated M.Tech CSE · Sri Ramakrishna Engineering College, Coimbatore · 2027<br>
Python · FastAPI · LangGraph · Pydantic AI · RAG · React · Node · Postgres · Docker

---

#### 🛒 [Kirana Ops Agent](https://github.com/Mirdumurugesan/supermarket-ops-agent): run a grocery store from a Telegram chat
GST billing, credit ledgers (khata), stock, PDF invoices and analysis decks, all driven by an agent with 29 tools.
- The model can't invent a price: billing tools only accept product IDs from search. Overselling is blocked by the database, and three idempotency layers stop double bills
- All money is `Decimal`, and the CGST/SGST split reconciles to the paisa
- Groq → Groq → Gemini failover, with SDK retries disabled so failover actually fires
- **118 tests pass with the LLM removed** · [try the bot](https://t.me/mirdu_kirana_bot) · [4-min demo](https://drive.google.com/file/d/1QXx-IiGwTCdN1GP3v39Yl-ZqfJmVYHq5/view)

#### 🔧 [NEXUS](https://github.com/Mirdumurugesan/nexus): GitHub issue → verified patch
A LangGraph multi-agent loop (planner → engineer → reviewer ⇄ reflector) over hybrid RAG (tree-sitter chunks, BM25 + symbols + HyDE, RRF).
- A **deterministic patch gate** (`git apply`, compile check, tests) runs before any LLM review, so a model can't approve a diff that doesn't apply
- The reflector gets git's exact error, and the best attempt wins over the last one
- Runs offline: `python -m app.cli demo` · SWE-bench Lite runner that outputs official harness predictions · CI on 3.11–3.13

#### 🗣️ [Kural](https://github.com/Mirdumurugesan/kural): Tamil voice helpline for government schemes
Gnani AI STT + LLM + TTS. Noisy-phone audio cleanup, and Tamil/Tanglish hybrid retrieval (**20/20 top-1** on its benchmark). It escalates instead of guessing and redacts Aadhaar/PAN before storing anything.

#### 👥 [HRVerse AI](https://github.com/Mirdumurugesan/HRVerse-AI): full-stack HR platform · [live](https://hr-verse-ai.vercel.app)
React 19 + Express + MongoDB, 4-role RBAC, AI resume and interview scoring with a 3-level fallback chain, seeded at 15k employees and 300k attendance rows.

#### ⚙️ [ConcurrentQ](https://github.com/Mirdumurugesan/ConcurrentQ): thread-safe priority task scheduler
Heap + `Condition`, a token-bucket rate limiter, and retries with backoff. **6.3× speedup at 8 workers**, standard library only.

---

Web development intern @ Xcodefix (2025) · open to **full-stack / AI engineering internships**
