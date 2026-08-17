# datamining

경로 생성 기능을 구체화하기위한 데이터 마이닝 기법

경로 추천 기능(`feature/알고리즘설계.md`)이 규칙 기반 설계에서 막힌 지점(문제 A: 후보 선택 기준 없음, 문제 B: 설명 가능성 부재)을 데이터 마이닝 — 우선 연관 규칙(association rule) — 으로 풀어볼 수 있는지 실험/학습하는 공간이다.

앱이 실행 시점에 이 폴더를 참조하는 일은 없다. `python/`(route-graph 생성 파이프라인)과는 완전히 별개의 venv를 쓴다 — 이 둘을 섞지 않는다.

## 세팅 상태

- `.venv/` — 이 폴더 전용 격리된 가상환경 (`python -m venv .venv`로 생성, `python/`의 루트 `.venv`와 무관).
- 설치된 것: `pip`, `jupyterlab`, `ipykernel` 뿐.
- Jupyter 커널로 `moment-route datamining` (커널 이름: `datamining`) 등록 완료 — VS Code에서 `.ipynb` 열고 커널 선택 시 목록에 나타남.
- `notebooks/01-setup-check.ipynb` — 환경이 도는지만 확인하는 스모크 테스트 노트북.

**의도적으로 설치하지 않은 것**: 연관 규칙 마이닝에 실제로 쓸 라이브러리(예: Apriori 등을 어떤 패키지로 다룰지)와 예제 데이터셋. 무엇이 필요한지 파악하고 찾아서 설치하는 과정 자체가 다음 단계의 일이다.

## 실행 방법

```bash
# 가상환경 활성화 (PowerShell)
datamining\.venv\Scripts\Activate.ps1

# 또는 VS Code에서 notebooks/01-setup-check.ipynb를 열고
# 우측 상단 커널 선택에서 "moment-route datamining" 선택 후 셀 실행
```

라이브러리를 새로 설치할 때는 반드시 이 venv를 활성화한 상태에서 `pip install`을 실행한다 (루트 `.venv`나 시스템 Python에 설치하지 않는다).
