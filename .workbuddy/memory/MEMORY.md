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

⚠️ **本机外网出口依赖 Clash 系统代理**，但**端口会变，务必先实测**（2026-11-05 实测：旧记录的 33210 已失效，当前是 Clash Verge 的 `mixed-port` 7897）。

**实测流程（别凭记忆写端口）：**

```bash
networksetup -getsecurewebproxy Wi-Fi    # 读系统代理配置里的端口
nc -z -G 1 127.0.0.1 <port>              # 端口是否真的在监听
curl --proxy http://127.0.0.1:<port> ...  # 显式走代理重测
```

- `curl` / `git` **不读 macOS 系统代理**，不走代理表现为 `000` 或 `CONNECT 502`，极易误判成「该域名不可达」。
- ⚠️ **Clash Verge 可能没在运行**：配置里写着 7897 但端口没监听时，先 `open -a "Clash Verge"` 再测。
- ⚠️ **Clash Verge 首次启动 GLOBAL 组会选中「剩余流量：50 GB」**（订阅信息占位节点，不是真节点）→ 症状是 baidu 200、github/douyin 全 000，**极易误判为「域名不可达」**。
  **修法**（控制器端口 = `mixed-port + 100`，无 secret）：
  ```bash
  curl -X PUT http://127.0.0.1:9097/proxies/GLOBAL \
    -H "Content-Type: application/json" -d '{"name":"新加坡01aws"}'
  ```
  切到真实节点后 douyin / github / google 全部 200。
- 走代理后**全部 GitHub 域名均可达**，包括此前被误判为「稳定不通」的 `raw.githubusercontent.com`。

Git 已按域名配好代理，日常 `git push/pull` 无需额外设置。

### 平台反爬与自动化（2026-11-05 抖音实测）

- **抖音**：短链 → `www.iesdouyin.com/share/video/<aweme_id>` → `www.douyin.com/video/<aweme_id>`。
  直连返回 JS VM 反爬壳；`aweme/detail` API 需 `a_bogus` 签名（与 cookie/UA 绑定，**外搬无效**）。
  → **唯一可行路径是 bsk 浏览器自动化**，详见 `~/.workbuddy/skills/browser-skill`。
- **视频 CDN 直链可绕过签名**：`document.querySelector('video').currentSrc` 拿到 `v*-webf.douyinvod.com` URL，
  带 `Referer: https://www.douyin.com/` 即可 curl 下载。
- **平台自带「章节要点」= 免费官方大纲**：长视频页面 DOM 里直接有 9 个章节标记 + 时间戳，**读 DOM 就有，不用 ASR**。


## Git 仓库

- 位置：`/Users/wenjuxu/AI_Study/知识库`，分支 `main`
- 远程：`https://github.com/ZiqianStars/knowledge-vault.git`（HTTPS，走 Clash 代理）
- 认证：Personal Access Token，已存入 `osxkeychain`（`acct=ZiqianStars`），推送免密
- 状态：已推送并与远端同步（2026-09-13 验证）
