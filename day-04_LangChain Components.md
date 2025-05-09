## LangChain Components

---

## Models

LangChain-এ “Models” মানে হচ্ছে যেসব LLM (Large Language Models) ব্যবহার করা হয় — যেমন OpenAI GPT, Anthropic Claude, Google Gemini ইত্যাদি।
LangChain এই মডেলগুলোকে wrapper-এর মাধ্যমে ব্যবহারযোগ্য করে তোলে, যেন developer সহজেই integrate করতে পারে।

---

## Prompts

Prompt হলো LLM-এর কাছে প্রশ্ন বা ইনস্ট্রাকশন পাঠানোর স্ট্রাকচার।
LangChain-এ PromptTemplate দিয়ে dinamic এবং reusable prompt বানানো যায়।
Prompt engineering মানেই ভালোভাবে prompt বানানো, যাতে model থেকে কাঙ্ক্ষিত output আসে।

---

## Chains

Chain হলো একাধিক স্টেপের লজিক্যাল সিরিজ — যেখানে একটার আউটপুট অন্যটার ইনপুট হয়।
Simple example: Prompt -> LLM -> Output
Complex chain-এ Document retriever, memory, tool call — সব একসাথে থাকতে পারে।

LangChain-এ অনেক প্রি-মেইড chain আছে (যেমন: LLMChain, SequentialChain) — আর চাইলে custom chain বানানো যায়।

---

## Indexes

Indexes দিয়ে অনেকগুলো ডকুমেন্ট থেকে দরকারি তথ্য বের করে আনা যায়।
LangChain-এর retriever system Vectordb (যেমন: FAISS, Chroma) use করে embedding-based search করে।
এই technique কে বলা হয় Retrieval-Augmented Generation (RAG)।
এটা LLM-এর hallucination কমায় কারণ model real ডেটার সাথে সংযুক্ত থাকে।

---

## Memory

LLM সাধারণত আগের কথাবার্তা মনে রাখতে পারে না।
LangChain-এর memory module আগের conversation store করে রাখে, যাতে model context-aware হয়।

Types of memory:

* ConversationBufferMemory
* SummaryMemory
* TokenBufferMemory
  এগুলো দিয়ে chatbot বা assistant আগের কথা “মনে রাখতে” পারে।

---

## Agents

Agents হচ্ছে এমন system যারা নিজেরাই ঠিক করে কী করতে হবে — কোন টুল ব্যবহার করবে, কোন স্টেপ নিবে।
Agents tool ব্যবহার করতে পারে যেমন: calculator, web search, code executor ইত্যাদি।

LangChain-এ agent system খুব flexible, আর এগুলা autonomous task completion-এর জন্য খুব কাজের।

Agents decision নেয় step by step reasoning-এর মাধ্যমে, যেমন “thought → action → observation → final answer” এই ফরম্যাটে।
