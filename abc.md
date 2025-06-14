# Vojta 猜想（Vojta Conjecture）

Vojta 猜想是數論和代數幾何中的一個重要猜想，特別是關於代數曲線和數域上的有理點的分布。

## 猜想內容解釋

設 $X$ 是一個定義在數域 $k$ 上的光滑、幾何連通的射影曲線，$D$ 是 $X$ 上的一個約化除子（reduced divisor），$U_X := X \setminus D$ 表示去掉 $D$ 後的開子集。設 $\omega_X$ 為 $X$ 上的典範層（canonical sheaf）。假設 $U_X$ 是一條雙曲曲線，即 $\deg(\omega_X(D)) > 0$。

對於任意 $d \in \mathbb{Z}_{>0}$ 和 $\epsilon \in \mathbb{R}_{>0}$，Vojta 猜想斷言：

$$
\mathrm{ht}_{\omega_X(D)} \lesssim (1+\epsilon)(\log\text{-}\mathrm{diff}_X + \log\text{-}\mathrm{cond}_D)
$$

這裡 $\mathrm{ht}_{\omega_X(D)}$ 是與 $\omega_X(D)$ 相關的高度函數，$\log\text{-}\mathrm{diff}_X$ 和 $\log\text{-}\mathrm{cond}_D$ 分別是與 $X$ 和 $D$ 相關的對數微分和對數條件數。

這個不等式對所有定義在 $\overline{\mathbb{Q}}$ 上、度數不超過 $d$ 的 $U_X$ 上的點成立，除了有限多個例外。

## 數學意義

Vojta 猜想將代數幾何中的高度理論與數論中的有理點分布聯繫起來，並且與著名的 $abc$ 猜想等深刻命題密切相關。它預測了在某些條件下，有理點的高度受到嚴格限制，這對理解有理點的分布和算術幾何有重要意義。

## 詞彙表

- **約化除子（reduced divisor）**：在代數幾何中，[除子](#除子divisor)是指在曲線上的形式和整數係數的有限點集。約化除子是指所有點的係數都為0或1的除子，也就是說，每個點最多只出現一次，沒有重複。

- **典範層（canonical sheaf）**：典範層是代數幾何中描述曲線上[正則微分形式](#正則微分形式regular-differential-form)的線性系統。對於一條光滑曲線 $X$，其典範層 $\omega_X$ 是所有[正則微分形式](#正則微分形式regular-differential-form)構成的層。它在研究曲線的幾何性質和分類時非常重要。

- **高度函數（height function）**：
  高度函數是數論中用來衡量有理點「複雜度」或「大小」的工具。對於射影空間 $\mathbb{P}^n$ 上的有理點 $P = [x_0 : x_1 : \cdots : x_n]$，其中 $x_i$ 為整數且互質，則其絕對高度定義為：
  $$
  H(P) = \max\{|x_0|, |x_1|, \ldots, |x_n|\}
  $$
  對於一般數域 $K$，有理點 $P = [x_0 : \cdots : x_n]$，其高度定義為：
  $$
  H_K(P) = \prod_{v \in M_K} \max\{|x_0|_v, \ldots, |x_n|_v\}^{d_v/[K: \mathbb{Q}]}
  $$
  其中 $M_K$ 為 $K$ 的所有[價](#價valuation)，$|\cdot|_v$ 為 $v$ 上的絕對值，$d_v$ 為 $v$ 的局部度數。

- **正則微分形式（regular differential form）**：
  在代數幾何中，[正則微分形式](#正則微分形式regular-differential-form)是指在光滑代數曲線（或更一般的光滑代數簇）上處處無奇異點的微分形式。對於一條光滑曲線 $X$，[正則微分形式](#正則微分形式regular-differential-form)可以寫作 $f(x)dx$，其中 $f(x)$ 在 $X$ 上是正則函數。所有[正則微分形式](#正則微分形式regular-differential-form)構成的層即為[典範層](#典範層canonical-sheaf)。 

- **對數微分（logarithmic differential）**：
  設 $X$ 是定義在數域 $k$ 上的光滑射影曲線，$K$ 是 $k$ 的有限擴張。對於 $X$ 上的點 $P \in X(K)$，其對數微分 $\log\text{-}\mathrm{diff}_X(P)$ 定義為：
  $$
  \log\text{-}\mathrm{diff}_X(P) = \sum_{v \in M_K} \max\{0, -\log|\omega|_v(P)\}
  $$
  其中 $M_K$ 是 $K$ 的所有[價](#價valuation)的集合，$|\cdot|_v$ 是 $v$ 上的絕對值，$\omega$ 是 $X$ 上的[典範微分形式](#正則微分形式regular-differential-form)。這個量衡量了點 $P$ 在每個素數位置上的[分歧](#分歧ramification)程度。

- **對數條件數（logarithmic conductor）**：
  設 $D$ 是 $X$ 上的一個[約化除子](#約化除子reduced-divisor)，$K$ 是 $k$ 的有限擴張。對於 $X$ 上的點 $P \in X(K)$，其對數條件數 $\log\text{-}\mathrm{cond}_D(P)$ 定義為：
  $$
  \log\text{-}\mathrm{cond}_D(P) = \sum_{v \in M_K} \max\{0, -\log|f_D|_v(P)\}
  $$
  其中 $f_D$ 是定義除子 $D$ 的局部方程。這個量描述了點 $P$ 相對於除子 $D$ 的算術行為，特別是在素數位置上的[分歧](#分歧ramification)性質。

- **分歧（ramification）**：
  在代數數論和代數幾何中，分歧是指數域擴張或覆蓋映射中的特殊現象。具體來說：

  1. **數域擴張中的分歧**：
     設 $L/K$ 是數域的有限擴張，$v$ 是 $K$ 的一個[價](#價valuation)。如果 $v$ 在 $L$ 中的延拓 $w$ 滿足 $e(w|v) > 1$，其中 $e(w|v)$ 是分歧指數，則稱 $v$ 在 $L/K$ 中分歧。分歧指數 $e(w|v)$ 衡量了 $v$ 在擴張中的"分裂程度"。

  2. **代數曲線覆蓋中的分歧**：
     設 $f: Y \to X$ 是代數曲線之間的有限覆蓋映射。點 $P \in Y$ 稱為分歧點，如果 $f$ 在 $P$ 處的微分 $df_P$ 為零。分歧點集是 $Y$ 上的有限點集，其像在 $X$ 上稱為分支點（branch point）。

  分歧理論在 Vojta 猜想中扮演重要角色，因為它直接影響了[對數微分](#對數微分logarithmic-differential)和[對數條件數](#對數條件數logarithmic-conductor)的計算。

- **價（valuation）**：
  在數論中，價是定義在數域上的函數，用於衡量數的"大小"。對於數域 $K$，其價 $v$ 是一個從 $K^\times$ 到實數的函數，滿足：
  1. $v(ab) = v(a) + v(b)$
  2. $v(a+b) \geq \min\{v(a), v(b)\}$
  3. $v(a) = \infty$ 當且僅當 $a = 0$

  價在[對數微分](#對數微分logarithmic-differential)和[對數條件數](#對數條件數logarithmic-conductor)的定義中起著關鍵作用，用於衡量數在不同素數位置上的行為。

- **除子（divisor）**：
  在代數幾何中，除子是指在曲線上的形式和整數係數的有限點集。形式上，一個除子 $D$ 可以寫作：
  $$
  D = \sum_{P \in X} n_P P
  $$
  其中 $n_P$ 是整數，且只有有限多個 $n_P$ 不為零。除子是研究代數曲線的重要工具，在[對數條件數](#對數條件數logarithmic-conductor)的定義中起著核心作用。 