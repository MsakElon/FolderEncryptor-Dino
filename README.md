简体中文 | [English](./README.en.md) | [日本語](./README.ja.md) | [한국어](./README.ko.md)

# Folder Encryptor V5

`Folder Encryptor V5` 是一个面向 Windows 的轻量级文件夹加密小工具。

当前仓库提供可直接使用的发布包和使用文档，方便下载、体验和分享。源码、许可证和更完整的技术说明会在后续整理后逐步补充。

## 软件定位

- 面向 Windows 桌面环境的文件夹加密/解密工具
- 提供安装版和便携版两种分发方式
- 支持手动输入密码，也支持随机生成强密码
- 随机生成密码时会自动在桌面追加保存一份密码备份，降低遗忘风险

## 下载内容

| 文件 | 说明 | 大小 |
| --- | --- | ---: |
| [`FolderEncryptor_Dino_SmartSetup.exe`](https://github.com/MsakElon/FolderEncryptor-Dino/raw/main/dist/FolderEncryptor_Dino_SmartSetup.exe) | 安装版，适合常规使用 | 69.7 MB |
| [`FolderEncryptor_V5_Dino.exe`](https://github.com/MsakElon/FolderEncryptor-Dino/raw/main/dist/FolderEncryptor_V5_Dino.exe) | 便携版，适合直接运行 | 34.9 MB |

点击文件名即可直接下载对应版本。

## 核心功能

- 选择目标文件夹进行加密或解密
- 自定义输入主密码
- 点击 `随机生成` 按钮快速生成强密码
- 自动在桌面保存随机密码备份
- 支持重复生成，密码备份内容采用追加写入，不会覆盖旧记录

## 随机密码与备份说明

如果你不想自己手动设置密码，可以直接点击界面中的 `随机生成` 按钮。

程序会：

1. 自动生成一组强密码
2. 将生成的密码写入桌面的密码备份文本文件
3. 再次点击时继续向同一个文本文件追加新记录，而不是覆盖旧内容

备份内容示例：

```text
【V5 专属加密密码备份】
密码: euZi^oahxuKq2Zm6

【V5 专属加密密码备份】
密码: JSE7CWTg54#CSH!Q
```

建议在完成加密后妥善保管该备份文件，避免密码和加密文件长期存放在同一位置。

## 快速开始

### 1. 选择运行方式

- 如果你希望正常安装，优先使用 `FolderEncryptor_Dino_SmartSetup.exe`
- 如果你希望免安装直接体验，可以使用 `FolderEncryptor_V5_Dino.exe`

### 2. 加密文件夹

推荐流程如下：

1. 启动 `Folder Encryptor V5`
2. 在 `Target Folder / 目标文件夹` 处选择需要保护的文件夹
3. 在 `Master Password / 安全密码` 处手动输入密码，或者点击 `随机生成`
4. 点击 `隐形加密 (Encrypt)`
5. 等待处理完成并检查结果

### 3. 解密文件夹

1. 启动 `Folder Encryptor V5`
2. 选择已经加密过的目标文件夹
3. 输入对应密码
4. 点击 `一键还原 (Decrypt)`
5. 确认文件恢复正常后再进行后续处理

## SHA256 校验

```text
F656ABB26310F83526EEBEDC685ABDD9D79D12672882D8E38D902D30D3AE50A1  dist/FolderEncryptor_Dino_SmartSetup.exe
EB1A4C324AAE3372214E1A6C904B67472FCB626B3D071165C97533DEC33ECE52  dist/FolderEncryptor_V5_Dino.exe
```

## 使用建议

- 第一次使用时，建议先拿测试文件夹演练完整流程
- 对重要资料操作前，建议先额外备份一次
- 如果使用随机生成密码，请及时查看并妥善保存桌面备份文件
- 当前公开版本主要面向 Windows 使用环境

## 仓库内容

- 使用说明：
- [简体中文](./docs/usage-guide.md)
- [English](./docs/usage-guide.en.md)
- [日本語](./docs/usage-guide.ja.md)
- [한국어](./docs/usage-guide.ko.md)
- [校验信息](./checksums.txt)

## 当前状态

当前仓库是一个先公开可用版本、再继续完善开源资料的整理版发布。

这意味着：

- 现在可以直接下载和使用发布包
- 文档已经补齐到可以对外展示和分发
- 后续会继续整理源码、许可证和更完整的技术说明

## License

本项目采用 [MIT License](./LICENSE)。

这意味着你可以在保留原始许可证声明的前提下，自由使用、复制、修改和分发本项目内容；项目按“现状”提供，不附带任何担保。
