# Xget

**[English](README.en.md)**

[![Chromium Extension](https://img.shields.io/badge/Chromium%20Extension-4285F4?logo=googlechrome&logoColor=white)](#-生态系统集成)
[![Cloudflare Workers](https://img.shields.io/badge/Cloudflare%20Workers-F38020?&logo=cloudflare&logoColor=white)](#cloudflare-workers-一键部署)

[![GitHub](https://img.shields.io/badge/GitHub-181717?&logo=github&logoColor=white)](#github)
[![GitLab](https://img.shields.io/badge/GitLab-FC6D26?&logo=gitlab&logoColor=white)](#gitlab)
[![Gitea](https://img.shields.io/badge/Gitea-609926?&logo=gitea&logoColor=white)](#gitea)
[![Codeberg](https://img.shields.io/badge/Codeberg-2185D0?&logo=codeberg&logoColor=white)](#codeberg)
[![SourceForge](https://img.shields.io/badge/SourceForge-FF6600?&logo=sourceforge&logoColor=white)](#sourceforge)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?&logo=huggingface&logoColor=white)](#作为-hugging-face-镜像)
[![npm](https://img.shields.io/badge/npm-CB3837?logo=npm&logoColor=white)](#npm-包管理加速)
[![PyPI](https://img.shields.io/badge/PyPI-3775A9?logo=pypi&logoColor=white)](#python-包管理加速)
[![conda](https://img.shields.io/badge/conda-44A833?logo=anaconda&logoColor=white)](#conda-包管理加速)
[![Maven](https://img.shields.io/badge/Maven-C71A36?logo=apachemaven&logoColor=white)](#maven-包管理加速)
[![Gradle](https://img.shields.io/badge/Gradle-02303A?logo=gradle&logoColor=white)](#gradle-包管理加速)
[![RubyGems](https://img.shields.io/badge/RubyGems-CC342D?logo=rubygems&logoColor=white)](#ruby-包管理加速)
[![Go](https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white)](#go-模块加速)
[![NuGet](https://img.shields.io/badge/NuGet-004880?logo=nuget&logoColor=white)](#nuget-包管理加速)
[![Packagist](https://img.shields.io/badge/Packagist-F28D1A?logo=packagist&logoColor=white)](#php-包管理加速)
[![Debian](https://img.shields.io/badge/Debian-A81D33?logo=debian&logoColor=white)](#linux-发行版加速)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?logo=ubuntu&logoColor=white)](#linux-发行版加速)
[![Fedora](https://img.shields.io/badge/Fedora-294172?logo=fedora&logoColor=white)](#linux-发行版加速)
[![Rocky Linux](https://img.shields.io/badge/Rocky%20Linux-10B981?logo=rockylinux&logoColor=white)](#linux-发行版加速)
[![Arch Linux](https://img.shields.io/badge/Arch%20Linux-1793D1?logo=archlinux&logoColor=white)](#linux-发行版加速)
[![arXiv](https://img.shields.io/badge/arXiv-B31B1B?logo=arxiv&logoColor=white)](#学术资源加速)
[![容器注册表](https://img.shields.io/badge/容器注册表-%23007EC6.svg?logo=docker&logoColor=white)](#容器注册表)

超高性能、安全的一站式开源资源获取加速引擎。其性能远超传统加速器，为您提供跨多个平台的统一高效的下载体验，涵盖代码储存库、包管理、容器镜像、模型及数据集等。

## 🎯 快速使用

**公共实例：**[**`xget.xi-xu.me`**](https://xget.xi-xu.me) - 开箱即用，无需部署！

> **⚡ 立即体验极速下载**：无需注册，无需配置，直接使用即可感受飞一般的下载速度！

## 🌟 核心优势 - 为什么选择 Xget？

### ⚡ 极速性能 - 突破传统加速器瓶颈

- **⚡ 毫秒级响应**：Cloudflare 全球 330+ 边缘节点，平均响应时间 < 50ms
- **🌐 HTTP/3 极速协议**：启用最新 HTTP/3 协议，连接延迟降低 40%，传输速度提升 30%
- **📦 智能多重压缩**：gzip、deflate、brotli 三重压缩算法，传输效率提升 60%
- **🔗 零延迟预连接**：连接预热和保持活跃，消除握手开销，实现秒级响应
- **⚡ 并行分片下载**：完整支持 HTTP Range 请求，多线程下载速度倍增
- **🎯 智能路由优化**：自动选择最优传输路径，避开网络拥堵节点

### 🌐 多平台深度集成

- **一站式多平台支持**：统一支持代码存储库、包管理器、容器注册表、模型与数据集托管平台的高速下载
- **智能识别与转换**：自动识别平台前缀并转换为目标平台的正确 URL 结构
- **一致的加速体验**：无论文件类型或来源，均可享受统一且稳定的极速下载服务

### 🔒 企业级安全保障

- **多层安全标头**：
  - `Strict-Transport-Security`：强制 HTTPS 传输，预防中间人攻击
  - `X-Frame-Options: DENY`：防止点击劫持攻击
  - `X-XSS-Protection`：内置 XSS 防护机制
  - `Content-Security-Policy`：严格的内容安全策略
  - `Referrer-Policy`：控制引用信息泄露
- **请求验证机制**：
  - HTTP 方法白名单：常规请求限制为 GET/HEAD，Git 操作动态允许 POST
  - 路径长度限制：防止超长 URL 攻击（最大 2048 字符）
  - 输入清理：防止路径遍历和注入攻击
- **超时保护**：30 秒请求超时，防止资源耗尽和恶意请求

### 🚀 现代架构与可靠性

- **智能重试机制**：
  - 最大 3 次重试，线性延迟策略（1000ms × 重试次数）
  - 自动错误恢复，提高下载成功率
  - 超时检测和中断处理
- **高效缓存策略**：
  - 1800 秒（30 分钟）默认缓存时长，显著减少源站压力
  - Git 操作跳过缓存，确保实时性
  - 基于 Cloudflare Cache API 的边缘缓存
- **性能监控系统**：
  - 内置 `PerformanceMonitor` 类，实时追踪请求各阶段耗时
  - 通过 `X-Performance-Metrics` 响应头提供详细性能数据
  - 支持缓存命中率统计和优化建议

### 🎯 Git 协议完全兼容

- **智能协议检测**：
  - 自动识别 Git 特定端点（`/info/refs`、`/git-upload-pack`、`/git-receive-pack`）
  - 检测 Git 客户端 User-Agent 模式
  - 支持 `service=git-upload-pack` 等查询参数
- **完整操作支持**：
  - `git clone`：完整存储库克隆，支持浅克隆和分支指定
  - `git push`：代码推送和分支管理
  - `git pull/fetch`：增量更新和远程同步
  - `git submodule`：子模块递归克隆
- **协议优化**：
  - 保持 Git 专用请求头和认证信息
  - 智能 User-Agent 处理（默认 `git/2.34.1`）
  - 支持 Git LFS 大文件传输

### 📱 生态系统集成

- **专用浏览器扩展**：[Xget for Chromium](https://github.com/xixu-me/Xget-for-Chromium) 提供无缝体验
  - 自动链接重定向，无需手动修改 URL
  - 支持自定义 Xget 实例域名
  - 多平台偏好设置和黑白名单管理
  - 本地处理，确保隐私安全
- **下载工具兼容**：完美支持 wget、cURL、aria2、IDM 等主流下载工具
- **CI/CD 集成**：可直接在 GitHub Actions、GitLab CI 等环境中使用

## 📖 链接转换规则

使用公共实例 [**`xget.xi-xu.me`**](https://xget.xi-xu.me) 或你自己部署的实例，只需简单替换域名并添加平台前缀：

### 转换格式

| 平台 | 平台前缀 | 原始链接格式 | 加速链接格式 |
|------|----------|--------------|--------------|
| GitHub | `gh` | `https://github.com/...` | `https://xget.xi-xu.me/gh/...` |
| GitLab | `gl` | `https://gitlab.com/...` | `https://xget.xi-xu.me/gl/...` |
| Gitea | `gitea` | `https://gitea.com/...` | `https://xget.xi-xu.me/gitea/...` |
| Codeberg | `codeberg` | `https://codeberg.org/...` | `https://xget.xi-xu.me/codeberg/...` |
| SourceForge | `sf` | `https://sourceforge.net/...` | `https://xget.xi-xu.me/sf/...` |
| Hugging Face | `hf` | `https://huggingface.co/...` | `https://xget.xi-xu.me/hf/...` |
| npm | `npm` | `https://registry.npmjs.org/...` | `https://xget.xi-xu.me/npm/...` |
| PyPI | `pypi` | `https://pypi.org/...` | `https://xget.xi-xu.me/pypi/...` |
| conda | `conda` | `https://repo.anaconda.com/...` 和 `https://conda.anaconda.org/...` | `https://xget.xi-xu.me/conda/...` 和 `https://xget.xi-xu.me/conda/community/...` |
| Maven | `maven` | `https://repo1.maven.org/...` | `https://xget.xi-xu.me/maven/...` |
| Gradle | `gradle` | `https://plugins.gradle.org/...` | `https://xget.xi-xu.me/gradle/...` |
| RubyGems | `rubygems` | `https://rubygems.org/...` | `https://xget.xi-xu.me/rubygems/...` |
| Go 模块 | `golang` | `https://proxy.golang.org/...` | `https://xget.xi-xu.me/golang/...` |
| NuGet | `nuget` | `https://api.nuget.org/...` | `https://xget.xi-xu.me/nuget/...` |
| Packagist | `packagist` | `https://repo.packagist.org/...` | `https://xget.xi-xu.me/packagist/...` |
| Debian | `debian` | `https://deb.debian.org/...` | `https://xget.xi-xu.me/debian/...` |
| Ubuntu | `ubuntu` | `https://archive.ubuntu.com/...` | `https://xget.xi-xu.me/ubuntu/...` |
| Fedora | `fedora` | `https://dl.fedoraproject.org/...` | `https://xget.xi-xu.me/fedora/...` |
| Rocky Linux | `rocky` | `https://download.rockylinux.org/...` | `https://xget.xi-xu.me/rocky/...` |
| Arch Linux | `arch` | `https://geo.mirror.pkgbuild.com/...` | `https://xget.xi-xu.me/arch/...` |
| arXiv | `arxiv` | `https://arxiv.org/...` | `https://xget.xi-xu.me/arxiv/...` |
| 容器注册表 | `cr` | 见[容器注册表](#容器注册表) | 见[容器注册表](#容器注册表) |

### 各平台转换示例

#### GitHub

```url
# 原始链接
https://github.com/microsoft/vscode/archive/refs/heads/main.zip

# 转换后（添加 gh 前缀）
https://xget.xi-xu.me/gh/microsoft/vscode/archive/refs/heads/main.zip
```

#### GitLab

```url
# 原始链接
https://gitlab.com/gitlab-org/gitlab/-/archive/master/gitlab-master.zip

# 转换后（添加 gl 前缀）
https://xget.xi-xu.me/gl/gitlab-org/gitlab/-/archive/master/gitlab-master.zip
```

#### Gitea

```url
# 原始链接
https://gitea.com/gitea/gitea/archive/main.zip

# 转换后（添加 gitea 前缀）
https://xget.xi-xu.me/gitea/gitea/gitea/archive/main.zip
```

#### Codeberg

```url
# 原始链接
https://codeberg.org/forgejo/forgejo/archive/forgejo.zip

# 转换后（添加 codeberg 前缀）
https://xget.xi-xu.me/codeberg/forgejo/forgejo/archive/forgejo.zip
```

#### SourceForge

```url
# 原始链接
https://sourceforge.net/projects/sevenzip/files/7-Zip/23.01/7z2301-x64.exe/download

# 转换后（添加 sf 前缀）
https://xget.xi-xu.me/sf/projects/sevenzip/files/7-Zip/23.01/7z2301-x64.exe/download
```

#### Hugging Face

```url
# 模型文件原始链接
https://huggingface.co/microsoft/DialoGPT-medium/resolve/main/pytorch_model.bin

# 转换后（添加 hf 前缀）
https://xget.xi-xu.me/hf/microsoft/DialoGPT-medium/resolve/main/pytorch_model.bin

# 数据集文件原始链接
https://huggingface.co/datasets/rajpurkar/squad/resolve/main/plain_text/train-00000-of-00001.parquet

# 转换后（添加 hf 前缀）
https://xget.xi-xu.me/hf/datasets/rajpurkar/squad/resolve/main/plain_text/train-00000-of-00001.parquet
```

#### npm

```url
# 包文件原始链接
https://registry.npmjs.org/react/-/react-18.2.0.tgz

# 转换后（添加 npm 前缀）
https://xget.xi-xu.me/npm/react/-/react-18.2.0.tgz

# 包元数据原始链接
https://registry.npmjs.org/lodash

# 转换后（添加 npm 前缀）
https://xget.xi-xu.me/npm/lodash
```

#### PyPI

```url
# Python 包文件原始链接
https://pypi.org/packages/source/r/requests/requests-2.31.0.tar.gz

# 转换后（添加 pypi 前缀）
https://xget.xi-xu.me/pypi/packages/source/r/requests/requests-2.31.0.tar.gz

# Wheel 文件原始链接
https://pypi.org/packages/py3/r/requests/requests-2.31.0-py3-none-any.whl

# 转换后（添加 pypi 前缀）
https://xget.xi-xu.me/pypi/packages/py3/r/requests/requests-2.31.0-py3-none-any.whl
```

#### conda

```url
# 默认频道包文件原始链接
https://repo.anaconda.com/pkgs/main/linux-64/numpy-1.24.3-py311h08b1b3b_1.conda

# 转换后（添加 conda 前缀）
https://xget.xi-xu.me/conda/pkgs/main/linux-64/numpy-1.24.3-py311h08b1b3b_1.conda

# 社区频道元数据原始链接
https://conda.anaconda.org/conda-forge/linux-64/repodata.json

# 转换后（添加 conda/community 前缀）
https://xget.xi-xu.me/conda/community/conda-forge/linux-64/repodata.json
```

#### Maven

```url
# Maven 中央仓库 JAR 文件原始链接
https://repo1.maven.org/maven2/org/springframework/spring-core/5.3.21/spring-core-5.3.21.jar

# 转换后（添加 maven 前缀）
https://xget.xi-xu.me/maven/maven2/org/springframework/spring-core/5.3.21/spring-core-5.3.21.jar

# Maven 元数据原始链接
https://repo1.maven.org/maven2/org/apache/commons/commons-lang3/maven-metadata.xml

# 转换后（添加 maven 前缀）
https://xget.xi-xu.me/maven/maven2/org/apache/commons/commons-lang3/maven-metadata.xml
```

#### Gradle

```url
# Gradle 插件门户 JAR 文件原始链接
https://plugins.gradle.org/m2/org/gradle/gradle-enterprise-gradle-plugin/3.13.4/gradle-enterprise-gradle-plugin-3.13.4.jar

# 转换后（添加 gradle 前缀）
https://xget.xi-xu.me/gradle/m2/org/gradle/gradle-enterprise-gradle-plugin/3.13.4/gradle-enterprise-gradle-plugin-3.13.4.jar

# Gradle 插件元数据原始链接
https://plugins.gradle.org/api/gradle/7.6/plugin/use/org.springframework.boot

# 转换后（添加 gradle 前缀）
https://xget.xi-xu.me/gradle/api/gradle/7.6/plugin/use/org.springframework.boot
```

#### RubyGems

```url
# RubyGems 包文件原始链接
https://rubygems.org/gems/rails-7.0.4.gem

# 转换后（添加 rubygems 前缀）
https://xget.xi-xu.me/rubygems/gems/rails-7.0.4.gem

# RubyGems API 原始链接
https://rubygems.org/api/v1/gems/nokogiri.json

# 转换后（添加 rubygems 前缀）
https://xget.xi-xu.me/rubygems/api/v1/gems/nokogiri.json
```

#### Go 模块

```url
# Go 模块代理原始链接
https://proxy.golang.org/github.com/gin-gonic/gin/@v/v1.9.1.zip

# 转换后（添加 golang 前缀）
https://xget.xi-xu.me/golang/github.com/gin-gonic/gin/@v/v1.9.1.zip

# Go 模块信息原始链接
https://proxy.golang.org/github.com/gorilla/mux/@v/list

# 转换后（添加 golang 前缀）
https://xget.xi-xu.me/golang/github.com/gorilla/mux/@v/list
```

#### NuGet

```url
# NuGet 包下载原始链接
https://api.nuget.org/v3-flatcontainer/newtonsoft.json/13.0.3/newtonsoft.json.13.0.3.nupkg

# 转换后（添加 nuget 前缀）
https://xget.xi-xu.me/nuget/v3-flatcontainer/newtonsoft.json/13.0.3/newtonsoft.json.13.0.3.nupkg

# NuGet 包元数据原始链接
https://api.nuget.org/v3/registration5-semver1/microsoft.aspnetcore.app/index.json

# 转换后（添加 nuget 前缀）
https://xget.xi-xu.me/nuget/v3/registration5-semver1/microsoft.aspnetcore.app/index.json
```

#### Packagist

```url
# Packagist 包元数据原始链接
https://repo.packagist.org/p2/symfony/console.json

# 转换后（添加 packagist 前缀）
https://xget.xi-xu.me/packagist/p2/symfony/console.json

# Packagist 包列表原始链接
https://repo.packagist.org/packages/list.json

# 转换后（添加 packagist 前缀）
https://xget.xi-xu.me/packagist/packages/list.json
```

#### Linux 发行版

```url
# Debian 包原始链接
https://deb.debian.org/debian/pool/main/c/curl/curl_7.88.1-10+deb12u4_amd64.deb

# 转换后（添加 debian 前缀）
https://xget.xi-xu.me/debian/debian/pool/main/c/curl/curl_7.88.1-10+deb12u4_amd64.deb

# Ubuntu 包原始链接
https://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.34.1-1ubuntu1.9_amd64.deb

# 转换后（添加 ubuntu 前缀）
https://xget.xi-xu.me/ubuntu/ubuntu/pool/main/g/git/git_2.34.1-1ubuntu1.9_amd64.deb

# Fedora 包原始链接
https://dl.fedoraproject.org/pub/fedora/linux/releases/39/Everything/x86_64/os/Packages/n/nginx-1.24.0-1.fc39.x86_64.rpm

# 转换后（添加 fedora 前缀）
https://xget.xi-xu.me/fedora/pub/fedora/linux/releases/39/Everything/x86_64/os/Packages/n/nginx-1.24.0-1.fc39.x86_64.rpm

# Rocky Linux 包原始链接
https://download.rockylinux.org/pub/rocky/9/BaseOS/x86_64/os/Packages/b/bash-5.1.8-6.el9.x86_64.rpm

# 转换后（添加 rocky 前缀）
https://xget.xi-xu.me/rocky/pub/rocky/9/BaseOS/x86_64/os/Packages/b/bash-5.1.8-6.el9.x86_64.rpm

# Arch Linux 包原始链接
https://geo.mirror.pkgbuild.com/core/os/x86_64/linux-6.6.10.arch1-1-x86_64.pkg.tar.zst

# 转换后（添加 arch 前缀）
https://xget.xi-xu.me/arch/core/os/x86_64/linux-6.6.10.arch1-1-x86_64.pkg.tar.zst
```

#### arXiv

```url
# arXiv 论文 PDF 原始链接
https://arxiv.org/pdf/2301.07041.pdf

# 转换后（添加 arxiv 前缀）
https://xget.xi-xu.me/arxiv/pdf/2301.07041.pdf

# arXiv 论文源码原始链接
https://arxiv.org/e-print/2301.07041

# 转换后（添加 arxiv 前缀）
https://xget.xi-xu.me/arxiv/e-print/2301.07041
```

#### 容器注册表

Xget 支持多个容器注册表，使用 `cr/[容器注册表前缀]` 格式：

| 容器注册表 | 容器注册表前缀 | 原始链接格式 | 加速链接格式 |
|----------|------|--------------|--------------|
| Quay.io | `quay` | `https://quay.io/...` | `https://xget.xi-xu.me/cr/quay/...` |
| 谷歌 | `gcr` | `https://gcr.io/...` | `https://xget.xi-xu.me/cr/gcr/...` |
| 微软 | `mcr` | `https://mcr.microsoft.com/...` | `https://xget.xi-xu.me/cr/mcr/...` |
| Amazon ECR | `ecr` | `https://public.ecr.aws/...` | `https://xget.xi-xu.me/cr/ecr/...` |
| GitHub | `ghcr` | `https://ghcr.io/...` | `https://xget.xi-xu.me/cr/ghcr/...` |
| GitLab | `gitlab` | `https://registry.gitlab.com/...` | `https://xget.xi-xu.me/cr/gitlab/...` |
| Red Hat | `redhat` | `https://registry.redhat.io/...` | `https://xget.xi-xu.me/cr/redhat/...` |
| Oracle | `oracle` | `https://container-registry.oracle.com/...` | `https://xget.xi-xu.me/cr/oracle/...` |
| Cloudsmith | `cloudsmith` | `https://docker.cloudsmith.io/...` | `https://xget.xi-xu.me/cr/cloudsmith/...` |
| DigitalOcean | `digitalocean` | `https://registry.digitalocean.com/...` | `https://xget.xi-xu.me/cr/digitalocean/...` |
| VMware | `vmware` | `https://projects.registry.vmware.com/...` | `https://xget.xi-xu.me/cr/vmware/...` |
| Kubernetes | `k8s` | `https://registry.k8s.io/...` | `https://xget.xi-xu.me/cr/k8s/...` |
| Heroku | `heroku` | `https://registry.heroku.com/...` | `https://xget.xi-xu.me/cr/heroku/...` |
| SUSE | `suse` | `https://registry.suse.com/...` | `https://xget.xi-xu.me/cr/suse/...` |
| openSUSE | `opensuse` | `https://registry.opensuse.org/...` | `https://xget.xi-xu.me/cr/opensuse/...` |
| Gitpod | `gitpod` | `https://registry.gitpod.io/...` | `https://xget.xi-xu.me/cr/gitpod/...` |

```url
# GitHub 容器容器注册表原始链接
https://ghcr.io/v2/nginxinc/nginx-unprivileged/manifests/latest

# 转换后（添加 cr/ghcr 前缀）
https://xget.xi-xu.me/cr/ghcr/v2/nginxinc/nginx-unprivileged/manifests/latest

# Google 容器容器注册表原始链接
https://gcr.io/v2/distroless/base/manifests/latest

# 转换后（添加 cr/gcr 前缀）
https://xget.xi-xu.me/cr/gcr/v2/distroless/base/manifests/latest
```

## 🎯 应用场景

### Git 操作与配置

Xget 完全兼容 Git 协议，支持所有标准 Git 操作，并提供全局加速配置：

#### Git 操作

```bash
# 克隆存储库
git clone https://xget.xi-xu.me/gh/microsoft/vscode.git

# 克隆指定分支
git clone -b main https://xget.xi-xu.me/gh/facebook/react.git

# 浅克隆（仅最新提交）
git clone --depth 1 https://xget.xi-xu.me/gh/torvalds/linux.git

# 克隆 GitLab 存储库
git clone https://xget.xi-xu.me/gl/gitlab-org/gitlab.git

# 克隆 Gitea 存储库
git clone https://xget.xi-xu.me/gitea/gitea/gitea.git

# 克隆 Codeberg 存储库
git clone https://xget.xi-xu.me/codeberg/forgejo/forgejo.git

# 克隆 SourceForge 存储库
git clone https://xget.xi-xu.me/sf/projects/mingw-w64/code.git

# 添加远程存储库
git remote add upstream https://xget.xi-xu.me/gh/[所有者]/[存储库].git

# 拉取更新
git pull https://xget.xi-xu.me/gh/microsoft/vscode.git main

# 子模块递归克隆
git clone --recursive https://xget.xi-xu.me/gh/[用户名]/[带子模块的存储库].git
```

#### Git 全局加速配置

```bash
# 为特定域名配置 Git 使用 Xget
git config --global url."https://xget.xi-xu.me/gh/".insteadOf "https://github.com/"
git config --global url."https://xget.xi-xu.me/gl/".insteadOf "https://gitlab.com/"
git config --global url."https://xget.xi-xu.me/gitea/".insteadOf "https://gitea.com/"
git config --global url."https://xget.xi-xu.me/codeberg/".insteadOf "https://codeberg.org/"
git config --global url."https://xget.xi-xu.me/sf/".insteadOf "https://sourceforge.net/"

# 验证配置
git config --global --get-regexp url

# 现在所有相关平台的 git clone 都会自动使用 Xget 加速
git clone https://github.com/microsoft/vscode.git  # 自动转换为 Xget 链接
git clone https://gitlab.com/gitlab-org/gitlab.git  # 自动转换为 Xget 链接
git clone https://codeberg.org/forgejo/forgejo.git  # 自动转换为 Xget 链接
```

### 主流下载工具集成

#### wget 下载

```bash
# 下载单个文件
wget https://xget.xi-xu.me/gh/microsoft/vscode/archive/refs/heads/main.zip

# 断点续传
wget -c https://xget.xi-xu.me/hf/microsoft/DialoGPT-large/resolve/main/pytorch_model.bin

# 批量下载
wget -i urls.txt  # urls.txt 包含多个 Xget 链接
```

#### cURL 下载

```bash
# 基本下载
curl -L -O https://xget.xi-xu.me/gh/golang/go/archive/refs/tags/go1.22.0.tar.gz

# 显示进度条
curl -L --progress-bar -o model.bin https://xget.xi-xu.me/hf/openai/whisper-large-v3/resolve/main/pytorch_model.bin

# 设置用户代理
curl -L -H "User-Agent: MyApp/1.0" https://xget.xi-xu.me/gl/gitlab-org/gitlab-runner/-/archive/main/gitlab-runner-main.zip
```

#### aria2 多线程下载

```bash
# 多线程下载大文件
aria2c -x 16 -s 16 https://xget.xi-xu.me/hf/microsoft/DialoGPT-large/resolve/main/pytorch_model.bin

# 断点续传
aria2c -c https://xget.xi-xu.me/gh/microsoft/vscode/archive/refs/heads/main.zip

# 批量下载配置文件
aria2c -i download-list.txt  # 包含多个 Xget 链接的文件
```

### 作为 Hugging Face 镜像

```python
import os
from transformers import AutoTokenizer, AutoModelForCausalLM

# 设置环境变量，让 transformers 库自动使用 Xget 镜像
os.environ['HF_ENDPOINT'] = 'https://xget.xi-xu.me/hf'

# 定义模型名称
model_name = 'microsoft/DialoGPT-medium'

print(f"正在从镜像下载模型: {model_name}")

# 使用 AutoModelForCausalLM 来加载对话生成模型
# 由于上面设置了环境变量，这里无需添加任何额外参数
tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModelForCausalLM.from_pretrained(model_name)

print("模型和分词器加载成功！")

# 你现在可以使用 tokenizer 和 model 了
# 例如:
# new_user_input_ids = tokenizer.encode("Hello, how are you?", return_tensors='pt')
# chat_history_ids = model.generate(new_user_input_ids, max_length=1000, pad_token_id=tokenizer.eos_token_id)
# print(tokenizer.decode(chat_history_ids[:, new_user_input_ids.shape[-1]:][0], skip_special_tokens=True))
```

### npm 包管理加速

#### 配置 npm 使用 Xget 镜像

```bash
# 临时使用 Xget 镜像
npm install --registry https://xget.xi-xu.me/npm/

# 全局配置 npm 镜像
npm config set registry https://xget.xi-xu.me/npm/

# 验证配置
npm config get registry
```

#### 在项目中使用

```bash
# 在 .npmrc 文件中配置项目级镜像
echo "registry=https://xget.xi-xu.me/npm/" > .npmrc

# 安装依赖
npm install

# 或者使用 yarn
yarn config set registry https://xget.xi-xu.me/npm/
yarn install
```

### Python 包管理加速

#### 配置 pip 使用 Xget 镜像

```bash
# 临时使用 Xget 镜像
pip install requests -i https://xget.xi-xu.me/pypi/simple/

# 全局配置 pip 镜像
pip config set global.index-url https://xget.xi-xu.me/pypi/simple/
pip config set global.trusted-host xget.xi-xu.me

# 验证配置
pip config list
```

#### 在项目中使用

```bash
# 创建 pip.conf 文件（Linux/macOS）
mkdir -p ~/.pip
cat > ~/.pip/pip.conf << EOF
[global]
index-url = https://xget.xi-xu.me/pypi/simple/
trusted-host = xget.xi-xu.me
EOF

# 或在项目根目录创建 pip.conf
cat > pip.conf << EOF
[global]
index-url = https://xget.xi-xu.me/pypi/simple/
trusted-host = xget.xi-xu.me
EOF

# 使用配置文件安装
pip install -r requirements.txt --config-file pip.conf
```

#### 在 requirements.txt 中指定镜像

```txt
# requirements.txt
--index-url https://xget.xi-xu.me/pypi/simple/
--trusted-host xget.xi-xu.me

requests>=2.25.0
numpy>=1.21.0
pandas>=1.3.0
matplotlib>=3.4.0
```

### conda 包管理加速

#### 配置 conda 使用 Xget 镜像

```bash
# 配置默认频道镜像
conda config --add default_channels https://xget.xi-xu.me/conda/pkgs/msys2
conda config --add default_channels https://xget.xi-xu.me/conda/pkgs/r
conda config --add default_channels https://xget.xi-xu.me/conda/pkgs/main

# 配置所有社区频道镜像（推荐）
conda config --set channel_alias https://xget.xi-xu.me/conda/community

# 或配置特定社区频道
conda config --add channels https://xget.xi-xu.me/conda/community/conda-forge
conda config --add channels https://xget.xi-xu.me/conda/community/bioconda

# 设置频道优先级
conda config --set channel_priority strict

# 验证配置
conda config --show
```

#### 在 .condarc 中配置

.condarc 文件可以放在用户主目录（`~/.condarc`）或项目根目录下：

```yaml
default_channels:
  - https://xget.xi-xu.me/conda/pkgs/main
  - https://xget.xi-xu.me/conda/pkgs/r
  - https://xget.xi-xu.me/conda/pkgs/msys2
channel_alias: https://xget.xi-xu.me/conda/community
channel_priority: strict
show_channel_urls: true
```

#### 使用环境文件

环境文件中可以直接指定完整的镜像 URL：

```yaml
# environment.yml
name: myproject
channels:
  - https://xget.xi-xu.me/conda/pkgs/main
  - https://xget.xi-xu.me/conda/pkgs/r
  - https://xget.xi-xu.me/conda/community/bioconda
  - https://xget.xi-xu.me/conda/community/conda-forge
dependencies:
  - python=3.11
  - numpy>=1.24.0
  - pandas>=2.0.0
  - matplotlib>=3.7.0
  - scipy>=1.10.0
  - pip
  - pip:
    - requests>=2.28.0
```

```bash
# 使用环境文件创建环境
conda env create -f environment.yml

# 更新环境
conda env update -f environment.yml
```

### Maven 包管理加速

#### 配置 Maven 使用 Xget 镜像

```xml
<!-- 在 ~/.m2/settings.xml 中配置 Maven 镜像 -->
<settings>
  <mirrors>
    <mirror>
      <id>xget-maven-central</id>
      <mirrorOf>central</mirrorOf>
      <name>Xget Maven Central Mirror</name>
      <url>https://xget.xi-xu.me/maven/maven2</url>
    </mirror>
  </mirrors>
</settings>
```

#### 在项目中使用

```xml
<!-- 在 pom.xml 中配置项目级镜像 -->
<project>
  <repositories>
    <repository>
      <id>xget-maven-central</id>
      <name>Xget Maven Central</name>
      <url>https://xget.xi-xu.me/maven/maven2</url>
    </repository>
  </repositories>
  
  <pluginRepositories>
    <pluginRepository>
      <id>xget-maven-central</id>
      <name>Xget Maven Central</name>
      <url>https://xget.xi-xu.me/maven/maven2</url>
    </pluginRepository>
  </pluginRepositories>
</project>
```

```bash
# 使用命令行指定镜像
mvn clean install -Dmaven.repo.remote=https://xget.xi-xu.me/maven/maven2

# 下载特定依赖
mvn dependency:get -Dartifact=org.springframework:spring-core:5.3.21 \
  -DremoteRepositories=https://xget.xi-xu.me/maven/maven2
```

### Gradle 包管理加速

#### 配置 Gradle 使用 Xget 镜像

```gradle
// 在 build.gradle 中配置 Gradle 镜像
repositories {
    maven {
        url 'https://xget.xi-xu.me/maven/maven2'
    }
    gradlePluginPortal {
        url 'https://xget.xi-xu.me/gradle/m2'
    }
}

// 配置插件仓库
pluginManagement {
    repositories {
        maven {
            url 'https://xget.xi-xu.me/gradle/m2'
        }
        gradlePluginPortal()
    }
}
```

#### 全局配置

```gradle
// 在 ~/.gradle/init.gradle 中配置全局镜像
allprojects {
    repositories {
        maven {
            url 'https://xget.xi-xu.me/maven/maven2'
        }
    }
}

settingsEvaluated { settings ->
    settings.pluginManagement {
        repositories {
            maven {
                url 'https://xget.xi-xu.me/gradle/m2'
            }
            gradlePluginPortal()
        }
    }
}
```

```bash
# 使用命令行指定镜像
gradle build -Dmaven.repo.remote=https://xget.xi-xu.me/maven/maven2

# 刷新依赖
gradle build --refresh-dependencies
```

### Ruby 包管理加速

#### 配置 RubyGems 使用 Xget 镜像

```bash
# 临时使用 Xget 镜像
gem install rails --source https://xget.xi-xu.me/rubygems/

# 全局配置 RubyGems 镜像
gem sources --add https://xget.xi-xu.me/rubygems/
gem sources --remove https://rubygems.org/

# 验证配置
gem sources -l
```

#### 在项目中使用

```ruby
# 在 Gemfile 中配置项目级镜像
source 'https://xget.xi-xu.me/rubygems/'

gem 'rails', '~> 7.0.0'
gem 'pg', '~> 1.1'
gem 'puma', '~> 5.0'
```

```bash
# 使用 bundle 安装
bundle config mirror.https://rubygems.org https://xget.xi-xu.me/rubygems/
bundle install
```

### Go 模块加速

#### 配置 Go 使用 Xget 代理

```bash
# 配置 Go 模块代理
export GOPROXY=https://xget.xi-xu.me/golang,direct
export GOSUMDB=off

# 或者永久配置
go env -w GOPROXY=https://xget.xi-xu.me/golang,direct
go env -w GOSUMDB=off

# 验证配置
go env GOPROXY
```

#### 在项目中使用

```bash
# 下载依赖
go mod download

# 更新依赖
go get -u ./...

# 清理模块缓存
go clean -modcache
```

### NuGet 包管理加速

#### 配置 NuGet 使用 Xget 镜像

```bash
# 添加 Xget 包源
dotnet nuget add source https://xget.xi-xu.me/nuget/v3/index.json -n xget

# 列出包源
dotnet nuget list source

# 在项目中使用
dotnet restore --source https://xget.xi-xu.me/nuget/v3/index.json
```

#### 在 NuGet.Config 中配置

```xml
<!-- NuGet.Config -->
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <add key="xget" value="https://xget.xi-xu.me/nuget/v3/index.json" />
  </packageSources>
</configuration>
```

### PHP 包管理加速

#### 配置 Composer 使用 Xget 镜像

```bash
# 全局配置 Composer 镜像
composer config -g repo.packagist composer https://xget.xi-xu.me/packagist/

# 项目级配置
composer config repo.packagist composer https://xget.xi-xu.me/packagist/

# 验证配置
composer config -l
```

#### 在 composer.json 中配置

```json
{
  "repositories": [
    {
      "type": "composer",
      "url": "https://xget.xi-xu.me/packagist/"
    }
  ],
  "require": {
    "symfony/console": "^6.0",
    "guzzlehttp/guzzle": "^7.0"
  }
}
```

### Linux 发行版加速

#### Debian/Ubuntu APT 配置

```bash
# 备份原始源列表
sudo cp /etc/apt/sources.list /etc/apt/sources.list.backup

# 配置 Debian 镜像
echo "deb https://xget.xi-xu.me/debian/debian bookworm main" | sudo tee /etc/apt/sources.list
echo "deb https://xget.xi-xu.me/debian/debian-security bookworm-security main" | sudo tee -a /etc/apt/sources.list

# 配置 Ubuntu 镜像
echo "deb https://xget.xi-xu.me/ubuntu/ubuntu jammy main restricted universe multiverse" | sudo tee /etc/apt/sources.list
echo "deb https://xget.xi-xu.me/ubuntu/ubuntu jammy-updates main restricted universe multiverse" | sudo tee -a /etc/apt/sources.list

# 更新包列表
sudo apt update
```

#### Fedora DNF 配置

```bash
# 配置 Fedora 镜像
sudo sed -i 's|^metalink=|#metalink=|g' /etc/yum.repos.d/fedora*.repo
sudo sed -i 's|^#baseurl=http://download.example/pub/fedora/linux|baseurl=https://xget.xi-xu.me/fedora/pub/fedora/linux|g' /etc/yum.repos.d/fedora*.repo

# 更新包缓存
sudo dnf makecache
```

#### Rocky Linux DNF 配置

```bash
# 配置 Rocky Linux 镜像
sudo sed -i 's|^mirrorlist=|#mirrorlist=|g' /etc/yum.repos.d/rocky*.repo
sudo sed -i 's|^#baseurl=http://dl.rockylinux.org|baseurl=https://xget.xi-xu.me/rocky|g' /etc/yum.repos.d/rocky*.repo

# 更新包缓存
sudo dnf makecache
```

#### Arch Linux Pacman 配置

```bash
# 备份原始镜像列表
sudo cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.backup

# 配置 Arch Linux 镜像
echo 'Server = https://xget.xi-xu.me/arch/$repo/os/$arch' | sudo tee /etc/pacman.d/mirrorlist

# 更新包数据库
sudo pacman -Sy
```

### 学术资源加速

#### arXiv 论文下载

```bash
# 下载 arXiv 论文 PDF
wget https://xget.xi-xu.me/arxiv/pdf/2301.07041.pdf

# 下载论文源码
curl -L -O https://xget.xi-xu.me/arxiv/e-print/2301.07041

# 批量下载多篇论文
for id in 2301.07041 2302.13971 2303.08774; do
  wget https://xget.xi-xu.me/arxiv/pdf/${id}.pdf
done
```

#### 在学术工具中使用

```python
# 在 Python 中使用 arXiv 加速下载
import requests

def download_arxiv_paper(arxiv_id, output_path):
    url = f"https://xget.xi-xu.me/arxiv/pdf/{arxiv_id}.pdf"
    response = requests.get(url)
    
    if response.status_code == 200:
        with open(output_path, 'wb') as f:
            f.write(response.content)
        print(f"Downloaded {arxiv_id} to {output_path}")
    else:
        print(f"Failed to download {arxiv_id}")

# 下载论文
download_arxiv_paper("2301.07041", "attention_is_all_you_need.pdf")
```

### 容器镜像加速

Xget 为容器镜像拉取提供全面的加速支持，兼容 Docker、Podman、containerd 等容器运行时。

#### Docker 配置

```bash
# 配置 Docker 使用 Xget 镜像加速
# 编辑 /etc/docker/daemon.json（Linux）或 ~/.docker/daemon.json（macOS/Windows）
{
  "registry-mirrors": [
    "https://xget.xi-xu.me/cr/ghcr"
  ]
}

# 重启 Docker 服务
sudo systemctl restart docker  # Linux
# 或在 Docker Desktop 中重启服务

# 验证配置
docker info | grep -A 10 "Registry Mirrors"
```

#### 直接拉取镜像

```bash
# 拉取 GitHub Container Registry 镜像
docker pull xget.xi-xu.me/cr/ghcr/nginxinc/nginx-unprivileged:latest

# 拉取 Google Container Registry 镜像
docker pull xget.xi-xu.me/cr/gcr/distroless/base:latest

# 拉取 Microsoft Container Registry 镜像
docker pull xget.xi-xu.me/cr/mcr/dotnet/runtime:8.0
```

#### Kubernetes 部署配置

```yaml
# deployment.yaml - 使用 Xget 加速的镜像
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: xget.xi-xu.me/cr/ghcr/nginxinc/nginx-unprivileged:latest
        ports:
        - containerPort: 80
      - name: redis
        image: xget.xi-xu.me/cr/ghcr/bitnami/redis:alpine
        ports:
        - containerPort: 6379
```

#### Docker Compose 配置

```yaml
# docker-compose.yml - 使用 Xget 加速镜像
version: '3.8'
services:
  web:
    image: xget.xi-xu.me/cr/ghcr/nginxinc/nginx-unprivileged:latest
    ports:
      - "80:80"
    volumes:
      - ./html:/usr/share/nginx/html
  
  database:
    image: xget.xi-xu.me/cr/mcr/mssql/server:2022-latest
    environment:
      ACCEPT_EULA: Y
      SA_PASSWORD: "MyStrongPassword123!"
    volumes:
      - mssql_data:/var/opt/mssql
  
  cache:
    image: xget.xi-xu.me/cr/ghcr/bitnami/redis:alpine
    ports:
      - "6379:6379"

volumes:
  mssql_data:
```

#### Dockerfile 优化

```dockerfile
# 在 Dockerfile 中使用 Xget 加速基础镜像
FROM xget.xi-xu.me/cr/ghcr/nodejs/node:18-alpine AS builder

WORKDIR /app
COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build

# 生产阶段
FROM xget.xi-xu.me/cr/ghcr/nginxinc/nginx-unprivileged:latest
COPY --from=builder /app/dist /usr/share/nginx/html

# 使用 Microsoft 容器容器注册表的 .NET 镜像
FROM xget.xi-xu.me/cr/mcr/dotnet/aspnet:8.0 AS runtime
WORKDIR /app
COPY --from=builder /app/publish .
ENTRYPOINT ["dotnet", "MyApp.dll"]
```

#### CI/CD 集成

```yaml
# GitHub Actions - 使用 Xget 加速容器构建
name: Build and Deploy
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      
      - name: Build with accelerated base images
        run: |
          # 构建时使用 Xget 加速的基础镜像
          docker build -t myapp:latest \
            --build-arg BASE_IMAGE=xget.xi-xu.me/cr/ghcr/nodejs/node:18-alpine .
          
      - name: Test with accelerated images
        run: |
          # 使用加速镜像进行测试
          docker run --rm \
            xget.xi-xu.me/cr/mcr/dotnet/runtime:8.0 \
            dotnet --version
```

#### Podman 配置

```bash
# 配置 Podman 使用 Xget 镜像加速
# 编辑 /etc/containers/registries.conf
[[registry]]
prefix = "ghcr.io"
location = "xget.xi-xu.me/cr/ghcr"

# 或者直接拉取
podman pull xget.xi-xu.me/cr/ghcr/alpine/alpine:latest
podman pull xget.xi-xu.me/cr/ghcr/nginxinc/nginx-unprivileged:latest
```

#### containerd 配置

```toml
# 配置 containerd 使用 Xget 加速
# 编辑 /etc/containerd/config.toml
[plugins."io.containerd.grpc.v1.cri".registry.mirrors]
  [plugins."io.containerd.grpc.v1.cri".registry.mirrors."ghcr.io"]
    endpoint = ["https://xget.xi-xu.me/cr/ghcr"]
  [plugins."io.containerd.grpc.v1.cri".registry.mirrors."gcr.io"]
    endpoint = ["https://xget.xi-xu.me/cr/gcr"]
```

```bash
# 重启 containerd
sudo systemctl restart containerd
```

### CI/CD 环境集成

#### GitHub Actions

```yaml
name: Download Dependencies
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4
      
      - name: Download model files
        run: |
          # 使用 Xget 加速下载大型模型文件
          wget https://xget.xi-xu.me/hf/microsoft/DialoGPT-medium/resolve/main/pytorch_model.bin
          
      - name: Clone dependency repo
        run: |
          # 使用 Xget 加速 Git 克隆
          git clone https://xget.xi-xu.me/gh/[所有者]/[存储库].git
          
      - name: Download release assets
        run: |
          # 批量下载发布文件
          curl -L -O https://xget.xi-xu.me/gh/[所有者]/[存储库]/releases/download/v1.0.0/[文件名].tar.gz
          curl -L -O https://xget.xi-xu.me/gh/[所有者]/[存储库]/releases/download/v1.0.0/[文件名].zip
```

#### GitLab CI

```yaml
stages:
  - download
  - build

download_dependencies:
  stage: download
  script:
    # 使用 Xget 加速下载
    - wget https://xget.xi-xu.me/gl/gitlab-org/gitlab-runner/-/archive/main/gitlab-runner-main.zip
    - git clone https://xget.xi-xu.me/gh/[所有者]/[依赖存储库].git
    # 下载 Hugging Face 数据集
    - curl -L -O https://xget.xi-xu.me/hf/datasets/wikitext/resolve/main/wikitext-103-v1/wiki.train.tokens
  artifacts:
    paths:
      - "*.zip"
      - "*.json"
      - dependency/
```

#### Docker 构建优化

```dockerfile
FROM ubuntu:22.04

# 在 Docker 构建中使用 Xget 加速下载
RUN apt-get update && apt-get install -y wget curl git

# 下载大型文件
RUN wget https://xget.xi-xu.me/gh/microsoft/vscode/archive/refs/heads/main.zip

# 克隆源码
RUN git clone https://xget.xi-xu.me/gh/[所有者]/[源码存储库].git /app

# 下载模型文件
RUN curl -L -O /models/model.bin https://xget.xi-xu.me/hf/microsoft/DialoGPT-medium/resolve/main/pytorch_model.bin

# 配置并安装 conda 包
RUN echo "default_channels:" > ~/.condarc && \
    echo "  - https://xget.xi-xu.me/conda/pkgs/main" >> ~/.condarc && \
    echo "  - https://xget.xi-xu.me/conda/pkgs/r" >> ~/.condarc && \
    echo "  - https://xget.xi-xu.me/conda/pkgs/msys2" >> ~/.condarc && \
    echo "channel_alias: https://xget.xi-xu.me/conda/community" >> ~/.condarc && \
    echo "channel_priority: strict" >> ~/.condarc && \
    conda install -y numpy pandas matplotlib

WORKDIR /app
```

## 🚀 部署选择

### Cloudflare Workers 一键部署

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/xixu-me/Xget)

部署后，你的 Xget 服务将在 `your-worker-name.your-subdomain.workers.dev` 上可用。

### 手动部署

如果你更喜欢手动部署或需要自定义配置：

#### 前置要求

1. 注册 [Cloudflare 账户](https://dash.cloudflare.com/sign-up/workers-and-pages)
2. 安装 [Node.js](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)

#### 部署步骤

1. **克隆存储库**

   ```bash
   git clone https://github.com/xixu-me/Xget.git
   cd Xget
   ```

2. **安装依赖并认证**

   ```bash
   npm install
   npx wrangler auth login
   ```

3. **自定义配置（可选）**

   编辑 `wrangler.toml` 文件设置你的存储库名称：

   ```toml
   name = "你的-xget-项目名"
   ```

4. **部署**

   ```bash
   npm run deploy
   ```

部署完成后，你的 Xget 服务将在 `your-worker-name.your-subdomain.workers.dev` 上可用。

## 🔧 配置

### 配置参数

你可以通过修改 `src/config/index.js` 来自定义配置：

```javascript
export const CONFIG = {
  TIMEOUT_SECONDS: 30,       // 请求超时时间（秒）
  MAX_RETRIES: 3,            // 最大重试次数
  RETRY_DELAY_MS: 1000,      // 重试延迟时间（毫秒）
  CACHE_DURATION: 1800,      // 缓存持续时间（1800秒 = 30分钟）
  SECURITY: {
    ALLOWED_METHODS: ["GET", "HEAD"],  // 允许的 HTTP 方法（Git 操作会动态允许 POST）
    ALLOWED_ORIGINS: ["*"],            // 允许的 CORS 源
    MAX_PATH_LENGTH: 2048,             // 最大路径长度（字符）
  },
};
```

### 性能调优建议

- **缓存优化**：根据使用模式调整 `CACHE_DURATION`，频繁更新的存储库可适当降低
- **超时设置**：网络条件较差时可适当增加 `TIMEOUT_SECONDS`
- **重试策略**：高延迟环境下可增加 `MAX_RETRIES` 和 `RETRY_DELAY_MS`

### 添加新平台

要添加对新平台的支持，编辑 `src/config/platforms.js`：

```javascript
export const PLATFORMS = {
  // 现有平台...
  
  // 新平台示例
  custom: {
    base: "https://example.com",
    transform: (path) => path.replace(/^\/custom\//, "/"),
  },
};
```

## 🚧 开发

1. **存储库设置**

   ```bash
   git clone https://github.com/xixu-me/Xget.git
   cd Xget
   npm install
   npx wrangler auth login  # 首次使用
   ```

2. **本地开发**

   ```bash
   npm run dev              # 启动开发服务器 (http://localhost:8787)
   npm run test:run         # 运行完整测试套件
   npm run test:coverage    # 生成测试覆盖率报告
   npm run lint             # 代码检查
   npm run format           # 代码格式化
   npm run deploy           # 部署到生产
   ```

## 🧪 测试

存储库包含完整的测试套件，确保代码质量和功能正确性。

### 完整测试

```bash
# 安装测试依赖
npm install

# 运行所有测试
npm run test:run

# 生成覆盖率报告
npm run test:coverage

# 监视模式
npm run test:watch
```

### 测试覆盖

- **单元测试**: 核心功能、平台配置、性能监控
- **集成测试**: 端到端流程、平台集成、Git 协议
- **安全测试**: 输入验证、安全头、权限控制
- **性能测试**: 响应时间、内存使用、并发处理

## 🔍 故障排除

### 常见问题

**Q: 下载速度没有明显提升？**  
A: 检查源文件是否已经在 CDN 边缘节点缓存，首次访问可能较慢，后续访问会显著提升。

**Q: Git 操作失败？**  
A: 确认使用了正确的 URL 格式，且 Git 客户端版本支持 HTTPS 代理。

**Q: 部署后无法访问？**  
A: 检查 Cloudflare Workers 域名是否正确绑定，确认 `wrangler.toml` 配置正确。

**Q: 出现 400 错误？**  
A: 检查 URL 路径格式，确认平台前缀正确使用。

### 性能监控

服务会在响应头中返回性能指标：

- `X-Performance-Metrics`: 包含请求各阶段的耗时统计
- `X-Cache-Status`: 显示缓存命中状态

### 日志调试

在开发环境中，你可以通过 Cloudflare Workers 控制台查看详细日志：

```bash
npx wrangler dev --log-level debug
```

## ⚠️ 免责声明

- **合法使用**：本存储库仅用于加速合法的公开文件下载和 Git 操作，请遵守相关平台的使用条款和当地法律法规
- **服务可用性**：公共实例 `xget.xi-xu.me` 为免费服务，不保证 100% 可用性，建议生产环境部署自己的实例
- **数据安全**：虽然 Xget 不存储或记录用户数据，但请谨慎处理敏感信息的下载
- **责任限制**：使用本服务造成的任何直接或间接损失，开发者不承担责任
- **第三方平台**：请尊重 GitHub、GitLab、Gitea、Codeberg、SourceForge、Hugging Face 等平台的服务条款和速率限制

## 🤝 贡献

我们欢迎各种形式的贡献！请查看[贡献指南](CONTRIBUTING.md)了解如何参与存储库开发。

1. **报告问题**: 使用 [issue 模板](https://github.com/xixu-me/Xget/issues/new/choose)报告 bug 或提出功能请求
2. **提交代码**: fork 存储库，创建功能分支，提交 pull request
3. **改进文档**: 修正错误、添加示例、完善说明
4. **测试反馈**: 在不同环境下测试并提供反馈

## 🌟 Star 历史

<a href="https://www.star-history.com/#xixu-me/Xget&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=xixu-me/Xget&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=xixu-me/Xget&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=xixu-me/Xget&type=Date" />
 </picture>
</a>

## 📞 联系方式

- **作者**: [Xi Xu](https://xi-xu.me)
- **邮箱**: [联系邮箱](mailto:i@xi-xu.me)
- **赞助**: [赞助链接](https://xi-xu.me/#sponsorships)

## 📝 许可证

本存储库采用 GPL-3.0 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

---

<div align="center">

**如果这个存储库对您有帮助，请考虑给它一个 ⭐ star！**

Made with ❤️ by [Xi Xu](https://xi-xu.me)

</div>
