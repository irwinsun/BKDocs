# 软件包简介

解压 `bkce_basic_suite-6.1.0.tgz` 安装包后，`src` 即为软件包目录，存放了蓝鲸基础平台、官方 SaaS 包、开源组件等内容，`install` 则为蓝鲸部署脚本。

## 软件包目录结构

请按照目录结构检查对应文件目录是否存在，版本号会随着每次更新而变更，请以官网下载的实际版本号为准：

### 基础套餐

```bash
[root@VM-0-1 src]# pwd
/data/src
[root@VM-0-1 src]# tree -F -L 1
.

├── bkiam_ce-1.10.4.tgz
├── bkiam_search_engine-1.0.6.tgz
├── bknodeman_ee-2.2.11-bkofficial.tgz
├── bkssm_ce-1.0.8.tgz
├── blueking.env
├── cmdb_ce-3.10.15.tgz
├── COMMON_MD5
├── COMMON_VERSION
├── gse_agent_ce-3.6.18.tgz
├── gse_ce-3.6.18.tgz
├── gse_plugins
├── image
├── java8.tgz
├── job_ce-3.5.0.10.tgz
├── license_ce-3.1.5.tgz
├── node-v14.17.0-linux-x64.tar.gz
├── official_saas
├── open_paas_ce-2.14.8-bkofficial.tgz
├── paas_agent_ce-3.2.4.tgz
├── python
├── usermgr_ce-2.3.4-beta.16-bkofficial.tar.gz
├── VERSION
└── yum

```

### 增强套餐

解压 bkce_co_suite-6.1.0.tgz 安装包后，包含的是各产品的监控平台、日志平台和故障自愈的整包

### 增强软件包目录结构

`*.tgz` 为产品安装包。包含了自身产品的 **后台包** 以及 **SaaS 包**。

```bash
[root@VM-1-1-centos ~]# tar tf bkce_co_package-6.1.0.tgz
bklog_package-4.3.1-257.tgz
bkmonitorv3_package-3.4.2653.tgz
fta_package-5.2.15-ce.tgz
```

这里重点说明各产品下的 `support-files/` 目录，以权限中心的为例：

- **bkiam**: 存放初始化权限文件。
- **pkgs**： 存放依赖包，比如 Python 工程的 pip 包。
- **sql**： 存放初始化或升级时用到的 sql 文件。
- **templates**： 存放模块的模板文件，安装时会替换里面的 类似 `__VAR_NAME__`： 形式的变量。

## 软件包内容说明

蓝鲸基础平台及 SaaS 详细说明请参考 [产品白皮书](https://bk.tencent.com/docs/)，开源组件版本和配置方式可参考版本日志。

- **bkiam：** 权限中心后台
- **bklog：** 日志平台后台
- **bkmonitorv3：** 监控平台后台
- **bknodeman：** 节点管理后台
- **bkssm：** 凭证管理后台
- **blueking.env：** 证书环境变量
- **cert：** 证书文件目录
- **cmdb：** 配置平台后台
- **COMMON_VERSION：** 开源组件包版本号
- **fta：** 故障自愈后台
- **gse：** 管控平台后台
- **gse_plugins：** 官方采集器插件目录
- **image：** SaaS 基础镜像目录
- **java8.tgz：** JDK 安装包
- **job：** 作业平台后台
- **license：** 鉴权服务
- **MD5：** MD5 校验文件
- **official_saas：** 官方 SaaS 包
- **open_paas：** PaaS 后台
- **paas_agent：** PaaS Agent 后台
- **python：** 蓝鲸定制 Python 解释器目录
- **usermgr：** 用户管理后台
- **VERSION：** 社区版版本号
- **yum：** 开源组件 RPM 包目录
