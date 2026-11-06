# furry-art-assets

美术素材库（与画廊分开），供组件读取。

本仓库只存放素材文件，不含页面或代码。角色画廊在另一个仓库 [furry-character-gallery](https://github.com/Merphy0305/furry-character-gallery)。

## 目录结构

```
furry-art-assets/
├── 01/                      剑杖谭角色卡专用素材
├── xenoblade2/              异度神剑2角色卡表情立绘
├── 異世界冒険_片頭_剪辑版v9.mp4   异世界冒险片头成片（剪辑版 v9）
└── README.md
```

## 文件夹用途

### `01/`：剑杖谭角色卡美术素材库

「剑杖谭」角色卡使用的美术素材，包括：

| 类型 | 文件 |
| --- | --- |
| 背景 | `bg_loop.webp`、`bg_loop.mp4`（循环背景） |
| 按钮 | `btn_big.webp`、`btn_small.webp`、`btn_end.webp` |
| 转场 / 特效 | `burn_fwd.mp4`、`burn_rev.mp4`、`burn_map.png`（燃烧转场及其遮罩图） |
| 头像 / 横幅 | `v2_avatar.webp`、`v2_banner.webp` |
| 风格参考与其他图 | `style_frame.png`、`019.png`～`022.png`、`ComfyUI_temp_vnuic_00011_.jpg` |

### `xenoblade2/`：异度神剑2角色卡表情立绘

异度神剑2角色卡使用的角色表情立绘，格式为 `.webp`。

- 命名规则：`角色名_表情.webp`，全部小写英文，用下划线连接。
- 角色：rex、nia、tora、morag、zeke、pandoria、dromarch、brighid、hana、jin、azurda、malos。
- 表情：normal、serious、smile、sad、worry、angry、surprise、proud、panic、shy、smirk、tease、laugh、relaxed、stern 等，每个角色只有其中一部分。
- 例：`rex_normal.webp`、`nia_shy.webp`。

### 根目录视频

`異世界冒険_片頭_剪辑版v9.mp4` 是异世界冒险片头的剪辑成片，不属于任何组件的固定素材目录。

## 链接规则

仓库是公开的，分支为 `main`。组件读取素材时，把「仓库路径」拼到下面任一前缀后面即可。

| 方式 | 前缀 |
| --- | --- |
| GitHub Raw | `https://raw.githubusercontent.com/Merphy0305/furry-art-assets/main/` |
| jsDelivr CDN | `https://cdn.jsdelivr.net/gh/Merphy0305/furry-art-assets@main/` |

示例：

```
https://raw.githubusercontent.com/Merphy0305/furry-art-assets/main/xenoblade2/rex_normal.webp
https://cdn.jsdelivr.net/gh/Merphy0305/furry-art-assets@main/01/bg_loop.webp
```

注意事项：

- 路径区分大小写，文件名必须与仓库中完全一致。
- jsDelivr 会缓存，更新后可能要等一段时间才生效；需要立即看到改动时用 Raw 链接。
- 含中文或日文的文件名（如根目录的 mp4）需要做 URL 编码后再引用。

## 添加素材约定

- 文件放进对应文件夹，不要散落在根目录。
- 文件名只用小写英文、数字和下划线，方便拼接链接。
- 静态图优先用 `.webp`；有透明通道的图用 `.webp` 或 `.png`。
- 新增角色卡素材时，建议新建独立文件夹，并在本 README 的「文件夹用途」中补一段说明。
