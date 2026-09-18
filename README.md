# skill-license-fixtures

MCP Portal（社内スキルポータル）のライセンス判定を確かめるための fixture 置き場です。
判定の確認にだけ使う空のスキルが入っています。

| フォルダ | 置いたもの | 期待する判定 |
|---|---|---|
| `skills/mit-file` | LICENSE に MIT | 許容（ライセンスファイル） |
| `skills/frontmatter-only` | SKILL.md に `license: MIT` | 許容（frontmatter）・注記が同梱される |
| `skills/gpl-only` | LICENSE に GPL-3.0 | 許容外で投稿できない |
| `skills/no-license` | 表記なし | 投稿できない |
| `skills/readme-only` | README にだけ MIT | 運営の確認待ち |
| `skills/conflict` | LICENSE は Apache-2.0・frontmatter は MIT | 運営の確認待ち（食い違い） |
| `apache-tree/skills/inherits` | 上位フォルダに Apache-2.0 の LICENSE | 許容（上位フォルダから取り込む） |

リポジトリのルートには LICENSE を置いていません。置くと全フォルダが継いでしまい、表記なしの fixture が成立しません。
