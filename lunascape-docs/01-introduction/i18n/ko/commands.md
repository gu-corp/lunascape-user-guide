# 명령 목록

명령 팔레트(`⇧⌘P` / `Ctrl+Shift+P`)에서 "Lunascape Docs"를 입력하면 다음 명령을 실행할 수 있습니다.

| 명령 | 기능 |
|---|---|
| Lunascape Docs: 사양서 뷰어 열기 | 가장 가까운 문서 루트를 뷰어에서 엽니다. 읽기, 편집, 검사, 번역은 이 화면에서 합니다 |
| Lunascape Docs: 사양서 뷰어로 열기 | 편집기에서 열려 있는 Markdown 파일을 뷰어에 표시합니다 |
| Lunascape Docs: 템플릿에서 문서 만들기 | 문서 폴더가 없는 프로젝트에 최초의 문서 한 벌을 만듭니다 |
| Lunascape Docs: 문서 루트 검증 | 문서 루트 전체를 docs-lint로 검사하고 결과를 문서 도구와 [문제] 패널에 표시합니다 |
| Lunascape Docs: 도움말 열기 | 이 도움말 가이드를 엽니다 |

## 탐색기에서의 조작

탐색기에서 `.md`, `.markdown`, `.mdx` 파일을 마우스 오른쪽 버튼으로 클릭하면 [Lunascape Docs: 사양서 뷰어로 열기]를 선택할 수 있습니다.

> **힌트**
>
> Markdown 파일을 평소처럼 열었을 때도 Lunascape Docs로 표시하려면 작업 영역 설정에 편집기 연결을 추가합니다.
>
> ```json
> {
>   "workbench.editorAssociations": {
>     "*.md": "lunascapeDocEditor.markdownPortal"
>   }
> }
> ```

## 연습

VS Code의 [도움말] 메뉴 → [시작]에 있는 연습 "Lunascape Docs 시작하기"에서 첫 조작을 차례대로 해 볼 수 있습니다.

## 관련 항목

- [기본 조작](../02-reading/README.md)
- [키보드 조작 목록](../08-reference/keyboard.md)
