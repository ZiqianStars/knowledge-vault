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
- 该机器可访问的域名不含 `github.com`、`raw.githubusercontent.com`（CONNECT 返回 502 / 000），但 `api.github.com`、`*.githubusercontent.com`、`ghcr.io`、`formulae.brew.sh` 可达
  - 国内镜像可达：`mirrors.ustc.edu.cn` / `mirrors.tuna.tsinghua.edu.cn` / `mirrors.cloud.tencent.com` / `mirrors.aliyun.com`（已验证 USTC 的 `brew.git` 可 `git ls-remote`）
  - 若需安装 Homebrew，**标准安装脚本会卡在 `git clone github.com/Homebrew/brew` 这一步**，必须走国内镜像
- Git `2.50.1 (Apple Git-155)`，随 Xcode CLT 提供（`/usr/bin/git`），无 Homebrew
  - 系统级已配 `credential.helper=osxkeychain`、`init.defaultBranch=main`
  - 用户级身份需配置（`~/.gitconfig`）
