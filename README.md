# Talos Shader · Technical Preview

通用渲染器 **Talos Shader** 的技术预览版，面向 Koikatsu Sunshine CharaStudio。

This is a **technical preview** of **Talos Shader**, a general-purpose renderer for Koikatsu Sunshine CharaStudio. Features, properties, UI and file names may still change before a full release.

当前预览仅包含五个角色的核心角色渲染流程：一键还原、光照预设、自阴影、展示舞台与调色。不含毛发壳、场景着色器及其他完整版功能。

This preview covers the core character pipeline for five characters: one-click restore, lighting presets, self-shadow, overview stage, and colour grading. Hair shells, the scene renderer, and other full-release features are not included.

支持角色 / Supported characters: **罗茜 Rossi · 诀 Arcane · 杰尔佩塔 Gilberta · 提弗洛斯 Typhoea · 伊冯 Yvonne**

---

## 下载 / Downloads

预览版分为两个包，**都需要安装**。

Both packages are required.

| 包 / Package | 内容 / Contents | 获取 / Get |
|---|---|---|
| 插件与模组包 / Plugin & mod pack | 着色器 zipmod、展示舞台 zipmod、Studio 插件 | [GitHub Releases](https://github.com/nekochan1122/TalosShader-TechPreview/releases/latest) |
| 材质包 / Texture pack | 五个角色的贴图与公共贴图 | [gofile](https://gofile.io/d/lf6eB1tN) |

当前版本 / Current version: **v0.1.0**（2026-10-01）

- 插件与模组包：[`Talos_Shader_TechPreview_v0.1.0.zip`](https://github.com/nekochan1122/TalosShader-TechPreview/releases/latest)
- 材质包：<https://gofile.io/d/lf6eB1tN>

以后若只更新插件或着色器，通常只需更换插件与模组包。材质包仅在贴图变更时更新。

---

## 依赖 / Requirements

- Koikatsu Sunshine BetterRepack（含 BepInEx、KKAPI、Sideloader、MaterialEditor）
- 导入 FBX 时需要 AssetImport

---

## 安装 / Install

1. 关闭 KKS。运行中无法替换 zipmod。
2. 将两个压缩包中的 `mods` 与 `BepInEx` 解压到游戏根目录，允许合并文件夹。
3. 更新时先删除 `mods/MyMods` 里的旧版 `[Talos] ... CharacterNPR ...zipmod`。同时只能保留一份；移到 `mods` 的子目录不算删除。

Close KKS first. Extract the `mods` and `BepInEx` folders from both archives into the game root, merging folders. When updating, remove the previous CharacterNPR zipmod from `mods/MyMods`. Sideloader scans subfolders recursively.

---

## 使用 / Usage

在 Studio 中按 **Ctrl+Shift+E** 打开窗口（标题为 Tech Preview）。

Press **Ctrl+Shift+E** in Studio. The window title reads Tech Preview.

1. 在窗口顶部选择角色。选中场景中的角色时会按名称尝试识别。
2. Setup 页确认材质包已安装。若提示贴图未安装，请解压材质包。
3. 在 Workspace 中选中角色，点击 **Restore selected character**。
   - **KKS 角色卡**：按 UV 识别上述五个角色的服装部件，写入着色器与材质参数，并经 MaterialEditor 保存。
   - **FBX**（AssetImport，Alt+I）：额外绑定贴图。本预览**不附带模型**。
4. Lighting / Stage / Image 页可调整光照、展示舞台与调色。细节见窗口 Log 页。

一键可重复执行，结果不会叠加。

---

## 预览范围 / Preview scope

本预览暂不包含：其他角色、毛发壳、场景着色器、地面阴影与反射、NPR 点光/聚光、后处理，以及完整版中的部分手动工具。

Not included: other characters, hair shells, scene shaders, floor shadows/reflections, NPR point/spot lights, post-processing, and some full-release manual tools.

描边平滑法线与头部朝向不随场景存档，读档后由插件自动重建。

---

## 说明 / Notes

本项目为非官方爱好者作品。请仅使用你拥有合法授权的素材。公开的 R18 用途须自行遵守所在地法律与各平台条款。

This is an unofficial fan project. Use only materials you are legally authorized to use. Public R18 use remains your responsibility under applicable law and platform terms.
