# Mesh RPG Craft

Doki 魔改网状 RPG 的锁序与踩坑：立绘 / alpha intro / 粒子、场景静帧与 idle loop、NPC 拍门控认知、导演只消费已闸内容、世界书与硬节点、GUI 数值绑定。

本 skill 管**锁序、停手标准、转交哪个生成器**，不重写 Imagine / PixVerse / 世界书的字段表。GitHub 技能能省时间，Doki 接线不能省。

```text
/mesh-rpg-craft
```

当前：**1.0.1**

## 安装

```bash
npx skills add luaproxy1993/mesh-rpg-craft -y
```

或：

```bash
./install.sh                  # ~/.grok/skills/mesh-rpg-craft
./install.sh --dir ~/.cursor/skills/mesh-rpg-craft
./install.sh --dir ~/.cursor/skills/mesh-rpg-craft --force
```

详见 `INSTALL.md`。打分享包：`./scripts/package.sh`。

## 它做什么

先锁主外观（一张图 + 一句话）。之后立绘轨（静帧 RGBA → alpha intro → 人设粒子叠层）和场景轨（静帧 → idle loop）可以并行。世界书与硬节点齐了，才写 NPC 拍门控卡；导演只读当前拍；GUI 数值只绑 flags。一层未过，下一层不开。

未锁主外观时禁止并行开特效。失败或未对齐的静帧 / 视频不得当下一稿参考，也不得拼进正片。

## 相关仓库

本包**不替代**生成器或出包门。请同时按需安装：

| 用途 | 仓库 |
|------|------|
| 世界书 / 核心规则书 | [world-bible](https://github.com/luaproxy1993/world-bible) |
| 角色、地图、地点美术包 | [world-bible-pack](https://github.com/luaproxy1993/world-bible-pack) |
| 一切口树与可玩 sitting | [rpg-campaign-maker](https://github.com/luaproxy1993/rpg-campaign-maker) |
| 卡带封装 | [doki-game-maker](https://github.com/luaproxy1993/doki-game-maker) |
| 出包质检 | [world-ship-qa](https://github.com/luaproxy1993/world-ship-qa) |

和 `/rpg-campaign-maker` 的接法见 `references/HANDOFF.md`。

## License

Skill text and scripts: use and modify. Do not ship other people's campaign books, official-book extracts, or secrets (`director.env`, API keys) in packs.
