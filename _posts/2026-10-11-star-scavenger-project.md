---
layout: teardown
title: 《星际回收工》开发中项目
subtitle: 俯视角搜打撤 · Unity 6 + QFramework · 单人开发
category: 开发中项目
tags: [Unity 6, QFramework, 搜打撤, 单人开发]
icon: 🛠️
tagline: SELF-DEV PROJECT
date: 2026-10-11
excerpt: 个人开发的俯视角搜打撤游戏：核心循环完整可玩，QFramework 架构 + 119 项自动化测试。本页为系统策划案节选——场景模块、商店改装、物品视野、移动负重、枪械防具、装备 UI 六大模块的设计图与解读，附实机演示视频。
---

<div class="pdf-strip">
  <span>下方为实机演示视频（含旁白讲解），系统设计图见各节。</span>
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
    <li><a href="#sec3"><span class="toc-num">03</span>场景模块规划</a></li>
    <li><a href="#sec4"><span class="toc-num">04</span>商店 / 制作 / 改装</a></li>
    <li><a href="#sec5"><span class="toc-num">05</span>物品存储与视野机制</a></li>
    <li><a href="#sec6"><span class="toc-num">06</span>移动 / 负重 / 噪音</a></li>
    <li><a href="#sec7"><span class="toc-num">07</span>枪械防具数值设计</a></li>
    <li><a href="#sec8"><span class="toc-num">08</span>装备 UI 与工程化</a></li>
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

  <p>一款俯视角 3D 搜打撤游戏，设计上参考《三角洲行动》、《逃离塔克夫》。玩家从空间站港口出发进入危险区，
  搜刮物资、对抗敌人、前往撤离点结算；带回的物资出售换取货币，投入装备养成与公司派系升级，再进入下一局。</p>

  <div class="card-grid">
    <div class="info-card">
      <div class="card-icon">🏗️</div>
      <h4>架构</h4>
      <p>QFramework：UIKit 管全部界面、配置表驱动物品/敌人/任务数据、命令层处理玩家操作、Model 层持有存档——界面与逻辑分离，改数据不动代码。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🎨</div>
      <h4>美术现状</h4>
      <p>Kenney 免费素材 + 灰色占位，专注玩法验证；表现层留了统一替换入口。</p>
    </div>
  </div>

  <div class="callout analysis">
    <div class="callout-title">🎯 设计三支柱</div>
    <p>取舍感 &gt; 成长兑现 &gt; 可读可控——搜打撤的乐趣核心在于"带什么进去、放弃什么、能不能活着带出来"，
    所有系统设计都优先服务这三条排序。</p>
  </div>
</div>

<div class="section" id="sec2">
  <div class="sec-num">02</div>
  <h2 class="sec-title">实机演示</h2>

  <p>演示流程：港口仓库 → 商店与改装台 → 进入危险区搜刮 → 遭遇敌人（AI 士气表现）→
  手雷投掷与闪避 AI → 撤离结算。</p>

  <div class="video-card">
    <video controls preload="metadata">
      <source src="/assets/vid/demo.mp4" type="video/mp4">
      您的浏览器不支持视频播放，<a href="/assets/vid/demo.mp4" target="_blank">点此下载观看</a>。
    </video>
  </div>
</div>

<div class="section" id="sec3">
  <div class="sec-num">03</div>
  <h2 class="sec-title">场景模块规划</h2>

  <p>主场景为空间站港口，五大功能模块围绕它展开，各自承担经营循环的一个环节：</p>

  <div class="card-grid">
    <div class="info-card">
      <div class="card-icon">📦</div>
      <h4>仓库</h4>
      <p>存储和出售玩家账号名下的各类资产：局内收集物、局外购买物、装备配件与消耗品。
      页面左侧展示角色当前装备，右侧为库存页面。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🏪</div>
      <h4>交易站</h4>
      <p>为玩家提供购买物资的功能模块——用局内赚的货币补充弹药、医疗和消耗品。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🚀</div>
      <h4>飞船站</h4>
      <p>购买与升级局内支援：攻击机支援呼叫、升级支援的击伤能力与支援次数——局内战斗的战术资源来源。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🔧</div>
      <h4>多功能站</h4>
      <p>制作物品与改装装备的模块集合：制作台消耗物资货币合成高级物资，改装台在此使用配件改装装备。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🏢</div>
      <h4>公司部门</h4>
      <p>派系任务与角色升级的模块集合：公司派系系统（接取不同派系任务提升派系等级）与员工等级系统（消耗员工解锁并升级技能）。</p>
    </div>
  </div>

  <img src="/assets/img/project/main-scene-modules.png" alt="主场景模块设定图">
</div>

<div class="section" id="sec4">
  <div class="sec-num">04</div>
  <h2 class="sec-title">商店 / 制作 / 改装</h2>

  <p>三个经营终端共用一套"页签 + 卡片网格"的 UI 框架，玩家学一个就会全部：</p>

  <div class="card-grid">
    <div class="info-card">
      <div class="card-icon">🏪</div>
      <h4>商店</h4>
      <p>页签分类：枪械 / 护具 / 背包 / 弹药 / 医疗。商品卡片双列展示（贴图+名称+数量+购买按钮），
      悬停 2 秒显示物品详情卡。购买后优先放背包，容量不足自动转仓库，仓库不足给出提示。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">⚗️</div>
      <h4>制作台</h4>
      <p>同样的卡片布局，按配方合成物资；制作前扫描背包与仓库库存并优先消耗背包内物品，
      资源不足给出明确提示。产出优先放背包，容量不足转仓库。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🔧</div>
      <h4>改装台</h4>
      <p>左侧枪械数据展示 + 主物品放置槽 + 四个配件槽（枪口/弹匣/瞄具/枪托）。
      点击槽位扫描背包、装备槽、仓库中的可用配件供选择；应用改装后数值实时更新到展示区，
      清空改装则配件整体返还。</p>
    </div>
  </div>

  <img src="/assets/img/project/craft-shop-modules.png" alt="商店与多功能终端模块设定图">

  <div class="callout design">
    <div class="callout-title">💡 设计说明</div>
    <p>三个终端刻意共用同一套交互范式（页签切换/卡片悬停详情/按钮行为一致），
    降低玩家的学习成本——经营模块的复杂度应该花在"选择"上，而不是"怎么操作"上。</p>
  </div>
</div>

<div class="section" id="sec5">
  <div class="sec-num">05</div>
  <h2 class="sec-title">物品存储与视野机制</h2>

  <p>角色页分三区：<strong>左侧装备槽区</strong>（头盔/护具/远程武器1/远程武器2/近战/投掷物 + 保险箱）、
  <strong>中部背包网格区</strong>、<strong>右侧地面容器网格区</strong>（与交互中容器联动）。
  支持拖拽穿戴、旋转摆放、双击快速转移、点装备槽卸下。</p>

  <p><strong>物品与存储</strong>：物品分种类和等级（品质六色：白绿蓝紫金红），物品占用网格空间
  （如初步步枪占 2×4 格），仓库和背包内可自由规划摆放，物品允许旋转。弹药目前仅允许堆叠（90 发一组）。
  背包本身是一种容器——换背包或丢弃背包时，物品留在背包里，类似"移动式容器"。</p>

  <p><strong>视野机制</strong>：分两层——周身视野（角色周围 3m 小范围可视）+ 视线视野（面朝方向 60° 平面锥形）；
  非可视范围以灰暗蒙版覆盖，只显示静态物品、不显示敌人等行为角色。
  瞄准时视野平滑收窄至 30°——想要精确瞄准就要承担视野压力。受击时在角色周围短暂显示指向受击方向的红色小三角。</p>

  <img src="/assets/img/project/mechanics-items-vision.png" alt="物品存储与视野机制设定图">

  <div class="callout design">
    <div class="callout-title">💡 设计说明</div>
    <p>网格化存储 + 旋转摆放 + 容器嵌套，全部服务于搜打撤的核心乐趣："带什么、放弃什么"的取舍决策；
    视野收窄机制则把"瞄得准"变成一个资源管理问题，而不是无代价的辅助。</p>
  </div>
</div>

<div class="section" id="sec6">
  <div class="sec-num">06</div>
  <h2 class="sec-title">移动 / 负重 / 噪音</h2>

  <p>移动机制：正常行走 / 缓步走（静步，不消耗体力，移速 70%）/ 疾跑与翻越（消耗体力）。
  移速应用物理表现——移动有加速过程，停止到行走有完加速过程（参考现实物理）；
  受击瞬间减速且命中后一小段时间内保持定速值且加速度归零。</p>

  <table class="data-table">
    <thead><tr><th>移速</th><th>噪音范围</th></tr></thead>
    <tbody>
      <tr><td>行走</td><td>6m</td></tr>
      <tr><td>静步</td><td>3m</td></tr>
      <tr><td>疾跑</td><td>15m</td></tr>
      <tr><td>翻越</td><td>10m</td></tr>
    </tbody>
  </table>

  <p>噪音范围直接喂给敌人 AI 的听觉感知——移动方式即暴露风险的决策。
  瞄准与开火时移速受枪械类型影响（步枪/散弹 80% → 机枪/重武器 70%），
  跑步中被击中则移速减至行走速度且 1 秒内无法获得加速度。</p>

  <p><strong>负重系统</strong>：人物有基础负重上限（装备与背包内物资均有重量），
  超限后限制移动——搜多了跑不动，这是搜打撤"取舍"的物理载体。
  负重等级与减速惩罚叠加：</p>

  <table class="data-table">
    <thead><tr><th>负重等级（当前负重值）</th><th>减速惩罚（叠加）</th></tr></thead>
    <tbody>
      <tr><td>上限值 80%</td><td>体力消耗加快 50%</td></tr>
      <tr><td>上限值 90%</td><td>体力消耗+50%、体力恢复速度降低 50%</td></tr>
      <tr><td>上限值 100%</td><td>体力消耗+50%、恢复降低 50%、强制最慢移速、禁止大动作</td></tr>
      <tr><td>上限值 150%</td><td>"难以前行"，禁止移动</td></tr>
    </tbody>
  </table>

  <img src="/assets/img/project/mechanics-movement.png" alt="移动负重噪音机制设定图">
</div>

<div class="section" id="sec7">
  <div class="sec-num">07</div>
  <h2 class="sec-title">枪械防具数值设计</h2>

  <p>武器性能由四个维度描述，全部受人机功效影响：
  <strong>后坐力</strong>（影响开火散步与准星回收）、<strong>操作性</strong>（影响开火移速、举镜收束速度）、
  <strong>人机功效</strong>（影响枪口跟随鼠标速度）、伤害与射速。
  射击伤害由枪械属性中的伤害等级决定，弹药等级只决定穿透和加成。</p>

  <table class="data-table">
    <thead><tr><th>枪械分类</th><th>腰射散布</th><th>瞄准散布</th><th>人机功效</th><th>生态定位</th></tr></thead>
    <tbody>
      <tr><td>步枪类</td><td>较差</td><td>近至中距离较好</td><td>中等</td><td>中近距离的基准武器</td></tr>
      <tr><td>散弹枪类</td><td>弹孔散布中等</td><td>瞄准收束弹孔散步，飞行移动扩散增强</td><td>中等</td><td>近距离特化武器</td></tr>
      <tr><td>手枪、冲锋枪类</td><td>中等</td><td>中至近距离较差</td><td>较好</td><td>近距离灵活武器</td></tr>
      <tr><td>机枪、重武器类</td><td>较差</td><td>近至中距离较好</td><td>差</td><td>固定架点火力</td></tr>
      <tr><td>狙击、精确武器类</td><td>差</td><td>中至远距离高射极好</td><td>中等</td><td>中远距离精准火力</td></tr>
    </tbody>
  </table>

  <p><strong>护具与弹药联动</strong>：护具 5 个等级、弹药 6 个等级，护甲值受击时消耗。
  关键规则：<strong>高等级弹药可无视低等级护具的阻挡，造成减伤后伤害</strong>（如 T3 弹对护具等级 2 造成对生命值的 90% 伤害），
  形成"穿深对抗护甲"的数值轴——玩家在配装弹药时就是在选择对付什么类型的敌人。</p>

  <img src="/assets/img/project/items-weapons-armor.png" alt="枪械防具数值设定图">
</div>

<div class="section" id="sec8">
  <div class="sec-num">08</div>
  <h2 class="sec-title">装备 UI 与工程化</h2>

  <div class="callout analysis">
    <div class="callout-title">📌 工程化现状与后续计划</div>
    <p>当前为灰盒可玩阶段：搜打撤核心循环（进图→搜刮→战斗→撤离→经营）已完整跑通，
    119 项自动化断言保障迭代质量；物品/枪械/敌人/任务全部配置表驱动。
    后续计划：表现层升级（替换占位素材）、可玩包发布、危险区内容扩充。</p>
  </div>
</div>

</main>
</div>
