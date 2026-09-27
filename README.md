# Tonton Copy — プライバシーポリシー／サポート／特商法表記

iOS アプリ「Tonton Copy」の公開用ページ（GitHub Pages 前提の静的 HTML）。
構成・書きぶりは Kakotte の同じページ（`/Users/sato/Desktop/Claude/kakotte-privacy/`）に合わせてある。

| ファイル | 中身 | App Store Connect で使う欄 |
|---|---|---|
| `index.html` | プライバシーポリシー | App 情報 › プライバシーポリシー URL |
| `support.html` | サポート・よくある質問・問い合わせ先 | バージョン情報 › サポート URL |
| `tokushoho.html` | 特定商取引法に基づく表記 | （必須欄なし。アプリ内・サポートから辿れるようにする） |
| `mascot.png` | ブタのアイコン（`Clip Buddy/TontonCopy/Assets.xcassets/MascotSmall.imageset/mascot-small.png` の写し） | — |

## 公開前にオーナーが決めること・埋めること

- [ ] `tokushoho.html` の **販売URL**：`[要記入]`（App Store のページ URL。審査通過・公開後に確定）
- [ ] **問い合わせ先**：いまは Kakotte と同じ `kakotte.app@gmail.com`。Tonton Copy 専用のアドレスにするか決める（3 ファイルすべてに出てくる）
- [ ] 特商法の **所在地・電話番号**：Kakotte と同じく「請求があれば遅滞なく開示」にしてある。このままでよいか確認
- [ ] 公開してよいか（下の手順はすべて外部への公開。オーナーの確認後に実行）

## 公開手順（GitHub Pages）

> ⚠️ ここから先は外部公開。**オーナーの確認を取ってから**行う。

1. GitHub で新規リポジトリを作成
   - オーナー：`sator0413-sudo`
   - 名前：**`tontoncopy-privacy`**（案）
   - Public（GitHub Pages を無料で使うため）。README などは追加しない
2. このフォルダを push
   ```bash
   cd /Users/sato/Desktop/Claude/tontoncopy-privacy
   git remote add origin https://github.com/sator0413-sudo/tontoncopy-privacy.git
   git branch -M main
   git push -u origin main
   ```
3. リポジトリの **Settings › Pages**
   - Source：**Deploy from a branch**
   - Branch：**`main`** ／ フォルダ **`/ (root)`** → Save
4. 数分待って、下の URL を**実際に開いて**タイトルまで確かめる（`curl -sL <URL> | grep '<title>'` でも可）

## 公開後の URL（案）

| ページ | URL |
|---|---|
| プライバシーポリシー | https://sator0413-sudo.github.io/tontoncopy-privacy/ |
| サポート | https://sator0413-sudo.github.io/tontoncopy-privacy/support.html |
| 特商法表記 | https://sator0413-sudo.github.io/tontoncopy-privacy/tokushoho.html |

App Store Connect に入れるときは、上の URL を**完全一致**で貼り、保存前に実際に踏んで着地を確かめる。

## 内容を変えたら

- アプリの挙動（保存期間、無料の件数、キーボードのフルアクセスの用途、購入）を変えたら、`index.html` と `support.html` を合わせて直す
- 直したページの「最終更新日」を更新する
- 事実の出どころ：`/Users/sato/Desktop/Claude/Clip Buddy/docs/設計メモ_Phase1.md`、`TontonCopy/Store/ProStore.swift`、`TontonCopy/PrivacyInfo.xcprivacy`
