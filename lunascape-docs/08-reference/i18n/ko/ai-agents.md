# AI에서 사용하기

확장 기능은 읽기 전용 Language Model Tool `lunascape_getDocsSpecification`을 VS Code에 등록합니다. 이에 대응하는 VS Code 에이전트는 Lunascape Docs의 기능, 설정, 문서 규약에 대해 질문받았을 때, 이 도구로 이 도움말의 내용(일반 사양)을 가져올 수 있습니다.

## 사용법

VS Code 채팅에서 `#lunascapeDocs`를 붙여 질문하거나, Lunascape Docs의 설정이나 문서 구성에 대해 질문합니다.

```text
#lunascapeDocs lunascape-docs.json で英語の翻訳を有効にするには？
```

## 도구의 인수

| 인수 | 내용 |
|---|---|
| `topic` | 가져올 장입니다. `all`, `usage`(기본 조작), `structure`(문서 루트와 파일 규약), `editing`(문서 편집), `configuration`(프로젝트 설정), `security`(보안과 저장 경계), `ai`(AI에서 사용하기) |
| `locale` | 도움말의 언어입니다(`ja`, `en` 등, 동봉 도움말의 언어 태그). 생략하면 VS Code의 표시 언어, 없으면 일본어 도움말을 반환합니다 |

> **참고**
>
> - 도구는 문서 본문을 외부로 전송하지 않습니다.
> - 도구는 작업 영역 이름이나 로컬 경로를 반환하지 않습니다.
> - 도구는 파일을 변경하지 않습니다.
> - `AGENTS.md`가 없어도 VS Code의 대응 에이전트에서 사용할 수 있습니다. 확장 기능의 도구 API를 사용하지 않는 다른 AI 클라이언트에는 자동으로 공유되지 않습니다.

## 관련 항목

- [도움말 표시하기](../02-reading/help.md)
- [보안과 저장 경계](security.md)
