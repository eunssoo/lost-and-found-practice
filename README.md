# lost-and-found-practice

교내 분실물을 쉽게 등록하고 찾을 수 있는 관리 서비스를 만들기 위한 Python 실습 프로젝트입니다.

현재 단계는 **프로젝트 초기 구조 생성 단계**입니다.

## 기본 폴더 안내

- `src/lost_and_found/`: 앞으로 Python 프로그램 코드를 작성할 폴더입니다.
- `tests/`: 앞으로 프로그램이 올바르게 동작하는지 확인하는 코드를 둘 폴더입니다.
- `docs/`: 프로젝트 설명과 설계 문서를 정리할 폴더입니다.

고려대학교 분실물 관리 서비스 실습 저장소

## 프로젝트 구조

```text
src/lost_and_found/
├── main.py          # FastAPI 앱 진입점
├── api.py           # 분실물 API
├── config.py        # 환경 설정
├── models.py        # 도메인 모델
├── schemas.py       # 요청/응답 스키마
└── repository.py    # 저장소 구현
tests/               # API 테스트
docs/                # 설계 문서
```

## 시작하기

Python 3.11 이상에서 가상 환경을 만든 뒤 개발 의존성을 설치합니다.

```powershell
python -m venv .venv
.\\.venv\\Scripts\\Activate.ps1
python -m pip install -e ".[dev]"
```

개발 서버 실행:

```powershell
uvicorn lost_and_found.main:app --reload
```

실행 후 API 문서는 `http://127.0.0.1:8000/docs`에서 확인할 수 있습니다.

테스트 실행:

```powershell
pytest
```

현재 저장소는 개발을 빠르게 시작할 수 있도록 메모리 저장소를 사용합니다. 운영 전에는
`repository.py`를 SQLite 또는 PostgreSQL 구현으로 교체해야 합니다.

## 요구사항 분석
### 고객 요구사항
- 고객 요구사항을 분석하기 위한 문서 작성

### 소프트웨어 요구사항 분석

### TDD
### 단위 테스트

## 아키텍처 설계
