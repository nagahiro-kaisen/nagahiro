# メニュー変更ガイド（Mac）

このページの料理名・価格・説明・表示写真は、\`menu-data.csv\` で管理します。ホームページ本体（\`index.html\`）は変更しません。

## 初回の準備
1. Macに無料の **GitHub Desktop** をインストールし、GitHubにログインします。
2. GitHub Desktopで **File → Clone repository** を選び、\`nagahiro-kaisen/nagahiro\` を選択してMacに保存します。
3. 保存したフォルダ内の \ `menu-data.csv` をNumbersで開きます。

## 料理名・価格を変更する
- 料理名：\`name\` 列
- 説明：\`description\` 列
- 通常価格（税込）：\`price\` 列（例：2420）
- 土日祝価格（税込）：\`holiday_price\` 列（設定しない場合は空欄）
- 写真：\`image\` 列（\`assets\` フォルダ内の画像ファイル名）
- 表示順：\`sort\` 列（1、2、3…）

## 新しい料理を追加する
同じ分類の行をNumbersで複製して、料理名・説明・価格・写真・表示順を変更します。
- \ `category\` は \ `lunch\`（ランチ）、\`night\`（夜の御膳）、\`course\`（コース）
- \ `type\` は通常の料理なら \ `item\`
- 単品・ドリンクの紙メニュー画像を追加する場合は \ `type\` を \ `sheet\` にします。

## 公開する
1. Numbersで編集後、CSV形式（UTF-8）で \ `menu-data.csv\` に保存します。通常はカンマ区切りのCSVを選びます。
2. GitHub Desktopを開くと変更が表示されます。
3. Summaryに「メニュー更新」と入力し、**Commit to main** を押します。
4. **Push origin** を押します。サイトに反映されます。

## 注意
- 価格は税込の数字だけを入力します（例：2420）。「円」や「税込」は入力しません。
- 写真ファイル名は、すでに \ `assets\` フォルダにあるものを指定してください。
- \ `type\`、\ `category\`、列の見出しは消したり変更したりしないでください。
