# VS Code 설정 목록

VS Code 설정(`⌘,` / `Ctrl+,`)에서 "Lunascape Docs"를 검색하면 다음 항목을 변경할 수 있습니다. 모두 사용자별 설정이며, 프로젝트 문서에는 저장되지 않습니다.

## 문서 루트

| 설정 | 값 | 기본값 | 기능 |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto`는 열려 있는 Markdown에서 가장 가까운 문서 루트를 자동으로 선택하며, 어느 루트에도 속하지 않으면 상위 폴더를 일시적으로 엽니다. `fixed`는 항상 `root`의 문서 루트를 엽니다 |
| `lunascapeDocEditor.rootDirectoryNames` | 문자열 배열 | `["docs"]` | `auto`에서 문서 루트로 자동 검색할 폴더 이름입니다. `lunascape-docs.json`이 있는 폴더는 이름과 관계없이 검색됩니다. 리포지토리 최상위의 `lunascape-docs.json`에 `defaultFolder` 또는 `roots`가 있으면 그쪽이 우선합니다 |
| `lunascapeDocEditor.root` | 경로 | `docs` | `fixed` 모드 또는 명령으로 열 때 사용하는, 작업 영역 기준 상대 문서 루트입니다 |
| `lunascapeDocEditor.startPage` | 경로 | `README.md` | 문서 루트 기준 상대 시작 페이지입니다 |
| `lunascapeDocEditor.title` | 문자열 | `Lunascape Docs` | 문서 탭의 제목을 덮어씁니다. 문서 루트의 선택 이름에는 영향을 주지 않습니다 |
| `lunascapeDocEditor.ignoredDirectories` | 문자열 배열 | `["99-archive"]` | INDEX에서 제외할 폴더 이름입니다 |

## 표시

| 설정 | 값 | 기본값 | 기능 |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light`는 흰색 배경이고, `auto`는 VS Code의 색상 테마를 따릅니다 |
| `lunascapeDocEditor.locale` | 언어 태그 | 없음 | 사용할 수 있는 경우 우선하여 표시할 개인 문서 언어입니다. 프로젝트의 정본 언어는 변경하지 않습니다 |
| `lunascapeDocEditor.documentMetadata.compact` | 참/거짓 | `true` | H1 바로 뒤의 문서 관리 표를 "문서 정보" 행으로 접습니다 |
| `lunascapeDocEditor.tree.showFileNames` | 참/거짓 | `false` | INDEX에 문서 이름 대신 파일 이름을 표시합니다 |
| `lunascapeDocEditor.tree.showDocumentIcons` | 참/거짓 | `false` | INDEX에 문서 아이콘을 표시합니다 |
| `lunascapeDocEditor.tree.showFolderIcons` | 참/거짓 | `false` | INDEX에 폴더 아이콘을 표시합니다 |
| `lunascapeDocEditor.tree.showItemCounts` | 참/거짓 | `false` | INDEX에 폴더 바로 아래 항목 수를 표시합니다 |
| `lunascapeDocEditor.tree.showGuides` | 참/거짓 | `true` | INDEX에 계층 안내선을 표시합니다 |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | INDEX의 행 간격입니다 |
| `lunascapeDocEditor.tree.autoHideSingleItem` | 참/거짓 | `true` | 문서가 1개뿐일 때 INDEX를 처음 한 번만 닫습니다 |

## 편집

| 설정 | 값 | 기본값 | 기능 |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | 아직 전환하지 않았을 때의 편집 표시입니다. 마지막으로 사용한 표시가 우선합니다 |
| `lunascapeDocEditor.editor.showEditButton` | 참/거짓 | `true` | 본문 오른쪽 아래에 [편집]을 표시합니다 |

## 다이어그램

| 설정 | 값 | 기본값 | 기능 |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | TikZ의 렌더링 런타임입니다. `bundled`는 함께 포함된 승인 런타임(현재 배포판에는 포함되어 있지 않습니다), `workspace`는 신뢰할 수 있는 작업 영역 최상위의 `node-tikzjax` 1.0.5(개발·평가 전용), `disabled`는 렌더링하지 않습니다 |

## 사용을 권장하지 않는 설정

| 설정 | 대신 사용할 것 |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `lunascape-docs.json`의 `defaultLocale` |
| `lunascapeDocEditor.locales` | `lunascape-docs.json`의 `locales` |

개인 설정으로 프로젝트의 언어를 덮어쓸 수는 없습니다.

## 관련 항목

- [표시 설정 변경하기](../02-reading/display-settings.md)
- [프로젝트 설정](../04-document-tools/project-configuration.md)
