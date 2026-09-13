# 문서 루트 전환하기

문서 루트는 한 세트의 문서를 담는 최상위 폴더입니다. INDEX, 필터, 검사, 번역은 모두 문서 루트 단위로 동작합니다.

## 문서 루트를 찾는 방법

Lunascape Docs는 열려 있는 Markdown 파일에서 상위 폴더를 거슬러 올라가, 다음 중 하나에 해당하는 가장 가까운 폴더를 문서 루트로 삼습니다.

- `lunascape-docs.json`이 있는 폴더(폴더 이름은 상관없습니다)
- `docs`라는 이름의 폴더(설정 `lunascapeDocEditor.rootDirectoryNames`로 이름을 추가할 수 있습니다)

"Lunascape Docs: 사양서 뷰어 열기"를 실행하면 설정 `lunascapeDocEditor.root`(기본값 `docs`)의 문서 루트를 엽니다.

## 다른 문서 루트로 전환하기

작업 영역에 문서 루트가 여러 개 있으면, 도구 모음 맨 왼쪽의 문서 루트 이름이 풀다운 메뉴가 됩니다.

1. 도구 모음 맨 왼쪽의 문서 루트 이름을 누릅니다.
2. 목록에서 문서 루트를 선택합니다.
   선택한 문서 루트의 시작 페이지가 표시되고 INDEX가 전환됩니다.

> **힌트**
>
> 목록에 표시되는 이름은 다음 순서로 정해집니다. 표시 언어를 전환해도 바뀌지 않습니다.
>
> 1. `lunascape-docs.json`의 `title`
> 2. 루트의 `README.md`에 있는 `navigation.title`, 없으면 그 H1
> 3. 루트의 `index.md`에 있는 `navigation.title`, 없으면 그 H1
> 4. 폴더 이름(표준 `docs` 폴더에서는 그 상위 폴더 이름)

## 문서 루트에 속하지 않는 Markdown 열기

문서 루트에 포함되지 않은 Markdown 파일을 열면, 그 파일이 있는 폴더를 임시 문서 루트로 표시합니다. INDEX에는 같은 폴더와 그 아래에 있는 Markdown 파일이 나열됩니다.

- 도구 모음의 [상위 폴더로]를 누르면 작업 영역 안의 상위 폴더까지 표시 범위를 넓힐 수 있습니다.
- 이 표시에서는 프로젝트의 언어 설정과 일괄 번역을 사용할 수 없습니다. 해당 폴더에 `lunascape-docs.json`을 두어 문서 루트로 만들면 사용할 수 있습니다.

## 항상 정해진 문서 루트 열기

설정 `lunascapeDocEditor.rootMode`를 `fixed`로 지정하면, 어떤 Markdown을 열어도 항상 `lunascapeDocEditor.root`의 문서 루트를 엽니다.

## 관련 항목

- [문서 루트와 파일 규약](../04-document-tools/structure.md)
- [프로젝트 설정](../04-document-tools/project-configuration.md)
- [VS Code 설정 목록](../08-reference/settings.md)
