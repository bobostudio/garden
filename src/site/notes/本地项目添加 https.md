---
{"dg-publish":true,"permalink":"/https/","tags":["gardenEntry"]}
---



window 安装 [mkcert](https://github.com/FiloSottile/mkcert)
`mkcert -install`
在项目下执行 `mkcert localhost`
配置生成的 `key` 和 `cert`

```ts
export default defineConfig(({ command, mode }): UserConfig => {
	return {
		server: {
            https: {
                key: join(__dirname, './src/ssl/localhost-key.pem'),
                cert: join(__dirname, './src/ssl/localhost.pem')
            },
            }
	}
}))
```

配置修改需要重启服务
