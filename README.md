# explore-it

Claude Code の Agent Skill。エージェントに「探索的テスト」をさせる。

事前に書いたテストケースを消化させるのではなく、実物を触りながら観点を連鎖的に増やしていく。
見つけたバグは横展開し、仕様の曖昧さはエッジを突いて炙り出す。
中間成果物のテストチャーターは、探索しながら育てる。

成果は「バグの発見」と「曖昧な仕様の発見」。

## インストール

```bash
git clone https://github.com/yodakeisuke/skill-explore-it.git ~/.claude/skills/explore-it
```

プロジェクト単位で使うなら、リポジトリ内の `.claude/skills/explore-it` に置く。

## 使い方

```
/explore-it ローカルで起動している画面の、今回追加した絞り込み機能を探索して
```

`disable-model-invocation: true` なので自動では発火しない。明示的に呼ぶ。

実物を操作する手段（ブラウザ操作、CLI、API を叩くツールなど）は、このスキルには含まれない。セッション側で用意しておく。

中身は [SKILL.md](SKILL.md) がすべて。
