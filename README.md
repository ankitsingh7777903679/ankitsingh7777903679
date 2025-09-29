<h1 align="center">Hi 👋, I'm Ankit Singh</h1>

<h3 align="center">Full Stack Developer | Learning LangChain.js | RAG & AI Agents Enthusiast</h3>

<p align="center">
  <a href="https://visitcount.itsvg.in">
    <img src="https://visitcount.itsvg.in/api?id=ankitsingh7777903679&icon=0&color=6" alt="Profile Views"/>
  </a>
</p>

---

## 🌐 Socials

<p align="left">
  <!-- Replace the # with your actual links -->
  <a href="mailto:ankitsingh77779036@gmail.com"><img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&labelColor=&style=for-the-badge" height="28" alt="gmail"/></a>
  <a href="https://github.com/ankitsingh7777903679"><img src="https://img.shields.io/static/v1?message=GitHub&logo=github&label=&color=181717&logoColor=white&labelColor=&style=for-the-badge" height="28" alt="github"/></a>
  <a href="YOUR_LINKEDIN_URL"><img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0A66C2&logoColor=white&labelColor=&style=for-the-badge" height="28" alt="linkedin"/></a>
  <a href="https://twitter.com/YOUR_TWITTER_HANDLE"><img src="https://img.shields.io/static/v1?message=Twitter&logo=twitter&label=&color=1DA1F2&logoColor=white&labelColor=&style=for-the-badge" height="28" alt="twitter"/></a>
  <a href="#"><img src="https://img.shields.io/static/v1?message=Portfolio&logo=vercel&label=&color=000000&logoColor=white&labelColor=&style=for-the-badge" height="28" alt="portfolio"/></a>
</p>

---

## 💻 Tech Stack

<div align="left">

<!-- Languages -->
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="38" alt="html5" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="38" alt="css3" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" height="38" alt="bootstrap" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="38" alt="javascript" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="38" alt="react" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg" height="38" alt="tailwind" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" height="38" alt="php" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" height="38" alt="mysql" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" height="38" alt="mongodb" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" height="38" alt="c" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" height="38" alt="c++" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="38" alt="java" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="38" alt="python" />
<img width="6" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" height="38" alt="figma" />

<!-- Concepts / Current -->
<br/><br/>
<img src="https://img.shields.io/badge/LangChain.js-0A0F25?style=for-the-badge&logo=chainlink&logoColor=white" height="28" />
<img src="https://img.shields.io/badge/RAG-1E90FF?style=for-the-badge" height="28" />
<img src="https://img.shields.io/badge/AI%20Agents-8A2BE2?style=for-the-badge" height="28" />
<img src="https://img.shields.io/badge/Supabase-181818?style=for-the-badge&logo=supabase&logoColor=3ECF8E" height="28" />
<img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" height="28" />

</div>

---

## 🧪 Currently Learning

- LangChain.js (JavaScript LLM pipelines)
- Building Retrieval-Augmented Generation (RAG) flows
- Designing agent-like tool calling workflows
- Supabase (as backend + vector storage)
- Prisma (schema & DB abstraction)

---

## 📂 Highlighted Repositories

| Project | Description | Stack |
|--------|-------------|-------|
| [toolHub](https://github.com/ankitsingh7777903679/toolHub) | Unified developer utilities hub | PHP, JS, Hack |
| [bot_n8n](https://github.com/ankitsingh7777903679/bot_n8n) | Automation workflows + AI powered logic | Python, JS |
| [Exame_Papers](https://github.com/ankitsingh7777903679/Exame_Papers) | Exam paper management & browsing | PHP / Org |
| [newhomepage](https://github.com/ankitsingh7777903679/newhomepage) | Modern responsive homepage UI | HTML, CSS, JS |

---

## 🧠 Mini RAG (LangChain.js Example)

```bash
npm install langchain @langchain/openai chromadb dotenv
```

```javascript
import 'dotenv/config';
import { RecursiveCharacterTextSplitter } from "langchain/text_splitter";
import { OpenAIEmbeddings, ChatOpenAI } from "@langchain/openai";
import { Chroma } from "langchain/vectorstores/chroma";

const docs = [
  { pageContent: "ToolHub is a unified toolkit for developers." },
  { pageContent: "Agents help automate multi-step reasoning." }
];

const splitter = new RecursiveCharacterTextSplitter({ chunkSize: 120, chunkOverlap: 20 });
const splitDocs = await splitter.splitDocuments(docs);

const embeddings = new OpenAIEmbeddings();
const vectorstore = await Chroma.fromDocuments(splitDocs, embeddings, { collectionName: "demo" });
const retriever = vectorstore.asRetriever(3);

const llm = new ChatOpenAI({ modelName: "gpt-3.5-turbo", temperature: 0 });

const query = "What does ToolHub do?";
const contextDocs = await retriever.getRelevantDocuments(query);
const context = contextDocs.map(d => d.pageContent).join("\n");

const prompt = `Use ONLY the context below.\nContext:\n${context}\n\nQ: ${query}\nA:`;
const res = await llm.invoke(prompt);
console.log(res.content);
```

---

## 📊 GitHub Logs

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg" />
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg" />
</picture>

---

## 📊 GitHub Stats

![](https://github-readme-stats.vercel.app/api?username=ankitsingh7777903679&theme=tokyonight&hide_border=false&include_all_commits=true&count_private=true)
![](https://github-readme-streak-stats.herokuapp.com/?user=ankitsingh7777903679&theme=tokyonight&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=ankitsingh7777903679&theme=tokyonight&hide_border=false&include_all_commits=true&count_private=true&layout=compact)

### 🔝 Top Contributed Repos
![](https://github-contributor-stats.vercel.app/api?username=ankitsingh7777903679&limit=5&theme=tokyonight&combine_all_yearly_contributions=true)

---

## 🎯 Goals (2025)

- Build a production-ready RAG prototype
- Implement first LangChain.js agent with tool invocation
- Integrate Supabase vectors + Prisma schema
- Ship a small AI-powered utility for developers

---

## 🧾 Philosophy

> Build consistently. Learn deliberately. Use AI to enhance—never to replace—your craft.

---

## 📬 Contact

Want to collaborate, brainstorm or build something?  
📧 Email: **ankitsingh77779036@gmail.com**

---

<p align="center">
  <i>If this profile inspired you, consider ⭐ starring a repo!</i>
</p>

<!--
Next steps for full effect:
1. Add Snake Action (see instructions below)
2. Replace social placeholders
3. (Optional) Add metrics.svg via lowlighter/metrics
-->

<!-- Snake GitHub Action (create .github/workflows/snake.yml) -->
<!--
name: Generate Snake
on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:
  push:
    branches: ["main"]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: ankitsingh7777903679
          outputs: |
            dist/snake.svg
            dist/snake-dark.svg?palette=github-dark
      - name: Push snake
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
-->
