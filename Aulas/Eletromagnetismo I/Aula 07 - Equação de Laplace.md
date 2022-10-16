# Equação de Laplace


Lembrando:
$$
\left\{
\begin{array}{l}
\vec \nabla \cdot \vec E = \dfrac{\rho}{\epsilon_0} \\
\vec E = - \vec \nabla V
\end{array}
\right.
\Longrightarrow \vec \nabla \cdot \vec \nabla V = -\dfrac{\rho}{\epsilon_0}
\Longrightarrow \nabla^2 V = -\dfrac{\rho}{\epsilon_0}, \ \ \ \ \ \text{Equação de Poisson}
$$

Em uma região onde não há cargas, temos que $\rho = 0$, logo:
$$\nabla^2 V = -\dfrac{\rho}{\epsilon_0} = \dfrac{0}{\epsilon_0}$$
$$\nabla^2 V = 0, \ \ \ \ \ \text{Equação de Laplace} $$
Em coordenadas cartesianas:
$$\nabla^2 V = 0 \Longrightarrow \dfrac{\partial^2 V}{\partial x^2} + \dfrac{\partial^2 V}{\partial y^2} + \dfrac{\partial^2 V}{\partial z^2} = 0, \ \ \ \ \text{onde: } V \equiv V(x, y, z)$$

## Equação de Laplace em uma Dimensão

$$V \equiv V(x), \ \ \ \ \ \dfrac{\partial^2 V}{\partial x^2} = 0$$
Uma função cuja segunda derivada é $0$ é uma função linear, logo onde $V(x) = ax + b$.

Disso obtemos algumas propriedades:

**1.** O valor do Potencial em determinado ponto é igual à média do Potencial em sua vizinhança.

![[Pasted image 20221016112047.png]]
$$V(x) = \dfrac{1}{2} (V(x + \delta) + V(x - \delta))$$

**2.** Se o potencial satisfaz a Equação de Laplace $\nabla^2 V = 0$, então o Potencial não possui máximos ou mínimos locais.

No caso de uma única dimensão, sabendo a solução da equação nas extremidades da região (condições de contorno) $V(x_1)$ e $V(x_2)$, os parâmetros $a$ e $b$ são univocamente determinados.

## Equação de Laplace em duas Dimensões
$$V \equiv V(x, y), \ \ \ \ \ \dfrac{\partial^2 V}{\partial x^2} + \dfrac{\partial^2 V}{\partial y^2} = 0$$
O valor do Potencial em determinado ponto é igual à média do Potencial ao redor deste ponto.

![[Pasted image 20221016120749.png]]

$$V(x, y) = \dfrac{\oint_S V(x,y) \ dl}{\oint_S dl}= \dfrac{\oint_S V(x,y) \ dl}{2 \pi R}$$

Nesta situação, o Potencial também não possui máximos ou mínimos locais.

## Equação de Laplace em três Dimensões
$$V \equiv V(x, y, z), \ \ \ \ \ \dfrac{\partial^2 V}{\partial x^2} + \dfrac{\partial^2 V}{\partial y^2} + \dfrac{\partial^2 V}{\partial z^2}= 0$$

O valor do Potencial em determinado ponto é igual à média do Potencial sobre uma esfera centrada em $\vec r$ deste ponto.

![[Pasted image 20221016121614.png]]
$$V(x, y, z) = \dfrac{\oint_S V(x,y,z) \ da}{\oint_S da}= \dfrac{\oint_S V(x,y,z) \ da}{4 \pi R^2}$$

**Exemplo**: Potencial médio sobre uma esfera de raio $R$ centrada na origem, devido a uma carga $q$ situada em $\vec r = z \hat k$ onde $z > R$. 
![[Pasted image 20221016122618.png]]
$$V = \dfrac{1}{4 \pi \epsilon_0} \dfrac{q}{r_q}, \ \ \ \ \ \ \vec r_q = \vec r' - \vec r, \ \ \ r_q = \sqrt{R^2 + z^2 - 2Rz \ cos \theta}$$
$$\bar V = \dfrac{1}{4 \pi R^2} \oint_S V(r')  \ da = \dfrac{1}{4 \pi R} \oint_S \dfrac{1}{4 \pi \epsilon_0} \dfrac{q}{r_q}  \ (R^2 \ sin \theta \ d \theta \ d \varphi )$$
$$\bar V = \dfrac{1}{4 \pi R^2} \dfrac{q}{4 \pi \epsilon_0}  \int_0^{2 \pi} d \varphi \int_0^{\pi}\dfrac{R^2 \ sin \theta \ }{(R^2 + z^2 - 2Rz \ cos \theta)^\frac{1}{2}}  \ d \theta$$
$$\bar V = \dfrac{1}{4 \pi R^2} \dfrac{q}{4 \pi \epsilon_0}  [2 \pi] \int_0^{\pi}\dfrac{R^2 \ sin \theta \ }{(R^2 + z^2 - 2Rz \ cos \theta)^\frac{1}{2}}  \ d \theta$$
Fazendo $u = R^2 + z^2 - 2Rz \ cos \theta$, $du = 2Rz \ sin \theta \ d \theta$, $u(0) = R^2 + z^2 - 2Rz \ cos (0) = R^2 + z^2 - 2Rz = (R - z)^2$ e $u(\pi) = R^2 + z^2 - 2Rz \ cos (\pi) = R^2 + z^2 + 2Rz = (R + z)^2$

$$\bar V = \dfrac{q}{8 \pi \epsilon_0}  \int_{(R - z)^2}^{(R + z)^2}\dfrac{sin \theta \ }{u^\frac{1}{2}}  \dfrac{1}{2Rz \ sin \theta} du$$
$$\bar V = \dfrac{q}{16 \pi \ R \ z \ \epsilon_0}  \int_{(R - z)^2}^{(R + z)^2} \dfrac{1 \ }{u^\frac{1}{2}}  du$$
$$\bar V = \dfrac{q}{16 \pi \ R \ z \ \epsilon_0}  \left[ 2 \sqrt{u}\right]_{(R - z)^2}^{(R + z)^2} $$
$$\bar V = \dfrac{q}{8 \pi \ R \ z \ \epsilon_0}  \left[ \sqrt{(R + z)^2} - \sqrt{(R - z)^2}\right]$$
$$\bar V = \dfrac{q}{8 \pi \ R \ z \ \epsilon_0}  \left[ |R + z| - |R - z|\right]$$
Como temos que $z > R$, então $|R - z| = (z - R)$:
$$\bar V = \dfrac{q}{8 \pi \ R \ z \ \epsilon_0}  \left[ R + z - (z - R)\right]$$
$$\bar V = \dfrac{q}{8 \pi \ R \ z \ \epsilon_0}  \left[ R + z - z + R\right]$$
$$\bar V = \dfrac{q}{8 \pi \ R \ z \ \epsilon_0}  \left[2R\right]$$
$$\bar V = \dfrac{q}{4 \pi \ z \ \epsilon_0}= \dfrac{1}{4 \pi\epsilon_0} \dfrac{q}{z}$$
Sendo $\bar V = \dfrac{1}{4 \pi\epsilon_0} \dfrac{q}{z}$, o potencial no centro da Esfera será  $V(0) = \dfrac{1}{4 \pi\epsilon_0} \dfrac{q}{z}$.