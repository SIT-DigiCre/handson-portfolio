# handson-portfolio

| ファイル名            | 説明        | ダウンロード                                                                                          |
| --------------------- | ----------- | ----------------------------------------------------------------------------------------------------- |
| `01-setup.md`         | 環境構築編  | [PDF](https://github.com/SIT-DigiCre/handson-portfolio/releases/latest/download/01-setup.pdf)         |
| `02-introduction.md`  | HTML/CSS 編 | [PDF](https://github.com/SIT-DigiCre/handson-portfolio/releases/latest/download/02-introduction.pdf)  |
| `03-html_practice.md` | 実践編      | [PDF](https://github.com/SIT-DigiCre/handson-portfolio/releases/latest/download/03-html_practice.pdf) |

## トラブルシューティング

### `error: your push would publish a private email address`

git config のメールアドレスを、以下のリンク先で表示されている`~~@users.noreply.github.com`のアドレスに変更してください。

https://github.com/settings/emails

```bash
git config --global user.email "~~@users.noreply.github.com"
```
