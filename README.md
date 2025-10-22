# 🧭 AI Engineering Roadmap for Backend Developers (6 Months)

## 🎯 Goal
백엔드 개발자로서 AI 서비스를 **직접 설계·구현·배포** 할 수 있는 수준에 도달한다.  
(모델 학습 아님 → **AI 활용 엔지니어링 중심**)

---

## 🩵 Phase 1 (1–2 Months) — AI 서비스화 기초 익히기

### 🎯 Objective
- LLM API를 백엔드에 붙여 실제 결과물을 프론트로 내보내는 경험 쌓기  
- 프롬프트 설계·응답 파싱·로깅 패턴 익히기  

### 🧰 Stack
`FastAPI` · `LangChain (basic chains)` · `OpenAI/DeepSeek API` · `Ollama`

### 🧩 Mini Projects
1. **AI 주식 리포트 생성 API**  
   - `yfinance`로 데이터 수집 → 프롬프트 주입 → Markdown 리포트 출력  
   - 요청/응답 로깅 및 에러 핸들링  

2. **PDF 요약 API**  
   - 문서 업로드 → 텍스트 추출 → LLM 요약 → JSON 응답  

### 📚 References
- [LangChain Quickstart](https://python.langchain.com/docs/get_started/quickstart)  
- [DeepSeek API](https://api-docs.deepseek.com)  
- [FastAPI LLM Proxy 예제](https://fastapi.tiangolo.com)

---

## 💙 Phase 2 (3–4 Months) — 데이터 결합 및 RAG 이해

### 🎯 Objective
- 내 데이터를 LLM과 결합해 검색형 AI 서비스 구성  
- Embedding / Vector DB / Retrieval 기초 습득  

### 🧰 Stack
`LangChain RetrievalQA` · `ChromaDB` or `FAISS` · `OpenAI/Ollama Embedding`

### 🧩 Mini Projects
1. **사내 매뉴얼 Q&A 봇**  
   - 문서 embedding → 벡터 DB 저장 → 질문 응답  

2. **연말정산 Q&A 어시스턴트**  
   - 세법 자료 임베딩 → 질문 요약 → 정확한 답변  

### 📚 References
- [LangChain RAG Tutorial](https://python.langchain.com/docs/tutorials/rag/)  
- [ChromaDB Docs](https://docs.trychroma.com)  
- [Pinecone Blog - RAG from Scratch](https://www.pinecone.io/learn/retrieval-augmented-generation/)

---

## 💜 Phase 3 (5–6 Months) — 배포 · 최적화 · 운영 고도화

### 🎯 Objective
- AI 백엔드 서비스를 운영 수준으로 구축 및 배포  
- 캐싱·스케줄링·모니터링 기능 추가  

### 🧰 Stack
`FastAPI` · `LangServe` or `LangGraph` · `Redis Cache` · `vLLM` or `Ollama Serve`

### 🧩 Mini Projects
1. **LLM 리포트 자동화 시스템**  
   - 매일 00:10 주식/ETF 리포트 생성 → DB 저장  
   - 스케줄러(`APScheduler` or `Celery`) 활용  

2. **RAG API 배포**  
   - Docker + Render/Railway/EC2  
   - Redis 캐시 + 에러 로그 모니터링  

### 📚 References
- [LangServe 배포 가이드](https://python.langchain.com/docs/langserve/)  
- [vLLM Inference Server](https://docs.vllm.ai)  
- [Redis + FastAPI 캐싱 가이드](https://redis.io/docs/latest/develop/clients/python/)

---

## 🧩 병행 학습 주제

| 주제 | 이유 | 방법 |
|------|------|------|
| Prompt Engineering | 모델의 출력 정확도 향상 | Prompt Engineering Guide |
| Embedding/Vector 개념 | RAG 이해의 핵심 | 3Blue1Brown “Vectors” 영상 |
| Token/Context 관리 | 비용 및 성능 제어 | OpenAI Tokenization 문서 |
| LangChain Memory | 대화 맥락 유지 | LangChain Cookbook 예제 |

---

## 🧠 선택 심화 단계
- Hugging Face 기반 **QLoRA Fine-tuning** 실습  
- **LLM Ops** (로그/모니터링/버전 관리)  
- **Multi-Agent Framework** (crewAI · Autogen 등)

---

## 🧩 요약

| 항목 | 내용 |
|------|------|
| 현재 레벨 | Lv 1.5 (프록시 서버 기반 AI API 경험자) |
| 추천 전략 | Top-Down 실습 + 필요 시 Selective Bottom-Up |
| 6개월 결과 | “AI 결과를 내 서버에서 서비스화할 수 있는 엔지니어” |

---
