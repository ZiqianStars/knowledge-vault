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
- ⚠️ **网络可达性会波动，用前必须实测，不要依赖历史结论**。注意：`curl -sI` 探测裸域名偶尔会误报，带真实路径测更可靠
  - 2026-09-13 晚实测：`github.com` 200 ✅、`codeload.github.com` 301 ✅、`api.github.com` 200 ✅、`ghcr.io` 301 ✅、`formulae.brew.sh` 200 ✅
  - **`raw.githubusercontent.com` 两次实测均为 000 ❌**，是本机唯一稳定不通的 GitHub 域名
  - 2026-09-11 曾出现 `github.com` 返回 502 / 000，属**临时**拦截，同日即恢复 —— 不要据此下长期结论
  - GitHub 的 git 操作已实测可行：`git ls-remote https://github.com/Homebrew/brew` 成功返回 commit 哈希
  - 国内镜像可达：USTC / 清华 TUNA / 腾讯云 / 阿里云
- Homebrew 安装注意：官方脚本（`raw.githubusercontent.com/Homebrew/install/HEAD/install.sh`）**下载不到**，但因 `github.com` 可用，可改为手动 `git clone https://github.com/Homebrew/brew` 完成安装
- Git `2.50.1 (Apple Git-155)`，随 Xcode CLT 提供（`/usr/bin/git`），无 Homebrew
  - 系统级已配 `credential.helper=osxkeychain`、`init.defaultBranch=main`
  - 用户级身份需配置（`~/.gitconfig`）
