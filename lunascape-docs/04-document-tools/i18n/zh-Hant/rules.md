# 變更檢查規則

您可以變更各檢查項目的通知層級（錯誤、警告、資訊），或設定為不使用。變更內容會儲存至文件根目錄的 `docs-lint.config.json`，並與團隊共用。

## 變更通知層級

1. 按下工具列的 [文件工具]，開啟 [檢查] 索引標籤。
2. 按下 [確認與變更規則]。
   檢查項目的清單會在同一張卡片中展開。各項目會顯示其用途，以及目前設定的提供來源（Project、Profile、Pack、Default）。
3. 選擇要變更的項目的通知層級。
4. 按下 [儲存並重新檢查]。
   設定會儲存，並以新的設定重新檢查整個文件根目錄。

| 選項 | 意義 |
|---|---|
| [標準設定（…）] | 刪除覆寫設定，回到依設定檔、Standard Pack、預設值的順序決定的標準設定 |
| [不使用] | 不檢查此項目 |
| [資訊] / [警告] / [錯誤] | 以此通知層級回報 |

> **注意**
>
> - 儲存需要受信任的工作區。
> - 儲存的只有各項目的通知層級。各項目的選項會維持原狀。Standard Pack 與設定檔本身不會在此畫面變更。
> - 若 `docs-lint.config.json` 在儲存前已被外部變更，儲存將會中止。請載入最新狀態後重試。
> - 若沒有 `docs-lint.config.json`，會在儲存時建立。

## 直接編輯設定檔

- 按下 [開啟詳細設定]，即可在 VS Code 中開啟 `docs-lint.config.json`。
- 開啟 [規則的提供來源與文件設定] 並按下 [編輯文件設定]，即可在 VS Code 中開啟 `lunascape-docs.json`。Standard Pack 與設定檔在此選擇。

這兩個檔案都可使用擴充功能隨附的 JSON Schema 所提供的輸入自動完成與說明。

## Standard Pack 與設定檔

Standard Pack 是彙整了必要文件種類、章節架構、用語與範本的文件標準。請以 `lunascape-docs.json` 的 `documentStandards` 選擇。

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

隨附的 Pack `builtin:gu-corp-software` 提供 `base`、`web-application`、`api-service`、`regulated-financial-product`、`smart-contract` 等設定檔。

## 相關項目

- [檢查文件](check.md)
- [專案設定](project-configuration.md)
