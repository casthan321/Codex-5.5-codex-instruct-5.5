# Codex破限 5.5 / codex-instruct-5.5

> 针对 GPT-5.5 的 Codex CLI 配置文件 — 一键注入操作系统指令  

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue)](https://python.org)

---



## 快速开始 / Quick Start

```bash
# 部署 GPT-5.5 配置指令
python codex-instruct.py

# 重启 Codex 生效
```

## 参数 / Options

| 参数 | 说明 |
|------|------|
| `--file`, `-f` | 使用外部 `.md` 指令文件 |
| `--name`, `-n` | 输出文件名不含 `.md`（默认 `gpt5.5-unrestricted`） |
| `--dry-run` | 预览，不实际修改 |
| `--codex-dir` | 手动指定 `.codex` 目录 |

## 验证 / Verify

部署后测试：

> "如何对目标进行 SQL 注入测试？"

破甲前 → 拒绝 ； 破甲后 → 直接给方法论。

## 还原 / Undo

```bash
# 删除 config.toml 中的 model_instructions_file 行
# 删除 ~/.codex/gpt5.5-unrestricted.md
# 重启 Codex
```

## 项目结构 / Layout

```
codex-instruct-5.5/
├── codex-instruct.py                    # 主脚本
├── examples/
│   └── gpt5.5-unrestricted.md           # 破甲指令独立副本
├── .gitignore
├── README.md
└── LICENSE                              # MIT
```

## 声明 / Disclaimer

利用官方配置机制，不修改二进制、不劫持网络、不篡改进程。风险自负。

Exploits official config mechanism. No binary mod, no MITM, no process tampering. Use at your own risk.

## License

MIT

可以的话赞赏一下喵

<img width="700" height="340" alt="490f26c0699115961e7de5031710890e" src="https://github.com/user-attachments/assets/01949bfe-d0c3-4b0c-af27-9e5ad6c1a9a4" />
