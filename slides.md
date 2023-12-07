---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## 2022 年 回顧與未來展望
# persist drawings in exports and build
drawings:
  persist: false
# use UnoCSS
css: unocss
download: true
dark: true
fonts:
# 与 css 中的 font-family 一致，你可以使用 `,` 来分割字体名，便于降级
  sans: 'Noto Sans TC'
---

# 2022年 回顧與未來展望

技術服務部 網頁組 呂正中

---
layout: center
---

# 回顧 2022 年 目標

去年給自己的目標

- <logos-cloudinary-icon /> 前端多媒體資源分離 - 可程式化的圖片媒體資源
- <vscode-icons-file-type-light-cypress /> 自動測試導入

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
layout: center
---

# 目標達成率

- <logos-cloudinary-icon /> 達成，但因成本考量只使用普通的CDN
- <logos-jest /> 未完全達成，只實作手動單元測試


<div class="bg-gradient-to-tr bg-clip-text from-green-500 to-sky-500 text-transparent text-8xl inline-block">75%</div>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
layout: center
---

# 未達成目標 <vscode-icons-file-type-light-cypress /> 自動測試導入

- 只導入單元測試、新增範例，測試覆蓋率2%
- 自動化流程由於前端多媒體資源分離完成時間較晚加上插件，尚未製作

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

# <fontisto-preview/> 2022重點工作產出

工單系統已有詳細清單，整理出以下為精華

- <icon-park-outline-blockchain /> NFT交易中心
    - <ant-design-skin-filled /> 皮膚系統 - 透過 css 變數設定快速調整版面色系
    - <simple-icons-iconify /> Icon 圖示套件更換為 Iconify - 超過10萬個 icon 可用的開源套件
- <img src="https://test-web-cdn.jlfafafa3.com/web_app_icon.png" inline-block w-6 h-6 /> 金銀島
    - <iconoir-chat-bubble-error /> 錯誤頁面改版 - 美化 UI 提升 UX 體驗，容易回報問題及查詢
    - <logos-jest /> 新增單元測試 - 新增程式範例，覆蓋率 2%
    - <mdi-image-multiple /> 前端多媒體資源分離 - CI/CD 加速 50% ，縮短 8 分鐘
    - 活動頁、說明頁公版優化 - 優化 UI 顯示，新增共用元件加速製程
- <la-slideshare /> 共用
    - <emojione-package /> 前端套件庫更換 npm <logos-npm-icon /> → pnpm <logos-pnpm /> - 更快速且節省硬碟空间

---

# 2023年 新目標

<br>
<br>

## <logos-jest /> 單元測試覆蓋率 50% 及自動化

<br>

## <vscode-icons-file-type-light-cypress /> End to End (E2E) cypress 終端測試導入

<br>

## <logos-nuxt-icon /> Nuxt 2 → <logos-nuxt-icon /> Nuxt 3 升級(意即 <logos-vue /> vue3 導入)

- 金銀島
- Admin2 改版為 <logos-nuxt-icon /> Nuxt 3 及流程改善

---

# <vscode-icons-file-type-light-cypress /> End to End (E2E) cypress 終端測試導入

## 痛點

- 只有 <logos-jest /> 單元測試，有時還不夠完整，無法模擬真正的使用者操作
- <logos-jest /> 的強項在於單元測試、對元件的測試相對難以使用

## 預計效益

- 模擬真正的使用者操作，當反覆修改時，可減少人工測試成本

---

# Admin2 <logos-vue /> vue3 導入

## 痛點

- 現行的後端網站 mixin 功能，無法高度客製頁面需求
- 開發製作邏輯、流程、畫面都綁著 mixin ，開發者往往要爬完 1000 行才能知其運作細節
- Admin2 `el-element-admin` 專案，直接遷移至 vue3 版本有難度

## 已知的新舊站整合 BUG

- 舊站把 `query` 當作頁面的 `path` 在使用，導致新站鑲嵌舊站時發生找不到頁面問題
- 新站鑲嵌舊站時，從舊站開啟新站的連結(無另開視窗)，會發生無限堆疊的鑲嵌情況

## 建議改善方案

- Vue 3 組合式 API 重構邏輯、流程、畫面，分層分類
- 改用 <logos-nuxt-icon /> Nuxt 3 製作
- 建議新舊站不要鑲嵌