# 확장 프로그램 설치하기

VS Code 확장 프로그램 "Lunascape Docs Pro"는 VSIX 파일로 배포합니다. 무료입니다. "Pro"는 AI에 작업을 넘기는 기능과 자체 업데이트 기능을 갖춘 버전임을 나타냅니다.

## 동작 환경

- VS Code 1.90 이상
- 문서 작성, INDEX에서의 정리, 검사 설정 저장, 번역 등 쓰기를 수반하는 기능은 VS Code에서 "신뢰할 수 있는" 것으로 표시한 작업 영역에서만 사용할 수 있습니다.

## 설치하기

1. VSIX 파일을 받습니다. 이 링크는 항상 최신 버전을 가리킵니다.

   [lunascape-docs-pro.vsix 다운로드](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. VS Code의 확장 프로그램 보기(`⇧⌘X` / `Ctrl+Shift+X`)를 엽니다.
3. 오른쪽 위의 `…` 메뉴에서 [VSIX에서 설치...]를 선택하고, 받은 파일을 지정합니다.

### 명령으로 설치하기

터미널에서 한 줄로 끝낼 수도 있습니다. 다운로드와 설치를 연달아 진행합니다.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows(PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **참고**
> `code`를 찾을 수 없을 때는 명령 팔레트(`⇧⌘P` / `Ctrl+Shift+P`)에서 [셸 명령: PATH에 'code' 명령 설치]를 실행하세요.

## 업데이트하기

새 버전이 공개되면 확장 프로그램이 스스로 받아서 설치합니다. VS Code가 창을 다시 불러올 것을 권하면, 그때 새 버전으로 전환됩니다. 설정과 문서는 그대로 남습니다.

확인은 하루에 한 번입니다. 바로 확인하고 싶을 때는 명령 팔레트(`⇧⌘P` / `Ctrl+Shift+P`)에서 [Lunascape Docs: 업데이트 확인]을 실행합니다.

동작은 설정 `lunascapeDocEditor.update.check`에서 바꿀 수 있습니다.

| 설정 | 동작 |
|---|---|
| 새 버전이 공개되면 설치한다 | 기본값 |
| 알린다. 설치할지는 그때그때 정한다 | 알림이 뜨고, [업데이트]를 눌렀을 때만 전환됩니다 |
| 확인하지 않는다 | 아무것도 하지 않습니다 |

### 업데이트할 수 없을 때

"업데이트를 가져올 수 없습니다: No Servers"라고 나오는 경우는 설치된 버전이 0.22.18 이전입니다. 그 버전의 업데이트 기능은 받아온 뒤의 마지막 단계에서 반드시 실패하므로, 스스로 새 버전으로 바뀌지 못합니다. 위 절차대로 한 번만 직접 다시 설치하세요. 이후에는 스스로 업데이트합니다.

## 버전 확인하기

확장 프로그램 보기에서 "Lunascape Docs Pro"를 열면 설치된 버전이 표시됩니다. 불편한 점을 신고할 때 필요합니다.

## 관련 항목

- [문서를 처음 작성하기](first-documents.md)
- [불편한 점 신고하기](../07-troubleshooting/report.md)
