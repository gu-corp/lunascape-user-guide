# 문서 루트와 파일 규약

Lunascape Docs가 문서를 찾아 INDEX를 구성할 때 따르는 규칙입니다. 파일 시스템 자체가 정본이 되므로, 대장이나 빌드 설정이 필요 없습니다.

## 문서 루트

- 가장 가까운 `docs` 폴더, 또는 `lunascape-docs.json`을 둔 폴더가 문서 루트가 됩니다.
- `lunascape-docs.json`을 두면 폴더 이름이 `docs`가 아니어도 됩니다.
- 어느 문서 루트에도 속하지 않는 Markdown을 열면, 그 폴더를 임시 문서 루트로 표시합니다.

## INDEX에 표시되는 파일

- `.md`, `.markdown`, `.mdx` 파일을 표시합니다. front matter나 내비게이션 정보가 없어도 새 파일은 반드시 표시됩니다.
- `.`으로 시작하는 폴더, `node_modules`, 그리고 `ignoredDirectories`(기본값은 `99-archive`)에 지정한 폴더는 표시되지 않습니다.
- `i18n/` 아래는 번역본으로 취급하며, INDEX에는 별도로 표시하지 않습니다.

## 폴더의 표지

- 본문이 있는 `README.md`(없으면 `index.md`)는 그 폴더의 표지가 됩니다. INDEX에서 폴더 이름을 누르면 표지가 열립니다.
- front matter만 있고 본문이 없는 `README.md`는 "설정 전용 기술자"로 취급하며, 페이지로는 표시하지 않습니다. 폴더의 제목이나 순서만 지정하고 싶을 때 사용합니다.
- `README.md`와 `index.md`가 모두 있을 때는 `README.md`를 우선합니다.

## 기본 언어와 번역본

- 기본 언어의 문서(정본)는 있던 자리에 그대로 둡니다.
- 번역본은 정본과 같은 폴더의 `i18n/<언어>/`에 같은 파일 이름으로 둡니다. 폴더 구조를 `i18n/` 아래에 다시 만드는 방식으로는 인식되지 않습니다.
- 해결 위치는 이 한 곳뿐입니다. 다른 곳에 둔 같은 이름의 번역본은 어느 문서의 번역으로도 취급되지 않는 고립 파일이 됩니다.

```text
docs/
  lunascape-docs.json
  README.md                  ← 문서 루트의 표지(시작 페이지)
  i18n/en/README.md          ← 그 영어판
  01-product/
    README.md                ← 폴더의 표지
    requirements.md
    i18n/en/README.md        ← 위 두 문서의 영어판
    i18n/en/requirements.md
  99-archive/                ← 기본으로 INDEX에서 제외
```

## `_meta.json`에 관하여

Nextra의 `_meta.json`은 내비게이션에 사용하지 않습니다. 기존 파일은 변경도 삭제도 하지 않습니다. 앞으로는 명시적인 가져오기·내보내기 기능에서만 다룰 예정입니다.

## 관련 항목

- [내비게이션 정보 설정하기](navigation-metadata.md)
- [프로젝트 설정](project-configuration.md)
- [문서 루트 전환하기](../02-reading/roots.md)
