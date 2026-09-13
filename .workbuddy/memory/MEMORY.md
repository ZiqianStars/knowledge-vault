# 项目长期笔记

## 这是什么项目

用户的个人知识库（Obsidian vault），路径 `/Users/wenjuxu/AI_Study/知识库`，同时是 WorkBuddy 的工作区根目录。

## 目录约定

采用 PARA 简化版，**目录名带数字前缀**，改动时需同步更新相关 wikilink：

| 目录 | 用途 |
| --- | --- |
| `01-收件箱` | 新笔记默认落点，不分类 |
| `02-项目` | 有终点的事 |
| `03-领域` | 长期维持的范围 |
| `04-资源` | 知识与素材 |
| `05-归档` | 已完成 / 失效内容 |
| `06-附件` | 图片与文件（附件默认落点） |
| `07-日记` | 每日笔记，格式 `YYYY-MM-DD` |
| `99-模板` | 模板集中存放 |

## 写作约定

- 每条笔记**只讲一个概念**，标题即概念名（便于 `[[概念名]]` 引用）
- 资源类笔记按**概念**命名，不按来源命名
- 正文用中文，frontmatter 字段用英文（`tags` / `created` / `status` / `source`）
- 链接一律用 Obsidian wikilink `[[...]]`，不用 Markdown 链接

## 环境信息

- Obsidian 1.13.7，安装于 `/Applications/Obsidian.app`
- Git `2.50.1 (Apple Git-155)`，随 Xcode CLT 提供（`/usr/bin/git`），无 Homebrew
  - 系统级已配 `credential.helper=osxkeychain`、`init.defaultBranch=main`
  - 用户级身份：`ZiqianStars` / `64132382+ZiqianStars@users.noreply.github.com`
  - 全局代理：`http.https://github.com.proxy = http://127.0.0.1:33210`

### 网络：命令行必须显式走代理（重要）

⚠️ **本机外网出口依赖「艾可云」(Clash) 系统代理** —— HTTP `127.0.0.1:33210`、SOCKS `33211`。而 **`curl` / `git` 不会自动读取 macOS 系统代理**，不走代理时表现为 `000` 或 `CONNECT tunnel failed 502`，极易误判成「该域名不可达」。

走代理后**全部 GitHub 域名均可达**，包括此前被误判为「稳定不通」的 `raw.githubusercontent.com`。

```bash
networksetup -getsecurewebproxy Wi-Fi    # 读代理端口
curl --proxy http://127.0.0.1:33210 ...  # 显式走代理重测
```

Git 已按域名配好代理，日常 `git push/pull` 无需额外设置。

## Git 仓库

- 位置：`/Users/wenjuxu/AI_Study/知识库`，分支 `main`
- 远程：`https://github.com/ZiqianStars/knowledge-vault.git`（HTTPS，走 Clash 代理）
- 认证：Personal Access Token，已存入 `osxkeychain`（`acct=ZiqianStars`），推送免密
- 状态：已推送并与远端同步（2026-09-13 验证）
