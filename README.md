# LLM Hub 🤖

**LLM Hub** 是一款开源的移动应用，支持在设备上运行 LLM 聊天和图像生成，适用于 **Android** 和 **iOS** 平台。它针对移动设备进行了优化（支持 CPU/GPU/NPU 加速），并支持多种模型格式，让你可以在本地私密地运行强大的 AI 模型。

## 下载

<table>
  <tr>
    <td valign="center">
      <a href="https://play.google.com/store/apps/details?id=com.llmhub.llmhub"><img src="https://play.google.com/intl/zh-CN/badges/static/images/badges/zh_badge_web_generic.png" height="75"></a>
    </td>
    <td valign="center">
      <a href="https://apps.apple.com/au/app/llm-hub/id6762511820"><img src="https://developer.apple.com/app-store/marketing/guidelines/images/badge-download-on-the-app-store.svg" height="50"></a>
    </td>
  </tr>
</table>


## 📸 截图

<div style="display:flex;gap:12px;flex-wrap:wrap;align-items:flex-start;">
   <figure style="margin:0;flex:0 1 300px;max-width:300px;text-align:center">
      <img src="android/assets/screenshots/Screenshot_20260214_201455.png" alt="AI 功能" style="width:300px;height:auto;border-radius:8px;display:block;" />
   </figure>
   <figure style="margin:0;flex:0 1 300px;max-width:300px;text-align:center">
      <img src="android/assets/screenshots/Screenshot_20251007_042114_LLM%20Hub.jpg" alt="聊天界面" style="width:300px;height:auto;border-radius:8px;display:block;" />
   </figure>
   <figure style="margin:0;flex:0 1 300px;max-width:300px;text-align:center">
      <img src="android/assets/screenshots/Screenshot_20251007_042146_LLM%20Hub.jpg" alt="聊天界面 2" style="width:300px;height:auto;border-radius:8px;display:block;" />
   </figure>
</div>

## 🚀 功能特性

### 🛠️ AI 工具套件
| 工具 | 描述 |
|------|------|
| **💬 聊天** | 支持多轮对话、RAG 记忆、网页搜索、TTS 自动朗读和多模态输入 |
| **🤖 creAItor** | **[新增]** 秒速创建自定义 AI 角色，支持专业系统提示词（PCTF 格式） |
| **💻 Vibe Coder** | **[新增]** 描述你的应用想法，实时生成 HTML/JS 代码并预览 |
| **✍️ 写作助手** | 摘要、扩写、重写、语法改进或根据描述生成代码 |
| **🎨 图像生成器** | 使用 Stable Diffusion 1.5 从文本提示创建图像，支持滑动画廊 |
| **🌍 翻译器** | 支持 50+ 语言的文本、图像（OCR）和音频翻译 - 离线可用 |
| **🎙️ 语音转文字** | 设备端处理语音转文字 |
| **🛡️ 诈骗检测器** | 分析消息和图像中的网络钓鱼风险 |

### ✨ Vibes & Creators
- **Vibes**: 完整的设备端编码环境。LLM 根据你的需求编写 HTML/JS/CSS，你可以在安全沙箱中即时预览/运行应用。
- **creAItor**: 强大的角色生成功能，可以创建从有趣个性角色到系统架构师的任何内容。只需描述一个角色（如"像海盗一样回应"或"用 markdown 规范描述一个代码代理来生成全栈系统"），设备端 LLM 会生成复杂的系统提示词（PCTF 格式）供你在聊天中使用。

### 👶 儿童模式
在设置中激活儿童模式，设置 PIN 码后，模式将保持生效直到用相同 PIN 码解锁。
- **安全探索**: 家庭可以放心地向孩子介绍私密的本地 AI。
- **模型级保护**: 自动在**所有**工具（聊天、写作助手、图像生成等）的模型推理层激活严格的安全协议。
- **安心使用**: 确保所有生成内容适合年龄，同时不影响设备端处理的隐私优势。

### 🔐 隐私优先
- **100% 设备端处理** - 推理无需联网
- **零数据收集** - 对话永不离开你的设备
- **无需账户，无追踪** - 完全私密
- **开源** - 完全透明

### ⚡ 高级功能
- GPU/NPU 加速，性能更快
- 文本转语音自动朗读
- RAG 全局记忆增强响应
- 支持导入自定义模型（.task, .litertlm, .qnn, .mnn, .gguf）
- 直接从 HF Mirror 下载模型
- 支持 16 种语言界面（新增中文支持）

## 快速开始
1. 从 **Google Play** 或 **App Store** 下载，或从源码构建
2. 打开设置 → 下载模型 → 下载或导入模型
3. 选择模型并开始聊天或生成图像

## 支持的模型系列（摘要）
- Gemma (LiteRT Task)
- Llama (Task + GGUF 变体)
- Phi (LiteRT LM)
- LiquidAI LFM (LFM 2.5 1.2B + LFM VL 1.6B 支持视觉)
- Ministral / Mistral 系列 (GGUF / ONNX)
- IBM Granite (GGUF)
- **新增**: Gemma-4 去审查系列模型（适合手机使用）

## 模型格式
- Task / LiteRT (.task): MediaPipe/LiteRT 优化模型（支持 GPU/NPU）
- LiteRT LM (.litertlm): LiteRT 语言模型
- GGUF (.gguf): 量化模型 — 由 Nexa SDK 提供 CPU 推理；部分支持视觉的 GGUF 模型需要额外的 `mmproj` 视觉投影文件
- ONNX (.onnx): 跨平台模型运行时

## GGUF 兼容性说明
- 并非所有 Android 设备都能加载 GGUF 模型
- GGUF 加载/运行时依赖 Nexa SDK 原生库和设备/ABI 支持；在不支持的设备上，即使模型文件有效，GGUF 模型加载也可能失败
- 在本应用中，GGUF NPU 选项仅对 Snapdragon 8 Gen 4 级别的设备显示

## 导入模型
- 设置 → 下载模型 → 导入模型 → 选择 `.task`, `.litertlm`, `.qnn`, `.gguf`, 或 `.mnn` 文件
- 完整的模型列表和下载链接位于 `app/src/.../data/ModelData.kt`（不要在 README 中详尽列出所有变体）

## 今日更新内容（2026-04-28）

### 1. 新增功能
- ✅ 添加中文语言支持，语言选择界面显示"简体中文"
- ✅ 解锁所有高级功能（无需付费即可使用网络搜索、全局记忆、自动朗读等）

### 2. 模型更新
- ✅ 将所有模型下载源从 HuggingFace 改为 **HF Mirror** (`https://hf-mirror.com`)，国内用户下载更快
- ✅ 新增 Gemma-4 去审查系列模型（适合手机使用）：
  - Gemma-4 E2B Uncensored (~1.5GB, 6GB+ RAM)
  - Gemma-4 E4B Uncensored (~3GB, 8GB+ RAM)
  - Gemma-4 E2B JANG_4M Crack (~1.5GB, 6GB+ RAM)
  - Gemma-4 E2B Uncensored Aggressive (~1.5GB, 6GB+ RAM)
  - Gemma-4 E2B Obliterated (~1.5GB, 6GB+ RAM)
- ✅ 添加 DeepSeek-V4 Flash 模型（~10GB, 12GB+ RAM）
- ✅ 移除超过 20B 参数的大型模型（不适合手机使用）

### 3. 技术优化
- ✅ 修复 ONNX Runtime 重复库冲突问题
- ✅ 更新 GitHub Actions 工作流，支持 Node.js 24
- ✅ 优化构建配置，确保所有语言版本功能一致

## 技术栈
- **Android**: Kotlin + Jetpack Compose (Material 3)
- **iOS**: Swift + SwiftUI, Run Anywhere SDK, Apple Foundation Model
- **LLM Runtime**: MediaPipe, LiteRT, Nexa SDK, Llama.cpp (via Run Anywhere)
- **图像生成**: MNN / Qualcomm QNN
- **量化**: INT4/INT8/MLX (Apple Foundation Model)

## 致谢
- **Nexa SDK** — GGUF 模型推理支持（应用内关于页面显示致谢）⚡
- **Google, Meta, Microsoft, IBM, LiquidAI, Mistral, HuggingFace** — 模型和工具贡献
- **HF Mirror** — 国内镜像服务，加速模型下载

## 开发环境搭建

### Android 本地开发（Android Studio + Gradle）
```bash
git clone https://github.com/huxu7755/LLM-Hub.git
cd LLM-Hub/android
./gradlew assembleDebug
./gradlew installDebug
```

### Android 本地配置

#### 设置 Hugging Face Token（开发用）
要使用私有或 gated 模型，请将你的 HuggingFace token 添加到 `android/local.properties`（不要提交此文件）：
```properties
HF_TOKEN=hf_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```
保存并在 Android Studio 中同步 Gradle；应用将在构建时读取 `BuildConfig.HF_TOKEN`。

#### 开发高级版标志
要跳过广告并在本地解锁所有高级功能（无需真实 IAP 购买），请在 `android/local.properties` 中添加：
```properties
DEBUG_PREMIUM=true
```
在构建生产版本前请设置回 `false`。

#### 模型许可接受
HuggingFace 上的某些模型（特别是 Google 和 Meta 的模型）需要明确接受许可才能下载。在本地构建应用时：

1. 确保在 `local.properties` 中有有效的 HuggingFace 读取 token（见上文）
2. **对于每个要下载的模型：**
   - 访问模型的 HuggingFace 页面（例如 https://huggingface.co/google/gemma-3n-E2B-it-litert-lm）
   - 点击"Access repository"或许可接受按钮
   - 同意模型的许可条款
   - 再次尝试在应用中下载模型

**注意：** 这仅适用于本地开发构建。Play Store 版本使用不同的身份验证，不需要为每个模型手动接受许可。

### iOS 本地开发（macOS + Xcode）

#### 前提条件
- 安装 Xcode 的 macOS（使用与你的 iOS 设备版本匹配的版本）
- 在 Xcode 中登录 Apple ID（免费个人团队适用于本地设备测试）
- 如果在真机上运行，需在 iPhone 上启用开发者模式

#### 在 iPhone 上构建和运行
1. 克隆仓库并打开 iOS 项目：
```bash
git clone https://github.com/huxu7755/LLM-Hub.git
cd LLM-Hub
open ios/LLMHub/LLMHub.xcodeproj
```
2. 在 Xcode 中，选择目标 **LLMHub** → **Signing & Capabilities**：
   - 设置你的 **Team**
   - 设置唯一的 **Bundle Identifier**（例如：`com.yourname.llmhub`）
   - 保持 **Automatically manage signing** 启用
3. 选择你的 iPhone 作为运行目标并按 **Run**。

#### 如果使用 Xcode beta
如果你的手机运行较新的 iOS 版本并需要 Xcode beta 支持，请切换 CLI 工具：
```bash
sudo xcode-select -s /Applications/Xcode-beta.app/Contents/Developer
xcodebuild -version
```

#### iOS 开发故障排除
- 如果签名失败，请重新检查目标设置中的 Team + Bundle Identifier
- 如果构建缓存过期，请清理 DerivedData：
```bash
rm -rf ~/Library/Developer/Xcode/DerivedData/LLMHub-*
```
- 构建日志：**Report Navigator** (`Cmd+9`)
- 运行时日志：**Debug Console** (`Cmd+Shift+Y`)

## 贡献
- Fork → 创建分支 → 提交 PR。请参阅 CONTRIBUTING.md（如有疑问可开 issue 或讨论）。

## 许可证
- 源代码采用 [PolyForm Noncommercial License 1.0.0](LICENSE) 许可。
- 你可以免费使用、学习和基于此项目进行非商业目的的开发。

## 支持
- Issues & Discussions: GitHub

## 说明
- 本 README 有意保持简洁 — 有关确切的模型变体、大小和格式详情，请查阅 `ModelData.kt`。

## 版权声明
本项目是基于 [timmyy123/LLM-Hub](https://github.com/timmyy123/LLM-Hub) 修改的衍生版本。感谢原作者的开源贡献。

## Star 历史

[![Star History Chart](https://api.star-history.com/svg?repos=huxu7755/LLM-Hub&type=date&legend=top-left)](https://www.star-history.com/#huxu7755/LLM-Hub&type=date&legend=top-left)
