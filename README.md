# Portray (刻画) · Intelligent User Profiling Platform

> Delineating every user. From theory to practice — understand, build, serve.

[Live Demo](https://zheng-qinghe.github.io/Portray) &nbsp;|&nbsp; [Introduction Page](https://zheng-qinghe.github.io/Portray/docs/)

---

## How It Works

**刻画** is an intelligent user profiling platform powered by a local compute engine. The public repository contains the interactive demo interface; the core engine runs entirely on your machine.

```
  Open your browser        Your local machine does all the heavy lifting
  ───────────────         ──────────────────────────────────────
  demo/index.html  ──→   Local API (127.0.0.1:8080)  ──→  Tag Engine
                              │                             Embedding Vectors
                              │                             Predictive Scores
                              │                             Lookalike Similarity
                              └──→  Real-time Profile Updates
```

## Quick Start

```bash
# 1. Start the local compute engine (requires private engine pack)
python -m uvicorn api:app --host 127.0.0.1 --port 8080

# 2. Open the demo in your browser
open demo/index.html
```

The demo connects automatically to your local engine. All computation — rule engine, embedding vectors, predictive scores, cross-cultural analysis — runs locally on your machine. No data ever leaves your computer.

## Demo Features

| Tab | What it shows |
|-----|---------------|
| **Profile** | Churn risk, LTV score, purchase intent, activity score |
| **Tags** | Multi-dimensional tags (demographic, behavioral, preference, predictive, cultural) |
| **Scenarios** | E-commerce recommendations, content push, ad targeting |
| **Lookalike** | Vector similarity search (128-dim embedding, Top-50 nearest users) |
| **Cross-Cultural** | Hofstede 6-D model — China, Brazil, Portugal, Angola markets |

## Architecture

```
L1 Data Fusion    ── Behavior logs / Transactions / Device fingerprints
L2 Compute Engine ── Real-time streaming (sliding window) + Batch processing
L3 AI Layer      ── Rule engine + Embedding vectors + Predictive scoring
L4 Applications  ── E-commerce / Content push / Ad targeting / Lookalike
```

## Academic Foundation

Every technical component is backed by published academic research — 16 papers with direct PDF links for further reading. See the [full literature reference table](https://docs.qq.com/sheet/DQkFGU2RmV2tmVHZz?_fid=BAFSdfWkfTvs) (Chinese).

| Component | Original Paper |
|-----------|---------------|
| User Profiling | Alan Cooper, *The Inmates Are Running the Asylum*, 1999 |
| Embedding Vectors | Tomas Mikolov et al., *Word2Vec*, arXiv:1301.3781, 2013 |
| Similarity Search | Jeff Johnson et al., *Faiss*, arXiv:1702.08734, 2017 |
| Recommendation | Paul Covington et al., *YouTube DNN*, RecSys 2016 |
| Streaming | Brian Babcock et al., *Data Stream Systems*, PODS 2002 |
| Lambda Architecture | Nathan Marz & James Warren, *Big Data*, Manning 2015 |
| Cross-Cultural | Geert Hofstede, *Culture's Consequences*, 1980 |

## Team

Project maintained by 张静怡 · 润禾 · 于硕

## License

Demo code and documentation: MIT License.
Core engine: proprietary (runs locally).
