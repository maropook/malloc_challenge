# malloc_challenge

[![Cloud Shellで開く](https://gstatic.com/cloudssh/images/open-btn.svg)](https://shell.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https%3A%2F%2Fgithub.com%2Fhikalium%2Fmalloc_challenge&cloudshell_open_in_editor=malloc.c&cloudshell_workspace=malloc)

- `malloc`はこの課題で使用するメモリ割り当て関数です。詳細な仕様と実装についてはこのドキュメントおよび[malloc/malloc.c](./malloc/malloc.c)を参照してください。
- `visualizer/`ディレクトリには、メモリ割り当てのトレースを可視化するツールが含まれています。

## 課題内容

[malloc.c](./malloc/malloc.c)において、メモリ割り当ての効率性と速度を向上させる改良版のメモリ管理ロジックを実装してください。

## ベンチマークのビルドと実行方法

```
# このリポジトリをクローンする
git clone https://github.com/hikalium/malloc_challenge.git

# mallocディレクトリに移動
cd malloc_challenge
cd malloc

# ビルド実行
make

# スコアボード用ベンチマークの実行
make run

# トレース用の小規模ベンチマーク実行（スコアボード用ではなく、可視化およびデバッグ目的）
make run_trace
```

上記のコマンドが動作しない場合は、以下のパッケージがインストールされていることを確認してください。
```
# Debian系OSの場合
sudo apt install make clang
```

別の方法として、以下のコマンドを直接実行することで課題のビルドと実行が可能です：

```
gcc -Wall -O3 -lm -o malloc_challenge.bin main.c malloc.c simple_malloc.c
./malloc_challenge.bin
```

## 謝辞

本課題の実装は[xharaken氏のmalloc_challenge.c](https://github.com/xharaken/step2/blob/master/malloc_challenge.c)を基にしています。haraken-san、ありがとうございました！
