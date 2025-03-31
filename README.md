# 🚗 2023-car-ragbot: 차량 매뉴얼 기반 RAG 챗봇

**차량 매뉴얼을 이해하고, 음성으로 질문하면 문서 기반 답변을 제공하는 챗봇 시스템입니다.**  
LangChain과 OpenAI API를 활용해 Retrieval-Augmented Generation(RAG) 구조로 구현되었습니다.

---

## 🔍 주요 기능

- ✅ **RAG 구조 기반 문서 검색 + 생성 응답**
- ✅ **차량 매뉴얼(PDF) 임베딩 후 벡터 검색**
- ✅ **LangChain으로 체인 구성 및 프롬프트 템플릿 설계**
- ✅ **사용자 질문에 대해 문서 기반 정확한 답변 제공**
- ✅ **음성 입력 → 텍스트 변환(STT) 기능 연동 (선택)**

---

## 🛠 사용 기술

| 구성 요소     | 사용 내용                         |
|--------------|----------------------------------|
| LangChain     | Retrieval QA Chain, PromptTemplate |
| OpenAI API    | GPT-3.5 Turbo (or GPT-4)          |
| FAISS         | 로컬 벡터 검색 인덱스               |
| PyPDF         | 차량 매뉴얼 텍스트 추출              |
| Streamlit (선택) | 웹 UI 구현용 (또는 CLI 기반)          |
| Whisper / STT (선택) | 음성 입력 인식                    |

---

## 📁 프로젝트 구조

