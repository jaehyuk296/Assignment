# FastAPI 기본 틀

## 개발 환경 세팅 (uv)

1. Python 3.7 이상이 설치되어 있어야 합니다.
2. 실 개발환경과 비슷하게 진행하기 위해 파이썬 패키지 매니저로는 [uv](https://github.com/astral-sh/uv) 를 사용합니다.
설치 방법은 다음과 같습니다:

macOS/Linux:
```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

Windows (PowerShell):
```powershell
irm https://astral.sh/uv/install.ps1 | iex
```

3. 패키지 설치:

```bash
uv install -r requirements.txt
```

4. (선택) 가상환경 세팅:

- Python 내장 venv 사용:

```bash
python -m venv .venv
source .venv/bin/activate  # macOS/Linux
.venv\Scripts\activate    # Windows
```

- uv로 가상환경 생성 및 활성화:

```bash
uv venv .venv
uv venv exec .venv
```

5. 서버 실행 (uvicorn):

```bash
uvicorn run app.main:app --reload
```

- `--reload` 옵션은 코드 변경 시 자동으로 서버를 재시작합니다.
- 서버가 실행되면 [http://127.0.0.1:8000](http://127.0.0.1:8000) 에서 확인할 수 있습니다.

## 기타
- FastAPI 공식 문서: https://fastapi.tiangolo.com/ko/
- Uvicorn 공식 문서: https://www.uvicorn.org/
- UV 공식 문서: https://docs.astral.sh/uv/

## 과제 수행 방식
과제는 다음과 같은 방식으로 이루어집니다.
1. **과제 기본 틀 Clone**: 이 레포지토리의 코드를 클론합니다.
2. **개발 환경 세팅**: 위의 개발 환경 세팅을 따라 uv를 설치하고 패키지를 설치합니다.
3. **브랜치 생성**: 각자 작업할 브랜치를 생성합니다. 
이때, 브랜치 이름은 `feat/분야/이름/과제 주차` 형식으로 생성합니다. 예: `feat/backend/홍길동/1주차`.  
4. **과제 수행**: 각자의 브랜치에서 과제를 수행합니다.
5. **커밋 및 푸시**: 작업이 완료되면 커밋하고 원격 저장소에 푸시합니다.
6. **Pull Request 생성**: 작업이 완료된 브랜치에서 `main` 브랜치로 Pull Request를 생성합니다. 이때, PR 제목은 `feat/분야/이름/과제 주차` 형식으로 작성합니다. 예: `feat/홍길동/1주차`.  
또한 PR 설명에는 자신의 과제에 대한 간단한 설명과 해결해낸 단계를 작성합니다.