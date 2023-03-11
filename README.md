# template.deno.land

Deno のテンプレートリポジトリ

---

[最初に Deno をインストールしましょう。](https://github.com/denoland/deno#install)

----

Deno には `deno task` という機能があります。

Node.js の `script` のようなものです。

```json
  "tasks": {
    "start": "deno run src/mod.ts",
    "dev": "deno run --watch src/mod.ts",
    "compile": "deno compile --output=./target/app src/mod.ts",
    "fmt": "deno fmt --watch src/",
    "fmt:check": "deno fmt --check",
    "lint": "deno lint",
    "lint:json": "deno lint --json",
    "cache": "deno cache deps.ts"
  }
```

- `start`: `deno task start`
  - `src/mod.ts` を実行します。
- `dev`: `deno task dev`
  - `src/mod.ts` を開発モードで実行します。
  - ファイルが更新されると自動でリフレッシュされます。
- `compile`: `deno task compile`
  - `./target` 配下に実行可能ファイルを生成します。
- `fmt`: `deno task fmt`
  - **deno fmt** を実行します。
  - ファイルが更新されると自動でリフレッシュされます。
- `fmt:check`: `deno task fmt:check`
  - **deno fmt** をチェックモードで実行します。
- `lint`: `deno task lint`
  - **deno lint** を実行します。
- `lint:json`: `deno task lint:json`
  - **deno lint** を実行します。
  - lintの結果をJSON方式で吐き出します。
- `cache`: `deno task cache`
  - `deps.ts` の依存関係をキャッシュします。
