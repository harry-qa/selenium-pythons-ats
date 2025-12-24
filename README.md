# *이 프로젝트의 코드는 ChatGPT로 작성되었습니다.
# Python & Selenium 기반 이커머스 자동화 테스트 (ATS)

본 프로젝트는 엘리스(Elice) QA 트랙 과정을 통해 구축한 쿠팡(Coupang) 웹 서비스 자동화 테스트 프레임워크입니다.

## 1. 프로젝트 개요
- **목표**: 이커머스 핵심 비즈니스 로직(로그인, 상품 검색, 필터링)에 대한 회귀 테스트 자동화 구현
- **핵심 가치**: 테스트 스크립트의 유지보수성 향상 및 실행 안정성 확보

## 2. 주요 구현 내용
- **POM(Page Object Model) 설계**: UI 요소와 테스트 로직을 분리하여 사이트 구조 변경 시 대응 비용을 최소화하는 구조적 설계 적용
- **Pytest 프레임워크 활용**: `conftest.py`를 통한 중앙 집중식 브라우저 제어 및 공통 설정(Fixtures) 관리
- **동적 대기(Explicit Wait)**: `WebDriverWait`를 적용하여 네트워크 지연 및 비동기 로딩 상황에서의 테스트 신뢰도(Stability) 확보
- **예외 처리 및 리포팅**: 테스트 실패 시 자동 스크린샷 저장 로직을 구현하여 결함 분석 가시성 증대

## 3. 기술 스택
- **Language**: Python 3.x
- **Library**: Selenium WebDriver, Pytest
- **Configuration**: 환경별 설정 분리 관리를 위한 `testconfig` 모듈 구축

## 4. 프로젝트 구조

```text
.
├── pages/                # Page Object 클래스 (UI 요소 및 액션 정의)
│   ├── login_test.py
│   ├── main_element.py
│   └── search.py
├── conftest.py           # Pytest 실행 환경 및 공통 설정
├── testconfig.py         # 테스트 환경 변수 관리
└── .gitignore            # Git 관리 제외 파일 설정
```
## 5. 실행 방법 

# 의존성 설치
pip install selenium pytest

# 테스트 실행
pytest
