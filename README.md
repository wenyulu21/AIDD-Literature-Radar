<div align="center">
  <img src="docs/images/aidd-literature-radar.png" width="112" alt="AIDD 文献雷达 Logo">
  <h1>AIDD 文献雷达 v1.0</h1>
  <p>面向 AI 药物研发研究者的本地文献发现、筛选、去重与阅读管理工具</p>

  <a href="https://github.com/wenyulu21/AIDD-Literature-Radar/releases/download/v1.0/AIDD-Literature-Radar-v1.0-Windows-x64.zip">
    <img src="https://img.shields.io/badge/点击下载-Windows%20v1.0-1677ff?style=for-the-badge&logo=windows&logoColor=white" alt="点击下载 Windows v1.0">
  </a>

  <p>
    <img src="https://img.shields.io/badge/release-v1.0-168bd2?style=flat-square" alt="release v1.0">
    <img src="https://img.shields.io/badge/Windows-10%20%7C%2011-1677ff?style=flat-square&logo=windows&logoColor=white" alt="Windows 10 或 11">
    <img src="https://img.shields.io/badge/license-Proprietary-c0392b?style=flat-square" alt="Proprietary license">
  </p>
</div>

> 无需账号、无需 API Key、无需安装 Python。论文库、中文摘要、收藏和阅读状态全部保存在本机。

> 支持中国大陆网络直接使用。由于部分论文数据源和翻译服务位于境外，使用合规的网络加速工具通常会更快；获取过程中建议保持网络线路稳定。

仅提供 Windows 可执行版本。

![主界面](docs/images/main-interface.png)

## 为什么做这个工具

AIDD 的新研究分散在期刊 online-first / ASAP 页面、会议论文集和预印本平台中。只按题目订阅关键词，容易漏掉那些仅在摘要中说明 AI 方法的论文；搜索条件过宽，又会混入大量普通化学、天然产物药理和材料研究。预印本后来正式发表时，还可能在不同平台重复出现。

AIDD 文献雷达希望把这些工作集中到一个本地工具中：持续获取用户真正关注的来源，保存题目、摘要、作者、DOI 和发表信息，再结合题目与摘要进行 AIDD 初筛、分类和版本关联。用户既能快速浏览 AIDD 候选，也能切换到“全部论文”检查是否存在漏筛。

## 我的日常

获取最新文献→→筛选关注的细分方向→→点击一篇论文查看摘要→→感兴趣的话，双击进入官方网站→→下载论文→→在工具中把这篇论文标为已读（对，下载了就算读过了）→→下一篇……


## 主要功能

- **多来源统一获取**：在同一个界面选择期刊、会议、arXiv 与 bioRxiv；
- **全部论文可回看**：保存已选来源的基础文献记录，可切换查看 AIDD 或全部论文；
- **关注最新发表阶段**：覆盖期刊 ASAP / online-first 元数据，会议按年份获取，预印本按日期获取；
- **AIDD 宽分类**：覆盖分子生成、分子优化、结构基础设计、性质预测、药物靶点、合成规划、基础模型等方向；
- **本地阅读管理**：支持搜索、组合筛选、收藏、已读/未读、本次新增和 CSV 导出；
- **隐私优先**：不需要注册账号，论文库和阅读状态保存在用户自己的电脑上。

## 下载与安装

1. 打开 [最新版本下载页面](https://github.com/wenyulu21/AIDD-Literature-Radar/releases/latest)；
2. 在页面下方找到 **Assets**，下载 `AIDD-Literature-Radar-v1.0-Windows-x64.zip`；
3. 不要下载 `Source code (zip)` 或 `Source code (tar.gz)`，它们是 GitHub 自动生成的页面文件压缩包，不是软件安装包；
4. `AIDD-Literature-Radar-v1.0-Windows-x64.sha256` 只是可选的完整性校验文件，不能运行；
5. 将下载的 ZIP 完整解压到一个可写文件夹，不要直接在压缩包内启动；
6. 双击解压后的 `AIDD文献雷达-v1.0.exe`；
7. 首次运行会在程序旁创建本地数据目录；
8. 点击“获取论文”，选择来源和时间范围后开始获取。

如果 Windows SmartScreen 显示“未知发布者”，请先确认文件来自上述官方发布页；确认无误后点击“更多信息”→“仍要运行”。

## 当前覆盖的来源

### 期刊

默认内置 Advanced Science、Science Advances、Nature Communications、Nature、Science、Cell、Nature Machine Intelligence、Nature Computational Science、Journal of Chemical Information and Modeling、Journal of Medicinal Chemistry 和 Chemical Science。用户也可以在软件中通过ISSN码自行添加或删除期刊。

### 会议

目前支持 NeurIPS、IJCAI、ICML、ICLR、CVPR 和 ACL。会议按年份获取；当年论文尚未公布时可能暂时得到 0 篇，之后仍可重新获取。

### 预印本

目前只支持 arXiv 和 bioRxiv。

## 下载前需要知道

- 这个工具以发现最新研究、整理元数据和阅读摘要为主，不以批量下载论文 PDF 为核心功能；
- 论文出现时间取决于出版社和数据平台何时公开或登记元数据，不能保证论文发布后立即出现；
- AIDD 分类用于文献雷达和初筛，不替代研究者的最终判断，因此软件保留“全部论文”视图；
- 中文摘要依赖在线翻译服务，网络不可达或服务限流时可以稍后重新翻译；

## 使用方法

### 1. 获取论文

点击“获取论文”，选择“获取最新”或“按范围获取”。期刊、会议和预印本可分别选择；执行前软件会再次显示实际来源与范围。

![获取论文](docs/images/fetch-papers.png)

“完整摘要筛选（耗时较长）”会尽量为范围内全部论文补充摘要。普通模式先保存完整的基础记录，只为 AIDD 宽松候选补充摘要。建议勾选完整摘要筛选。

### 2. 搜索和筛选

搜索不区分大小写，并支持单词中的连续片段。可以组合使用论文范围、阅读状态、分类和来源筛选。

![搜索和筛选](docs/images/search-and-filter.png)

### 3. 查看获取记录

获取记录按来源显示已经覆盖的时间范围、最近成功时间和运行结果。期刊、会议、bioRxiv 与 arXiv 分别维护进度。

![获取记录](docs/images/scan-history.png)

## 本地数据与隐私

软件没有注册登录、遥测或云同步。论文元数据、中文摘要、收藏、阅读状态、获取进度和排除记录均保存在程序旁的本地数据库中。升级或移动软件时，请一并保留 `data` 文件夹。

## 使用许可

仅允许下载者将官方发布的可执行版本用于个人、非商业的学习和科研。未经书面许可，不得复制传播、重新发布、销售、出租、修改、反编译、反汇编、逆向工程，或将其用于商业服务。完整条款见 [软件使用许可](LICENSE.txt)。

第三方论文元数据、摘要和原文仍受各来源平台及出版商条款约束。

## 联系方式

如有任何困惑、问题、需求，欢迎联系：[wenyulu21@163.com](mailto:wenyulu21@163.com)，我将尽可能快速回复并解决您的问题。
