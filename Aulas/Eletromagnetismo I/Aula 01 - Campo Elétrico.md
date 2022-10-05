# Revisão de Análise Vetorial

## Análise Vetorial em 3 dimensões

### Operador Nabla
$$\vec \nabla = \dfrac{\partial}{\partial x} \hat \imath + \dfrac{\partial}{\partial y} \hat \jmath + \dfrac{\partial}{\partial z} \hat k \; \; \; \text{\textit{(pseudo vetor para 3 dimênsões cartesianas)} }$$
### Gradiente
$$\vec \nabla f(x,y,z) = \dfrac{\partial f(x,y,z)}{\partial x} \hat \imath + \dfrac{\partial f(x,y,z)}{\partial y} \hat \jmath + \dfrac{\partial f(x,y,z)}{\partial z} \hat k$$
### Divergente
$$\vec  \nabla \cdot \vec{f}(x,y,z) = \dfrac{\partial f_x}{\partial x} + \dfrac{\partial f_y}{\partial y} + \dfrac{\partial f_z}{\partial z} \ \ \ \text{; onde } \vec{f}(x,y,z) = f_x \; \hat \imath + f_y \; \hat \jmath + f_z \; \hat k $$
### Rotacional
$$\vec \nabla \times \vec{f}(x,y,z) =
\left( \dfrac{\partial f_z}{\partial y} - \dfrac{\partial f_y}{\partial z}\right) \hat \imath +
\left( \dfrac{\partial f_x}{\partial z} - \dfrac{\partial f_z}{\partial x}\right) \hat \jmath +
\left( \dfrac{\partial f_y}{\partial x} - \dfrac{\partial f_x}{\partial y}\right) \hat k$$
### Laplaciano
$$\vec \nabla^2 \; f(x, y, z) = \dfrac{\partial^2 f}{\partial x^2} f + \dfrac{\partial^2 f}{\partial y^2} f + \dfrac{\partial^2 f}{\partial z^2} f$$
$$\vec \nabla^2 \; \vec{f}(x, y, z) = \dfrac{\partial^2 f}{\partial x^2} f_x \; \hat \imath + \dfrac{\partial^2 f}{\partial y^2} f_y \; \hat \jmath+ \dfrac{\partial^2 f}{\partial z^2} f_z \; \hat k$$
### Relações importantes
#### Divergente do Rotacional
$$\vec \nabla \cdot ( \vec \nabla \times \vec f \;) = 0$$
#### Rotacional do Rotacional
$$\vec \nabla \times (\vec \nabla \times \vec f) = \vec \nabla(\vec \nabla \cdot \vec f) - \nabla^2 \; \vec f $$
### Teorema de Gauss
A integral do Divergente de uma função em um volume $V$ é igual à integral fechada desta mesma função sobre a superfície $S$ deste volume.
$$

\int_V \; (\vec \nabla \cdot \vec f \; )\;  dV = \oint_S \vec f \cdot d \vec A$$
### Teorema de Stokes
A integral fechada do Rotacional de uma função em uma superfície $S$ é igual à integral fechada no caminho $C$ no bordo desta superfície. 
$$\int_S \; (\vec \nabla \times \vec f) \; \cdot d \vec A = \oint_C \vec f \cdot d \vec l $$

# Campo Elétrico

Considerando duas cargas pontuais $q_1$ e $q_2$: 

![[Pasted image 20221005165057.png]]

Logo existe uma força entre estas duas cargas.

A carga $q_1$ exerce uma força $\vec F_{12}$ sobre a carga $q_2$ que é proporcional ao inverso do quadrado da distância entre elas na direção da carga $q_1$ até a carga $q_2$.
$$\vec F_{12} = \dfrac{1}{4 \pi \epsilon_0} \dfrac{q_1 q_2}{|\vec r_2 - \vec r_1|^2} \dfrac{\vec r_2 - \vec r_1}{| \vec r_2 - \vec r_1|}$$
Onde $\epsilon_0$ é a permissividade do vácuo e equivale a $\epsilon_0 = 8,85 \times 10^{-12} C^2 / N \cdot m^2$.
 
Então, considerando $\vec r_{12} = \vec r_2 - \vec r_1$, temos que $\hat r_{12} = \dfrac{\vec r_{12}}{| \vec r_{12} |} = \dfrac{\vec r_2 - \vec r_1}{| \vec r_2 - \vec r_1|}$, temos:
$$\vec F_{12} = \dfrac{1}{4 \pi \epsilon_0} \dfrac{q_1 q_2}{|\vec r_{12}|^2} \dfrac{\vec r_{12}}{| \vec r_{12} |} = \dfrac{1}{4 \pi \epsilon_0} \dfrac{q_1 q_2}{|\vec r_{12}|^3} \vec r_{12} = \dfrac{1}{4 \pi \epsilon_0} \dfrac{q_1 q_2}{ (r_{12})^3} \vec r_{12}= \dfrac{1}{4 \pi \epsilon_0} \dfrac{q_1 q_2}{ (r_{12})^2} \hat r_{12}$$
E esta relação é chamada **Lei de Coulomb**.

Expandindo o mesmo raciocínio para várias cargas:

![[Pasted image 20221005172002.png]]

Temos que $\vec F_{iQ} = \dfrac{1}{4 \pi \epsilon_0} \dfrac{q_i Q}{\vec (r_{iQ})^2} \hat r_{iQ}$ para cada uma das $q_i$ cargas.

Então a Força Total que age sobre a carga $Q$ será:
$$\vec F_Q = \dfrac{Q}{4 \pi \epsilon_0} \sum_{i=1}^n \dfrac{q_i}{(r_{iQ})^2} \hat r_{iQ} = Q \vec E(\vec r), \ \ \ \ \ \text{onde: } \vec E (\vec r) = \dfrac{1}{4 \pi \epsilon_0} \sum_{i=1}^n \dfrac{q_i}{(r_{i})^2} \hat r_{i} $$

Temos então o **Campo Elétrico** em uma posição $\vec r$ devido a uma distribuição discreta de cargas $q_i$. 
$$\vec E (\vec r) = \dfrac{1}{4 \pi \epsilon_0} \sum_{i=1}^n \dfrac{q_i}{(r_{i})^2} \hat r_{i} = \dfrac{1}{4 \pi \epsilon_0} \sum_{i=1}^n \dfrac{q_i}{|\vec r - \vec r_i|^2} \dfrac{\vec r - \vec r_i}{|\vec r - \vec r_i|}$$
Com isso, temos uma característica onde se tivermos uma carga $Q$ no ponto $\vec r$, teremos uma Força $\vec F_Q = Q \vec E(\vec r)$ neste ponto.

Expandindo esta dedução para uma distribuição contínua, temos que $n \longrightarrow \infty$ e $q_i \longrightarrow dq$, teremos:
$$\vec E(\vec r) = \dfrac{1}{4 \pi \epsilon_0} \int \dfrac{dq}{(r_p)^2} \hat r_p $$
Onde $\hat r_p$ é o versor que aponta do elemento de carga $dq$ ao ponto $P$ localizado em $\vec r$, e $r_p$ é a distância entre o elemento de carga $dq$ e o ponto $P(\vec r)$.

As distribuições contínuas poderão ser:

- Distribuições Lineares: $dq = \lambda \ dx$, onde $\lambda$ é a densidade linear de carga
- Distribuições Superficiais: $dq = \sigma \ dA$, onde $\sigma$ é a densidade superficial de carga
- Distribuições Volumétricas: $dq = \rho \  dV$, onde $\rho$ é a densidade volumétrica de carga

Na distribuição Volumétrica de cargas $dq$ posicionadas em $\vec r'$, o campo elétrico na posição $\vec r$ será:
$$E(\vec r) = \dfrac{1}{4 \pi \epsilon_0} \int_{V'} \dfrac{\rho (\vec r') dV'}{(r_p)^2} \hat r_p, \ \ \ \ \ \text{onde } r_p = \vec r - \vec r' $$
