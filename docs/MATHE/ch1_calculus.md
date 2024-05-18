# Calculus

## 向量代数与解析几何

混合积
$$
\vec{a}\times(\vec{b}\cdot\vec{c})=
\begin{vmatrix}
a_x & a_y & a_z \\\
b_x & b_y & b_z \\\
c_x & c_y & c_z
\end{vmatrix}
$$

## 多元函数微分学

### 隐函数存在的条件

* 函数$F(P_0)$在$U(P_0)$连续
* $F(P_0)=0$
* 在$U(P_0)$内存在连续偏导数$F_x^{'}(P),F_y^{'}(P)$
* $F_x^{'}(P)\neq0,orF_y^{'}(P)\neq0$

### 基本性质

1. 一阶偏导连续一定可微，二阶偏导连续二阶混合偏导相等

2. 若函数$f$可微，则$\frac{ \partial f }{ \partial \vec l_0 }=\nabla f\cdot \vec l_0$

3. 几何上的应用

* $l=F \cap G$,则$l$在$P_0$的切向量平行于$(\frac{ \partial(F,G) }{ \partial(y,z) },\frac{ \partial(F,G) }{ \partial(z,x) },\frac{ \partial(F,G) }{ \partial(x,y) })$
   $$
   \vec l=(x(u,v),y(u,v),z(u,v))\\
   则其法向量为
   \left|\begin {array}{c}
   \vec i&\vec j&\vec k\\\
   x_u&y_u&z_u\\\
   x_v&y_v&z_v \\
   \end{array}\right|
   $$
* $F(x,y,z)的法向量为\vec n=(F_x^{'},F_y^{'},F_z^{'})$

## 多元函数积分学

### 重积分

* 常常采用剖分，以圆锥面、圆面为积分单元、对于对称域去掉奇函数相消，对于相同结构的积分以I(a)函数代替

* 变量替换

$$
\iint \limits_D f(x,y)dxdy=\iint \limits_Df(x(u,v),y(u,v))\lvert \frac{ \partial(x,y) }{ \partial(u,v) } \rvert  dxdy
$$
,其中有$\frac{ \partial(x,y) }{ \partial(u,v) }\cdot\frac{ \partial(u,v) }{ \partial(x,y) }=1\\$
对于三重积分$\lvert \frac{ \partial(x,y,z) }{ \partial(u,v,w) }\rvert ,\\$
若为线性变换,则是点到点，线到线的替换

非线性替换也往往是边界到边界的变换

* 积分微元
  二重积分$\quad rdrd\theta \\$ 
  三重积分$\quad \rho^2sin\varphi d\theta d\varphi d\rho$

### 曲线积分

曲线上的点满足一定关系

1. 第一类曲线积分

$$
\int_Lf(x,y)ds=\int_\alpha^{\beta}f(x(t),y(t))\sqrt{x^{'2}(t)+y^{'2}(t)}dt,\alpha <\beta
$$

1. 第二类曲线积分

#### 基本公式

$$
\int \limits_{\Gamma}\vec A\cdot d\vec s=\int \limits_{\Gamma}\vec A\cdot \vec \gamma_0ds
\\
\int Pdx+Ady+Rdz=\int (P,Q,R)\cdot\vec \gamma_0 ds,则dx=cos\alpha ds
$$

#### 格林公式

$$
\iint \limits_D \left|\begin {array}{c}
\frac{ \partial }{ \partial x}&\frac{ \partial }{ \partial y} \\
P&Q \\
\end{array}\right|dxdy=\oint_{L^+}Pdx+Qdy,
$$

#### 路径无关

单连通闭区域内  $du=Pdx+Qdy$

### 曲面积分

曲面上的点满足一定关系

#### 第一类曲面积分

$\iint \limits_Sf(x,y,z)dS\\= \iint \limits_{D_{xy}}f(x,y,z(x,y))\sqrt{z_x^{'2}+z_y^{'2}+1}dxdy\\=\iint \limits_{D_{xy}}f(x,y,z(x,y))\frac{1}{\lvert F_z^{'} \rvert}\sqrt{F_x^{'2}+F_y^{'2}+F_z^{'2}}dxdy$

对于$\vec r=(x(u,v),y(u,v),z(u,v)),$有
$$
dS=\lvert \vec r_u \times \vec r_v \rvert dudv\\
\vec r_u \times \vec r_v=(\frac {\partial (y,z)}{\partial (u,v)},\frac {\partial (z,x)}{\partial (u,v)},\frac{\partial (x,y)}{\partial (u,v)})\\
$$

$\lvert \vec r_u \times \vec r_v \rvert$用根号下模长的平方减去内积的平方计算

#### 第二类曲面积分

##### 基本公式

$$
\iint \limits_S Pdydz+Qdzdx+Rdxdy=\iint \limits_S(Pcos\alpha+Qcos\beta+Rcos\gamma)dS
$$

取曲面的上侧为正，则$\iint \limits_{\Sigma}R(x,y,z)dxdy=\iint \limits_{D_{xy}}R(x,y,z(x,y))dxdy$

取曲面上侧为正，若$z=f(x,y),则\iint \limits_L Pdydz+Qdzdx+Rdxdy=\iint \limits_{D_{xy}}(P,Q,R)\cdot (-f_x^{'},-f_y^{'},1)dxdy$

##### 高斯公式

三重积分与第二类面积分
$$
\iiint_V(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z})dxdydz=\iint_{\mathbb{S}}\kern{-18.8pt}\subset\kern{-2pt}\supset  Pdydz+Qdzdx+Rdxdy
$$

即$\iiint_V div \vec A dV=\iint_{\mathbb{S}}\kern{-18.8pt}\subset\kern{-2pt}\supset \vec A\cdot d\vec S.$
$div \vec A$为$\vec A=(P,Q,R)$的散度，
$div \vec A=\nabla \cdot A$

##### Stokes公式

第二类面积分与第二类线积分
$$
\iint \limits_S \left|\begin {array}{c}
cos\alpha& cos\beta& cos\gamma\\\
\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\\
P&Q&R
\end{array}\right|= \iint \limits_S \left|\begin {array}{c}
dydz& dzdx& dxdy\\\
\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\\
P&Q&R 
\end{array}\right|dS=\oint_L Pdx+Qdy+Rdz
$$
即$\iint \limits_S rot \vec A\cdot d\vec S =\oint_L A \cdot d\vec S$

其中
$$
rot\vec A=\nabla \times \vec A
$$

$$
rot\vec A=\left|\begin {array}{c}
 \vec i& \vec j& \vec k\\
\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\
P&Q&R \\
\end{array}\right|
$$

##### 场论初步

梯度场是无旋场

$rot(grad u)=\vec 0\qquad$

旋度场是无源场
$div(rot \vec A)=0\qquad$

$\vec A$既是无源场，又是无旋场，则一定存在势函数u,且$\Delta u =0$.
