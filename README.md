# AIA SAM RAG Admin - Release Artifacts

## 구조
- `app.jar` — 백엔드 코드 (~435KB, 매 릴리즈 push)
- `libs/` — 의존성 라이브러리 (~72MB, 의존성 변경 시만 push)
- `frontend/` — 프론트엔드 빌드 (~15MB, UI 변경 시 push)

## 폐쇄망 배포
```bash
cd src/dist && git pull && cd ../..
cp src/dist/app.jar ./app.jar
cp -r src/dist/libs ./libs
cp -r src/dist/frontend ./frontend
docker compose restart app
```
