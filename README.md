# LTスライド作成Skill

- [作例](https://kakira9618.github.io/vector_based_ai_development/)
- [作例のリポジトリ](https://github.com/kakira9618/vector_based_ai_development)

markdown に骨子を書いて、AIに「main.md を元にLTスライド作って」など指示することで、簡単にLT向けのスライドが作れます。

## Claude Code Skill としての使い方

`.claude/skills/lt-slides/` に Claude Code の Skill があります。
他のプロジェクトにコピーして使えば、同じ高橋メソッド風の LT スライドが簡単に作れます。

### セットアップ

プロジェクト単位で使いたいときは、そのプロジェクトの直下に skill ディレクトリをコピーします：

```
mkdir -p <new-project>/.claude/skills
cp -r .claude/skills/lt-slides <new-project>/.claude/skills/
```

グローバルに置いておきたいときは `~/.claude/skills/` に置きます：

```
mkdir -p ~/.claude/skills
cp -r .claude/skills/lt-slides ~/.claude/skills/
```

### プロジェクトの初期化

まっさらなプロジェクトから始める場合は、claude code に初期化をお願いしましょう：

```
LT スライドのプロジェクトを初期化して
```

`slide/` や `slide/resources/` ディレクトリ、`main.md` の雛形、`package.json` などを用意してくれます。

### スライドの生成

あとは通常どおり main.md を書いて、claude code にお願いすればスライドが生成されます：

```
main.md からスライド作って
```

### スライドの追従・PDF 化

追従や pdf 化も、同じセッションで普通に日本語で依頼するだけで skill が動きます：

```
main.md を更新したので追従して欲しい
```

```
スライドを PDF にして
```

詳しい仕様は `.claude/skills/lt-slides/SKILL.md` を見てください。
