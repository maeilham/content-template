# 매일함 콘텐츠 repo 등록 가이드

이 repo를 템플릿으로 사용해 자신만의 콘텐츠 repo를 만들고,
매일함 서비스에 등록할 수 있습니다.

## 구조

```
your-repo/
└── content/
    ├── 0001-slug.md
    ├── 0002-slug.md
    └── ...
```

`content/` 디렉토리 안에 마크다운 파일만 두면 됩니다.

## 파일 이름 규칙

`NNNN-slug.md`

- `NNNN`: 4자리 숫자 (예: `0001`, `0042`). repo 안에서 unique.
- `slug`: 소문자 영문/숫자/하이픈 (예: `goroutine-vs-thread`)
- 숫자 순서대로 발송됩니다.

## frontmatter

각 파일은 YAML frontmatter로 시작해야 합니다.

```yaml
---
title: "오늘 탐구할 주제"
preview: "이 주제를 공부하게 된 이유나 핵심 호기심 한 줄."
tags: [go, concurrency]
---
```

| 필드 | 필수 | 설명 |
|---|---|---|
| `title` | ✓ | 메일 제목 및 Discussion 제목으로 사용됩니다 |
| `preview` | ✓ | 메일 본문에 노출되는 1-2줄 |
| `tags` | | 검색·분류용 |

## 본문

본문에는 참고 자료만 적습니다. 답안이나 설명은 적지 않아도 됩니다.
학습 내용 정리와 토론은 자동 생성되는 GitHub Discussion에서 이루어집니다.

```markdown
## 참고 자료
- [링크](https://...)
```

## 동작 방식

1. 파일이 `main` 브랜치에 머지되면 매일함 서버가 자동으로 감지합니다.
2. 해당 콘텐츠의 GitHub Discussion이 자동 생성됩니다.
3. 구독자에게 메일이 발송됩니다.
4. 제목이 바뀌면 Discussion 제목도 자동으로 업데이트됩니다.

## 등록 문의

repo를 매일함에 등록하려면 메인테이너에게 문의해 주세요.
