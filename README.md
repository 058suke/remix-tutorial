# Remix Tutorial

[Remix Docs](https://remix.run/docs)の[チュートリアル](https://remix.run/docs/en/main/start/tutorial)をやってみた。


# チュートリアル メモ

## 開発サーバーを立ち上げる

```sh
npm run dev
```

* `development`モードでアプリケーションを立ち上げる（ホットリロード対応）
* [http://localhost:5173](http://localhost:5173)にブラウザでアクセスできる。


## スタイルシートの読み込み

```typescript
import type { LinksFunction } from "@remix-run/node";

import appStyleHref from "./app.css?url";

export const links: LinksFunction = () => [
  { rel: "stylesheet", href: appStyleHref },
];
```

* `LinksFunction`を用いると`<link>`Elementを追加できる。