# Why Your #1 Best-Seller Isn't Necessarily a Core Menu Item

**Menu Engineer** · article for operators and menu analysts  
**Author:** [Huaxia Li](https://x.com/MenuEngineerHX) · **Try the app (free Windows, demo embedded):** [Dual-Metric v1.0.1](https://github.com/lhx618257/magicmenu/releases/tag/menu-engineer-dual-metric-1.0.1)

---

**Summary:** Every restaurant tracks a sales leaderboard. That's useful—but it answers a different question than whether a dish deserves a long-term place on your **core menu**. Volume tells you what sold. **Core** dishes are better judged by whether guests **come back** and whether they **order that same item again**—**store repurchase** and **same-dish repurchase**.

---

## 1. "#1 in sales" answers a different question

Top-seller reports from your POS, delivery platform, or daily ops review all measure the same thing: **which SKU had the most units or revenue in a period**.

That matters—but the limits are clear:

- Openings, discounts, platform traffic, and bundled combos can push a dish to **#1 for a few weeks**;
- Large portions, default combo items, and staff push can **inflate volume** without building loyalty to that dish;
- If you only watch sales rank, you often label **traffic drivers, promos, or one-off hits** as **strategic anchors**.

So: **#1 in sales is a popularity metric—not a full definition of "core menu item."**

---

## 2. What "core menu item" usually means

In menu engineering and chain operations, a **core** item typically satisfies at least one of these—ideally both:

1. **Sustained business contribution**—not a three-day spike, but stable volume and margin (or contribution profit when you have recipe cost) across multiple periods.
2. **A real relationship with guests**—they **return to the store** and **order the same dish again** (or the same clearly defined product).

The second point is easy to skip—and hard to fake:  
Promos can inflate sales; they rarely inflate **repurchase structure**.

---

## 3. Two repurchase rates: closer to "core" than volume alone

If you have **order-line data plus a user key** (member ID, hashed phone, or de-duplicated guest per order), you can split "core" into two measurable dimensions:

| Dimension | Plain meaning | vs. sales rank |
|-----------|---------------|----------------|
| **Store repurchase rate** | Among guests who ordered this dish in the window, how many **came back to the store** (any purchase) | High sales + low store repurchase → often **promo/acquisition**, weak retention |
| **Same-dish repurchase rate** | Among guests who ordered this dish, how many **ordered that same dish again** | High sales + low same-dish repurchase → **trial without repeat**—"viral try-once" behavior |

Your **#1 best-seller** can easily look like this:

- **Low store + low same-dish repurchase**—sells a lot, guests don't return or re-order → **traffic or experiment**, not a long-term core.
- **High store, low same-dish**—guests return but order something else → **traffic hub**; needs pairing, combos, and messaging—not a solo loyalty hero.
- **High same-dish, relatively lower store**—loyalty to the dish, fewer extra visits → **niche breakout**; worth studying visibility and visit drivers.
- **Both relatively high**—closest to what many operators mean by a **true core item**.

**Sales rank and "core item" are not synonyms.**

---

## 4. A fictional example (same logic as real stores)

Assume a 60-day window on staple items:

- **Dish A: Sour cabbage fish**—**#1 in units**, **low same-dish repurchase**, **medium store repurchase**.
  - Read: combos and seasonal push drove volume; some guests return but **don't order this fish again**.
  - Action: check consistency, combo dilution, portion mix—don't treat it as your **only flagship** without evidence.

- **Dish B: Signature beef noodles**—**#5 in units**, **high same-dish repurchase**, **high store repurchase**.
  - Read: not the biggest seller, but guests who try it **come back and order the same bowl again**.
  - Action: menu placement, staff recommendation, stock and kitchen capacity—**core candidate**.

A volume-only leaderboard steers you toward A; a repurchase view steers resources toward B.  
**That's what menu engineering is supposed to surface.**

---

## 5. How this relates to the classic popularity × margin matrix

The traditional menu matrix uses **sales (or mix %) × contribution margin**—stars, plowhorses, puzzles, dogs, etc.

The two repurchase metrics **don't replace** margin analysis; they add the **behavior** side:

- Without food cost, you can still run a **behavior quadrant** with **store × same-dish repurchase**;
- With cost, flag **high margin + high same-dish repurchase** as **profit-and-loyalty core**.

A #1 seller sitting in "high volume, low repurchase" is often **risk or traffic**, not core—on a behavior map.

---

## 6. Three practical takeaways for operators

1. **Keep the bestseller list**—but add a repurchase note: **TOP sales ≠ strategic core**.
2. **After menu changes** (price, rename, combo structure), don't only compare **sales week-over-week**. Compare **cohort store and same-dish repurchase**—otherwise you won't know if you moved **hype** or **relationship**.
3. **When resources are tight**: protect **dual-high repurchase** items first; for **high volume, low repurchase**, diagnose product, price, or bundle structure before delisting or doubling down.

---

## 7. Data you need—and tools

Minimum fields (typical POS exports):

- Order date, order ID, user ID (optional but strongly recommended), category, dish name/SKU, quantity, net amount

With those, you can build cohorts and same-dish repurchase in an observation window.  
**Aggregated sales only**—no guest key—can't strictly separate **core** from **one-off hits**.

**Menu Engineer — Dual-Metric Edition** plots each dish on a **store repurchase × same-dish repurchase** bubble quadrant. Bilingual built-in demos; import CSV and explore.

- Installer: https://github.com/lhx618257/magicmenu/releases/tag/menu-engineer-dual-metric-1.0.1
- Updates: https://x.com/MenuEngineerHX

---

## Closing

**#1 in sales is an outcome.** A **core menu item** is a **relationship plus persistence**.  
If analytics stops at the TOP 10 list, menu decisions will systematically favor short-term heat.  
Adding **store** and **same-dish repurchase** doesn't reject sales—it gives "core" a defensible definition.

---

---

# 为什么销量第一的菜，不一定是菜单里的「核心菜」

**Menu Engineer 菜单工程师** · 面向餐饮经营者与菜单分析  
**作者：** [栗华夏 / Huaxia Li](https://x.com/MenuEngineerHX) · **免费试用（Windows，演示内嵌）：** [双率专版 v1.0.1](https://github.com/lhx618257/magicmenu/releases/tag/menu-engineer-dual-metric-1.0.1)

---

**摘要：** 餐饮门店几乎都会看「销量排行第一」，但这回答的是「哪道菜卖得多」，并不等同于这道菜该不该作为长期 **核心菜**。销量是热度；核心菜更要看顾客是否 **再次到店**，以及是否 **再次点同一道菜**——**到店复购**与**同菜复购**。

---

## 一、销量第一，回答的是另一个问题

畅销榜、POS 报表、外卖 TOP 菜，衡量的是：**某段时间里哪道菜销量最高**。

这很重要，但边界也很清楚：

- 开业、打折、平台流量、套餐捆绑，都能把菜 **短期顶到第一**；
- 大份、默认套餐项、员工推荐，会让 SKU **量很大**，不等于顾客「认这道菜」；
- 只盯销量，容易把 **引流菜、促销菜、一次性爆款** 当成 **菜单支柱**。

**销量第一是热度指标，不是「核心菜」的完整定义。**

---

## 二、什么叫菜单里的「核心菜」？

在菜单工程（Menu Engineering）实践中，「核心菜」通常至少满足其一，最好两者兼具：

1. **持续贡献**——多周期稳定出量、稳定毛利（有成本时还可看贡献利润）。
2. **与顾客有关系**——愿意 **再次到店**，并愿意 **再次点同一道菜**。

第二条最难伪造：促销能拉高销量，很难伪造 **复购结构**。

---

## 三、两个复购率：比销量更接近「核心」

若有 **订单行 + 用户标识**（会员 ID、订单用户去重等），可把「核心」拆成两维：

| 维度 | 含义 | 与销量 |
|------|------|--------|
| **到店复购率** | 点过该菜的用户中，之后又 **来过店**（任意消费）的比例 | 高销量、低到店复购 → 可能靠拉新/促销， **没留住人** |
| **同菜复购率** | 点过该菜的用户中，之后 **再点同一道菜** 的比例 | 高销量、低同菜复购 → **试过一次不再点** |

**销量第一** 仍可能是：

- 双复购都低 → **流量/试验菜**，不宜当长期核心；
- 到店高、同菜低 → **引流底盘**，需搭配与话术；
- 同菜高、到店相对低 → **黑马菜**，值得研究曝光；
- 双高 → 更接近 **真·核心菜**。

**排行第一 ≠ 核心菜。**

---

## 四、虚构例子（与真实门店逻辑一致）

观察窗 60 天，主食类：

- **A 酸菜鱼**：销量 **第 1**，同菜复购 **偏低**，到店复购 **中等** → 套餐/推广抬量，顾客未必再点这道菜；慎当唯一招牌。
- **B 招牌牛肉面**：销量 **第 5**，同菜与到店复购 **都高** → 吃过的人会再来、再点同一碗；宜加大露出与出餐保障。

只看销量榜会押 A；用复购视角更应倾向 B。

---

## 五、与「人气 × 毛利」矩阵的关系

传统四象限用 **销量 × 毛利贡献**。  
双复购 **不替代** 毛利，而是补上 **行为侧**；无成本时仍可做 **行为四象限**；有成本后再标 **高毛利 + 高同菜复购** 为利润型核心。

---

## 六、三条实用结论

1. 畅销榜继续看，但记住：**销量 TOP ≠ 战略核心**。
2. **改菜单**（改价、改名、改套餐）后，别只比销量环比，要比 **cohort 到店与同菜复购**。
3. 资源有限时，优先保护 **双复购双高** 的菜；对 **量高复购低** 先诊断再决定下架或改配。

---

## 七、数据与工具

最少字段：营业日期、订单号、用户 ID（强烈建议）、品类、菜名/SKU、数量、实付金额。  
仅有汇总销量、无用户维度时，**无法严格区分** 核心菜与爆款。

**Menu Engineer 双率专版** 用 **到店复购 × 同菜复购** 气泡四象限看每道菜；内置中英 demo，导入 CSV 即可试。

- 安装包：https://github.com/lhx618257/magicmenu/releases/tag/menu-engineer-dual-metric-1.0.1
- 动态：https://x.com/MenuEngineerHX

---

## 结语

销量第一是 **结果**；核心菜是 **关系 + 持续性**。  
只刷新 TOP 10，菜单决策会系统性偏向短期热度；把 **到店复购** 与 **同菜复购** 摆上台面，不是否定销量，而是给「核心菜」更可辩护的定义。

---

## Keywords / 关键词

menu engineering, restaurant analytics, repurchase rate, store repurchase, same-dish repurchase, bestseller, core menu item, menu optimization, POS order data, bubble chart, cohort analysis, 菜单工程, 餐饮数据分析, 复购率, 同菜复购, 到店复购, 核心菜, 畅销菜, 菜品分析
