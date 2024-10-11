# 環境

このリポジトリは、Apple Silicon搭載のMacで`mlx-community/gemma-2-2b-jpn-it`を使って見るリポジトリです、
`mlx-community/gemma-2-2b-jpn-it`は`google/gemma-2-2b-jpn-it`をAppleシリコン上での実行に対応した機械学習ライブラリMLX
用に変換したものです。

<https://huggingface.co/mlx-community/gemma-2-2b-jpn-it>

※ MacOS 14.0以上推奨です

## 使い方

### 1. uvをインストールする(ない場合)

以下のコマンドを実行して `uv` をインストールしてください：

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### 2. 環境を同期する

`pyproject.toml`と`uv.lock`に従って環境を構築するには、以下のコマンドを実行します：

```bash
uv sync
```

これで、`python 3.12環境とllmの実行に必要なパッケージが.venvインストールされます

### 3. 仮想環境の有効化

以下のコマンドを実行して、仮想環境を有効化します：

```bash
. .venv/bin/activate
```

### 4. 仮想環境の無効化

仮想環境を終了するには、以下のコマンドを実行します：

```bash
deactivate
```

## uv の使用方法

### パッケージの追加

パッケージを追加するには、以下のコマンドを使用します：

```bash
uv add <パッケージ名>
uv add numpy==1.26.4 # ver指定する場合
```

### パッケージの削除

不要なパッケージを削除するには、以下のコマンドを使用します：

```bash
uv remove <パッケージ名>
```

### 環境の同期

uv を使用して環境を最新の状態に同期するには、以下のコマンドを実行します：

```bash
uv sync
```

### Python バージョンの固定

指定したバージョンのPythonを固定するには、以下のコマンドを実行します（例：Python 3.12を使用する場合）：

```bash
uv python pin 3.12
```
