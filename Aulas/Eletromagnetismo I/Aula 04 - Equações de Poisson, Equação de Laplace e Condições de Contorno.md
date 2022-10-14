# Equação de Poisson e Equação de Laplace

Lembrando que:

$$
\left\{
\begin{array}{l}
\vec \nabla \cdot \vec E = \dfrac{\rho}{\epsilon_0} \\
\vec E = -\vec \nabla V
\end{array}
\right.
\Longrightarrow
\vec \nabla \cdot (-\vec \nabla V) = \dfrac{\rho}{\epsilon_0}
\Longrightarrow
\nabla^2 V = -\dfrac{\rho}{\epsilon_0}
\ \ \ \ \ \ \ \ \text{Equação de Poisson}
$$
Em regiões onde não existe carga elétrica $\rho = 0$:
$$\nabla^2 V = 0
\ \ \ \ \ \ \ \ \text{Equação de Laplace}$$

Conforme visto, o Potencial Elétrico de uma carga centrada na origem será:
$$V(r) = \dfrac{1}{4 \pi \epsilon_0} \dfrac{q}{r} $$

Para uma carga em qualquer outro local ($\vec r'$) em um ponto $P$ em ($\vec r_p$): 

![[Pasted image 20221013171325.png]]

$$V(r) = \dfrac{1}{4 \pi \epsilon_0} \dfrac{q}{r_p} $$
Como o Campo Elétrico é aditivo, o Potencial que deriva do Campo Elétrico também será, logo para uma distribuição discreta de $n$ cargas:	$$V(r) = \dfrac{1}{4 \pi \epsilon_0} \sum_{i=1}^n \dfrac{q_i}{r_{pi}}$$
Onde $r_{pi}$ é o vetor que aponta de cada carga $i$ ao ponto $P$ em $\vec r$, sendo $\vec r_{pi} = \vec r - \vec r_i$.

Então, para uma distribuição contínua de cargas, analogamente:

![[Pasted image 20221014113046.png]]

$$V(\vec r) = \dfrac{1}{4 \pi \epsilon_0} 
\int_{V'} \dfrac{dq}{r_p} = \dfrac{1}{4 \pi \epsilon_0} 
\int_{V'} \dfrac{\rho(\vec r)}{r_p} \ dV', \ \ \ \ \ \ \ \ \ r_p = |\vec r - \vec r'|$$

**Exemplo**: Potencial de uma Casca Esférica de raio $R$ e com uma distribuição de carga uniforme sobre a superfície com densidade de carga $\sigma$.

![[Pasted image 20221014120634.png]]

Sendo então:
$$dq = \sigma \ dA, \ \ \ \ \ \ \ \ \ \ dA = R^2 \ sin \theta \ d \theta \ d \varphi $$
$$\vec r = r \hat z, \ \ \ \ \ \ \ \ \ \ \vec r' = R \ \hat r$$
$$(r_p)^2 = (R \ sin \theta)^2 + (z - R \ cos \theta)^2 = R^2 sin^2 \theta + z^2 + R^2 cos^ \theta - 2Rz \ cos \theta$$
$$(r_p)^2 = R^2 (sin^2 \theta + cos^2 \theta) + z^2 - 2Rz \ cos \theta = R^2 + z^2 - 2Rz \ cos \theta $$
Logo:
$$V(\vec r) = \dfrac{1}{4 \pi \epsilon_0} \int_{S} \dfrac{\sigma(\vec r)}{r_p} dA = \dfrac{1}{4 \pi \epsilon_0} \int_{S} \dfrac{\sigma(\vec r)}{(R^2 + z^2 - 2Rz \ cos \theta)^{\frac{1}{2}}} (R^2 \ sin \theta \ d \theta \ d \varphi)$$
$$V(\vec r) = \dfrac{1}{4 \pi \epsilon_0} \int_{S} \dfrac{\sigma(\vec r)}{(R^2 + z^2 - 2Rz \ cos \theta)^{\frac{1}{2}}} (R^2 \ sin \theta \ d \theta \ d \varphi)$$
$$V(\vec r) = \dfrac{R^2 \ \sigma(\vec r)}{4 \pi \epsilon_0} \int_0^{2 \pi} d \varphi \int_0^\pi \dfrac{sin \theta}{(R^2 + z^2 - 2Rz \ cos \theta)^{\frac{1}{2}}} \ d \theta$$
$$\text{Se } u = cos \theta, du = -sin \theta d \theta, u(0) = cos(0) = 1, u(\pi) cos(\pi) = -1$$
$$V(\vec r) = \dfrac{R^2 \ \sigma(\vec r)}{4 \pi \epsilon_0} [2 \pi] \int_1^{-1} \dfrac{sin \theta}{(R^2 + z^2 - 2Rz u)^{\frac{1}{2}}}  \dfrac{-1}{sin \theta} du$$
$$V(\vec r) = \dfrac{R^2 \ \sigma(\vec r)}{2 \epsilon_0} \int_{-1}^{1} \dfrac{1}{(R^2 + z^2 - 2Rz u)^{\frac{1}{2}}} du$$
$$V(\vec r) = \dfrac{R^2 \ \sigma(\vec r)}{2 \epsilon_0} \int_{-1}^{1} \dfrac{1}{(2Rz)^{\frac{1}{2}}(\frac{R^2 + z^2}{2Rz} - u)^{\frac{1}{2}}} du$$
$$V(\vec r) = \dfrac{R^2 \ \sigma(\vec r)}{2 \epsilon_0} \dfrac{1}{(2Rz)^{\frac{1}{2}}} \int_{-1}^{1} \dfrac{1}{(\frac{R^2 + z^2}{2Rz} - u)^{\frac{1}{2}}} du$$
$$\text{Se } s =\dfrac{R^2 + z^2}{2Rz} - u, ds = -1 du, s(-1) =\dfrac{R^2 + z^2}{2Rz} + 1,  s(1) =\dfrac{R^2 + z^2}{2Rz} - 1$$
$$V(\vec r) = \dfrac{R^2 \ \sigma(\vec r)}{2 \epsilon_0} \dfrac{1}{(2Rz)^{\frac{1}{2}}} \int_{\frac{R^2 + z^2}{2Rz} - 1}^{\frac{R^2 + z^2}{2Rz} + 1} u^{-\frac{1}{2}} du$$
$$V(\vec r) = \dfrac{R^2 \ \sigma(\vec r)}{2 \epsilon_0} \dfrac{1}{(2Rz)^{\frac{1}{2}}} \left[ 2 u^\frac{1}{2}\right]_{\frac{R^2 + z^2}{2Rz} - 1}^{\frac{R^2 + z^2}{2Rz} + 1}$$
$$V(\vec r) = \dfrac{R^2 \ \sigma(\vec r)}{\epsilon_0} \dfrac{1}{(2Rz)^{\frac{1}{2}}} \left[ \left(\frac{R^2 + z^2}{2Rz} + 1 \right)^\frac{1}{2} - \left(\frac{R^2 + z^2}{2Rz} - 1\right)^\frac{1}{2}\right]$$
$$V(\vec r) = \dfrac{R^2 \ \sigma(\vec r)}{\epsilon_0} \dfrac{1}{(2Rz)^{\frac{1}{2}}} \dfrac{1}{(2Rz)^{\frac{1}{2}}} \left[ \left(R^2 + z^2 + 2Rz \right)^\frac{1}{2} - \left(R^2 + z^2- 2Rz\right)^\frac{1}{2}\right]$$
$$V(\vec r) = \dfrac{R \ \sigma(\vec r)}{\epsilon_0} \dfrac{1}{2z} \left[ \left(R^2 + z^2 + 2Rz \right)^\frac{1}{2} - \left(R^2 + z^2- 2Rz\right)^\frac{1}{2}\right]$$
$$V(\vec r) = \dfrac{R \ \sigma(\vec r)}{2z\epsilon_0} \left[ \left(R + z)^2\right)^\frac{1}{2} - \left((R - z)^2\right)^\frac{1}{2}\right]$$
$$V(\vec r) = \dfrac{R \ \sigma(\vec r)}{2z \epsilon_0} \left( \ |R + z| - |R - z| \ \right)$$

Para $z > R$, o $P$ está fora da Casca Esférica, logo $|R - z| = (z - R)$:

$$V(\vec r) = \dfrac{R \ \sigma(\vec r)}{2z \epsilon_0} \left( \ (R + z) - (z - R)  \right) = \dfrac{R \ \sigma(\vec r)}{2z \epsilon_0} \left( R + z - z + R \right)$$
$$V(\vec r) = \dfrac{R \ \sigma(\vec r)}{2z \epsilon_0} \left( \ (R + z) - (z - R)  \right) = \dfrac{R \ \sigma(\vec r)}{2z \epsilon_0} \left( 2R \right)$$
$$V(\vec r) = \dfrac{R ^2\ \sigma(\vec r)}{z \epsilon_0} = \dfrac{R ^2}{z \epsilon_0} \dfrac{Q}{4 \pi R^2} = \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{z}$$

Para $z < R$, o $P$ está dentro da Casca Esférica, logo $|R - z| = (R - z)$:

$$V(\vec r) = \dfrac{R \ \sigma(\vec r)}{2z \epsilon_0} \left( \ (R + z) - (R - z)  \right) = \dfrac{R \ \sigma(\vec r)}{2z \epsilon_0} \left( R + z - R + z \right)$$
$$V(\vec r) = \dfrac{R \ \sigma(\vec r)}{2z \epsilon_0} \left( 2z \right) = \dfrac{R \ \sigma(\vec r)}{\epsilon_0} = \dfrac{R \ }{\epsilon_0} \dfrac{Q}{4 \pi R^2} = \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{R}$$

Temos que dentro da Casca Esférica o Potencial Elétrico é constante e fora ele diminui proporcional ao inverso de $z$.


# Condições de Contorno na Eletrostática

Considerando um plano com a superfície $S$ que possui uma densidade de carga $\sigma$, o Campo Elétrico imediatamente acima (ou abaixo) da superfície do plano será:
$$\vec E_S = \dfrac{\sigma}{2 \epsilon_0} \hat k \ \ \ \ \ \ \text{acima do plano}$$
$$\vec E_S = -\dfrac{\sigma}{2 \epsilon_0} \hat k \ \ \ \ \ \ \text{abaixo do plano}$$
Se consideramos que existem também um Campo Elétrico externo:

![[Pasted image 20221014140118.png]]

Sendo este Campo Elétrico externo na forma:
$$\vec E_t = E_x \hat \imath +E_y \hat \jmath +E_z \hat k$$
Chamaremos:
$$\vec E_+ \text{ : o Campo Elétrico total acima do plano }$$
$$\vec E_- \text{ : o Campo Elétrico total abaixo do plano }$$
Então:
$$\vec E_+ = E_x \hat \imath +E_y \hat \jmath + \left( E_z + \dfrac{\sigma}{2 \epsilon_0} \right) \hat k $$

$$\vec E_- = E_x \hat \imath +E_y \hat \jmath + \left(E_z - \dfrac{\sigma}{2 \epsilon_0} \right) \hat k $$$$\Delta \vec E \text{ : diferença entre os campos acima e abaixo da superfície carregada}$$$$\Delta \vec E = \vec E_+ - \vec E_- = \dfrac{\sigma}{\epsilon_0} \hat k$$Vemos então que nesta situação só houve descontinuidade na direção $\hat k$, ou seja, na direção perpendicular à superfície do plano.

De forma mais genérica:
$$\vec E = \vec E_\parallel + \vec E_\perp, \ \ \ \ \text{onde :}
\left\{
\begin{array}{l}
\vec E_\parallel \perp \hat n \\
\vec E_\perp \parallel \hat n
\end{array}
\right.
$$
Então:
$$\vec E_{\parallel+}= \vec E_{\parallel+}$$

$$\vec E_{\perp +} = \vec E_{\perp} + \frac{\sigma}{2 \epsilon_0} \hat n$$
$$\vec E_{\perp -} = \vec E_{\perp} - \frac{\sigma}{2 \epsilon_0} \hat n$$
$$\Delta \vec E = \vec E_{\perp +} - \vec E_{\perp -} = \dfrac{\sigma}{\epsilon_0} \hat n$$

Logo, podemos sempre separar um Campo Elétrico externo em uma componente que é perpendicular à superfície carregada e outra componente que é perpendicular, e assim a direção preferencial do campo ao passar pela superfície carregada será a direção normal à superfície carregada.

Do mesmo modo, para o Potencial Elétrico, para pontos $a$ e $b$ onde $a$ está de um lado da superfície carregada e $b$ está do outro lado, considerando a superfície com uma largura $\varepsilon$ muito pequena: 
$$V(a) - V(b) = - 
\int_a^b \vec E \cdot d \vec l $$
Quando $\varepsilon \rightarrow 0$, então $a$ e $b$ são tão próximos que podem ser considerados o mesmo ponto, então, $\Delta V \rightarrow 0$, então o Potencial Elétrico é o mesmo em ambos os lados da superfície muito fina:
$$V^+ = V^-$$

Relacionando então o Campo Elétrico com o Potencial Elétrico:
$$\left\{
\begin{array}{l}
\Delta \vec E = \vec E_+ - \vec E_- = \dfrac{\sigma}{\epsilon_0} \hat n \\
\vec E = -\vec \nabla V
\end{array}
\right.
\ \ \ \ \Longrightarrow
- \vec \nabla V_+ + \vec \nabla V_- = \dfrac{\sigma}{\epsilon_0} \hat n
$$
Como $\vec \nabla \cdot \hat n = \frac{\partial}{\partial n}$:
$$\dfrac{\partial V_+}{\partial n} - \frac{\partial V_-}{\partial n} = -\dfrac{\sigma}{\epsilon_0}$$
O Potencial Elétrico é contínuo ao passar de um lado para o outro da superfície carregada, mas sua derivada espacial é descontínua.