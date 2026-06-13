# CrunnY CasA

> To Dare Is To Do

개인 아카이브 사이트입니다. Jekyll로 만들어졌고 GitHub Pages로 배포됩니다.

배포 URL: https://leesomyung.github.io/

## 구조

메뉴(탭)는 Spurs / Actors / Memories 3개이고, 각 메뉴마다 Posts / Photos / Links 하위 탭이 있습니다.

```
spurs/      actors/      memories/
  index.md    index.md     index.md
  posts.md    posts.md     posts.md
  photos.md   photos.md    photos.md
  links.md    links.md     links.md
```

## 콘텐츠 추가 방법

### 1. 글(Posts) 추가하기

`_posts/` 폴더에 `YYYY-MM-DD-제목.md` 형식으로 파일을 만듭니다.

```markdown
---
title: 글 제목
date: 2026-06-13
categories: [spurs]   # spurs / actors / memories 중 하나
---

본문 내용을 마크다운으로 작성합니다.
```

`categories`에 적은 카테고리의 Posts 탭에 자동으로 목록이 표시됩니다.

### 2. 사진(Photos) 추가하기

1. 이미지 파일을 `assets/images/<카테고리>/` 폴더에 넣습니다. (예: `assets/images/spurs/photo1.jpg`)
2. `_data/photos.yml`에 항목을 추가합니다.

```yaml
spurs:
  - src: /assets/images/spurs/photo1.jpg
    alt: 사진 설명
    caption: 화면에 표시될 캡션
```

### 3. 링크(Links) 추가하기

`_data/links.yml`에 항목을 추가합니다.

```yaml
spurs:
  - title: 링크 제목
    url: https://example.com
    description: 간단한 설명
```

## 로컬에서 미리보기

```bash
bundle exec jekyll serve
```

이후 http://127.0.0.1:4000 에서 확인합니다.

(이 macOS 환경에서는 Ruby 헤더 경로 문제로 아래처럼 SDKROOT를 지정해야 합니다)

```bash
SDKROOT=/Library/Developer/CommandLineTools/SDKs/MacOSX12.3.sdk bundle exec jekyll serve
```

## 배포

`main` 브랜치에 push하면 `.github/workflows/pages.yml`의 GitHub Actions가 자동으로 빌드 후 GitHub Pages에 배포합니다.

처음 한 번은 저장소 Settings → Pages → Build and deployment → Source를 **GitHub Actions**로 설정해야 합니다.
