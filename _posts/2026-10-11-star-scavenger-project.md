---
layout: teardown
title: 《星际回收工》开发中项目
subtitle: 俯视角搜打撤 · Unity 6 + QFramework · 单人开发
category: 开发中项目
tags: [Unity 6, QFramework, 搜打撤, 单人开发]
icon: 🛠️
tagline: SELF-DEV PROJECT
date: 2026-10-11
excerpt: 个人开发的俯视角搜打撤游戏：完整可玩循环（港口经营→进图搜打撤→结算），QFramework 架构 + 自动化测试管线，附演示视频与系统模块设计图。
---

<div class="pdf-strip">
  <span>下方为实机演示视频（含旁白），模块设计图见各节。</span>
  <a href="/assets/vid/demo.mp4" target="_blank">新标签页打开视频 ↗</a>
</div>

<div class="layout">

<aside class="sidebar">
  <div class="sidebar-header">
    <h2>开发中项目</h2>
    <p>《星际回收工》· 个人独立开发</p>
  </div>
  <ul class="toc-list">
    <li><a href="#sec1"><span class="toc-num">01</span>项目概览</a></li>
    <li><a href="#sec2"><span class="toc-num">02</span>实机演示</a></li>
    <li><a href="#sec3"><span class="toc-num">03</span>场景与部门模块</a></li>
    <li><a href="#sec4"><span class="toc-num">04</span>商店与制作改装</a></li>
    <li><a href="#sec5"><span class="toc-num">05</span>核心机制设计</a></li>
    <li><a href="#sec6"><span class="toc-num">06</span>物品与装备体系</a></li>
    <li><a href="#sec7"><span class="toc-num">07</span>装备 UI 与工程化</a></li>
  </ul>
  <a class="back-btn" href="/">← 返回作品集</a>
</aside>

<main class="main">

<div class="hero">
  <span class="badge">SELF-DEV PROJECT · IN DEVELOPMENT</span>
  <h1>《星际回收工》</h1>
  <p class="subtitle">俯视角 3D 搜打撤：港口经营 → 进图搜打撤 → 结算成长，完整循环已可玩</p>
  <div class="hero-meta">
    <div class="meta-item"><span class="meta-label">引擎</span><span class="meta-value">Unity 6 · C#</span></div>
    <div class="meta-item"><span class="meta-label">架构</span><span class="meta-value">QFramework</span></div>
    <div class="meta-item"><span class="meta-label">团队</span><span class="meta-value">单人开发</span></div>
    <div class="meta-item"><span class="meta-label">状态</span><span class="meta-value">核心循环已跑通</span></div>
  </div>
</div>

<div class="section" id="sec1">
  <div class="sec-num">01</div>
  <h2 class="sec-title">项目概览</h2>

  <p>一款俯视角 3D 搜打撤游戏，参考《地狱潜兵 2》的战场支援循环：
  玩家从港口出发进入危险区，搜刮物资、对抗敌人、前往撤离点结算；
  带回的物资在港口出售，用于商店购买、武器改装与设施升级，再进入下一局。</p>

  <div class="card-grid">
    <div class="info-card">
      <div class="card-icon">🏗️</div>
      <h4>架构</h4>
      <p>QFramework：UIKit 管全部界面、TableKit 驱动物品配置表、命令层处理玩家操作，
      Model 层持有存档数据——界面/数据/逻辑三层分离。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🎬</div>
      <h4>场景管线</h4>
      <p>关卡由编辑器脚本一键生成，生成后可在编辑器手调，摆位可导出存档并在重建后自动恢复。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🧪</div>
      <h4>自动化测试</h4>
      <p>119 项断言的命令行冒烟测试，每次改动后全量回归——单人开发的质量底线。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🎨</div>
      <h4>美术现状</h4>
      <p>Kenney 免费素材 + 灰色占位，专注功能与玩法验证；表现层为后续替换预留了统一入口。</p>
    </div>
  </div>
</div>

<div class="section" id="sec2">
  <div class="sec-num">02</div>
  <h2 class="sec-title">实机演示</h2>

  <p>演示流程：港口仓库 → 商店与改装台 → 进入危险区搜刮 → 遭遇敌人（AI 士气表现）→
  手雷投掷 → 撤离结算，旁白同步讲解各系统实现。</p>

  <div class="video-card">
    <video controls preload="metadata" poster="">
      <source src="/assets/vid/demo.mp4" type="video/mp4">
      您的浏览器不支持视频播放，<a href="/assets/vid/demo.mp4" target="_blank">点此下载观看</a>。
    </video>
  </div>
</div>

<div class="section" id="sec3">
  <div class="sec-num">03</div>
  <h2 class="sec-title">场景与部门模块</h2>

  <p>主场景的模块划分：出发港口（仓库/商店/改装/飞船/管理终端）与危险区的空间关系、
  玩家动线和交互点位。</p>
  <img src="/assets/img/project/main-scene-modules.png" alt="主场景模块设定">

  <p>港口功能以"公司部门"形式组织：每个部门对应一个终端面板与一条养成线，
  部门等级解锁对应功能——用统一的框架承载所有经营入口。</p>
  <img src="/assets/img/project/company-departments.png" alt="公司部门模块设定">
</div>

<div class="section" id="sec4">
  <div class="sec-num">04</div>
  <h2 class="sec-title">商店与制作改装</h2>

  <p>商店按分类页签组织商品，购买优先入背包、满则转仓库；
  多功能终端集成制作台与改装台两页：制作消耗材料合成物资，改装为武器挂载配件并实时改写武器数值。</p>
  <img src="/assets/img/project/craft-shop-modules.png" alt="多功能与商店模块设定">
</div>

<div class="section" id="sec5">
  <div class="sec-num">05</div>
  <h2 class="sec-title">核心机制设计</h2>

  <p>物品系统（类型×品质×堆叠）、视野迷雾（未探索遮蔽+障碍物半透明化）的规则设定。</p>
  <img src="/assets/img/project/mechanics-items-vision.png" alt="物品与视野机制设定">

  <p>移动系统：静止/行走/疾跑三档速度对应不同噪音半径，直接喂给敌人 AI 的听觉感知——
  移动方式即风险决策。</p>
  <img src="/assets/img/project/mechanics-movement.png" alt="移动机制设定">
</div>

<div class="section" id="sec6">
  <div class="sec-num">06</div>
  <h2 class="sec-title">物品与装备体系</h2>

  <p>枪械与防具的数值框架：武器分类型与弹药等级，防具按部位提供护甲值；
  掉落表按容器类型配置，品质决定基础价值。</p>
  <img src="/assets/img/project/items-weapons-armor.png" alt="枪械防具设定">
</div>

<div class="section" id="sec7">
  <div class="sec-num">07</div>
  <h2 class="sec-title">装备 UI 与工程化</h2>

  <p>角色页装备 UI 的布局设定：装备槽 + 背包网格 + 保险箱三区，
  支持拖拽穿戴、旋转摆放、双击快速转移。</p>
  <img src="/assets/img/project/equip-ui.png" alt="角色装备UI设定">

  <div class="callout analysis">
    <div class="callout-title">📌 工程化现状</div>
    <p>当前为灰盒可玩阶段：核心循环（搜打撤→经营→再出发）已完整跑通，
    自动化测试保障迭代质量；后续计划为表现层升级与可玩包发布。</p>
  </div>
</div>

</main>
</div>
