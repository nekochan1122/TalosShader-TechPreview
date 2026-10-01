# Talos Shader · Technical Preview

通用渲染器 **Talos Shader** 的技术预览版，面向 Koikatsu Sunshine CharaStudio。

This is a **technical preview** of **Talos Shader**, a general-purpose renderer for Koikatsu Sunshine CharaStudio.

**本预览仅开放部分已相对稳定的功能，其完成度、效果与稳定性均不代表正式版品质。** 功能、属性、界面与文件名在正式发布前仍可能调整。

**This preview only includes a subset of relatively stable features. It does not represent the quality, completeness, or stability of the full release.** Features, properties, UI and file names may still change.

当前预览包含五个角色的核心角色渲染流程：一键还原、光照预设、自阴影、展示舞台与调色。不含毛发壳、场景着色器及其他完整版功能。

This preview covers the core character pipeline for five characters: one-click restore, lighting presets, self-shadow, overview stage, and colour grading. Hair shells, the scene renderer, and other full-release features are not included.

支持角色 / Supported characters: **罗茜 Rossi · 诀 Arcane · 杰尔佩塔 Gilberta · 提弗洛斯 Typhoea · 伊冯 Yvonne**

---

## 免责声明 / Disclaimer

**所有内容仅供学习使用。禁止公开发布使用本渲染器制作的 R18 视频。**

**All content is for study only. Do not publicly publish R18 videos produced with this renderer.**

- 本项目**不提供游戏资产**，亦不提供、不附带、不传播任何受版权保护的第三方内容。请仅使用你依法享有授权的素材。
- **禁止公开发布使用 Talos Shader 制作的 R18 视频。**
- **本预览仅开放部分已相对稳定的功能，不代表正式版品质。**
- 你须对自身素材、产出与发布行为承担全部责任。使用、发布或分发即视为同意本声明。

- This project **does not provide game assets**, and does not provide, bundle, or distribute copyrighted third-party content. Use only materials you are legally authorized to use.
- **Do not publicly publish R18 videos produced with Talos Shader.**
- **This preview only includes some relatively stable features and does not represent full-release quality.**
- You are solely responsible for your assets, outputs, and publications. By using, publishing, or distributing these materials, you agree to this disclaimer.

---

## 下载 / Downloads

当前版本 / Current version: **v0.1.0**（2026-10-01）

插件与模组包 / Plugin & mod pack：[Talos_Shader_TechPreview_v0.1.0.zip](https://github.com/nekochan1122/TalosShader-TechPreview/releases/latest)

`
aHR0cHM6Ly9nb2ZpbGUuaW8vZC9sZjZlQjF0Tg==
`

---

## 依赖 / Requirements

- Koikatsu Sunshine BetterRepack（含 BepInEx、KKAPI、Sideloader、MaterialEditor）
- 导入 FBX 时需要 AssetImport

---

## 安装 / Install

插件与模组包、材质包**都需要安装**。 Both the plugin/mod pack and the texture pack are required.

1. 关闭 KKS。运行中无法替换 zipmod。
2. 将插件与模组包、材质包中的 mods 与 BepInEx 解压到游戏根目录，允许合并文件夹。

Close KKS first. Extract the mods and BepInEx folders from **both** archives into the game root, merging folders. When updating, remove the previous CharacterNPR zipmod from mods/MyMods. Sideloader scans subfolders recursively.

本预览不提供游戏资产。请仅使用你依法享有授权的素材。
This preview does not provide game assets. Use only materials you are legally authorized to use.

---

## 使用 / Usage

在 Studio 中按 **Ctrl+Shift+E** 打开窗口（标题为 Tech Preview）。

Press **Ctrl+Shift+E** in Studio. The window title reads Tech Preview.

1. 在窗口顶部选择角色。选中场景中的角色时会按名称尝试识别。
2. Setup 页确认**材质包已安装**。若提示贴图未安装，请先安装材质包后再继续。
3. 在 Workspace 中选中角色，点击 **Restore selected character**。
   - **KKS 角色卡**：按 UV 识别上述五个角色的服装部件，写入着色器与材质参数，并经 MaterialEditor 保存。
   - **FBX**（AssetImport，Alt+I）：额外绑定贴图。本预览**不附带模型或游戏资产**。
4. Lighting / Stage / Image 页可调整光照、展示舞台与调色。细节见窗口 Log 页。

一键可重复执行，结果不会叠加。

---

## 预览范围 / Preview scope

本预览暂不包含：其他角色、毛发壳、场景着色器、地面阴影与反射、NPR 点光/聚光、后处理，以及完整版中的部分手动工具。预览效果不代表正式版品质。

Not included: other characters, hair shells, scene shaders, floor shadows/reflections, NPR point/spot lights, post-processing, and some full-release manual tools. Preview quality is not representative of the full release.
