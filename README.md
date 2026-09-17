# 展示会視察レポート - EXPO REPORT

展示会で視察したサプライヤ情報をスマートフォンで記録・管理するPWAアプリです。

## 📱 機能

- サプライヤ情報（企業名・出展品目・特色・評価・写真）の記録
- 写真の自動圧縮（カメラ撮影・ライブラリ選択）
- PDF印刷 / CSV(Excel)出力 / PowerPoint出力
- メール本文コピー
- アーカイブ機能（展示会ごとに報告書を保存）
- 再編集機能
- データはIndexedDBに自動保存（ページを閉じても消えない）
- **完全オフライン動作**（インターネット不要）

---

## 🚀 GitHub Pagesでの公開手順

### 1. GitHubリポジトリを作成

1. [GitHub](https://github.com) にログイン
2. 右上「+」→「New repository」
3. Repository name: `expo-report`（任意）
4. **Public** を選択
5. 「Create repository」をクリック

### 2. ファイルをアップロード

以下のファイルをすべてアップロードしてください：

```
index.html       ← メインアプリ
manifest.json    ← PWA設定
sw.js            ← オフライン対応
icon-192.png     ← アプリアイコン
icon-512.png     ← アプリアイコン（大）
```

GitHubの「Add file」→「Upload files」から一括アップロードできます。

### 3. GitHub Pagesを有効化

1. リポジトリの「Settings」タブ
2. 左メニュー「Pages」
3. Source: **Deploy from a branch**
4. Branch: **main** / **/ (root)**
5. 「Save」をクリック

### 4. アクセス

数分後に以下のURLでアクセスできます：
```
https://[GitHubユーザー名].github.io/expo-report/
```

---

## 📲 スマートフォンにインストール（PWA）

### iPhone (Safari)
1. Safariでアプリのページを開く
2. 下部の「共有」ボタン →「ホーム画面に追加」

### Android (Chrome)
1. ChromeでアプリのURLを開く
2. アドレスバー右の「⋮」→「ホーム画面に追加」
   または自動表示されるインストールバナーをタップ

---

## 💾 データについて

- データはブラウザの **IndexedDB** に保存されます
- 同じブラウザ・同じURLでアクセスする限りデータは保持されます
- ブラウザのデータ消去を行うと削除されます
- アーカイブのCSV/Excel出力でバックアップすることをお勧めします

---

## 🛠 ローカルで使う場合

`index.html` をブラウザで直接開いても使えます。
その場合、データは開いたファイルのパスに紐付いて保存されます。
