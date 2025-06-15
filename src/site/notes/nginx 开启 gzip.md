---
{"dg-publish":true,"permalink":"/nginx-gzip/"}
---


```bash
http {
	# gzip
    gzip on;
    gzip_static on;
    gzip_types text/css application/javascript application/json image/svg+xml;
}
```