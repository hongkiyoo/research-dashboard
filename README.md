# 연구 현황 대시보드

랩 멤버용 비공개 대시보드. 단일 HTML 파일을 StatiCrypt로 암호화해 GitHub Pages로 배포합니다.

이 README는 GitHub repo 첫 페이지에도 노출됩니다 — **민감한 정보는 적지 마세요.**

## 보는 사람용

`https://<owner>.github.io/<repo>/` 로 접속 → 비밀번호 입력 → 대시보드.

비번은 [@hongkiyoo](mailto:hongkiyoo@gmail.com) 에게 문의.

## 운영자용 (한국기 본인)

### 일상

- 더블클릭: `update.command`
- 흐름: 데이터 추출 → HTML 빌드 → 암호화 → `git push` → 로컬 미리보기
- 푸시 후 ~1분 뒤 GitHub Pages에 반영됨

### 비번 변경

```sh
echo -n "새-긴-비번-15자이상" > .password
chmod 600 .password
./update.command   # 새 비번으로 재암호화 + 배포
```

기존 링크를 알고 있던 사람은 새 비번을 받기 전까지 페이지를 못 봅니다.

### 셋업 다시 하기

`setup.command` 더블클릭. `.password` 와 git remote 를 갱신합니다.
