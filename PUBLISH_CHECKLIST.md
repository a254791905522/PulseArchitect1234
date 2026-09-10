# Flick Kick Football — App Store 发布检查清单

> 基于 PUBLISH_CHECKLIST.md 模板，已替换为实际游戏信息。

---

## 项目信息

| 字段 | 值 |
|------|-----|
| App 名称 | `Flick Kick Football` |
| Bundle ID | `com.rosewood.game.flick_kick_football` |
| 版本号 | `1.0.0` |
| 构建号 | `1` |
| 版权 | `© 2026 Rosewood` |
| App Store Connect Team | 需在 Xcode 中确认 Team ID |

---

## 输出文件目录结构

```
publish/
├── index.html              # 游戏介绍页（全英文）
├── privacy.html            # 隐私政策页（全英文）
├── keywords.txt            # 关键词（≤100字符）
├── PUBLISH_CHECKLIST.md    # 本清单
├── screenshots_65/         # iPhone 6.5寸 (1284×2778)
│   ├── 01_menu.png
│   ├── 02_level_select.png
│   ├── 03_gameplay.png
│   ├── 04_goal.png
│   └── 05_gameover.png
└── screenshots_55/         # iPhone 5.5寸 (1242×2208)
    ├── 01_menu.png
    ├── 02_level_select.png
    ├── 03_gameplay.png
    ├── 04_goal.png
    └── 05_gameover.png
```

---

## 1. Archive 构建

### 构建命令
```bash
cd /Users/wxj/888ios/pre-good-game/flick_kick_football
xcodebuild -project GameFlickKickFootball.xcodeproj \
  -scheme GameFlickKickFootball \
  -configuration Release \
  clean archive \
  -archivePath build/GameFlickKickFootball.xcarchive
```

### Archive 检查清单
- [x] `PRODUCT_BUNDLE_IDENTIFIER` = `com.rosewood.game.flick_kick_football`
- [x] `CFBundleDisplayName` = `Flick Kick Football`（Info.plist 已添加）
- [x] App Icon 无 Alpha 通道（已转换为 RGB）
- [x] `ITSAppUsesNonExemptEncryption` = false（Info.plist + pbxproj 已设置）
- [x] `CFBundleIconName` = `AppIcon`（Info.plist 已添加）
- [x] `ASSETCATALOG_COMPILER_APPICON_NAME` = `AppIcon`（pbxproj 已修复）
- [ ] `DEVELOPMENT_TEAM` = 需在 Xcode 中设置你的开发者团队

---

## 2. 上传方式

### Transporter（推荐）
1. Mac App Store 下载 Transporter
2. 打开后拖入 `.xcarchive` 文件
3. 点击 Deliver

---

## 3. App Store Connect 填写规范

### 基本信息

| 字段 | 填写内容 |
|------|---------|
| App 名称 | `Flick Kick Football` |
| 副标题 | `Swipe to Shoot & Score Goals` |
| 主语言 | `English` |
| Bundle ID | `com.rosewood.game.flick_kick_football` |
| 版本号 | `1.0.0` |
| 隐私政策 URL | 需部署 privacy.html 后填入 |

### 关键词（94字符）
```
football,soccer,kick,flick,shoot,goal,penalty,freekick,sports,casual,physics,arcade,strike,scoring,challenge
```

### 推广文本（170字符）
```
Master the art of the free kick! Swipe to curve the ball past walls and goalkeepers in 50 challenging levels. No ads, no IAP — pure football action.
```

### 描述
```
Flick Kick Football puts you in control of every free kick. Swipe your finger to determine power, direction, and spin — then watch the ball bend around defensive walls and past diving goalkeepers.

MASTER THE SWIPE
The intuitive flick control lets you aim precisely while adding curl to your shots. Longer swipes mean more power; sideways movement creates curve. Simple to learn, impossible to put down.

50 LEVELS OF CHALLENGE
Progress through 5 difficulty tiers, from easy warm-ups to master-level tests. Each level features unique arrangements of walls, goalkeeper skill levels, and environmental effects like crosswinds.

EARN YOUR STARS
Score goals to earn up to 3 stars per level. Miss too many shots and you'll need to retry. Can you achieve a perfect 150-star record across all 50 levels?

REALISTIC PHYSICS
The ball reacts to your swipe with realistic trajectory physics. Curve shots around walls, chip over the goalkeeper, or blast it into the top corner. Every goal feels earned.

IMMERSIVE SOUND
Hear the satisfying thwack of your boot, the roar when you score, and the referee's whistle between rounds. Stadium atmosphere in your pocket.

KEY FEATURES:
• Intuitive swipe-to-shoot controls with realistic physics
• 50 levels across 5 difficulty tiers (Tutorial to Master)
• Dynamic obstacles: walls, wind, and agile goalkeepers
• Star rating system with level unlock progression
• Full offline play — no internet required
• Zero ads, zero in-app purchases
• Immersive stadium sound effects
• Supports iPhone and iPad
```

### 版权
```
© 2026 Rosewood
```

### 审核备注
```
This is a single-player football game with no login, no ads, no in-app purchases, and no data collection. All 50 levels are playable offline. To test: tap "Start Game" on the main menu, select any level, then swipe upward on the screen to shoot the ball toward the goal.
```

---

## 4. 加密文稿

| 字段 | 选择 |
|------|------|
| 你的 App 是否使用加密？ | **否** |

---

## 5. 截图规格

### 已生成尺寸

| 类型 | 尺寸 | 文件夹 | 数量 |
|------|------|--------|------|
| iPhone 6.5寸 | 1284×2778 px | `screenshots_65/` | 5 张 |
| iPhone 5.5寸 | 1242×2208 px | `screenshots_55/` | 5 张 |

### 截图内容
1. **01_menu.png** — 主菜单画面（标题 + TAP TO START）
2. **02_level_select.png** — 关卡选择界面（星级网格）
3. **03_gameplay.png** — 核心玩法画面（射门瞬间）
4. **04_goal.png** — 进球庆祝画面（GOAL!）
5. **05_gameover.png** — 结算画面（星级评分）

---

## 6. 隐私政策

- **类型**：纯单机无广告
- **声明**：不收集、不存储、不传输任何个人信息
- **无第三方服务**：无广告 SDK、无分析工具、无内购
- **儿童隐私**：适合所有年龄用户
- **文件**：`privacy.html`（全英文，已生成）

---

## 7. 游戏介绍页

- **文件**：`index.html`（全英文，已生成）
- **用途**：App Store 外展使用
- **包含**：游戏截图、功能特性、描述、应用信息

---

## 8. 提交流程

1. [x] 准备输出文件目录（截图 + index.html + privacy.html）
2. [ ] 部署 privacy.html 到可访问 URL
3. [ ] 在 Xcode 中设置 DEVELOPMENT_TEAM
4. [ ] 执行 Archive 构建并验证检查清单
5. [ ] 通过 Transporter 上传 `.xcarchive`
6. [ ] 登录 App Store Connect
7. [ ] 我的 App → 新建 App（名称 + Bundle ID）
8. [ ] 填写基本信息（名称、关键词、描述等）
9. [ ] 上传截图（6.5寸 + 5.5寸）
10. [ ] 填写加密文稿（选"否"）
11. [ ] 填写隐私政策 URL
12. [ ] 提交审核

---

## 9. 快速复制汇总

| 字段 | 内容 |
|------|------|
| **App 名称** | `Flick Kick Football` |
| **副标题** | `Swipe to Shoot & Score Goals` |
| **Bundle ID** | `com.rosewood.game.flick_kick_football` |
| **版本号** | `1.0.0` |
| **版权** | `© 2026 Rosewood` |
| **关键词** | `football,soccer,kick,flick,shoot,goal,penalty,freekick,sports,casual,physics,arcade,strike,scoring,challenge` |
| **隐私政策** | 待部署后填入 URL |
| **加密** | 否（离线游戏） |
| **Build** | `GameFlickKickFootball.xcarchive` |
