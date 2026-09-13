# 검사 규칙 변경

각 검사 항목의 알림 수준(오류, 경고, 정보)을 변경하거나 사용하지 않도록 설정할 수 있습니다. 변경 내용은 문서 루트의 `docs-lint.config.json`에 저장되어 팀과 공유됩니다.

## 알림 수준 변경

1. 도구 모음에서 [문서 도구]를 누르고 [검사] 탭을 엽니다.
2. [규칙 확인·변경]을 누릅니다.
   검사 항목 목록이 같은 카드 안에 펼쳐집니다. 각 항목에는 목적과 현재 설정의 제공처(Project, Profile, Pack, Default)가 표시됩니다.
3. 변경할 항목의 알림 수준을 선택합니다.
4. [저장하고 다시 검사]를 누릅니다.
   설정이 저장되고 문서 루트 전체가 새 설정으로 다시 검사됩니다.

| 선택지 | 의미 |
|---|---|
| [표준 설정(…)] | 재정의를 삭제하고 프로필, Standard Pack, 기본값 순으로 결정되는 표준 설정으로 되돌립니다 |
| [사용 안 함] | 이 항목을 검사하지 않습니다 |
| [정보] / [경고] / [오류] | 이 알림 수준으로 보고합니다 |

> **참고**
>
> - 저장하려면 신뢰할 수 있는 작업 영역이어야 합니다.
> - 저장되는 것은 각 항목의 알림 수준뿐입니다. 항목별 옵션은 그대로 유지됩니다. Standard Pack과 프로필 자체는 이 화면에서 변경하지 않습니다.
> - 저장 직전에 `docs-lint.config.json`이 외부에서 변경된 경우 저장이 중단됩니다. 최신 상태를 불러온 후 다시 시도하십시오.
> - `docs-lint.config.json`이 없으면 저장할 때 만들어집니다.

## 설정 파일 직접 편집

- [상세 설정 열기]를 누르면 `docs-lint.config.json`이 VS Code에서 열립니다.
- [규칙의 제공처와 문서 설정]을 열고 [문서 설정 편집]을 누르면 `lunascape-docs.json`이 VS Code에서 열립니다. Standard Pack과 프로필은 여기에서 선택합니다.

두 파일 모두 확장 기능에 포함된 JSON Schema에 의한 입력 완성과 설명을 사용할 수 있습니다.

## Standard Pack과 프로필

Standard Pack은 필요한 문서의 종류, 장 구성, 용어, 템플릿을 모아 놓은 문서 표준입니다. `lunascape-docs.json`의 `documentStandards`에서 선택합니다.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

포함된 Pack `builtin:gu-corp-software`에는 `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract` 프로필이 있습니다.

## 관련 항목

- [문서 검사](check.md)
- [프로젝트 설정](project-configuration.md)
