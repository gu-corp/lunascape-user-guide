# 내 문서를 웹에 게시하기

내 리포지토리의 문서를 GitHub Pages나 원하는 정적 호스팅에서 웹 사이트로 게시할 수 있습니다. 게시하는 방법은 두 가지입니다. 이 절차는 Lunascape Docs 리포지토리를 clone하고 `npm`을 사용할 수 있는 개발자를 위한 것입니다.

## 방법 1: 뷰어 파일 2개를 배치하기

뷰어 본체(`index.html`와 `lsdoc.js`)만 배치하고 문서는 GitHub에서 불러오는 방법입니다. 문서 자체는 사이트에 포함되지 않으므로 비공개 리포지토리에서도 안전합니다(열람자는 GitHub에서 로그인합니다).

1. Lunascape Docs 리포지토리에서 다음 명령을 실행합니다.

   ```sh
   npm run build:viewer
   ```

   `dist/viewer/`에 `index.html`와 `lsdoc.js`가 생성됩니다.
2. 두 파일을 게시하려는 리포지토리의 `docs/`에 배치합니다.
3. GitHub Pages를 활성화합니다.

표시할 문서 루트는 다음 순서로 결정됩니다.

1. `index.html` 안의 설정 `source`
2. 같은 폴더의 `lunascape-docs.json`에 기재된 `repository`
3. `*.github.io` URL과 브랜치 구성에서의 추정

## 방법 2: 문서를 포함한 정적 사이트로 내보내기

뷰어와 문서 파일을 함께 내보내어 그대로 호스팅하는 방법입니다.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

뷰어 일체, `docs/` 아래의 문서, 목록 파일 `lunascape-docs-manifest.json`, `.nojekyll`가 출력됩니다. 출력한 결과물을 S3나 GitHub Pages에 배치하면 게시할 수 있습니다. GitHub Actions로 자동 게시하는 예는 리포지토리의 `examples/workflows/publish-docs-pages.yml`을 참조하십시오.

> **참고**
>
> - **비공개 리포지토리의 문서를 내보내어 GitHub Pages에 두지 마십시오.** Enterprise Cloud 이외의 GitHub Pages는 누구나 열람할 수 있습니다. 한정 공개가 필요한 경우에는 방법 1을 사용하고, 열람자가 GitHub에서 로그인하도록 하십시오.
> - `index.html`를 `file://`로 직접 열어도 동작하지 않습니다. 브라우저가 인접 파일의 읽기와 ES 모듈의 실행을 금지하기 때문입니다. 직접 확인할 때는 VS Code 버전이나 HTTP 서버를 사용하십시오.
> - TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose의 렌더링 라이브러리는 표시할 때 불러옵니다. 내보낸 사이트에서는 `vendor/` 폴더도 함께 배치하십시오.

## 관련 항목

- [웹 버전에서 할 수 있는 일](README.md)
- [비공개 리포지토리 열람하기](private-repository.md)
