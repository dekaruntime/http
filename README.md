# `@deka/http`

HTTP/1.1 client in DekaScript on `@deka/tcp` and `@deka/tls`. There is no `http` host kind.

```ds
import { get, post, request } from "http"

const r = get("https://example.com/")
print(match (r) {
  Ok(resp) => resp.status,
  Err(e) => e
})
```

v1 is HTTP/1.1 only: `get`, `post`, `request`. Chunked transfer encoding, HTTP/2, cookies, and WebSockets are not in this package yet. Outbound hosts are gated by `deka.json` `security.allow.net`.
