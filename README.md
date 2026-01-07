# Spark 插件数据库

这是 Spark 应用的插件数据库，包含所有可用插件的元信息。

## 📁 目录结构

```
sparkdatabase/
├── README.md                    # 本文件
├── assets/                      # 资源文件
│   ├── spark-community-banner.jpeg
│   └── spark-freedom-banner.jpeg
└── plugins/                     # 插件配置
    ├── total-plugins.json       # 所有插件列表 (核心文件)
    ├── finder.json              # 探索页面内容
    ├── system.json              # 系统工具类
    ├── tools.json               # 搜索工具类
    ├── image.json               # 图像处理类
    ├── worker.json              # 效率工具类
    └── devPlugin.json           # 开发者工具类
```

## 🔧 使用方法

### 在 Spark 中配置

1. 打开 Spark → 插件市场 → 设置 → 本地启动
2. 配置 database url:
   ```
   https://code.srdcloud.cn/cd-framework23/frontend-fw/sparkdatabase/raw/master
   ```
3. 如果是私有仓库，填写 access token
4. 保存并重启插件市场

### 添加新插件

1. 在 npm 上发布你的插件包
2. 编辑 `plugins/total-plugins.json`
3. 添加插件信息：
   ```json
   {
     "name": "spark-plugin-your-plugin",
     "pluginName": "你的插件",
     "description": "插件描述",
     "version": "1.0.0",
     "author": "作者名",
     "logo": "https://your-cdn.com/logo.png",
     "pluginType": "ui",
     "main": "index.html",
     "features": [
       {
         "code": "your-feature",
         "explain": "功能说明",
         "cmds": ["命令1", "命令2"]
       }
     ]
   }
   ```
4. 提交并推送到仓库

## 📚 插件字段说明

### 必需字段

- `name`: npm 包名
- `pluginName`: 显示名称
- `description`: 插件描述
- `version`: 版本号
- `author`: 作者
- `logo`: 图标 URL
- `pluginType`: 插件类型 (ui/system)
- `features`: 功能列表

### 可选字段

- `main`: 入口文件 (UI 插件需要)
- `homepage`: 主页链接
- `development`: 开发环境地址
- `platform`: 支持的平台数组

## 🔗 相关链接

- **Spark 主项目**: [内网地址]
- **插件开发文档**: 见主项目 `ss_guide_md/PLUGIN_SYSTEM_GUIDE.md`

---

**维护**: Spark Team  
**最后更新**: 2026-01-07
