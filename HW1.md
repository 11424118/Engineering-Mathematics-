# First-Order ODE 第 1 題
## 題目：

## $$\frac{dy}{dx} = xy$$

## 解答過程:
1. 分離變數：將所有 $y$ 移至左側，所有 $x$ 移至右側：
   
$$\frac{1}{y} dy = x dx$$

2. 兩邊積分

$$\int \frac{1}{y} dy = \int x dx$$

$$\ln|y| = \frac{1}{2}x^2 + C_1$$

3. 求解y:

$$y = e^{\frac{1}{2}x^2 + C_1} = e^{C_1} \cdot e^{\frac{1}{2}x^2}$$

令 $C = e^{C_1}$，得到通解：

$$y = Ce^{\frac{1}{2}x^2}$

# Second-order ODEs 第 17 題
## 題目
## 已知 $y_1 = e^x$ 為 $y'' - 2y' + y = 0$ 的一個解，求第二個獨立解 $y_2$。

## 解答過程:
1. 設定 $y_2$ 形式：利用降階法，令 $y_2 = u(x)y_1 = u(x)e^x$。
2. 帶入公式：對於標準式 $y'' + P(x)y' + Q(x)y = 0$，公式為：

$$u(x) = \int \frac{e^{-\int P(x)dx}}{y_1^2} dx$$

3. 計算：在此題中 $P(x) = -2$：

$$e^{-\int -2 dx} = e^{2x}$$

$$u(x) = \int \frac{e^{2x}}{(e^x)^2} dx = \int \frac{e^{2x}}{e^{2x}} dx = \int 1 dx = x$$

4. 得到結果:

$$y_2 = x \cdot e^x$$ 

因此通解為 $y = C_1 e^x + C_2 x e^x$。
