# Rotacional do Campo Elétrico

Pelo teorema de Stokes, temos que a integral sobre uma superfície do Rotacional de uma função vetorial é igual à integral sobre o bordo desta superfície:

$$\int_S (\vec \nabla \times \vec f) \cdot d \vec a = \oint_C \vec f \cdot d \vec l, \ \ \ \ \ d \vec l = dr \ \hat r + r \ d \theta \ \hat \theta + r \ sin \theta \ d \varphi \ \hat \varphi$$
Logo, para o Campo Elétrico, que possui dependência apenas em $\hat r$:
$$\oint_C \vec E \cdot d \vec l = \oint_C \vec E \cdot d \vec l = \oint_C\dfrac{1}{4 \pi \epsilon_0} \dfrac{q}{r^2} \hat r \ (dr \ \hat r + r \ d \theta \ \hat \theta + r \ sin \theta \ d \varphi \ \hat \varphi)$$
$$\oint_C \vec E \cdot d \vec l = \oint_C \dfrac{1}{4 \pi \epsilon_0} \dfrac{q}{r^2} dr $$
Considerando um caminho do ponto $a$ ao ponto $b$:

$$\oint_C \vec E \cdot d \vec l = \dfrac{q}{4 \pi \epsilon_0} \int_a^b  \dfrac{1}{r^2} dr = \dfrac{q}{4 \pi \epsilon_0} \left[ \dfrac{1}{r} \right]_a^b = \dfrac{q}{4 \pi \epsilon_0} \left[ \dfrac{1}{b} - \dfrac{1}{a} \right]$$

Como a integral é fechada, $a = b$, logo:
$$\oint_C \vec E \cdot d \vec l = \dfrac{q}{4 \pi \epsilon_0} \left[ \dfrac{1}{c} - \dfrac{1}{c} \right] = 0$$
Pelo Teorema de Stokes:
$$\int_S (\vec \nabla \times \vec E) \cdot d \vec a = \oint_C \vec E \cdot d \vec l$$
$$\int_S (\vec \nabla \times \vec E) \cdot d \vec a = 0$$
Como esta relação precisa ser válida para qualquer superfície, precisamos que:
$$\vec \nabla \times \vec E = 0 \ \ \ \ \ \ \ \ \ \ \text{Lei de Ampère na forma Diferecial}$$
Então o Rotacional e todo Campo Elétrico é igual a $0$. Isso é válido para uma carga pontual, para uma distribuição discreta de cargas e mesmo para uma distribuição contínua de carga (contanto que as cargas não estejam em movimento).


# Potencial Elétrico

Vimos que:
$$\vec \nabla \times \ \vec E = 0 \ \Longrightarrow \oint_C \vec E \cdot d \vec l = \int_a^b \vec E \cdot d \vec l$$
Como a definição é válida para qualquer caminho fechado, então a integral é a mesma para quaisquer pontos $a$ e $b$, independe do caminho entre eles.

O Potencial Elétrico é definido por:
$$V(\vec r) = - \int_\mathcal{O}^{\vec r} \vec E \cdot d \vec l, \ \ \ \ \ \ \ \ \ \ \text{onde } \mathcal{O}: \text{ponto de referência fixo, Origem} $$
Onde $V(\vec r)$ depende apenas da posição de $\vec r$, e embora $\vec r$ dependa da Origem $\mathcal{O}$, dados dois pontos quaisquer no espaço, o Pontecial Elétrico depende apenas destes dois pontos, independente do ponto de referência.

$$V(\vec b) - V(\vec a) = - \int_\mathcal{O}^{\vec b} \vec E \cdot d \vec l + \int_\mathcal{O}^{\vec a} \vec E \cdot d \vec l = - \int_\mathcal{O}^{\vec b} \vec E \cdot d \vec l - \int^\mathcal{O}_{\vec a} \vec E \cdot d \vec l $$
$$V(\vec b) - V(\vec a) = - \int^\mathcal{\vec b}_{\vec a} \vec E \cdot d \vec l $$
E isto é válido para qualquer caminho entre $\vec a$ e $\vec b$.

Como visto anteriormente:

$$\int_{\vec a}^{\vec b} (\vec \nabla f) \cdot d \vec l = f(\vec b) - f(\vec a)$$
Logo:
$$V(\vec b) - V(\vec a) = \int_{\vec a}^{\vec b} (\vec \nabla V) \cdot d \vec l = - \int_{\vec a}^{\vec b} \vec E \cdot d \vec l$$
Como a relação é válida para qualquer caminho, temos necessariamente que:
$$\vec E = - \vec \nabla V$$
A unidade do potencial é o Volt [V].

**Exemplo**: Calcular o Potencial dentro e fora de uma Casca Esférica uniformemente carregada de raio $R$ e carga total $Q$.

Pela Lei de Gauss:$$\vec E = \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{r^2} \hat r, \ \ \ \ \ \text{para } r > R$$$$\vec E =0 , \ \ \ \ \ \text{para } r < R$$
Analisando então fora da Casca Esférica ($r > R$):

$$V(r) - V(\mathcal{O}) = - \int_{\mathcal{O}}^r \vec E \cdot d \vec l = - \int_{\mathcal{O}}^r \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{r^2} \hat r \cdot d \vec l, \ \ \ \ \ d \vec l = dr \ \hat r + r \ d \theta \ \hat \theta + r \ sin \theta \ d \varphi \ \hat \varphi$$
$$= - \dfrac{Q}{4 \pi \epsilon_0} \int_{\mathcal{O}}^r \dfrac{1}{r^2} dr = \dfrac{Q}{4 \pi \epsilon_0} \left[  \dfrac{1}{r} \right]_{\mathcal{O}}^r = \dfrac{Q}{4 \pi \epsilon_0} \left[  \dfrac{1}{r} - \dfrac{1}{\mathcal{O}} \right] $$
Definindo $\mathcal{O}$ muito distante, $\mathcal{O} \longrightarrow \infty$, $\frac{1}{\mathcal{O} }\longrightarrow 0$, logo:
$$V(r) - V(\mathcal{O}) = \dfrac{Q}{4 \pi \epsilon_0}  \dfrac{1}{r}$$
Definindo que $V(\infty) = 0$, temos:
$$V(r) = \dfrac{1}{4 \pi \epsilon_0}  \dfrac{Q}{r}$$

Analisando agora dentro da Casca Esférica ($r < R$):

Sabendo o potencial do ponto de referência no infinito até qualquer ponto fora da Casca Esférica, podemos calcular o potencial do infinito até a superfície da Casca Esférica e incrementar da casca até um ponto qualquer dentro dela:

$$V(r) = - \int_\infty^R \vec E_{fora} \cdot d \vec l - \int_R^r \vec E_{dentro} \cdot d \vec l$$
Como $\vec E_{dentro} = 0$, logo:
$$
V(r) = - \int_\infty^R \vec E_{fora} \cdot d \vec l - 0 = \dfrac{1}{4 \pi \epsilon_0}  \dfrac{Q}{R}
$$

Então Potencial dentro da esfera é constante e igual ao campo na superfície da Casca Esférica. Como o Campo Elétrico é $0$ dentro da Casca Esférica ele é referente a derivada ($\vec \nabla$) do Potencial, o potencial ser constante justifica esta afirmação.

Notamos também que o Potencial não possui descontinuidade como o Campo Elétrico.

![[Pasted image 20221013164006.png]]
 
