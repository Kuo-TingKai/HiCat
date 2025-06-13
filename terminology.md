Coherence - 在範疇論中，相干性指的是結構之間的相容性和一致性，特別是在高維範疇中，確保不同層次的結構能夠和諧地組合在一起。

Strictification - 將弱結構轉化為嚴格結構的過程，例如將弱2-範疇轉化為嚴格2-範疇，這是一個重要的技術工具，可以簡化某些證明。

Lax functor - 一種特殊的函子，其結構映射不要求嚴格相等，而是允許存在2-態射，比普通函子更靈活，在實際應用中更常見。

Horizontal equivalence - 在雙範疇中，對象之間的一種等價關係，與垂直等價相對，描述了不同層次的結構之間的關係。

Tabulator - 在雙範疇中，用於表示和組織數據的特殊結構，可以看作是某種"表格"或"矩陣"的抽象化。

span representation - 使用範疇論中的span（跨度）來表示某些數學結構，span是從一個對象到另一個對象的"橋樑"結構。

double comma - 一種特殊的極限構造，可以看作是普通逗號範疇的推廣。

transversal transformation - 在雙範疇中，連接不同層次結構的變換，與縱向變換相對。

intercategory - 一種特殊的範疇結構，用於描述不同範疇之間的交互，可以看作是範疇之間的"橋樑"。

Puppe exact category - 由Dieter Puppe引入的一種特殊範疇，用於研究正合序列和同調代數，在代數拓撲和代數幾何中有重要應用。

---

## Tabulator（表格化子）的深入解釋

在弱雙範疇 $\mathbb{A}$ 中，給定一個垂直箭頭 $u: X \to Y$，**1-維 tabulator**（或稱 cell representer）是與 $u$ 關聯的一個對象 $T = Tu$，並配有一個 cell $\pi: e_T \to u$。這裡 $e_T$ 是一個「單位」cell，$\pi$ 則是從 $e_T$ 到 $u$ 的一個2-態射。

這個結構滿足一個**普遍性條件**：對於任意對象 $A$ 及任意 cell $\varphi: e_A \to u$，存在唯一的水平箭頭 $h: A \to T$，使得 $\varphi = e_h \mid \pi$。這裡 $e_h$ 是由 $h$ 誘導的單位cell，$\mid$ 表示cell的組合。

用圖表示如下：

$$
\begin{array}{ccc}
T & \xrightarrow{p} & X \\
e_T \downarrow & \overset{\pi}{\Rightarrow} & \downarrow u \\
T & \xrightarrow{q} & Y
\end{array}
$$

這個普遍性條件意味著，tabulator $T$ 和cell $\pi$ 組成了一個從函子 $e: \mathrm{Hor}_0\mathbb{A} \to \mathrm{Hor}_1\mathbb{A}$ 到 $u$ 的**普遍箭頭**（universal arrow）。

### 具體意義

- **普遍性**：tabulator 的本質是「表示」所有從單位cell到 $u$ 的cell，並且這種表示是唯一的（up to unique horizontal map）。
- **伴隨函子**：如果所有這樣的tabulator都存在，則函子 $e$ 有右伴隨，這是範疇論中非常重要的性質。
- **與span的關係**：這使得 $\mathbb{A}$ 可以被看作是span的弱雙範疇。

### 1-維 cotabulator

cotabulator 是tabulator的對偶。給定 $u: X \to Y$，cotabulator是對象 $C = Lu$ 和一個普遍cell $\iota: u \to e_C$，滿足對偶的普遍性條件。cotabulator的存在意味著函子 $e$ 有左伴隨。

cotabulator的圖示如下：

$$
\begin{array}{ccc}
X & \xrightarrow{i} & C \\
u \downarrow & \overset{\iota}{\Rightarrow} & \downarrow e_C \\
Y & \xrightarrow{j} & C
\end{array}
$$

### 應用與意義

- **tabulator** 讓我們能夠用一個「代表性」對象來統一描述所有到 $u$ 的cell，這在構造和理解雙範疇的結構時非常有用。
- **cotabulator** 則對應於cospan的情形。
- 這些結構與極限、伴隨函子、普遍性等範疇論核心概念密切相關。

**簡單總結**：  
Tabulator 是一種在雙範疇中「代表」所有到某個cell的結構，並且這種代表具有普遍性和唯一性。它的存在與函子的伴隨性質密切相關，並且在理解span、cospan等結構時非常關鍵。