# omnivla_gazebo_logs

[omnivla_gazebo](https://github.com/mamoru1126/omnivla_gazebo) の走行ログ・学習ログ置き場 (本体リポジトリを軽く保つため分離)。

- `nav/<日時>/` : navigator の走行ログ (`steps.csv`, `events.log`, `summary.json`, `meta.json`, 画像)。
  解析は本体で `python3 tools/plot_nav_log.py ../omnivla_gazebo_logs/nav/<日時>`
- それ以外 : Docker ビルド・学習などのログ (2026-10 の試行錯誤時のもの)

追加するとき (本体リポジトリの隣にクローンしてある前提):
```bash
cp -r ../omnivla_gazebo/log/nav/<日時> nav/
git add nav/<日時> && git commit -m "nav log <日時>" && git push
```
