# FamersAI 프런트엔드

농장, 채용·지원, 이력서, 게시판, 컨설팅 화면이 있는 React 프로젝트의 포크입니다.
원본 저장소는 [kimjaehoug/famersai](https://github.com/kimjaehoug/famersai)입니다.

현재 `main`의 커밋 이력에는 원본 작업자들의 변경이 포함되어 있습니다.
이 포크에서 별도로 작성한 기능은 아직 기록되어 있지 않습니다.
원본 코드의 작성자와 변경 내역은 Git 이력을 기준으로 확인할 수 있습니다.

## 실행

Node.js 22 환경에서 잠금 파일을 기준으로 설치합니다.

```bash
npm ci
npm start
```

개발 화면은 `http://localhost:3000`에서 확인합니다.
백엔드 주소는 루트의 `.env.local`에 지정합니다.

```dotenv
REACT_APP_API=http://localhost:8080
```

위 주소는 로컬 설정 예시입니다. 백엔드는 이 저장소에 포함되어 있지 않아
회원가입, 로그인, 게시판 등 서버 요청이 필요한 기능은 백엔드가 있어야 동작합니다.

```bash
npm run build
CI=true npm test -- --watchAll=false
```

## 코드 위치

- `src/App.js`: 화면 경로
- `src/menu/`: 농장·채용·회원 관련 화면
- `src/board/`: 게시판 작성과 조회
- `src/customAxios.js`: API 주소와 공통 요청 설정
- `src/AuthContext.js`: 인증 상태

## 포크에서 작업할 때

변경은 별도 브랜치에서 진행하고 PR에 변경한 화면, 확인 방법, 백엔드 의존 여부를 적습니다.
원본에서 가져온 변경과 직접 수정한 변경은 커밋을 구분합니다.
실제 환경변수 값과 인증 정보는 커밋하지 않습니다.
