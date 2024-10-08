---
layout: single
title: "9-1)Plane Wave"
typora-root-url: ../
categories : "Electromagnetic"
tag : electrodynamics
#tag : [me, me2, me3]
toc : true
toc_sticky : true
author_profile : false
---
## Electromagnetic 

 #### Electromagnetic Wave

Maxwell equation은 다음과 같다.
$$
\begin{align}
&\triangledown \cdot E &&= 0
\\
&\triangledown \times E &&= -\frac{\partial B}{\partial t}
\\
&\triangledown \cdot B &&= 0
\\
&\triangledown \times B &&= \mu_0\epsilon_0\frac{\partial E}{\partial t}
\end{align}
$$
전기장과 자기장이 first-order, PDE 형태로  coupled 되어 있다.

전기장과 자기장을 de-coupling시켜보자.
$$
\begin{align}
&1. \triangledown \times (\triangledown \times \vec{E}) &&= -\triangledown \times \frac{\partial \vec{B}}{\partial t}
\\
&\triangledown^2\vec{E} &&= \mu_0 \epsilon_0 \frac{\partial ^2 \vec{E}}{\partial t^2} : \text{Helmholtz equation}
\\
&2. \triangledown \times (\triangledown \times \vec{B}) &&= \triangledown \times \mu_0 \epsilon_o \frac{\partial E}{\partial t}
\\
&\triangledown^2 \vec{B} &&= \mu_0 \epsilon_0 \frac{\partial ^2 \vec{B}}{\partial t ^2} : \text{Helmholtz equation}
\end{align}
$$
De-coupling을 시키면 second-order , PDE 형태로 decoupled 되어 있는 것을 확인 할 수 있다.

앞서 파동의 성질에서 $\triangledown ^2 f = \frac{1}{v^2}\frac{\partial ^2 f}{\partial t^2} $ 이므로

위의 식에서 다음을 알 수 있다.
$$
v = \frac{1}{\sqrt{\mu_0 \epsilon_0}} = 3.00 \times 10^8 m/s
$$

이를 조금 더 물리적인 의미가 느껴지도록 다가가보자.

다음과 같이 표현가능하다.
$$
\frac{\partial ^2 \vec{E}}{\partial t^2} = v^2 \frac{\partial^2 \vec{E}}{\partial x ^2}
$$
파동의 가속도의 관한 부분이 파동의 속도와 변곡성에 관해 비례한다는 것을 의미한다.

---

#### Plane wave

plane wave의 source는 점전하가 아니라 전류가 $\omega$에 따라 진동하는 무한 평면이다.

phasor에 개념을 통해 Maxwell equation을 쓰면 다음과 같다.
$$
\begin{align}
&\triangledown \cdot \vec{\bold{E}}(r) &&= 0
\\
&\triangledown \times \vec{\bold{E}}(r) &&= i \omega \vec{\bold{B}}(r)
\\
&\triangledown \cdot \vec{\bold{B}}(r) &&= 0
\\
&\triangledown \times \vec{\bold{B}}(r) &&= -i\omega \mu_0 \epsilon_0 \vec{\bold{E}}(r)
\end{align}
$$
이를 de-coupling시키면 다음과 같다.
$$
\begin{align}
&1. \triangledown ^2 \vec{\bold{E}}(r) + \omega ^2 \epsilon _0 \mu _0 \vec{\bold{E}}(r) =0
\\
&2. \triangledown ^2 \vec{\bold{B}}(r) + \omega ^2 \epsilon _0 \mu _0 \vec{\bold{B}}(r) =0
\\
\end{align}
$$

$$
\begin{align}
&\bold{\text{전자기파에 대한 operator는 } \triangledown ^2 \text{이다.}}
\\
&\omega ^2 \epsilon _0 \mu_0  = k^2 \text{이라 정의하자.} ~~~~\text{ 즉, eigenvalue :} k^2
\\
&\text{또한 plane wave이므로} ~ \vec{\bold{E}}(r) = \bold{E}(x)~\text{라 정의하자. 라고 쓰면 안된다.}
\\
&\vec{\bold{E}}(r) = {\bold{E}}(r) \hat{x}
\\
&\vec{\bold{E}} \text{가 z축에 대해 depend한다고 가정하자.}
\\
&\therefore \vec{\bold{E}}(z) = {\bold{E}}(z) \hat{x}
\end{align}
$$

이를 통해 다음을 구할 수 있다.
$$
\begin{align}
&\text{위 식을 적분하면 다음을 얻을 수 있다.}
\\
&\vec{\bold{E}}(z) = {\bold{E}}(z) \hat{x} = \hat{x} \bold{E}^+ _0 e^{ikz} +  \hat{x} \bold{E}^- _0 e^{-ikz} 
\\
&k\text{에 방향을 부여하고,} ~~~\vec{k} \cdot \vec{k} = k^2 \omega ^2 \epsilon _ 0 \mu _ 0 \text{라 정의하면 다음처럼 나타내는 것이 이제 가능하다.}
\\
&\divideontimes \hat{x} \bold{E}^- _0 e^{-ikz}\text{가 사라지는 term이 된다.}
\\
\\
&\vec{E}(z,t) = \hat{x} Real(\bold{E}e^{-i\omega t})= \hat{x}Real(\vec{E}_0 e^{(i\vec{k}\cdot \vec{r})}e^{-i\omega t})
\\
&\text{이를} \triangledown \cdot \vec{\bold{E}}(z) = 0\text{에 대입하여 어떻게 나오는지 살펴보자.}
\\
\\
&\text{divergence를 취하면 다음과 같다.}
\\
&\triangledown \cdot \vec{E}(z,t) = Real(i\vec{k} \cdot \vec{E}(z) e^{-i \omega t})
\\
&\therefore \hat{x}\triangledown \cdot \bold{E}(z) = \hat{x}i\vec{k}\cdot \bold{E}(z)
\\
\end{align}
$$
결론 1 : 전기장을 공간에 대해서 미분하는 것은 phasor에서 $-i \omega$ 를 곱할 때 처럼 $i\vec{k}$ 를 내적하면 된다.

결론 2 : 전기장은 다음처럼 나타낼 수 있다. $ \vec{x} E(r,t) = \vec{x} E_0 e^{i \vec{k} \cdot \vec{r}}$

결론 3 : $k > 0 $ , $\vec{k} \cdot \vec{k} = k^2 = \omega^2 \epsilon_0 \mu_0 $



자기장에 대해서는 다음과 같이 구한다.
$$
\begin{align}
\\
&\triangledown \times \vec{\bold{E}}(r) = i \omega \vec{\bold{B}}(r)\text{를 전개하면 다음과 같다.}
\\
&\vec{\bold{B}}(r) = \frac{\triangledown \times \vec{\bold{E}}(r)}{i \omega}
\\
&\text{위 식에서 전기장에 대한 식을 직접 구했으므로 외적하면 다음과 같다.}
\\
&\triangledown \times \bold{E}(r) = i \vec{k}\times \bold{E}(r) \text{를 구할 수 있다}
\\ 
&\bold{B}(r) = \frac{\triangledown \times \bold{E}(r)}{i \omega} \text{이므로}
\\
&\bold{B}(r) = \frac{i \vec{k}\times \bold{E}(r)}{i \omega}= \frac{k}{\omega}\hat{k}\times \bold{E}(r)= \frac{\hat{k}}{c}\times \bold{E}(r)
\end{align}
$$

정리

<img src="/images/9. Plane wave/image-20231227145303637.png" alt="image-20231227145303637" style="zoom:80%;" />

전기장의 공간에 대한 curl은 자기장의 시간에 대한 미분과 같다.

---

#### Poynting Vector

앞서 배웠던 것(1단원) Energy는 다음에 따라 계산된다.
$$
\begin{align}
W &= \frac{1}{2}\int \rho V d\tau = \frac{\epsilon_0}{2}\int (\triangledown \cdot E)V d\tau 
\\
&= \frac{\epsilon_0}{2}[-\int E \cdot (\triangledown V)d\tau + \oint_S V E\cdot da] \text{ : integration by parts}
\\
&= \frac{\epsilon_0}{2}(\int _V E^2 d\tau + \oint _s V E \cdot da) : \triangledown V = -E 
\\
&=\frac{\epsilon_0}{2} \int E^2 d\tau ~~\text{ in all space}
\end{align}
$$


에 따르면 Energy per unit volume은 다음과 같다.
$$
u_E(\vec{r}, t)= \frac{1}{2}\epsilon_0 E^2 (\vec{r},t)
\\
u_B(\vec{r}, t)= \frac{1}{2}\epsilon_0 B^2 (\vec{r},t)
\\
\vec{S}(\vec{r},t) = \frac{1}{\mu_0}(\vec{E}(\vec{r},t )\times \vec{B}(\vec{r},t))
$$

에너지에 대해서도 phasor 분석을 할 수 있을까? --> NO
$$
\begin{align}
&\bold{\text{Phasor} \times \text{Phasor 에 대해서는 Phasor를 구할 수 없다.}}
\\
&\text{이유} : \text{Phasor는 복소평면 그래프 상에서 생각할 수 있다.}
\\
&\text{Phasor 끼리 곱해버리면 복소평면 그래프를 벗어나버린다.(의미를 잃어버림)}
\end{align}
$$
**그러나! 시간평균에 대한 것은 Phasor를 통해 구할 수 있다.**

<img src="/images/2022-12-02-Plane wave/image-20230625173736143.png" alt="image-20230625173736143" style="zoom:67%;" />

평균값이 존재한다는 것을 phasor의 관점에서 설명할 수 있다고 생각하면 될 것같다.

따라서, Energy per unit volume을 시간평균에 대해 나타내면 다음과 같다.
$$
\begin{align}
&\text{내적에 대한 공식을 먼저 유도하자}
\\
&\vec{c}(\vec{r},t) = \vec{A}(\vec{r},t)\cdot \vec{B}(\vec{r},t), \text{when }\vec{A}, \vec{B}\text{가 모두 }\omega\text{로 진동할 때 상황이 있다 해보자.}
\\
&\text{phasor} \times \text{phasor로 나타낼 수 없기 때문에 우리가 알고 있던 정의를 사용하자.}
\\
&\vec{c}(\vec{r},t) = Real(\vec{\tilde A}(r)e^{-i\omega t})\cdot Real(\vec{\tilde B}(r)e^{-i\omega t})
\\
&\vec{c}(\vec{r},t) =(\frac{\vec{\tilde A}(r)e^{-i\omega t}+\vec{\tilde A}(r)^{*}e^{i\omega t}}{2})\cdot (\frac{\vec{\tilde B}(r)e^{-i\omega t}+\vec{\tilde B}(r)^{*}e^{i\omega t}}{2})
\\
&\vec{c}(\vec{r},t) =\frac{1}{4}(\vec{\tilde A}(r)\cdot \vec{\tilde{B}}(r)e^{-i2\omega t}+\vec{\tilde A}(r)^{*}\cdot \vec{\tilde{B}}(r)^{*}e^{-i2\omega t}+\vec{\tilde A}(r)\cdot \vec{\tilde{B}}(r)^{*}+\vec{\tilde A}(r)^{*}\cdot \vec{\tilde{B}}(r)) 
\\
&\text{시간평균을 구하면 다음과 같다.}
\\
&\langle \vec{c}(\vec{r},t)\rangle = \frac{1}{2}(\frac{\vec{\tilde A}(r)\cdot \vec{\tilde{B}}(r)^{*}+\vec{\tilde A}(r)^{*}\cdot \vec{\tilde{B}}(r)}{2}) = \frac{1}{2}Real(\vec{\tilde A}(r)\cdot \vec{\tilde B}(r)^{*})
\\
\end{align}
$$

**결론 : 내적의 시간 평균은 Phasor X 켤레phasor 의 절반의 Real Part이다.**

이를 전기장과 자기장에 대해 나타내면 다음과 같다.
$$
\begin{align}
&\text{Electric Energy density에 대한 시간평균 : } \langle u_E(\vec{r}, t)\rangle = \frac{1}{4}\epsilon_0 Real[\vec{\bold{E}}(r)\cdot \vec{\bold{E}}^*(r)]
\\
&\text{Magnetic Energy density에 대한 시간평균 : } \langle u_B(\vec{r}, t)\rangle = \frac{1}{4}\frac{1}{\mu_0} Real[\vec{\bold{B}}(r)\cdot \vec{\bold{B}}^*(r)] = \frac{1}{4}\epsilon_0 Real[\vec{\bold{E}}(r)\cdot \vec{\bold{E}}^*(r)] ~\because \vec{\bold{B}}= \frac{ik \times \vec{\bold{E}}}{i\omega}
\\
&\text{Planewave에서는 전기장과 자기장이 coupled 되어있다.}
\\
&\therefore \langle u(r,t)\rangle = \langle u_E(\vec{r}, t)\rangle + \langle u_B(\vec{r}, t)\rangle = \frac{1}{2}\epsilon_0 Real[\vec{\bold{E}}(r)\cdot \vec{\bold{E}}^*(r)] 
\end{align}
$$



Poynting Vector는 외적의 형태로 되어있다. 따라서 다음과 같이 나타내야한다.
$$
\begin{align}
\\
&\text{Poynting Vector의 평균은 다음과 같이 구할 수 있다.}
\\
&\langle \vec{S}(\vec{r},t)\rangle  = \frac{1}{2\mu_0}Real[\vec{\bold{E}}(r)\times \vec{\bold{B}}^*(r)]= \frac{1}{2\mu_0}Real[\vec{\bold{E}}(r)\times (\frac{ik \times \vec{\bold{E}}(r)}{i\omega})^*]
\\
&~~~~~~~~~~~~~~=\frac{1}{2 \mu_0}Real[\frac{\vec{k}}{\omega}\vec{\bold{E}}(r)\cdot \vec{\bold{E}}(r)^*] = \hat{k} \frac{1}{2} \frac{\sqrt{\epsilon_0 }}{\sqrt{\mu_0}}Real(\vec{\bold{E}}(r) \cdot \vec{\bold{E}}(r)^*) =  \hat{k} ~ c~ \langle u(r,t)\rangle \equiv I
\\
\end{align}
$$


정리 : Poynting Vector의 시간 평균은 Energy density 곱하기 속도이다. 이는 마치 
$$
\begin{align}
\\
&\vec{\triangledown} \cdot {\vec{J}} = \frac{\partial q}{\partial t} :\text{carrier에 대한 flux}
\\
&\vec{\triangledown} \cdot {\vec{S}} = \frac{\partial u}{\partial t} : \text{energy에 대한 flutx}\text{와 같으므로}
\\
&\text{Energy Flux} = \vec{S}
\\
&\text{Momentum denisty} = \vec{g} = \frac{1}{c^2} \vec{S}
\\
&\vec{J} = \rho \vec{v}\text{처럼} ~\vec{S}\text{를 생각할 수 있다.}
\end{align}
$$
와 같다.

---

#### Plane wave in matter

$$
\begin{align}
\triangledown \cdot \bold{D}(r) &= 0
\\
\triangledown \times \bold{E}(r) &= i \omega \bold{B}(r)
\\
\triangledown \cdot \bold{B}(r) &= 0
\\
\triangledown \times \bold{H}(r) &= \bold{J}_f(r) - i\omega \bold{D}(r)
\\
\\
\bold{D}(r) &= \epsilon(\omega, r)\bold{E}(r)
\\
\bold{H}(r) &= \frac{1}{\mu(\omega, r)}\bold{E}(r)
\end{align}
$$

1. $\vec{P}(\vec{r},t) = \chi(\vec{r},t)\otimes  \vec{E}(\vec{r},t)$ 가 $\epsilon$, $\mu$ 를 Phasor로 표현할 때 Linear  system인 $\vec{P}(\omega) = \chi(\omega)\vec{E}(\omega)$으로 나타낼 수 있다.
2. harmonic oscillator에서도 알 수 있으시 $\omega$ 에따라 $\epsilon$ 및 $\mu$ 가 바뀔 것이다.

 Homogeneous media(r에 무관)에서 plane wave를 살펴보자.
$$
\begin{align}
&\triangledown^2 \vec{\bold{E}}(r) + \omega ^2 \epsilon \mu \vec{\bold{E}}(r)= 0 : \text{Helmholtz equation}
\\
&1. \vec{k} \cdot \vec{k} = \omega ^2 \epsilon \mu : \text{주파수에 따라 k가 커지고, 물질에서 k가 커진다. 물질에서 파장이 줄어든다.}
\\
&2. \vec{k} \cdot \vec{k} = \omega ^2 \epsilon \mu = \omega ^2 \epsilon _0 \epsilon _r \mu_0 \mu_r = \epsilon _r\mu _r \frac{\omega  ^2}{c^2} ~~\because c = \frac{1}{\sqrt{\epsilon _ 0\mu_0}} \text{(모든 항이 1차 order라고 생각하면 편하다.)} 
\\
&3. \vec{k} \cdot \vec{k} = \epsilon _r\mu _r \frac{\omega  ^2}{c^2} = n^2 \frac{\omega ^2}{c^2} ~~\because n = \sqrt{\epsilon _r \mu _r} (c, \epsilon _0, \epsilon _r, \mu_0, \mu_r\text{모두 1차 order라고 생각하면 편하다.})
\\
&4. v = \frac{\omega}{k}= \frac{c}{n } : \text{phase velocity}\rightarrow \omega\text{는 그대로, } k\text{는 커짐}
\\
&5. \vec{S}(r,t) = \vec{E}(r,t)\times \vec{H}(r,t) = \frac{\vec{E}(r,t) \times \vec{B}(r,t)}{\mu}
\\
&6.I = \langle \vec{S}(r,t)\rangle = \frac{1}{2}Real(\frac{\vec{\bold{E}}(r)\times \vec{\bold{B}}^*(r)}{\mu}) = \frac{1}{2}Real(\vec{\bold{E}}(r) \times \vec{\bold{H}}^*(r))=\frac{1}{2 \mu}Real[\frac{\vec{k}}{\omega}\vec{\bold{E}}(r)\cdot \vec{\bold{E}}(r)^*] = \hat{k} \frac{1}{2} \frac{\sqrt{\epsilon }}{\sqrt{\mu}}Real(\vec{\bold{E}}(r) \cdot \vec{\bold{E}}(r)^*)
\end{align}
$$

---

#### Boundary Condition

$$
\begin{align}
& \text{homogeneous한 매질에서(source term이 0)}
\\
& \triangledown \cdot \vec{\bold{D}} = 0 &&--> &&& \epsilon_1 \vec{\bold{E_1}^{\perp}} = \epsilon_2 \vec{\bold{E_2}^{\perp}}
\\
& \triangledown \times \vec{\bold{E}} = i \omega \vec{\bold{B}} &&--> &&& \vec{\bold{E_2}^{\parallel}}= \vec{\bold{E_1}^{\parallel}} &&&&\text{중요}
\\
& \triangledown \cdot \vec{\bold{B}} = 0 &&--> &&& \vec{\bold{B_1}^{\perp}} =\vec{\bold{B_2}^{\perp}}
\\
& \triangledown \times \vec{\bold{H}} = - i \omega \vec{\bold{D}} &&--> &&& \vec{\bold{H_1}^{\parallel}} = \vec{\bold{H_2}^{\parallel}} &&&& \text{중요}
\end{align}
$$

<img src="/images/2022-12-02-Plane wave/image-20240102115723076.png" alt="image-20240102115723076" style="zoom:80%;" />
$$
\begin{align}
&\text{Boundary에서 Electric boundary condition은 다음과 같다.}
\\
&1) \vec{E} = \hat{x} E_0 e^{ikz}
\\
&2) \vec{E} = \hat{x}  ~rE_0 e^{-ikz}
\\
&3) \vec{E} = \hat{x} ~tE_0 e^{iKz}
\\
&\therefore 1+r = t ~\text(z = 0일 때)
\\
&\text{Boundary에서 Magentic boundary condition은 다음과 같다.}
\\
&1) \vec{H} = \frac{\triangledown \times \vec{E}}{i \omega \mu_1} =\frac{ik \hat{z}\times \vec{E}}{i \omega \mu_1} = \hat{y} \frac{kE_0 e^{ikz}}{\omega \mu_1}
\\
&2) \vec{H} = \frac{\triangledown \times \vec{E}}{i \omega \mu_1} =\hat{y} ~r \frac{-kE_0 e^{-ikz}}{\omega \mu_1}
\\
&3) \vec{H} = \frac{\triangledown \times \vec{E}}{i \omega \mu_2} =\hat{y} ~t \frac{KE_0 e^{iKz}}{\omega \mu_2}
\\
&\therefore \frac{k}{\mu _1} - \frac{rk}{\mu _1} = \frac{tK}{\mu_2} ~\text{(z = 0일 때)}
\\
&\therefore 1 - r = \frac{\sqrt{\epsilon _ 2 \mu _ 1}}{\sqrt{\epsilon _ 1 \mu _2}}t
\\
&\text{이를 연립하면 다음과 같다.}
\\
&t = \frac{2 \sqrt{\frac{\epsilon _1}{\mu_1}}}{\sqrt{\frac{\epsilon _1}{\mu _!}}+\sqrt{\frac{\epsilon _2}{\epsilon _2}}}
\approx \frac{2 n_1}{n_1 + n_2}
\\
&r = t-1 = \frac{\sqrt{\frac{\epsilon _1}{\mu_1}}-\sqrt{\frac{\epsilon _2}{\mu _2}}}{\sqrt{\frac{\epsilon _1}{\mu _!}}+\sqrt{\frac{\epsilon _2}{\epsilon _2}}} \approx \frac{n_1 - n_2}{n_1 + n_2}
\\
&\langle \vec{S}(r,t) \rangle = \hat{k} \frac{1}{2} \frac{\sqrt{\epsilon }}{\sqrt{\mu}}Real(\vec{\bold{E}}(r) \cdot \vec{\bold{E}}(r)^*) \text{이므로 이를 t, r에 나타내면 다음과 같다.}
\\
&R = \frac{I_{refl}}{I_{inci}} = \vert r\vert ^2 = (\frac{n_1 - n_2}{n_1 + n_2})^2
\\
&T = \frac{I_{trans}}{I_{inci}} = \frac{\sqrt{\frac{\epsilon _2}{\mu _2}}}{\sqrt{\frac{\epsilon _1}{\mu _1}}}\vert t\vert ^2 = \frac{\sqrt{\epsilon _2}}{\sqrt{\epsilon _1}}\vert t \vert ^2 = \frac{n_2}{n_1}\vert t \vert ^2 = \frac{4n_1 n_2}{(n_1 + n_2)^2}
\end{align}
$$

---

#### Boundary condition, R, T at oblique incidence

<img src="/images/2022-12-02-Plane wave/image-20240102140438397.png" alt="image-20240102140438397" style="zoom:80%;" />
$$
\begin{align}
&\text{Boundary에서 Electric boundary condition은 다음과 같다.}
\\
&1) \vec{E}_{\parallel} = (\vec{E}_0 e^{ikr})_{\parallel}
\\
&2) \vec{E}_{\parallel} = (~r\vec{E}_0 e^{-iKr})_{\parallel}
\\
&3) \vec{E}_{\parallel} = (~t\vec{E}_0 e^{iqr})_{\parallel}
\\
&\therefore 1+r = t ~\text(z = 0일 때) \text{이므로}~~ k_x = K_x = q_x ~ \& ~ k_y = K_y = q_y \text{를 반드시 만족시킨다.}
\\
&\text{물리적 의미 : }
\\
&1) \frac{k_y}{k_x} = \frac{K_y}{K_x} = \frac{q_y}{q_x} : \text{전자기파의 xy plane에 대한 정사영이 한 직선이다. 즉, incident of plane}
\\
&2) k sin\theta _i = K sin\theta _r = q sin\theta _t , \vec{k} \cdot \vec{k} = \omega ^2 \epsilon \mu\text{이므로}
\\
& n_1 sin\theta _i = n_1 sin\theta _r = n_2 sin\theta _t \text{이다. : Snell's Law}

\end{align}
$$

#### 정리

1. incident of plane : $k_x = K_x = q_x$ 와 $k_y = K_y = q_y$ 는 평행이동 symmetry에 대해서 성립하는 운동량 보존 값이다.
2. $1 + r = t , R^2, T^2$와 같이 에너지와 관련된 것들은 $(\vec{E}_1)_{\parallel} = (\vec{E}_2)_{\parallel}$와 같은 Boundary condition에서 성립하는 에너지 보존 법칙이다.

굴절률은 다음과 같이 Potential 느낌으로 해석할 수 있다.

<img src="/images/2022-12-02-Plane wave/image-20230626080904858.png" alt="image-20230626080904858" />

---

#### Plane of Incidence

임의의 각도에 입사하는 전자기파의 s-pol과 p-pol을 다루기 전에 $E_{\parallel}$ 이 같음을 통해서

1. 전자기파의 Plane of Incidence를 구성한다는 것
2. Snell's law를 나타난대난 것

을 알 수 있다. Plane of incidence에서 전기장이 수직이면 s-pol 자기장이 자기장이 수직이면 p-pol이다. 

#### S polarization

경계조건에서 

1. $E_{\parallel}$ 이 연속이다. 
2. Current가 흐르는 상황이 아니므로 $H_{\parallel}$ 이 연속이다 라는 조건으로 구해야한다.

$$
\begin{align}
&1. ~~1+r = t
\\
&2.-\frac{k_z}{\mu_1}e^{ik_xx}-\frac{k_z r}{\mu_1}e^{ik_xx} = -\frac{q_z t }{\mu_1}e^{iq_xx}
\\
&~~~~\frac{k_z}{\mu_1} + \frac{k_z}{\mu_1}r = \frac{q_z}{\mu_2}t
\\
\end{align}
$$

따라서 다음과 같다.
$$
\begin{align}
\\
&t = \frac{2k_z}{q_z+k_z}
\\
&r = \frac{\mu_2 k_z - \mu_1 q_z}{\mu_1 q_z + \mu_2 k_z}
\\
&T = \frac{n_2 cos\theta _t}{n_1 cos {\theta}_i}\vert t \vert ^2
\\
&R = \vert r \vert ^2
\end{align}
$$

#### P polarization

경계조건에서

1. current가 흐르는 상황이 아니므로 $H_{\parallel}$ 이 연속이다 
2. $E_{\parallel}$ 이 연속이다. 

$$
\begin{align}
&1. ~~1+r = t
\\
&2.-\frac{k_z}{\epsilon_1}e^{ik_xx}-\frac{k_z r}{\epsilon_1}e^{ik_xx} = -\frac{q_z t }{\epsilon_1}e^{iq_xx}
\\
&~~~~\frac{k_z}{\epsilon_1} + \frac{k_z}{\epsilon_1}r = \frac{q_z}{\epsilon_2}t
\\
\end{align}
$$

따라서 다음과 같다.
$$
\begin{align}
\\
&t = \frac{2\epsilon_2 k_z}{\epsilon_1 q_z+\epsilon_2 k_z}
\\
&r = \frac{\epsilon_2 k_z - \epsilon_1 q_z}{\epsilon_1 q_z + \epsilon_2 k_z}
\\
&T = \frac{\sqrt{\epsilon_1 \mu_2} cos\theta _t}{\sqrt{\epsilon_2 \mu_1} cos {\theta}_i}\vert t \vert ^2
\\
&R = \vert r \vert ^2
\end{align}
$$

---

#### Evanescent Field in S polarization전반사

<img src="/images/2022-12-02-Plane wave/image-20230626081607055-1723875783768-7.png" alt="image-20230626081607055" style="zoom:80%;" />
$$
\vec{E}_t = \text{Real}\left[ E_0 \cdot t \cdot \hat{y} \cdot e^{-\frac{\omega}{c}\sqrt{n_1^2 \sin^2\theta_i - n_2^2}z} \cdot e^{i\frac{\omega}{c}n_1 \sin \theta_i \cdot x} \cdot e^{-i\omega t} \right]
\\
\text{z축 방향으로는 움직이지 않음. x축 방향으로 움직임.}
$$
에너지는 통과하지 않을까?

Evanescent field에서 Energy $\langle S \rangle $ 을 구해보면 0 이 나오는 것을 확인할 수 있다. 즉, 입사되고 반사되는 에너지가 같다고 해석해야 한다고 생각한다.

<img src="/images/2022-12-02-Plane wave/image-20230626084601201-1723875783768-8.png" alt="image-20230626084601201" />

따라서, evanescent filed로 에너지가 통과되지만 k값이 0이기에 흡수되는 에너지 없이 모두 반사된다고 생각하였다.

---

#### S polarization & P polarization 전반사

<img src="/images/2022-12-02-Plane wave/image-20230626085216901.png" alt="image-20230626085216901" style="zoom:70%;" />

<img src="/images/2022-12-02-Plane wave/image-20230626085239340.png" alt="image-20230626085239340" style="zoom:70%;" />

---

#### Electromagnetic waves in matter

원자와 전자간의 힘을 다음과같은 harmonic oscillator로 나타낼 수 있다.

가정 : 전자기파의 전자를 땡기는 힘이 크지 않으므로 harmonic oscillator를 나타낼 것이다.

<img src="/images/2022-12-02-Plane wave/image-20230626090601694.png" alt="image-20230626090601694" style="zoom: 80%;" />
$$
\begin{align}
\\
m \frac{d^2 x}{dt^2} = F_{binding} + F_{driving}&+F_{damping}
\\
m \frac{d^2 x}{dt^2} + m\gamma\frac{dx}{dt}+m \omega^2_0x &=  qE_0 cos(\omega t)
\\
\text{Phasor로 나타내면} &\text{ 쉽게 다음을 구할 수 있다.}
\\
\widetilde{x}_0 &= \frac{q/m}{\omega^2_0 - \omega^2 - i \gamma \omega}E_0
\\
\text{한 원자에 전자가 무수히 많고 각 }& \text{전자-원자핵 간의 고유 frequency를 고려하면 다음과같다.}
\\
\widetilde{\bold{P}} &= \frac{Nq^2}{m}(\sum_j \frac{f_j}{\omega ^2 _j - \omega ^2 - i \gamma \omega})\widetilde{\bold{E}}
\\
\widetilde{\bold{P}} &= \epsilon_0 \widetilde{\chi}_e \widetilde{\bold{E}}
\\
\end{align}
$$
이를 통해 dielctric constant가 **complex dielectric constant** 를 구성한다는 것을 알 수 있다.

absorption coefficient : $\alpha = 2k$ 이유: Intensity는 제곱에 대한 값이기 때문에

skin depth : $d \equiv \frac{1}{k}$

---

#### Elctromagnetic waves in metals.

<img src="/images/2022-12-02-Plane wave/image-20230626091830392.png" alt="image-20230626091830392" style="zoom:80%;" />

이를 통해 위와 같이 서술하며면 다음을 얻을 수 있다.
$$
\begin{align}
\\
\widetilde{\epsilon}_{Drude} &= 1- \frac{nq^2}{m \epsilon _0}\frac{1}{\omega^2+i\gamma \omega}
\\
&= 1- \frac{\omega _p ^2}{\omega ^2 + i \gamma \omega}= [1- \frac{\omega^2_p}{\omega ^2 + \gamma ^2}]+i[\frac{\gamma \omega ^2 _p}{\omega (\omega ^2 + \gamma ^2)}]
\end{align}
$$
만약, $\gamma \approx \text{small}$ 이고 $\omega < \omega _p$ 이면 $\widetilde{\epsilon}_{Drude}$ 의 실수 부분이 음수가 된다.

결과 :
$$
\begin{align}
&1. \text{전자의 진동이 drving force에 비해 180도 phase out이 되어버린다.}
\\
&2. \text{전자기파가 지나갈 수 없다.}
\\
\end{align}
$$

#### Surface plasmon polariton

$\widetilde{\epsilon}_{Drude}$ 의 의미를 Interface에서 살펴보는 것. 

<img src="/images/2022-12-02-Plane wave/image-20230626092650210.png" alt="image-20230626092650210" style="zoom:50%;" />
$$
\begin{align}
&1.\epsilon_1(\omega)\epsilon_2(\omega)<0
\\
&2. \epsilon_1(\omega)+\epsilon_2(\omega)<0
\\
&\text{를 만족하면}
\\
&\text{계면에 수직방향으로 localized 되어 있고, 계면을 따라 움직이는 전자기파가 발생한다.}
\end{align}
$$
