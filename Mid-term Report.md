# 題目六：質量-彈簧-阻尼系統 (Mass-Spring-Damper System)

### 1. 工程問題建模
本案例分析車輛避震器受路面起伏影響的狀況。根據**牛頓第二運動定律**，該系統位移 $x(t)$ 的控制方程式如下：

$$m \frac{d^2x}{dt^2} + c \frac{dx}{dt} + kx = F_0 \cos(\omega t)$$

**參數說明：**
* **$m$**：車體質量
* **$c$**：避震器阻尼係數
* **$k$**：彈簧常數
* **$F_0 \cos(\omega t)$**：頻率為 $\omega$ 的正弦外力

---

### 2. 數學求解步驟與結果

#### (1) 齊次解 $x_h(t)$ (Transient Response)
令右式為 0，求齊次方程式 $mx'' + cx' + kx = 0$ 的解。此部分解會因阻尼作用隨時間衰減：
$$mr^2 + cr + k = 0 \implies x_h(t) = \dots$$

#### (2) 特解 $x_p(t)$ (Steady-State Response)
當外力為 $F_0 \cos(\omega t)$ 時，系統最終會趨於穩定的週期性震盪。假設 $x_p(t) = X \cos(\omega t - \phi)$，則：

**穩態振幅 $X$：**
$$X = \frac{F_0}{\sqrt{(k - m\omega^2)^2 + (c\omega)^2}}$$

**相位角 $\phi$：**
$$\phi = \tan^{-1} \left( \frac{c\omega}{k - m\omega^2} \right)$$

#### (3) 最終通解 $x(t)$
$$x(t) = x_h(t) + X \cos(\omega t - \phi)$$

---

### 3. 工程分析與結論
1. **暫態與穩態**：齊次解 $x_h(t)$ 在工程上稱為「暫態解」，會快速消失；而 $x_p(t)$ 為「穩態解」，是避震器在持續受力下的最終表現。
2. **避震設計**：透過調整阻尼係數 $c$，可以改變振幅 $X$ 與相位 $\phi$，避免車體產生共振（Resonance）並有效吸收路面能量。
