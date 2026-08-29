# WWUIResourcesFull

完整 UI 纹理与文案资源 · 按类型分类
Complete UI texture and text resources, organized by type.

当前版本 · Current version: **3.6**

## 目录索引 Directory Index

```
Textures/
├── Activity/      12393  # 活动玩法图像 · event / activity images
├── Icon/           8185  # 图标（角色/武器/怪物/道具等）· icons
├── Other/          5340  # 其余 UI 纹理 · other UI textures
├── UI/             2933  # 通用界面组件 · generic UI components
├── Map/            2444  # 世界地图瓦片与迷雾 · world map tiles & fog
├── Atlas/          1859  # UI 图集 · texture atlases
├── Background/     1412  # 背景图 · background images
├── Spine/          1548  # 2D 骨骼动画工程 (.skel/.atlas/.png) · 2D skeletal animation projects
├── Role/            491  # 角色相关 UI · role-related UI
├── Share/           103  # 角色/武器分享大图 (2560×1440) · share cards
└── Card/             53  # 标题卡片背景 (388×72) · title card backgrounds

Text/
├── ConfigDB/             # 文案数据库 · text databases (SQLite)
│   ├── *.db        490   # 结构表 · structure tables
│   └── <lang>/     450   # 13 种语言 × 各语言文本表 · 13 languages
│       ├── de/ en/ es/ fr/ id/ ja/ ko/ pt/ ru/ th/ vi/ zh-Hans/ zh-Hant/
│       └── lang_multi_text.db   # 主文本表，zh-Hans 313,690 条 · main string table
├── Localization/    18   # 引擎本地化资源 (.locres) · engine localization
└── export/               # 可读导出 · readable exports
    ├── <lang>/
    │   ├── _index.md     # 表清单与条数 · table list & row counts
    │   └── help.md       # 帮助文案（标题 + 配图名 + 正文）· help pages
        ├── levelentity.jsonl # 关卡实体 206,046 条（不分语言）· level entities, language-neutral
    └── <lang>/raw/  179  # 每表一份 JSONL，按 id 排序 · one JSONL per table
```

## 说明 Notes

- `Text/ConfigDB/` 保持游戏内的原生目录结构与文件名，便于版本间比对。
  `Text/ConfigDB/` mirrors the in-game layout and filenames so versions diff cleanly.
- `Text/export/` 是从 ConfigDB 派生的可读格式，可随时重新生成。
  `Text/export/` is derived from ConfigDB and can be regenerated at any time.
- 帮助文案的配图在 `Textures/UI/Help/` 下，文件名与 `help.md` 中标注的一致。
  Help page illustrations live in `Textures/UI/Help/`, matching the names in `help.md`.
- `Text/ConfigDB/db_level_entity.db`（147 MB）超出单文件 100 MB 上限，未收录，
  但其内容已导出为 `Text/export/levelentity.jsonl`（206,046 条：实体类型、
  所属地图、关卡编辑器命名与 AI 状态标签）。该表不参与本地化，无多语言版本。
  `Text/ConfigDB/db_level_entity.db` (147 MB) exceeds the 100 MB per-file limit,
  so its contents are provided as `Text/export/levelentity.jsonl` instead
  (206,046 records: entity type, map, editor names and AI state tags).
  This table is not localized, so it has no per-language variants.

## 免责声明 Disclaimer

所有游戏资产版权归 **库洛游戏 (Kuro Games)** 所有。
All game assets are © **Kuro Games**.
