---
layout: teardown
title: 《问剑长生》拆解
subtitle: 修仙放置挂机 · 系统深度分析
category: 拆解案
tags: [修仙放置, 系统拆解, 商业化分析]
icon: 🔍
tagline: TEARDOWN ANALYSIS
date: 2026-10-06
excerpt: 两个月实际游玩后的系统级拆解：核心闭环、养成线战力占比、宗门社交与商业化的完整分析，附人界篇全系统思维导图。
---

<div class="pdf-strip">
  <span>本页为拆解案网页精排版，完整原文档（含全部图表）可下载 PDF。</span>
  <a href="/assets/docs/wjcs-analysis.pdf" download>下载《问剑长生初步体验与分析》.pdf ↓</a>
</div>

<div class="layout">

<aside class="sidebar">
  <div class="sidebar-header">
    <h2>游戏拆解报告</h2>
    <p>《问剑长生》系统深度分析</p>
  </div>
  <ul class="toc-list">
    <li><a href="#sec1"><span class="toc-num">01</span>产品概述</a></li>
    <li><a href="#sec2"><span class="toc-num">02</span>市场表现</a></li>
    <li><a href="#sec3"><span class="toc-num">03</span>核心玩法与闭环</a></li>
    <li><a href="#sec4"><span class="toc-num">04</span>养成与战斗系统</a></li>
    <li><a href="#sec5"><span class="toc-num">05</span>宗门社交系统</a></li>
    <li><a href="#sec6"><span class="toc-num">06</span>系统全景导图</a></li>
    <li><a href="#sec7"><span class="toc-num">07</span>整体评价</a></li>
  </ul>
  <a class="back-btn" href="/">← 返回作品集</a>
</aside>

<main class="main">

<div class="hero">
  <span class="badge">TEARDOWN ANALYSIS · V1.0</span>
  <h1>《问剑长生》拆解报告</h1>
  <p class="subtitle">修仙 + 放置挂机：一套以战力为货币的社交驱动循环</p>
  <div class="hero-meta">
    <div class="meta-item"><span class="meta-label">游戏类型</span><span class="meta-value">修仙 · 放置挂机</span></div>
    <div class="meta-item"><span class="meta-label">开发商</span><span class="meta-value">吉比特 / 雷霆互动</span></div>
    <div class="meta-item"><span class="meta-label">拆解周期</span><span class="meta-value">2 个月实际游玩</span></div>
    <div class="meta-item"><span class="meta-label">文档版本</span><span class="meta-value">V1.0 · 2026.10</span></div>
  </div>
</div>

<div class="section" id="sec1">
  <div class="sec-num">01</div>
  <h2 class="sec-title">产品概述</h2>

  <div class="card-grid">
    <div class="info-card">
      <div class="card-icon">⛩️</div>
      <h4>题材与美术</h4>
      <p>传统修仙体系 + 御剑飞行、功法修炼；3D 卡通风格——在同类型以 2D 为主的市场里形成差异化视觉体验。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">⚔️</div>
      <h4>战斗表现</h4>
      <p>精美的 3D 自动战斗演出，为玩家养成成果提供展示平台，是留存与付费炫耀心理的载体。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🌀</div>
      <h4>养成系统</h4>
      <p>修为、功法、装备、灵宠等众多贴合修仙主题的养成线，内容广泛且深入，构成主要长线目标。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🤝</div>
      <h4>社交核心</h4>
      <p>以宗门、位面为分组开展跨宗门/跨位面对战；日常同区与跨区 PVP 排位，赛季小组战与宗门联合战，社交绑定强。</p>
    </div>
  </div>

  <div class="callout analysis">
    <div class="callout-title">📊 拆解者游玩基线</div>
    <p>时长两个月（日均 2-3 小时）· 修为等级返虚中期 · 充值约 700 元 · 区服排名 10-20 名区间。日常任务约 10 分钟完成，适合碎片时间；修仙体系完备、代入感好。</p>
  </div>
</div>

<div class="section" id="sec2">
  <div class="sec-num">02</div>
  <h2 class="sec-title">市场表现</h2>

  <div class="stat-row">
    <div class="stat-box">
      <div class="stat-val">96w</div>
      <div class="stat-label">近一年 iOS 国区下载</div>
      <div class="stat-src">七麦预估</div>
    </div>
    <div class="stat-box">
      <div class="stat-val">$383w</div>
      <div class="stat-label">近一年 iOS 国区收入</div>
      <div class="stat-src">七麦预估</div>
    </div>
    <div class="stat-box">
      <div class="stat-val">7.4</div>
      <div class="stat-label">TapTap 评分</div>
      <div class="stat-src">好评差评参半</div>
    </div>
  </div>

  <div class="fig-row">
    <figure class="fig">
      <img src="/assets/img/wjcs/image2.png" alt="近一年下载量预估">
      <figcaption>近一年 iOS 国区下载量估算 · 七麦数据</figcaption>
    </figure>
    <figure class="fig">
      <img src="/assets/img/wjcs/image3.png" alt="近一年收入预估">
      <figcaption>近一年 iOS 国区收入估算 · 七麦数据</figcaption>
    </figure>
  </div>

  <figure class="fig fig-single">
    <img src="/assets/img/wjcs/image5.png" alt="TapTap 评分详情">
    <figcaption>TapTap 评分 7.4 · 共 8,335 条评价</figcaption>
  </figure>

  <h3>搜索引擎指数</h3>
  <p>数据来源于百度指数，为近一年「问剑长生」关键词的预估搜索量走势——可反映公域热度的自然波动。</p>

  <figure class="fig">
    <img src="/assets/img/wjcs/image4.png" alt="百度指数近一年走势">
    <figcaption>百度指数 · 近一年搜索量走势（日均 557，同比 −30.39%）</figcaption>
  </figure>

  <h3>用户口碑</h3>

  <div class="card-grid">
    <div class="info-card">
      <div class="card-icon">👍</div>
      <h4>好评方向</h4>
      <p>画风：3D 修仙题材新颖；游戏性：神通自由搭配、放置收菜友好、3D 战斗表现好；社交元素充足、社区联系强。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">👎</div>
      <h4>差评方向</h4>
      <p>平衡性：平民与氪金玩家差距巨大、资源积累慢；后期日常单调内容空洞；运营活动氪金弹窗频繁、付费引导过强。</p>
    </div>
  </div>
</div>

<div class="section" id="sec3">
  <div class="sec-num">03</div>
  <h2 class="sec-title">核心玩法与闭环</h2>

  <div class="callout highlight">
    <div class="callout-title">💡 核心洞察</div>
    <p>游戏内系统众多，但各系统的循环驱动一致：<strong>玩家行为的出发点都是获取资源提升战力，进而提升活动竞争力，以获取更好的养成资源与社交体验</strong>——行为与目标彼此交替，构成核心动力循环。</p>
  </div>

  <img src="/assets/img/wjcs/image6.png" alt="核心循环">

  <div class="card-grid">
    <div class="info-card">
      <div class="card-icon">📈</div>
      <h4>提升战力</h4>
      <p>参与活动的基础门槛与养成进度的直接体现；主要方向：修为等级、神通等级、心法等级、装备等级。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🎒</div>
      <h4>获取养成资源</h4>
      <p>提升战力的物资基础，也是参与活动的目的之一；多种获取手段均需消耗对应的活动货币。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🏟️</div>
      <h4>参与活动</h4>
      <p>获取资源的手段、提升战力的目的；活动以战力为核心评判标准，战力高者获得更好的奖励。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">💬</div>
      <h4>参与社交</h4>
      <p>部分玩家的核心游玩动机——在游戏中结识同好，社交本身构成留存层。</p>
    </div>
  </div>

  <h3>核心闭环示例：论剑台（同区 PVP）</h3>
  <p>论剑台完整呈现了闭环在具体玩法中的形态：每日任务引导进入论剑 PVP → 对战获取<strong>论剑币 + 论剑积分</strong> → 货币在商店兑换神通养成资源、积分提升段位 → 特定神通解锁/升级材料与论剑商店绑定 → 赛季结算重置积分、按段位发放奖励与限时称号 → 驱动持续参与。</p>

  <img src="/assets/img/wjcs/image7.png" alt="论剑台流程">

  <div class="flow-list">
    <div class="flow-item">对战获取货币、提升段位</div>
    <div class="flow-item">兑换物资、提升战力</div>
    <div class="flow-item">对战获取货币、提升段位（循环）</div>
  </div>

  <table class="data-table">
    <thead><tr><th>资源</th><th>产出出口</th><th>消耗入口</th></tr></thead>
    <tbody>
      <tr><td>论剑币</td><td>对战胜利（每日上限 8 次）、每日段位发放、段位结算</td><td>论剑台商店</td></tr>
      <tr><td>论剑积分</td><td>对战胜利（每日上限 8 次）</td><td>赛季结算扣除</td></tr>
    </tbody>
  </table>

  <div class="callout analysis">
    <div class="callout-title">📊 个人体验数据</div>
    <p>一个赛季两周，资源产出总量约 3000 论剑币，足够兑换两份仙品（金）神通——在全游戏周期中资源获取性价比属中高档（对比攒抽卡资源或直接氪金）。</p>
  </div>
</div>

<div class="section" id="sec4">
  <div class="sec-num">04</div>
  <h2 class="sec-title">养成与战斗系统</h2>

  <p>战斗涉及的加成系统极广。以拆解者账号（总战力 62.54 亿）为例，19 个系统参与战力构成，其中 <strong>11 个模块贡献了 90% 的战力</strong>：</p>

  <table class="data-table">
    <thead><tr><th>#</th><th>系统</th><th>战力（亿）</th><th>占比</th><th>累计占比</th></tr></thead>
    <tbody>
      <tr><td>1</td><td>心法</td><td>8.69</td><td>13.89%</td><td>13.89%</td></tr>
      <tr><td>2</td><td>装备与法宝</td><td>6.98</td><td>11.16%</td><td>25.05%</td></tr>
      <tr><td>3</td><td>异宝养成</td><td>6.76</td><td>10.81%</td><td>35.86%</td></tr>
      <tr><td>4</td><td>神通</td><td>6.56</td><td>10.49%</td><td>46.35%</td></tr>
      <tr><td>5</td><td>命火加成</td><td>4.89</td><td>7.82%</td><td>54.17%</td></tr>
      <tr><td>6</td><td>灵兽</td><td>4.63</td><td>7.40%</td><td>61.57%</td></tr>
      <tr><td>7</td><td>飞行法器</td><td>4.47</td><td>7.15%</td><td>68.72%</td></tr>
      <tr><td>8</td><td>道业</td><td>3.99</td><td>6.38%</td><td>75.10%</td></tr>
      <tr><td>9</td><td>真灵血脉</td><td>3.80</td><td>6.08%</td><td>81.18%</td></tr>
      <tr><td>10</td><td>阴神养成</td><td>3.24</td><td>5.18%</td><td>86.36%</td></tr>
      <tr><td>11</td><td>人物修为</td><td>2.28</td><td>3.64%</td><td>90.00%</td></tr>
      <tr><td>12</td><td>罗盘加成</td><td>1.33</td><td>2.13%</td><td>92.13%</td></tr>
      <tr><td>13</td><td>精魄</td><td>1.23</td><td>1.97%</td><td>94.10%</td></tr>
      <tr><td>14</td><td>宗门加成</td><td>0.88</td><td>1.41%</td><td>95.51%</td></tr>
      <tr><td>15</td><td>魔族秘术</td><td>0.80</td><td>1.28%</td><td>96.79%</td></tr>
      <tr><td>16</td><td>终结秘宝</td><td>0.71</td><td>1.13%</td><td>97.92%</td></tr>
      <tr><td>17</td><td>天晶养成</td><td>0.61</td><td>0.98%</td><td>98.90%</td></tr>
      <tr><td>18</td><td>魂幡加成</td><td>0.50</td><td>0.80%</td><td>99.70%</td></tr>
      <tr><td>19</td><td>至宝加成</td><td>0.08</td><td>0.13%</td><td>99.83%</td></tr>
    </tbody>
  </table>

  <div class="callout analysis">
    <div class="callout-title">📊 分析结论</div>
    <p>11 个模块占总战力 90%，是养成的关键抓手。由于部分系统（如命火）在灵界篇章才解锁，下文只分析<strong>游戏初期即解锁且占关键占比</strong>的系统：四维与灵压、神通、心法与道业、法宝与装备、灵兽、异宝与古地。</p>
  </div>

  <h3>基础属性：四维与灵压</h3>
  <p><strong>四维</strong>代表基础战斗属性，从修为等级、装备、心法与道业等级等系统获得提升；<strong>灵压</strong>由飞行法器升级获取，对战开始时双方比拼灵压点数，低的一方被压制并进入一段眩晕（受抗性影响），眩晕期间无法反击。</p>

  <table class="data-table">
    <thead><tr><th>名称</th><th>描述</th><th>获取 / 提升方式</th></tr></thead>
    <tbody>
      <tr><td>神威</td><td>代表攻击、命中</td><td>修为等级、装备加成、心法加成、道业加成</td></tr>
      <tr><td>长生</td><td>代表生命值、暴击抗性</td><td>同上</td></tr>
      <tr><td>金甲</td><td>代表防御、闪避</td><td>同上</td></tr>
      <tr><td>融灵</td><td>代表法力、暴击率</td><td>同上</td></tr>
      <tr><td>灵压</td><td>战斗开始阶段点数比大小，小点数一方短暂眩晕</td><td>飞行法器升级时提升</td></tr>
    </tbody>
  </table>

  <p>灵压相关系统资源：</p>

  <table class="data-table">
    <thead><tr><th>资源</th><th>产出出口</th><th>消耗入口</th></tr></thead>
    <tbody>
      <tr><td>飞行法器碎片</td><td>论剑台、诸天商店、运营活动</td><td>飞行法器合成、升阶</td></tr>
      <tr><td>锻器晶</td><td>日常与周常任务、仙坊购买、运营活动</td><td>飞行法器升级</td></tr>
    </tbody>
  </table>

  <h3>神通：技能构筑的核心</h3>
  <p>神通即技能，分派系、品阶与等级，有多种获取途径，重复获取转换为同名碎片；升级消耗较多碎片，并可在出招顺序中调整技能释放顺序。人界篇中神通有<strong>三大派系，每系两个流派</strong>：</p>

  <table class="data-table">
    <thead><tr><th>派系</th><th>流派</th></tr></thead>
    <tbody>
      <tr><td>剑系</td><td>伏龙、重光</td></tr>
      <tr><td>火系</td><td>天炉、离火</td></tr>
      <tr><td>雷系</td><td>神霄、五雷</td></tr>
    </tbody>
  </table>

  <p>神通系统的相关设定：</p>

  <table class="data-table">
    <thead><tr><th>设定</th><th>描述</th></tr></thead>
    <tbody>
      <tr><td>神通</td><td>玩家技能构筑核心，最多装备 6 个；同派系装备 ≥4 个时激活对应派系法体（如 4 剑 + 1 火 + 1 雷 → 激活剑系法体）</td></tr>
      <tr><td>克制关系</td><td>法体之间存在克制：剑克制雷、雷克制火、火克制剑——鼓励玩家探索多样的技能构筑方案</td></tr>
      <tr><td>流派</td><td>装备同流派神通 ≥2 个时，激活对应的流派加成</td></tr>
      <tr><td>获取方式</td><td>观星崖消耗资源抽取（每次抽取得 1 点道蕴，可用道蕴在商店兑换神通）；论剑台商店、诸天商店、宗门宝库用对应货币兑换；神通碎片在一定条件下可相互转换，填补养成空缺</td></tr>
      <tr><td>升级与重置</td><td>神通内含多项属性等级，随神通等级逐步提升；升级消耗对应资源，且有重置功能，允许按养成需求回收资源并重新分配</td></tr>
    </tbody>
  </table>

  <p>神通品阶与等级划分（升级消耗）：</p>

  <table class="data-table">
    <thead><tr><th>品阶</th><th>等级</th><th>升级消耗</th></tr></thead>
    <tbody>
      <tr><td rowspan="12">仙品（金）</td><td>仙品一星</td><td>0（本体解锁）</td></tr>
      <tr><td>仙品二星</td><td>本体碎片 40</td></tr>
      <tr><td>仙品三星</td><td>本体碎片 40 + 紫色碎片 30 + 蓝色碎片 100</td></tr>
      <tr><td>仙品玄阶一星</td><td>本体碎片 40 + 紫色碎片 60 + 蓝色碎片 150</td></tr>
      <tr><td>仙品玄阶二星</td><td>本体碎片 40 + 金色碎片 40 + 紫色碎片 60 + 蓝色碎片 150</td></tr>
      <tr><td>仙品玄阶三星</td><td>本体碎片 40 + 金色碎片 40 + 紫色碎片 90 + 蓝色碎片 220</td></tr>
      <tr><td>仙品地阶一星</td><td>本体碎片 40 + 金色碎片 40 + 紫色碎片 90 + 蓝色碎片 220</td></tr>
      <tr><td>仙品地阶二星</td><td>本体碎片 40 + 金色碎片 40 + 紫色碎片 90 + 蓝色碎片 220</td></tr>
      <tr><td>仙品地阶三星</td><td>本体碎片 80 + 金色碎片 80 + 紫色碎片 200 + 蓝色碎片 500</td></tr>
      <tr><td>仙品天阶一星</td><td>本体碎片 80 + 金色碎片 80 + 紫色碎片 200 + 蓝色碎片 500</td></tr>
      <tr><td>仙品天阶二星</td><td>本体碎片 120 + 金色碎片 120 + 紫色碎片 300 + 蓝色碎片 750</td></tr>
      <tr><td>仙品天阶三星</td><td>本体碎片 120 + 金色碎片 120 + 紫色碎片 300 + 蓝色碎片 750</td></tr>
      <tr><td rowspan="3">极品（紫）</td><td>极品一星</td><td>0（本体解锁）</td></tr>
      <tr><td>极品二星</td><td>本体碎片 30</td></tr>
      <tr><td>极品三星</td><td>本体碎片 30 + 蓝色碎片 60</td></tr>
      <tr><td rowspan="3">上品（蓝）</td><td>上品一星</td><td>0（本体解锁）</td></tr>
      <tr><td>上品二星</td><td>本体碎片 20</td></tr>
      <tr><td>上品三星</td><td>本体碎片 60</td></tr>
    </tbody>
  </table>

  <div class="callout analysis">
    <div class="callout-title">📊 个人体验数据</div>
    <p>约 2 个月游玩 + 微氪，目前养成 1 份天阶三星、1 份天阶一星、2 份地阶、2 份玄阶，实际持有资源够养满两个天阶三星——养成难度与投入时间在个人可接受范围内。</p>
  </div>

  <h3>心法与道业</h3>
  <p>心法分神威类、长生类、金甲类、融灵类，各有加成偏重；道业是心法的附属子系统，作为心法拓展。心法有品阶、星级、等级，等级上限受品阶与星级影响。</p>

  <table class="data-table">
    <thead><tr><th>设定</th><th>描述</th></tr></thead>
    <tbody>
      <tr><td>心法</td><td>分四类：神威类、长生类、金甲类、融灵类，各自加成对应属性</td></tr>
      <tr><td>获取方式</td><td>观星崖消耗资源抽取（每次得 1 点道蕴，可用道蕴兑换心法自选礼包）；宗门宝库用对应货币兑换限定心法</td></tr>
      <tr><td>升级与重置</td><td>对四维的加成为「基础四维 + 侧重属性」，加成量与等级相关，等级上限受星级影响；有重置功能，可按需回收资源重新分配</td></tr>
      <tr><td>图鉴与传承</td><td>解锁未拥有的心法时获得对应属性加成；收集特定心法并达到对应总星级时，获得传承加成</td></tr>
      <tr><td>道业</td><td>收集到特定心法组时可消耗资源解锁；道业有阶级和等级，达成一定条件可提升等级；阶级受对应心法组总星级影响，同样依四维划分成四类</td></tr>
      <tr><td>等级与星级升级资源</td><td>等级升级消耗心法感悟和心法精义，星级升级消耗心法真意和本体碎片；三类资源可在心法感悟中抽取、仙坊购买、悬赏俸禄每日领取</td></tr>
      <tr><td>心法感悟</td><td>负责获取升级资源的模块，消耗灵泉果随机产出资源，可消耗高阶道具提升获取效率</td></tr>
    </tbody>
  </table>

  <p>心法与道业系统相关资源：</p>

  <table class="data-table">
    <thead><tr><th>资源</th><th>产出出口</th><th>消耗入口</th></tr></thead>
    <tbody>
      <tr><td>心法感悟</td><td>心法悟道消耗灵泉果/开悟果获得、仙坊购买、运营活动</td><td>心法修行普通等级升级</td></tr>
      <tr><td>心法精义</td><td>同上</td><td>心法修行节点等级突破</td></tr>
      <tr><td>心法真意</td><td>同上</td><td>心法星级升级</td></tr>
      <tr><td>灵泉果</td><td>日常与周常任务、仙坊购买、运营活动</td><td>心法悟道中作为基础消耗</td></tr>
      <tr><td>开悟果</td><td>同上</td><td>拥有数量 &gt;0 且悟道处于特殊节点时自动消耗，用于提升获得资源数量</td></tr>
      <tr><td>道业神蕴</td><td>同上</td><td>解锁与升级道业</td></tr>
    </tbody>
  </table>

  <h3>法宝与装备</h3>
  <div class="card-grid">
    <div class="info-card">
      <div class="card-icon">⚔️</div>
      <h4>法宝种类与设定</h4>
      <p>分攻击类（人界篇 4 种）与防御类（3 种）；两类各最多装备 3 件，不能同时装备同种法宝，法宝有等级与星级。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🔁</div>
      <h4>继承交互</h4>
      <p>更换法宝时新法宝继承旧法宝等级；因不同境界法宝种类不同，星级只允许同种类法宝继承。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🛡️</div>
      <h4>战斗表现</h4>
      <p>攻击法宝可与神通一起调整出招顺序；防御法宝调整承伤顺序并提供护盾值，护盾清空则法宝破碎，附属加成失效。</p>
    </div>
  </div>

  <div class="callout design">
    <div class="callout-title">⚙️ 设计点：境界驱动的重复消耗</div>
    <p>装备分 4 种分别影响四维，有升级等级与品阶等级，更换时继承旧等级；每种装备都有天晶槽位，镶嵌天晶可获小额战力加成（氪金点）。<strong>不同境界有不同法宝种类，且高境界法宝战力碾压低境界</strong>——目的是为每个新境界阶段提供重复的养成资源消耗点，避免一套装备重复使用，同时贴合传统修仙「炼器」的玩法要素。</p>
  </div>

  <p>法宝与装备系统相关资源：</p>

  <table class="data-table">
    <thead><tr><th>资源</th><th>产出出口</th><th>消耗入口</th></tr></thead>
    <tbody>
      <tr><td>法宝打造材料（攻击/防御类）</td><td>日常与周常任务、宗门商店、仙坊、悬赏俸禄每日领取、挂机</td><td>器鼎打造法宝时消耗</td></tr>
      <tr><td>法宝升级材料</td><td>仙坊购买、法宝分解</td><td>法宝升级</td></tr>
      <tr><td>法宝（攻击/防御类）</td><td>器鼎打造产出、拍卖场购买（金色）</td><td>金色法宝升星消耗同类法宝；可在拍卖场出售</td></tr>
      <tr><td>装备与对应碎片</td><td>宗门商店、仙坊、副本玩法、拍卖场、悬赏俸禄每日领取</td><td>器鼎分解、拍卖场出售</td></tr>
      <tr><td>装备升级材料</td><td>器鼎分解装备获得</td><td>装备升级</td></tr>
      <tr><td>天晶</td><td>副本玩法产出、拍卖场购买</td><td>天晶升级消耗同种天晶；可在拍卖场出售</td></tr>
    </tbody>
  </table>

  <h3>灵兽</h3>
  <div class="card-grid">
    <div class="info-card">
      <div class="card-icon">🐾</div>
      <h4>作用与等级</h4>
      <p>为玩家提供战力提升与技能辅助（使敌人眩晕、削弱抗性、提升爆发等）；灵兽共用境界等级，但各有独立的灵脉等级与技能等级。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🎯</div>
      <h4>战斗设定</h4>
      <p>出战位 3 个、助战位 2 个；出战灵兽提供 10% 属性加成，助战 5%。战斗按出战位顺序依次释放灵兽技能，释放完即下场轮换。</p>
    </div>
  </div>

  <p>灵兽系统相关资源：</p>

  <table class="data-table">
    <thead><tr><th>资源</th><th>产出出口</th><th>消耗入口</th></tr></thead>
    <tbody>
      <tr><td>探灵宝令（抽卡资源）</td><td>宗门商店、仙坊、悬赏等级升级领取、运营活动</td><td>灵兽抽取消耗</td></tr>
      <tr><td>灵脉与灵兽技能相关资源</td><td>抽取灵兽时获得、灵兽商店兑换、仙坊购买</td><td>提升灵兽技能等级、提升灵脉、灵兽化形</td></tr>
      <tr><td>育灵草（灵兽升级资源）</td><td>挂机获取、抽取灵兽时获得、灵兽商店兑换</td><td>灵兽等级升级</td></tr>
    </tbody>
  </table>

  <h3>子系统：异宝与星墟古地</h3>
  <div class="card-grid">
    <div class="info-card">
      <div class="card-icon">🏺</div>
      <h4>异宝设定</h4>
      <p>异宝分等级与星级、重复获取转碎片、等级可重置；按加成侧重分平衡／威能／守护三类。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🗺️</div>
      <h4>古地挑战</h4>
      <p>不同古地产出对应系列异宝，古地传承等级与系列异宝总星级挂钩；最多 6 人组队，4 个刷怪阶段，随机产出红／金／紫／蓝／白宝箱。</p>
    </div>
    <div class="info-card">
      <div class="card-icon">🎫</div>
      <h4>领奖限制</h4>
      <p>每周最多领取 10 次古地奖励：5 次免费 + 5 次仙玉购买——社交组队与付费门槛双重卡点。</p>
    </div>
  </div>

  <p>异宝与古地相关资源：</p>

  <table class="data-table">
    <thead><tr><th>资源</th><th>产出出口</th><th>消耗入口</th></tr></thead>
    <tbody>
      <tr><td>异宝</td><td>古地挑战、运营活动、异宝宝库抽奖</td><td>异宝解锁与升级</td></tr>
      <tr><td>异宝精华、异宝灵源</td><td>古地挑战、仙坊购买、异宝宝库抽奖</td><td>异宝升级</td></tr>
      <tr><td>异宝密钥</td><td>古地礼包购买</td><td>异宝宝库抽奖</td></tr>
    </tbody>
  </table>

  <h3>PVP 战斗阶段</h3>

  <div class="fig-row">
    <figure class="fig">
      <img src="/assets/img/wjcs/image8.png" alt="战斗系统界面">
      <figcaption>战斗系统加成结构</figcaption>
    </figure>
    <figure class="fig">
      <img src="/assets/img/wjcs/image9.png" alt="战斗流程">
      <figcaption>PVP 战斗阶段流程</figcaption>
    </figure>
  </div>

  <div class="callout design">
    <div class="callout-title">⚙️ 战斗机制：终结触发</div>
    <p>敌人血量降到终结触发区间时，先按终结法宝属性计算触发概率 → 触发则播放终结演出并结束战斗，触发者获胜——为自动战斗注入悬念与演出高光。</p>
  </div>
</div>

<div class="section" id="sec5">
  <div class="sec-num">05</div>
  <h2 class="sec-title">宗门社交系统</h2>

  <p>宗门是社交核心与大型活动的参与主体，为玩家提供组队合作、社交沟通与活动平台：</p>

  <table class="data-table">
    <thead><tr><th>功能</th><th>设计要点</th></tr></thead>
    <tbody>
      <tr><td>宗门管理</td><td>入退/创建；宗主超 3 天未上线自动禅位给活跃副宗主或高贡献成员</td></tr>
      <tr><td>修葺</td><td>成员交互：提升建设度、捐物资、获取贡献——每日活跃的基础锚点</td></tr>
      <tr><td>宗门等级</td><td>等级越高容量/职位/挂机收益/建筑上限越高</td></tr>
      <tr><td>职位</td><td>玩家在宗门中担任的职务，每周可领取对应档次的秘藏兑换卷——用职务绑定周常留存</td></tr>
      <tr><td>灵脉与灵矿</td><td>领地资源产出；无主矿脉可被抢占，战斗失败丢失席位——资源型 PVP 摩擦</td></tr>
      <tr><td>宗门任务</td><td>每日最多 5 个自动进行（红橙紫蓝四品阶，可刷新），产出凝神木</td></tr>
      <tr><td>宗门秘藏</td><td>消耗秘藏兑换卷兑换物资——职位俸禄的直接兑换出口</td></tr>
      <tr><td>宗门丹炉</td><td>每周日 20 点开炉：每 4 根凝神木产出随机品质凝神露，全员投入越多高品质概率越高</td></tr>
      <tr><td>宗门奖池</td><td>按宗门活动排名注入礼盒，玩家可赞助——集体荣誉与共享福利</td></tr>
      <tr><td>宗门加成</td><td>组队中同宗 ≥4 人获得战斗加成——用数值奖励强化同宗组队</td></tr>
    </tbody>
  </table>

  <table class="data-table">
    <thead><tr><th>资源</th><th>产出出口</th><th>消耗入口</th></tr></thead>
    <tbody>
      <tr><td>建设度</td><td>修葺</td><td>宗门等级升级</td></tr>
      <tr><td>宗门物资</td><td>修葺</td><td>占领灵脉、建设建筑、升级底蕴</td></tr>
      <tr><td>凝神木</td><td>宗门任务</td><td>宗门丹炉</td></tr>
      <tr><td>宗门贡献</td><td>任务、修葺、周常活动</td><td>贡献商店兑换</td></tr>
      <tr><td>玄晶石</td><td>灵矿采集</td><td>遗迹宝库兑换</td></tr>
      <tr><td>秘藏兑换卷</td><td>职位俸禄</td><td>宗门秘藏兑换</td></tr>
    </tbody>
  </table>

  <div class="callout analysis">
    <div class="callout-title">📊 设计意图解读</div>
    <p>丹炉、建设、奖池等机制的核心目的是<strong>用集体产出放大个体收益</strong>：鼓励高活跃度换取大量资源，用宗门活动凝聚团结度，提高游玩黏性与整体福利。周常宗门战按宗门总战力匹配跨服对手（1v1/2v2），持续制造社交对抗目标。</p>
  </div>
</div>

<div class="section" id="sec6">
  <div class="sec-num">06</div>
  <h2 class="sec-title">系统全景导图</h2>

  <img src="/assets/img/wjcs/image1.png" alt="系统框架">

  <p>人界篇全系统思维导图（源自 XMind，219 个节点；横向滚动查看，鼠标悬停节点看完整标题）：</p>

  <div class="mindmap-card">
    <div class="mindmap-title">思维导图 · 人界篇系统全览</div>
    <div class="mindmap-scroll"><img src="/assets/img/wjcs/mindmap.svg" alt="问剑长生（人界篇）系统拆解思维导图"></div>
  </div>

  <h3>导图全树（点击逐层展开）</h3>
  <div class="tree-box">
<details><summary>问剑长生（人界篇）</summary>
<details><summary>角色系统</summary>
<details><summary>养成系统</summary>
<details><summary>系统设定</summary>
<details><summary>主要四维</summary>
<span class="leaf">神威</span>
<span class="leaf">长生</span>
<span class="leaf">金甲</span>
<span class="leaf">融灵</span>
</details>
<span class="leaf">灵压</span>
</details>
<details><summary>角色养成</summary>
<details><summary>修为养成</summary>
<span class="leaf">修炼</span>
</details>
<details><summary>装备类养成</summary>
<details><summary>法宝</summary>
<span class="leaf">星级</span>
<span class="leaf">等级</span>
</details>
<details><summary>装备</summary>
<span class="leaf">种类</span>
<span class="leaf">等级</span>
</details>
<details><summary>飞行法器</summary>
<span class="leaf">品阶</span>
<span class="leaf">星级</span>
<span class="leaf">等级</span>
</details>
</details>
<details><summary>神通养成</summary>
<span class="leaf">派系</span>
<span class="leaf">品阶</span>
<span class="leaf">等级</span>
</details>
<details><summary>心法与道业养成</summary>
<span class="leaf">道业等级</span>
<details><summary>心法</summary>
<span class="leaf">星级</span>
<span class="leaf">等级</span>
</details>
<span class="leaf">图鉴</span>
</details>
</details>
<details><summary>附属养成</summary>
<details><summary>灵兽养成</summary>
<details><summary>灵兽</summary>
<span class="leaf">灵阵境界</span>
<span class="leaf">灵兽灵脉</span>
<span class="leaf">兽决</span>
</details>
<span class="leaf">紫微封妖录</span>
</details>
<details><summary>副本系统</summary>
<details><summary>异宝阁</summary>
<span class="leaf">异宝等级</span>
<span class="leaf">异宝星级</span>
<span class="leaf">传承等级</span>
</details>
</details>
<details><summary>各类杂项子系统</summary>
<span class="leaf">阴神</span>
<span class="leaf">真灵血脉</span>
<span class="leaf">魂幡</span>
<span class="leaf">证道至宝</span>
<span class="leaf">终结秘宝</span>
</details>
</details>
</details>
<details><summary>装饰系统</summary>
<details><summary>头像系统</summary>
<details><summary>装饰功能</summary>
<span class="leaf">头像、头像框、称号、对话气泡、组队外框</span>
</details>
</details>
<details><summary>换装系统</summary>
<details><summary>装饰功能</summary>
<span class="leaf">套装、衣服、发型、飞行法器、配饰</span>
</details>
</details>
</details>
<details><summary>背包系统</summary>
<details><summary>存储功能</summary>
<span class="leaf">存储和展示玩家拥有的各种资源</span>
</details>
</details>
</details>
<details><summary>运营活动</summary>
<details><summary>紫微宝库</summary>
<span class="leaf">日常礼包</span>
<span class="leaf">周常礼包</span>
<span class="leaf">生涯累充奖励</span>
<span class="leaf">优惠礼包</span>
<span class="leaf">月卡与永久卡</span>
</details>
<details><summary>周期活动</summary>
<span class="leaf">限时通行证</span>
<span class="leaf">优惠礼包</span>
</details>
</details>
<details><summary>核心体验</summary>
<span class="leaf">以角色战力养成作为主要的驱动力</span>
<span class="leaf">以玩家间合作、对战为主题的各种周常活动作为核心舞台</span>
<details><summary>特色亮点</summary>
<span class="leaf">较为华丽的3D战斗演出</span>
<span class="leaf">便捷的自动化行为</span>
<span class="leaf">易理解的养成点</span>
</details>
</details>
<details><summary>社交</summary>
<details><summary>好友系统</summary>
<span class="leaf">好友</span>
<span class="leaf">结义</span>
<span class="leaf">道缘</span>
</details>
<details><summary>宗门系统</summary>
<details><summary>宗门任务</summary>
<span class="leaf">接取后自动完成</span>
</details>
<details><summary>宗门建设</summary>
<span class="leaf">玩家每日花费仙玉获取贡献值</span>
</details>
<details><summary>宗门战舟</summary>
<span class="leaf">宗门成员战斗小组分配</span>
</details>
<details><summary>宗门商店</summary>
<span class="leaf">消耗贡献兑换养成资源</span>
</details>
</details>
<span class="leaf">排行榜</span>
<details><summary>聊天系统</summary>
<span class="leaf">聊天</span>
<span class="leaf">发布组队</span>
<span class="leaf">分享物品信息</span>
<span class="leaf">战力对比</span>
</details>
<details><summary>各类副本系统</summary>
<details><summary>日常·副本系统</summary>
<span class="leaf">星墟古地</span>
<span class="leaf">魔域深渊</span>
<span class="leaf">御魔之境</span>
<span class="leaf">天魔入侵</span>
</details>
</details>
<details><summary>聚仙城</summary>
<span class="leaf">渡劫台</span>
<span class="leaf">勘舆</span>
<span class="leaf">温泉</span>
</details>
<span class="leaf">邮件</span>
</details>
<details><summary>资源系统</summary>
<details><summary>货币系统</summary>
<details><summary>坊市</summary>
<span class="leaf">灵石</span>
</details>
<details><summary>仙坊</summary>
<span class="leaf">仙玉</span>
</details>
<details><summary>商会</summary>
<details><summary>拍卖行</summary>
<span class="leaf">仙元</span>
</details>
<details><summary>交易行</summary>
<span class="leaf">绑元</span>
</details>
</details>
</details>
<details><summary>抽卡系统</summary>
<span class="leaf">神通</span>
<span class="leaf">心法</span>
</details>
<span class="leaf">秘境挂机系统</span>
<details><summary>资源打造系统</summary>
<span class="leaf">丹炉</span>
<span class="leaf">器鼎</span>
</details>
<details><summary>PVP相关系统</summary>
<details><summary>问剑台</summary>
<span class="leaf">三榜论剑</span>
</details>
<details><summary>破界论剑</summary>
<span class="leaf">诸天大会</span>
</details>
</details>
<details><summary>PVE相关系统</summary>
<span class="leaf">天魔入侵</span>
<span class="leaf">星墟古地</span>
<span class="leaf">古地之巅</span>
<span class="leaf">魔念深渊</span>
</details>
<details><summary>悬赏系统</summary>
<span class="leaf">首领与爪牙</span>
<span class="leaf">俸禄</span>
</details>
</details>
<details><summary>战斗系统</summary>
<details><summary>战斗类型</summary>
<span class="leaf">PVP</span>
<span class="leaf">PVE</span>
</details>
<details><summary>战力</summary>
<details><summary>属性</summary>
<details><summary>主要四维</summary>
<span class="leaf">神威</span>
<span class="leaf">长生</span>
<span class="leaf">金甲</span>
<span class="leaf">融灵</span>
</details>
<span class="leaf">灵压</span>
<span class="leaf">灵兽</span>
</details>
<details><summary>法宝</summary>
<span class="leaf">攻击类</span>
<span class="leaf">防御类</span>
</details>
<details><summary>装备</summary>
<span class="leaf">冠、袍、履、佩</span>
</details>
<details><summary>阴神</summary>
<span class="leaf">阴神养成</span>
</details>
<span class="leaf">异宝</span>
<span class="leaf">魂幡</span>
<details><summary>神通</summary>
<span class="leaf">派系</span>
<span class="leaf">功法装配与出招顺序</span>
<span class="leaf">等级与星级</span>
</details>
<details><summary>心法</summary>
<details><summary>主要四维</summary>
<span class="leaf">神威</span>
<span class="leaf">长生</span>
<span class="leaf">金甲</span>
<span class="leaf">融灵</span>
</details>
<span class="leaf">等级与星级</span>
<span class="leaf">道业</span>
</details>
</details>
<details><summary>战斗阶段</summary>
<details><summary>开始阶段</summary>
<span class="leaf">灵压比拼</span>
</details>
<details><summary>喂招阶段</summary>
<span class="leaf">神通、法宝</span>
</details>
<details><summary>结束阶段</summary>
<span class="leaf">终结法宝</span>
</details>
<details><summary>战斗表现</summary>
<span class="leaf">入场</span>
<span class="leaf">技能释放</span>
<span class="leaf">法宝释放</span>
<span class="leaf">终结释放</span>
</details>
</details>
</details>
<details><summary>任务与剧情相关</summary>
<details><summary>任务系统</summary>
<details><summary>日常、周常任务</summary>
<details><summary>历练</summary>
<details><summary>活跃度系统入口</summary>
<span class="leaf">每日活跃奖励</span>
<span class="leaf">每周活跃奖励</span>
<span class="leaf">活跃度通行证</span>
</details>
</details>
</details>
<details><summary>新手任务</summary>
<span class="leaf">飞升之路：新手期奖励引导系统</span>
</details>
<details><summary>主线任务</summary>
<details><summary>神秘罗盘</summary>
<span class="leaf">轮盘引导主线推进</span>
</details>
</details>
<details><summary>长生阁</summary>
<span class="leaf">星官赐福：每日福利签到系统</span>
<span class="leaf">境界奖励：等级奖励系统（免费档次与付费档次）</span>
<span class="leaf">天纺绘锦：每周更新的常驻皮肤抽奖系统</span>
<span class="leaf">社区活动：公众号、社区群等入口</span>
</details>
</details>
<details><summary>剧情相关</summary>
<details><summary>剧情与NPC</summary>
<span class="leaf">道院地位</span>
<span class="leaf">执剑堂</span>
<span class="leaf">后山</span>
<span class="leaf">弟子堂</span>
<span class="leaf">任务引导</span>
</details>
<details><summary>关卡探索</summary>
<span class="leaf">战斗相关系统</span>
<details><summary>剧情文案相关系统</summary>
<span class="leaf">论道玉简</span>
<span class="leaf">道友录</span>
<span class="leaf">神念禁制</span>
<span class="leaf">尘仙笔录</span>
</details>
</details>
</details>
</details>
</details>
  </div>
</div>

<div class="section" id="sec7">
  <div class="sec-num">07</div>
  <h2 class="sec-title">整体评价</h2>

  <div class="callout highlight">
    <div class="callout-title">✅ 游戏优势</div>
    <p>传统放置挂机赛道以 2D 为主（一念逍遥/最强祖师/寻道大千），<strong>问剑长生用3D 画风与演出带来差异化新体验</strong>；相比同类高氪度基准，日常氪金需求属平民友好级；PVP/PVE/宗门战/跨区战/副本战玩法拓展充分，对重社交玩家吸引力强。</p>
  </div>

  <div class="callout risk">
    <div class="callout-title">⚠️ 游戏劣势</div>
    <p>运营活动氪金需求大、平民与氪金差距大、死区死服频繁；本质仍是氪金数值游戏，目标群体固化难以吸纳新血。系统层面：养成系统过多且打磨深度不足、部分系统强绑定氪金（如阴神系统单天赋树 + 单一氪金获取通道）——本质是<strong>过度创造养成缺口与氪金点</strong>，拉开玩家差距。</p>
  </div>

  <div class="callout design">
    <div class="callout-title">🛠️ 改善意见</div>
    <p>1）减少接入新养成系统，转为拓展打磨现有系统，减少养成注意力分散；2）提高运营活动福利力度、略微延长活动周期（现平均 3 天/轮），让平民与微氪玩家获得半成品资源，提升获得感、缩小差距感。</p>
  </div>

  <div class="callout analysis">
    <div class="callout-title">📌 总结</div>
    <p>表现符合中等评分定位：题材经典、玩法丰富、视觉体验好、社交乐趣足；但玩家阶级差距大、群体固化、运营活动过密。<strong>其系统设计与系统间关系值得研究借鉴，商业化开发上需要更多取舍思考。</strong></p>

</main>
</div>
