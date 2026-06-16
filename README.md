# Sbx Native

本仓库提供不同运行环境的 sing-box native 启动器，用于部署 VMess Ws + Argo、VLESS Reality、Hysteria2、TUIC、AnyTLS、SOCKS5 等代理，只有主进程，没有子进程。

请选择对应环境查看说明：

| 环境 | 说明文档 | 入口文件 |
| --- | --- | --- |
| Java | [JAVA.md](JAVA.md) | [java/src/main/java/dev/sbxnative/App.java](java/src/main/java/dev/sbxnative/App.java) |
| Node.js | [NODE.md](NODE.md) | [nodejs/index.js](nodejs/index.js) |
| Python | [PYTHON.md](PYTHON.md) | [python/app.py](python/app.py) |

## 目录结构

```text
.
├── java/
│   ├── pom.xml
│   └── src/main/java/dev/sbxnative/App.java
├── nodejs/
│   ├── index.js
│   └── package.json
├── python/
│   ├── app.py
│   └── requirements.txt
├── JAVA.md
├── NODE.md
├── PYTHON.md
└── README.md
```

## 简要说明

- 请先确认端口在部署平台开放并未被占用。
- Reality 会首次生成并持久化 `keypair.properties`，后续重启会复用同一对 key。
- HY2、TUIC、AnyTLS 会使用自签证书，客户端需要开启 `allow_insecure` 或等效选项。
- 请在符合当地法律法规和服务商规则的前提下使用。
