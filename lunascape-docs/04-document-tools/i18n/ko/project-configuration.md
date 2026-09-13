# 프로젝트 설정

문서 루트 바로 아래의 `lunascape-docs.json`은 팀에서 공유하는 문서 루트의 설정입니다. Git으로 관리합니다.

## 설정 파일을 만들고 편집하기

- 툴바의 [문서 도구] → [검사] 탭 → [규칙의 제공처와 문서 설정] → [문서 설정 편집]을 누르면 VS Code에서 열립니다. 파일이 없을 때는 이때 초기 파일이 만들어집니다.
- 파일 이름 `lunascape-docs.json`에는 동봉된 JSON Schema가 자동으로 연결되어, 입력 완성과 각 항목의 설명이 표시됩니다. `$schema` 기재는 필요 없습니다.

## 설정 예

```json
{
  "id": "product-docs",
  "title": "제품 문서",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## 항목 설명

| 항목 | 내용 | 기본값 |
|---|---|---|
| `id` | 사용자별 표시 설정을 저장하는 키입니다. 폴더를 옮겨도 설정을 이어받고 싶을 때 고정된 ID를 붙입니다 | 폴더 경로 |
| `title` | 툴바 왼쪽 끝과 문서 루트 목록에 표시하는 이름입니다. 표시 언어를 바꿔도 변하지 않습니다 | 루트의 README/index 제목, 없으면 폴더 이름 |
| `indexTitle` | INDEX의 제목입니다 | `INDEX` |
| `startPage` | 처음에 여는 문서(문서 루트 기준 상대 경로)입니다 | `README.md` |
| `appearance` | 배색입니다. `light`(항상 밝게) 또는 `auto`(VS Code 테마를 따름) | `light` |
| `defaultLocale` | 기본 언어(정본의 언어)입니다. BCP 47 언어 태그(`ja`, `en`, `zh-Hant` 등)로 지정합니다. 번역 원본이 됩니다 | 미설정(본문에서 추정하여 표시) |
| `fallbackLocale` | 열람 환경의 언어가 지원 언어 중 어느 것과도 일치하지 않는 독자에게 처음 보여줄 언어입니다. `locales`에 포함된 언어를 지정합니다 | 미설정(`defaultLocale`을 사용) |
| `locales` | 지원 언어 목록입니다. `defaultLocale`을 포함합니다. 언어 메뉴와 번역 대상의 후보가 됩니다 | `defaultLocale`만 |
| `ignoredDirectories` | INDEX, 검색, 검사에서 제외할 폴더 이름입니다. 지정하면 기본값을 대체합니다 | `["99-archive"]` |
| `tree` | INDEX 표시의 기본값입니다. 사용자는 표시 설정에서 덮어쓸 수 있습니다 | 위 예와 같음 |
| `editor.defaultMode` | 사용자가 아직 전환하지 않았을 때의 편집 표시입니다. `visual` 또는 `source` | `visual` |
| `editor.showEditButton` | 본문 오른쪽 아래의 [편집]을 표시할지 여부입니다 | `true` |
| `documentStandards.pack` | 문서 검사와 템플릿에 사용하는 Standard Pack입니다. `builtin:<이름>`, 또는 문서 루트 기준 상대 경로 | 없음 |
| `documentStandards.profile` | Pack이 정의하는 프로파일 이름입니다 | 없음 |
| `translation.enabled` | 번역안 작성과 일괄 번역을 활성화합니다 | `true` |
| `translation.contextFiles` | 번역 시 용어와 문체의 참고로 전달하는 정본 Markdown(문서 루트 기준 상대 경로)입니다 | `[]` |
| `translation.maxContextCharacters` | 참고 문서의 총 문자 수 상한입니다(최대 1048576) | `49152` |
| `description` | 문서 집합의 한 줄 설명입니다. 리포지토리 홈의 카드에 표시합니다. `title`과 마찬가지로 문자열 또는 언어별 객체로 쓸 수 있습니다 | 없음 |

## 리포지토리의 어디에 문서가 있는지 알려주기

리포지토리 바로 아래에 둔 `lunascape-docs.json`에는 그 폴더의 설정이 아니라 **리포지토리의 지도**를 쓸 수 있습니다. 다음 3개 항목 중 하나를 쓰면 지도가 되며, 그 폴더 자체는 문서 루트가 되지 않습니다.

| 항목 | 내용 | 기본값 |
|---|---|---|
| `defaultFolder` | 문서가 어느 폴더에 있는지입니다(바로 아래 기준 상대 경로). 가리키는 대상에는 설정 파일이 필요 없습니다 | 없음(`docs`를 사용) |
| `roots` | 여러 문서 집합을 가질 때의 그 목록입니다(바로 아래 기준 상대 경로, 표시 순서). 이 경우 바로 아래는 홈이 됩니다 | 없음 |
| `excludes` | 문서 루트 발견에서 제외할 폴더입니다(바로 아래 기준 상대 경로). `node_modules` 등의 기본 제외에 더합니다 | `[]` |
| `home.cards` | 홈의 README 아래에 문서 집합의 카드를 표시할지 여부입니다. README에 직접 링크를 쓸 때는 `false`로 합니다 | `true` |

문서 루트는 다음 순서로 정해집니다. 위에서부터 순서대로, 처음 찾은 것을 사용합니다.

1. 설정이나 명령으로 폴더를 지정했을 때, 그 폴더
2. 바로 아래 `lunascape-docs.json`의 `defaultFolder` 또는 `roots`가 가리키는 대상
3. `lunascape-docs.json`이 있는 폴더(공통 부모 아래에 2개 이상 있으면 그 부모가 홈)
4. `docs` 폴더(`lunascapeDocEditor.rootDirectoryNames`)
5. 리포지토리 바로 아래 그 자체

> **힌트**
>
> 아무것도 쓰지 않으면 4번이 작동하므로, `docs/`를 하나 가진 보통의 리포지토리는 지금까지와 같습니다. 폴더 이름을 `manual`로 하고 싶을 때만 `defaultFolder`를 씁니다.

### 지도 예

```json
{
  "title": "Lunascape 도움말",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## 설정의 우선순위

표시에 관한 항목은 다음 순서로 우선됩니다.

1. 사용자의 표시 설정([표시 설정] 패널)
2. VS Code의 설정(`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. 제품의 기본값

언어(`defaultLocale`, `fallbackLocale`, `locales`)만은 예외로, `lunascape-docs.json`이 정본입니다. VS Code의 개인 설정으로 프로젝트의 언어를 덮어쓸 수는 없습니다.

> **참고**
>
> `docs-lint.config.json`에도 `standard`로 Standard Pack을 지정할 수 있습니다. 양쪽에 있을 경우에는 `docs-lint.config.json`이 우선됩니다.

## 관련 항목

- [검사 규칙 변경하기](rules.md)
- [표시 설정 변경하기](../02-reading/display-settings.md)
- [VS Code 설정 목록](../08-reference/settings.md)
