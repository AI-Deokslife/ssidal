# 파이썬 학습 사이트 🐍

Gemini API와 Streamlit을 활용한 인터랙티브 파이썬 학습 플랫폼입니다.

## 🌟 주요 기능

### 📖 학습
- 초급, 중급, 고급 수준별 커리큘럼 제공
- AI가 생성하는 맞춤형 학습 콘텐츠
- 개념 설명, 코드 예제, 실습 문제 포함

### 📝 문제풀이
- 사용자가 문항 수와 범위 설정 가능
- 3가지 문제 유형:
  - 5지선다 객관식
  - 코드 빈칸 채우기
  - 단답식 문제
- 실시간 채점 및 해설 제공

### 💬 Q&A
- AI 튜터에게 파이썬 관련 질문
- 대화 기록 저장 및 관리
- 코드 예제를 포함한 상세한 답변

## 🚀 시작하기

### 1. 저장소 클론
```bash
git clone https://github.com/your-username/python-learning-site.git
cd python-learning-site
```

### 2. 가상환경 설정 (선택사항)
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3. 패키지 설치
```bash
pip install -r requirements.txt
```

### 4. Gemini API 키 획득
1. [Google AI Studio](https://makersuite.google.com/app/apikey)에서 API 키 생성
2. 생성된 API 키 복사

### 5. 로컬 실행
```bash
streamlit run app.py
```

## 📱 Streamlit Cloud 배포

### 1. GitHub에 Push
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

### 2. Streamlit Cloud 설정
1. [Streamlit Cloud](https://streamlit.io/cloud)에 로그인
2. "New app" 클릭
3. GitHub 저장소 선택
4. Branch: `main`, Main file path: `app.py` 설정

### 3. Secrets 설정
Streamlit Cloud 앱 설정에서 Secrets 탭에 다음 추가:
```toml
GEMINI_API_KEY = "your-gemini-api-key-here"
```

### 4. 배포
"Deploy" 버튼 클릭 후 앱이 빌드되고 배포될 때까지 대기

## 🔧 환경 설정

### API 키 설정 방법

#### 방법 1: Streamlit Secrets (권장 - 배포 시)
`.streamlit/secrets.toml` 파일 생성:
```toml
GEMINI_API_KEY = "your-api-key-here"
```

#### 방법 2: 앱에서 직접 입력
- 사이드바에서 API 키 입력란에 키 입력
- 세션 동안만 유효

## 📁 프로젝트 구조
```
python-learning-site/
│
├── app.py              # 메인 애플리케이션
├── requirements.txt    # 필요한 패키지
├── README.md          # 프로젝트 문서
├── .gitignore         # Git 제외 파일
└── .streamlit/        # Streamlit 설정 (선택사항)
    └── secrets.toml   # API 키 저장 (Git에서 제외)
```

## 🛠️ 커스터마이징

### 커리큘럼 수정
`app.py`의 `CURRICULUM` 딕셔너리를 수정하여 학습 주제 변경:
```python
CURRICULUM = {
    "초급": ["주제1", "주제2", ...],
    "중급": ["주제1", "주제2", ...],
    "고급": ["주제1", "주제2", ...]
}
```

### 스타일 변경
`app.py`의 CSS 스타일 섹션을 수정하여 디자인 커스터마이징

## 🤝 기여하기

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다.

## 📞 문의

프로젝트에 대한 문의사항이 있으시면 이슈를 생성해주세요.

---

Made with ❤️ for Python Learners
