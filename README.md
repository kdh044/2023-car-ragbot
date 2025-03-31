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

| 구성 요소         | 사용 내용                             |
|------------------|--------------------------------------|
| LangChain        | Retrieval QA Chain, PromptTemplate   |
| OpenAI API       | GPT-3.5 Turbo (or GPT-4)             |
| FAISS            | 로컬 벡터 검색 인덱스                |
| PyPDF            | 차량 매뉴얼 텍스트 추출               |
| Streamlit (선택) | 웹 UI 구현용 (또는 CLI 기반)          |
| Whisper / STT (선택) | 음성 입력 인식                     |

---

## 📁 프로젝트 구조

```
2023-car-ragbot/
├── app.py                      # 메인 실행 파일
├── retriever.py                # FAISS 기반 벡터 검색 모듈
├── prompt_template.py          # 사용자 질문 처리용 프롬프트 템플릿
├── pdf_loader.py               # 차량 매뉴얼 PDF 로딩 및 텍스트 추출
├── voice_input.py              # 음성(STT) 입력 처리 (선택)
├── requirements.txt            # 필요한 Python 패키지 목록
├── data/
│   └── manual.pdf              # 임베딩 대상 차량 매뉴얼 파일
├── vectorstore/
│   └── faiss_index/            # 벡터 인덱스 저장 폴더
└── README.md                   # 프로젝트 설명 파일
```

---

## ⚙️ 실행 방법

```bash
# 1. 프로젝트 클론
git clone https://github.com/your-username/2023-car-ragbot.git
cd 2023-car-ragbot

# 2. 패키지 설치
pip install -r requirements.txt

# 3. 차량 매뉴얼 PDF 임베딩 (최초 1회)
python retriever.py

# 4. 챗봇 실행 (음성 기능 포함 시, microphone 연결 필요)
python app.py
```

---

## 🧠 향후 계획

- Streamlit 또는 Gradio 기반 웹 인터페이스 추가  
- 차량 모델별 매뉴얼 자동 분류/탐색 기능  
- GPT-4 + LangGraph 연동으로 멀티스텝 추론  
- Whisper 모델 로컬 실행으로 음성 인식 고도화  

---

## 📌 참고

- [LangChain 공식 문서](https://docs.langchain.com/)
- [OpenAI GPT API 문서](https://platform.openai.com/docs)
- [FAISS (Facebook AI Similarity Search)](https://github.com/facebookresearch/faiss)
- [Whisper by OpenAI](https://github.com/openai/whisper)
