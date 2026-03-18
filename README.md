# JustRunMy.app 部署指南

本项目支持在 JustRunMy.app 平台快速部署基于 Node.js 环境的轻量化容器。通过配合 `zvps-super` 镜像，你可以将其作为一个简易的 VPS 使用，实现内网穿透及更多高级功能。

---

## 🚀 部署步骤

### 1. 源码打包 (关键)
为了确保平台能够正确识别入口文件，打包时请遵循“一级压缩”原则：
* 下载本项目源码并解压。
<img width="843" height="666" alt="image" src="https://github.com/user-attachments/assets/75df34b1-e2c2-4be3-a15f-cf0c19cb4c8d" />

* **选定所有文件（不要选定文件夹）** 重新压缩为 `.zip`。
* 确保压缩包打开后直接看到文件，而不是另一个目录。

<img width="280" height="93" alt="image" src="https://github.com/user-attachments/assets/4a5693b4-71e0-4f1e-9b91-460179671783" />

### 2. 上传至平台
在 [justrunmy.app](https://justrunmy.app) 控制台上传刚才准备好的压缩文件。

<img width="800" height="271" alt="image" src="https://github.com/user-attachments/assets/ba08c6a2-d984-4bc4-a896-bbc3e015237e" />

### 3. 环境与版本设置
* **Runtime Version**: 建议选择 **`22`** 以确保环境稳定性。
* 等待进度条读取完成。

<img width="467" height="526" alt="image" src="https://github.com/user-attachments/assets/2f407079-e548-46f6-9358-352793f00e70" />

<img width="1194" height="192" alt="image" src="https://github.com/user-attachments/assets/c4aad40c-05fa-4aba-857c-d388b248238a" />

### 4. 镜像与高级配置
镜像建议使用配套项目，或根据需求自定义：
* **推荐镜像**: [zvps-super](https://github.com/zv201413/zvps-super)
* **参数配置**: 详细参数含义请参考上述项目的说明文档。

<img width="923" height="416" alt="image" src="https://github.com/user-attachments/assets/9ce152a3-23c3-4ef7-986d-14d8b77f9758" />

> [!IMPORTANT]
> 注意**Settings**里的端口是内部端口
> <img width="1542" height="479" alt="image" src="https://github.com/user-attachments/assets/3ae74e2e-451b-4551-822b-54612b6c5758" />
> 生成节点后要在代理app中替换为**General**的外部端口
> <img width="1333" height="588" alt="image" src="https://github.com/user-attachments/assets/c19abda1-1216-4c33-92ce-ad8e5e50c813" />
> 注意**添加内部端口**之后需要重启容器才会更新外部端口，切忌直接使用设置的内部端口

### 5. 启动服务
确认无误后点击 **Start**。部署成功后，你可以在 Shell 终端进行实时操作。此时欢迎点个 Star ⭐️ 支持一下

<img width="1510" height="317" alt="image" src="https://github.com/user-attachments/assets/476eed4e-6ee7-4934-9a54-0967d75437ae" />

---

## 📝 补充说明
* **简易 VPS**: 本质上这是一个 Node.js 环境的容器，你可以通过 Web Shell 执行 Linux 命令。
* **本地 SSH**: 配合相关内网穿透项目，可实现本地终端直接 SSH 接入。
<img width="731" height="657" alt="image" src="https://github.com/user-attachments/assets/e8d7589a-0a9e-40a7-ae68-c40392c9fc64" />
