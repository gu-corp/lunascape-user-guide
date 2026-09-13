# 주요 사양

## 동작 환경

| 환경 | 요건 |
|---|---|
| VS Code 확장 | VS Code 1.90 이상. 쓰기가 따르는 기능은 신뢰할 수 있는 작업 영역에서 동작합니다 |
| 웹 브라우저판 | 최신 Chrome, Edge, Safari, Firefox. 로컬 폴더 열람은 폴더 선택(File System Access API)을 지원하는 브라우저 |
| Chromium 확장 | Manifest V3. 호스트 권한은 요구하지 않습니다 |

## 지원하는 문서

| 항목 | 내용 |
|---|---|
| 파일 | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown(표, 작업 목록, 코드 블록, 취소선), 로컬 이미지, YAML front matter |
| MDX | 허용된 컴포넌트만 표시합니다. 임의의 스크립트는 실행하지 않습니다 |
| HTML | DOMPurify 3.4.14로 무해화하여 표시합니다 |

## 다이어그램과 수식

| 종류 | 언어 이름 | 비고 |
|---|---|---|
| 수식 | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | 내장 데이터만. 외부 URL과 이미지 마크는 사용할 수 없습니다 |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | 엄격한 JSON만 |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | 배포판은 소스를 접은 상태로 표시. 입력 64 KiB, 15초, SVG 2 MiB의 상한 |
| Penrose(실험적) | `penrose` | `set-theory` 프리셋만 |

## 상한값

| 항목 | 값 |
|---|---|
| 템플릿의 전개 결과 | 4 MiB |
| 번역의 참조 컨텍스트 | 기본 49,152자, 최대 1,048,576자 |
| 일괄 번역의 1회 대상 | 1,000문서 |
| 이미지의 임의 너비 | 16~4096px |

## 파일

| 파일 | 역할 | Git 관리 |
|---|---|---|
| `lunascape-docs.json` | 문서 루트의 설정 | 함 |
| `docs-lint.config.json` | 검사 규칙의 설정 | 함 |
| `.lunascape-docs/translation-freshness.json` | 번역의 신선도 기록(경로, 언어, 해시, 일시만) | 함 |
| VS Code의 설정·작업 영역 상태 | 개인의 표시 설정, 공급자 선택, INDEX의 열림/닫힘 상태 | 안 함 |

## 동봉된 Standard Pack

`builtin:gu-corp-software` — 프로필: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## 관련 항목

- [VS Code 설정 목록](settings.md)
- [보안과 저장 경계](security.md)
