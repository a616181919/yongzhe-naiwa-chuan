# 勇者奶蛙传 · 憋笑魔王与豆公主

> 一肚子撞进城堡，一口气笑翻魔王。

完整 H5 网页游戏镜像，Phaser 3 制作，原生 Canvas 渲染。免安装、免下载，手机电脑打开即玩。

## 在线试玩

**https://a616181919.github.io/yongzhe-naiwa-chuan/**

## 游戏内容

七章冒险，从奶笑村一路打到无声王座：

| 章节 | 场景 | 波次 |
| --- | --- | --- |
| CHAPTER 01 | 奶笑村 | 5 / 8 |
| CHAPTER 02 | 咕咚小径 | 7 / 11 |
| CHAPTER 03 | 刀盾山道 | 9 / 13 / 17 |
| CHAPTER 04 | 风暴断桥 | 10 / 14 / 18 |
| CHAPTER 05 | 禁声墙堡 | 11 / 16 / 21 |
| CHAPTER 06 | 肃静大殿 | 12 / 17 / 23 |
| CHAPTER 07 | 无声王座 | BOSS 战 |

### 操作

- **移动**：`W A S D` 前后走位
- **攻击**：按住 `F` 连续直射奶球，松手停止
- **防御**：按住 `空格`
- **助阵**：`V` 呼叫奶蛋
- **大招**：捧腹大笑清场
- 手机端为触屏虚拟按键

### 敌人与 BOSS

探路小兵、盾卫、摇铃僧、弹琴小丑、宝箱怪、重锤怪、冰霜书吏、刀盾狗、企鹅（含狂暴态）；
四位 BOSS 均有二阶段变身与专属弹幕：铁桶队长、裂甲将军、缄默大元帅、憋笑魔王。

### 其他

- 大笑能量槽、奶蛙血条、奶球升级（自动追击 / 防御强化两档）
- 进度保存在浏览器本机
- 支持全屏、静音、暂停

## 技术说明

这是原站 Vite 构建产物的**完整镜像**，非重写：

- `index.html` — 入口
- `assets/game-*.js` / `assets/game-*.css` — 主包
- `assets/main-*.js` — 游戏逻辑（含资源清单与 SHA-256 完整性校验表）
- `assets/phaser-*.js` — Phaser 3 引擎
- `assets/backgrounds/` — 7 张场景背景 + 牢笼遮罩
- `assets/characters/` — 24 张角色立绘 + 17 张轮廓线稿 + 16 张 BOSS 变体
- `assets/audio/` — 8 段音频（主题曲、大笑、企鹅狂暴、奶蛋连招等）
- `assets/channels/` — 故事封面
- `manifest.json` / `favicon.svg` — PWA 清单与图标

全部 74 张图片均通过原站内置的 SHA-256 校验（74/74 一致）。

## 部署

纯静态站点，无构建步骤。克隆后任意静态服务器即可运行：

```bash
git clone https://github.com/a616181919/yongzhe-naiwa-chuan.git
cd yongzhe-naiwa-chuan
python -m http.server 8000
# 打开 http://127.0.0.1:8000
```

> 需通过 HTTP 访问，直接双击 `index.html` 会因 CORS 与前端路由限制无法加载。

## 声明

仅供学习与个人存档交流，游戏美术、音频与代码版权归原作者所有。
