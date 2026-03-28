# Unity Shader - Sci-Fi Energy Shield Dome

## 项目简介

这是一个基于 **Unity Shader** 实现的科幻风格能量护盾效果项目。  
项目通过六边形网格、边缘发光、透明叠加与整体穹顶造型，构建出具有未来科技感的 **半球形能量屏障** 视觉表现。

该效果适用于以下场景：

- 科幻游戏中的防护罩 / 基地屏障
- 技能释放时的范围护盾特效
- 场景中的能量结界、隔离区域
- 未来科技风 UI / 展示类 Shader 作品集项目

---

## 效果展示

> 目效果图 / GIF

<img width="1920" height="872" alt="image" src="https://github.com/user-attachments/assets/0001ff15-0af6-471c-a569-29353b7fdd22" />
![ezgif-83e6bd3c7181148c](https://github.com/user-attachments/assets/1cb75b98-a169-4b9a-a511-38c01e58a211)



---

## 项目亮点

- 实现了 **半球形能量护盾** 的整体视觉效果
- 使用 **六边形网格纹理/图案** 强化科技感
- 通过 **发光效果（Emission）** 提升视觉冲击力
- 支持 **透明材质叠加**，增强能量屏障质感
- 效果适合直接拓展为游戏中的护盾、结界、护罩类功能
- 项目结构清晰，适合作为 **Unity Shader 学习与作品集展示项目**

---

## 技术实现思路

该项目的核心实现可以拆分为以下几个部分：

### 1. 基础形体

以半球体或球体模型作为载体，将 Shader 挂载到模型材质上，实现整体护盾的空间表现。

### 2. 六边形图案生成/采样

通过纹理采样或程序化图案生成，在表面形成规则的六边形网格，使护盾具有明显的科幻结构感。

### 3. 边缘高亮

利用视角方向与法线方向的关系，计算边缘区域的高亮强度，形成常见的 **Fresnel 边缘发光效果**，让护盾轮廓更加突出。

### 4. 发光与透明混合

结合颜色、透明度和自发光参数，让网格线条在视觉上呈现出“能量流动”与“发亮”的感觉。

### 5. 可拓展动态效果

在当前基础上，还可以继续扩展：

- 护盾被击中时的波纹扩散
- 扫描线流动
- 呼吸闪烁
- 护盾生成/消失动画
- 根据时间驱动噪声扰动

---

## Shader 核心特点

本项目重点体现了以下 Shader 表现能力：

- **透明渲染**
- **自发光控制**
- **边缘光（Fresnel）**
- **图案重复采样**
- **科幻风材质表达**
- **适合作品集展示的视觉包装**

---

## 适用技术环境

- **Unity**：推荐 Unity 2021+ / Unity 6 均可
- **渲染管线**：可根据实际项目适配 Built-in / URP
- **开发语言**：ShaderLab / HLSL
- **平台**：PC

> 如果你项目使用的是 URP 或 Shader Graph，也可以把这里改成对应版本说明。

---

## 使用方法

1. 打开 Unity 项目
2. 导入 Shader、材质与对应模型资源
3. 将材质赋给球体或半球体模型
4. 调整以下参数以获得不同视觉效果：
   - 主颜色（Tint Color）
   - 发光强度（Emission Intensity）
   - 透明度（Alpha）
   - 六边形图案密度（Hex Tiling）
   - 边缘光强度（Fresnel Power）
5. 运行场景，查看护盾效果

---

## 参数说明（示例）

| 参数名 | 作用 |
|---|---|
| Tint Color | 控制护盾整体颜色 |
| Hex Texture / Pattern | 控制六边形网格图案 |
| Emission Intensity | 控制发光亮度 |
| Alpha | 控制透明程度 |
| Fresnel Power | 控制边缘高亮范围 |
| Tiling | 控制图案密度 |
| Speed | 控制动态流动速度（如有） |

---

## 项目结构示例

```text
Assets
├── Materials
│   └── Shield_Mat.mat
├── Shaders
│   └── EnergyShield.shader
├── Scenes
│   └── Demo.unity
├── Textures
│   └── HexPattern.png
└── Prefabs
    └── ShieldDome.prefab
