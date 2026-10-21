# Talos Shader · Technical Preview

通用渲染器 **Talos Shader** 的技术预览版，面向 Koikatsu Sunshine CharaStudio。

This is a **technical preview** of **Talos Shader**, a general-purpose renderer for Koikatsu Sunshine CharaStudio.

**本预览仅开放部分已相对稳定的功能，其完成度、效果与稳定性均不代表正式版品质。** 功能、属性、界面与文件名在正式发布前仍可能调整。

**This preview only includes a subset of relatively stable features. It does not represent the quality, completeness, or stability of the full release.** Features, properties, UI and file names may still change.

当前预览包含九个角色的核心角色渲染流程：一键还原、光照预设、自阴影、展示舞台与调色。不含毛发壳、场景着色器及其他完整版功能。

This preview covers the core character pipeline for nine characters: one-click restore, lighting presets, self-shadow, overview stage, and colour grading. Hair shells, the scene renderer, and other full-release features are not included.

支持角色 / Supported characters: **罗茜 Rossi · 诀 Arcane · 杰尔佩塔 Gilberta · 提弗洛斯 Typhoea · 伊冯 Yvonne · 祀 Si · 梨诺 Liino · 莱万汀 Laevatain · 庄方宜 Zhuang Fangyi**

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

当前版本 / Current version: **v0.1.7fix**（2026-10-21）

插件与模组包 / Plugin & mod pack：[EndField_TechPreview_v0.1.7fix.zip](https://github.com/nekochan1122/TalosShader-TechPreview/releases/latest)

修复部分头模卡眉心附近的眉毛透过刘海的问题。已安装原 v0.1.7 的用户请重新下载主包并再次执行一键还原；材质包无需更新。

**本次只更新主包。已安装 v0.1.6 材质包的用户无需重新下载材质包。**
**Update only the main pack. Keep the v0.1.6 texture pack if already installed.**

```
aHR0cHM6Ly9nb2ZpbGUuaW8vZC95ZDNNTXdtdQ==
```

---

## 依赖 / Requirements

建议使用最新 BetterRepack 版 KKS。本预览需要以下配套插件；BetterRepack 通常已包含前四项。导入 FBX 时另需 AssetImport。

Use the latest BetterRepack build of KKS. This preview requires the following companion plugins; BetterRepack typically already includes the first four. AssetImport is additionally required to import FBX.

- **BepInEx 5**：[github.com/BepInEx/BepInEx](https://github.com/BepInEx/BepInEx)
- **BepisPlugins**（Sideloader、ExtensibleSaveFormat）：[github.com/IllusionMods/BepisPlugins](https://github.com/IllusionMods/BepisPlugins)
- **IllusionModdingAPI**（KKSAPI / KKAPI）：[github.com/IllusionMods/IllusionModdingAPI](https://github.com/IllusionMods/IllusionModdingAPI)
- **MaterialEditor**（KK_Plugins）：[github.com/IllusionMods/KK_Plugins](https://github.com/IllusionMods/KK_Plugins)
- **AssetImport**（导入 FBX，可选）：[github.com/Njaecha/AssetImport](https://github.com/Njaecha/AssetImport)

---

## 安装 / Install

首次安装需要 v0.1.7 主包和 v0.1.6 材质包。从 v0.1.6 更新只需换主包；从 v0.1.5 及更早版本更新，还需安装 v0.1.6 材质包。

A first installation requires the v0.1.7 main pack and v0.1.6 texture pack. Updating from v0.1.6 requires only the main pack. Users updating from v0.1.5 or earlier also need the v0.1.6 texture pack.

1. 关闭 KKS。运行中无法替换 zipmod。
2. 将 `mods` 中旧版本的 `[Talos] EndField.Shader.CharacterNPR TechPreview ...zipmod` 移到 `mods` 以外备份。不要只移到 `mods` 的子文件夹，Sideloader 仍会读到它。
3. 把主包解压到游戏根目录，允许合并文件夹；仅在尚未安装 v0.1.6 材质包时补装材质包。压缩包内容应直接合并到 `mods` 与 `BepInEx`。
4. 已还原过的角色卡，请再点一次 **Restore selected character**。

Close KKS first. Back up the previous CharacterNPR zipmod outside `mods`. Extract the v0.1.7 main pack into the game root; install the v0.1.6 texture pack only if missing. Run **Restore selected character** again on cards that were already restored.

MaterialEditor 请使用 **5.0 或更高版本**。过旧版本可能导致角色卡读档后恢复失败。
Use MaterialEditor **5.0 or later**. Older builds can fail to restore a character card on load.

本预览不提供游戏资产。请仅使用你依法享有授权的素材。
This preview does not provide game assets. Use only materials you are legally authorized to use.

---

## 使用 / Usage

**角色卡一键还原只支持 [pixiv 用户 26299334](https://www.pixiv.net/users/26299334) 的角色卡**，其他作者不保证服装识别、贴图和颜色正确。**预览版暂不包含正式版的脖子接缝修复**，使用头模时脸与脖子之间可能有接缝。

**One-click card restore only supports cards by [pixiv user 26299334](https://www.pixiv.net/users/26299334).** Outfit matching, textures and colours are not guaranteed for other authors. **The preview does not include the full version's neck seam fix.**

在 Studio 中按 **Ctrl+Shift+E** 打开窗口（标题为 Tech Preview）。

Press **Ctrl+Shift+E** in Studio. The window title reads Tech Preview.

1. 在窗口顶部选择角色。选中场景中的角色时会按名称尝试识别。
2. Setup 页确认**材质包已安装**。若提示贴图未安装，请先安装材质包后再继续。
3. 在 Workspace 中选中角色，点击 **Restore selected character**。
   - **KKS 角色卡**：按 UV 识别上述九个角色的服装部件，写入着色器与材质参数，并经 MaterialEditor 保存。
   - **FBX**（AssetImport，Alt+I）：额外绑定贴图。本预览**不附带模型或游戏资产**。
4. Lighting / Stage / Image 页可调整光照、展示舞台与调色。细节见窗口 Log 页。

一键可重复执行，结果不会叠加。

---

## v0.1.7

- 身体肤色调色：一键还原最后一步把角色卡身体贴图调到对应角色的游戏肤色，脸和头模不变；Setup 页 Body skin tone 可切换前后效果或重新调色，随场景保存。
- 地面阴影：Stage 页，默认开启，CharInfo 舞台地面接收角色主光阴影，可调柔和度。
- 接触阴影：Lighting 页，默认关闭，补充刘海、眼皮等细小近距离阴影，可独立于自阴影使用。
- 地面反射：Stage 页，默认关闭，仅作用于支持平面反射的材质，目前为提弗洛斯 cloth_07；游戏角色页没有此效果。
- 主包更新到 v0.1.7，材质包沿用 v0.1.6。

- Body skin tone: the final card restore step matches body texture colour to the character's game skin tone, leaving the face/head mod unchanged. Toggle or recalibrate in Setup; saved with the scene.
- Floor shadows: enabled by default in Stage, with adjustable softness on the CharInfo stage.
- Contact shadows: disabled by default in Lighting; adds fine bangs/eyelid shadows independently of self-shadow.
- Floor reflections: disabled by default in Stage, only for compatible materials (currently Typhoea cloth_07); absent from the game's character page.
- Update the main pack to v0.1.7; keep the v0.1.6 texture pack.

完整累计公告 / Full cumulative changelog: [Release v0.1.7](https://github.com/nekochan1122/TalosShader-TechPreview/releases/tag/v0.1.7)

## v0.1.6（含 v0.1.3–v0.1.5 更新 / Includes v0.1.3–v0.1.5）

- 新增庄方宜：材质、光照预设、角色页灯光和相机，现支持九个角色。
- 更新祀的模型数据、材质和角色页灯光；兼容祀与庄方宜旧版模型角色卡的贴图。
- 改进服装识别，支持眼睛与眉毛透过刘海及半透明发丝层，并遵循 KKS 显示设置。
- 修复重复一键后瞳孔消失、部分头模左右眼眼睑阴影偏移的问题。
- 修复 MaterialEditor 向量属性的显示与编辑兼容性。
- **主包和材质包均需更新到 v0.1.6。**

- Adds Zhuang Fangyi with material data, lighting presets, page lights and camera; nine characters are supported.
- Updates Si's model data, materials and page lights, with legacy texture support for Si and Zhuang Fangyi cards.
- Improves outfit matching and supports eyes/brows through bangs with a translucent hair layer, following KKS display settings.
- Fixes disappearing irises after repeated restore and asymmetric eyelid shadow alignment on some head mods.
- Fixes MaterialEditor vector property display/editing compatibility.
- **Update both packs to v0.1.6.**

## v0.1.2

- 新增共用角色反射（Lighting 页默认开启），减少昏暗场景中金属部位发黑的问题。
- 游戏网格保留原材质的描边方向设置，修复部分服装描边。
- 修复部分头模眼白遮挡瞳孔的问题。
- 贴图包沿用 v0.1.1，支持角色不变。

- Adds shared character reflections, enabled by default in Lighting, to prevent dark scene probes from dimming metallic parts.
- Preserves the original material's outline direction for matched game meshes.
- Fixes iris occlusion by the eye-white material on some head mods.
- Keeps the v0.1.1 texture pack and the same eight supported characters.

## v0.1.1

- 新增祀 Si、梨诺 Liino、莱万汀 Laevatain。梨诺与莱万汀包含角色页灯光和相机；祀没有专属页面灯光，相机使用通用机位。
- 同一衣服槽内的同名材质不再互相覆盖。
- 由长筒袜改成的丝袜，其连带的大腿皮肤按皮肤处理。
- 洛茜 Rossi 的兜帽披风可以正常匹配；耳内白毛恢复整簇受光。
- Setup 页新增 Shader zipmod 状态。显示 `not loaded` 时，通常是 zipmod 未放入 `mods`，或解压多了一层文件夹。

- Adds Si, Liino, and Laevatain. Liino and Laevatain include their page lights and cameras. Si has no dedicated page lights and uses the shared camera.
- Materials that share a name inside one clothing slot no longer overwrite each other.
- Thigh skin attached to stockings converted from the base hosiery is treated as skin.
- Rossi's hooded cape now matches, and the white fur inside her ears receives light as one cluster.
- Setup shows Shader zipmod status. `not loaded` usually means the zipmod is not in `mods`, or the archive was extracted with an extra folder.

## 预览范围 / Preview scope

本预览暂不包含：其余角色、毛发壳、场景着色器、脖子接缝修复、NPR 点光/聚光、后处理，以及完整版中的部分手动工具。预览效果不代表正式版品质。

Not included: the remaining characters, hair shells, scene shaders, neck seam repair, NPR point/spot lights, post-processing, and some full-release manual tools. Preview quality is not representative of the full release.
