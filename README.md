# 庭院保卫战 · PVZ Web

基于 PVZ GOTY 逆向重建项目参数的独立 JavaScript / Canvas 网页游戏。

在线试玩：https://xianfeng01010.github.io/pvz-web/

## 玩法

选择植物后点击草坪种植，点击阳光收集。四种植物、三类僵尸、五波挑战，每行各有一次割草机救援。

快捷键：1–4 选植物，5 铲子，空格暂停，Esc 取消。

## 本地运行

直接打开 index.html，或运行 `python3 -m http.server 8765` 后访问 http://localhost:8765 。无需联网或安装依赖。

## 来源与边界

参数参考 Patoke/re-plants-vs-zombies 的 Plant.cpp、Zombie.cpp、Projectile.cpp：植物价格 50/100/50/175、基础生命值 300、坚果 4000、豌豆伤害 20、普通僵尸 270 血，路障/铁桶额外护甲 370/1100。

REA 已核验本地自行编译的 Windows PE，SHA-256 为 8405daef4fce998008cdeb1124496d77876c86c4727d15a0536ec97dac887be8；这不是官方原版二进制的反编译结果。

游戏逻辑为独立 Web 实现，画面为新绘 SVG/Canvas。没有包含原版贴图、音乐、音效或骨骼动画。关卡节奏与布局是本项目设计，不保证与原版一致。目前没有选关、夜晚/泳池、图鉴、商店或存档。

## 验证

通过真实 Chromium 浏览器检查：种植扣费、暂停、命中、割草机、胜负状态及手机宽度布局。胜负检查通过注入场景进行，尚未完成自然流程通关平衡验收。
