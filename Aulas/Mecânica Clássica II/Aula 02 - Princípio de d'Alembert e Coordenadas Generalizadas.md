# Princípio de d'Alembert

## Deslocamentos Virtuais

**Definição**: Deslocamentos infinitesimais de cada partícula que levam de uma configuração possível a outra configuração possível infinitesimalmente próxima no *mesmo instante* $t$.

Dado um sistema de $N$ partículas, os deslocamentos virtuais $\delta \vec r_i$, onde $i = 1, ..., N$ são deslocamentos infinitesimais das posições $\vec r_1, ..., \vec r_N$ realizados instantaneamente (conferindo um caráter fictício aos deslocamentos virtuais) e com a propriedade de serem compatíveis com os vínculos.

**Exemplo**: Uma partícula está restrita a uma superfície móvel, sendo $f(\vec r, t) = 0$ a equação da superfície. Um deslocamento virtual deve ser consistente com o vínculo, isto é, o ponto $\vec r$ e o ponto deslocado $\vec r + \delta \vec r$ devem pertencer à superfície no mesmo instante $t$.
![[Pasted image 20221001190242.png]]
$$f(\vec r + \delta \vec r, t) = 0 \;\;\;\;\; \Longrightarrow \;\;\;\;\; f(\vec r, t) + \nabla f \cdot \delta \vec r = 0 \;\;\;\;\; \Longrightarrow \;\;\;\;\; \nabla f \cdot \delta \vec r = 0$$
Como $\nabla f$ é perpendicular à superfície no instante $t$, o deslocamento virtual $\delta \vec r$ é tangente à superfície neste instante.

Contudo, um deslocamento real $d \vec r$ será um intervalo de tempo $dt$, portanto, para que a partícula permanece na superfície é preciso que
$$f(\vec r + d \vec r, t + dt) = 0 \;\;\; \Longrightarrow \;\;\; \nabla f \cdot d \vec r + \dfrac{\partial f}{\partial t} dt = 0$$
Deste modo, nota-se que $d \vec r$ não é tangente à superfície se $\dfrac{\partial f}{\partial t} \neq 0$. Somente o deslocamento virtual realizado a tempo fixo é tangente à superfície mesmo que ela esteja em movimento. 

## Trabalho Virtual

Considere um sistema de $N$ partículas. A força resultante sobre a $i$-ésima partícula pode ser descrita como:
$$\vec F_i = \vec F_i^{(a)} + \vec f_i$$
O **Trabalho Virtual** total sobre este sistema é definido como:
$$\sum_i^N \vec F_i \cdot \delta \vec r_i$$

Na situação de equilíbrio, temos que a força resultante total sobre cada partícula é igual a $0$, com isso o trabalho virtual deve ser $0$.
$$\vec F_i = 0, i = 1,..., N, \;\;\;\;\;\; \sum_i^N \vec F_i \cdot \delta \vec r_i = 0, \;\;\;\;\;\;  \sum_i^N \vec F_i^{(a)} \cdot \delta \vec r_i, +  \sum_i^N \vec f_i \cdot \delta \vec r_i,$$


Se a superfície à qual o movimento da partícula está restrito é idealmente lisa, a força de contato entre a partícula e a superfície não possui componente tangencial, mas apenas normal à superfície. Desta forma, o trabalho realizado pela força de vínculo por ocasião de um deslocamento virtual da partícula é nulo mesmo que a superfície esteja em movimento, diferentemente do trabalho realizado durante um deslocamento real, que não será necessariamente $0$.

Na maioria dos cados fisicamente interessantes, o trabalho virtual *total* das forças de vínculo se anula.

Interessante notar que para os vínculos ideais temos que o trabalho virtual total para as Forças de Vínculo é nulo.

Adotamos, de modo geral, que para situações onde não há dissipação de calor por atrito, os vínculos são ideais, logo:
$$ \sum_i^N \vec F_i \cdot \delta \vec r_i = 0 \;\;\;\;\; \text{(Em Equilíbrio)}$$
 Partindo da situação estática para a dinâmica, notamos que pela Segunda Lei de Newton:
 $$\vec F_i = \dot{\vec P_i}, \;\;\;\;\; \vec F_i - \dot{\vec P_i} = 0$$
 Assim:
 $$\sum_i^N \vec F_i \cdot \delta \vec r_i = \sum_i^N (\vec F_i - \dot{\vec P_i}) \cdot \delta \vec r_i = 0$$ Decompondo a Força total sobre a $i$-ésima partícula como $\vec F_i = \vec F_i^{(a)} + \vec f_i$, obtemos: 
 $$\sum_i^N (\vec F_i - \dot{\vec P_i}) \cdot \delta \vec r_i = \sum_i^N (\vec (\vec F_i^{(a)} + \vec f_i) - \dot{\vec P_i}) \cdot \delta \vec r_i = 0$$
$$\sum_i^N \vec F_i^{(a)} \cdot \delta \vec r_i + \sum_i^N \vec f_i \cdot \delta \vec r_i - \sum_i^N \dot{\vec P_i} \cdot \delta \vec r_i = 0$$
Assumindo vínculos ideais, $\vec f_i = 0, i=1, ..., N$:
$$\sum_i^N (\dot{\vec P_i} - \vec F_i^{(a)}) \cdot \delta \vec r_i = 0 \;\;\;\;\; \text{(Princípio de d'Alembert)}$$

**Exemplo**: Encontrar a aceleração em uma Máquina de Atwood.
![[Pasted image 20221001203112.png]]
Vínculo: $x_1 + x_2 = l = constante$

Aceleração: $a = \ddot x_1 = - \ddot x_2$

Forças:
$$\vec F_1^{(a)}=m_1 g \hat \imath \;\;\;\;\; \vec F_2^{(a)}=m_2 g \hat \imath$$
$$\vec P_1 = m_1 \dot x_1 \hat \imath \;\;\;\;\; \vec P_2 = m_2 \dot x_2 \hat \imath = - m_2 \dot x_1 \hat \imath$$
$$\dot{\vec P_1} = m_1 \ddot x_1 \hat \imath \;\;\;\;\; \vec P_2 = - m_2 \ddot x_1 \hat \imath$$

Pela equação de vínculo $x_1 + x_2 = l$, como $l$ é constante, os deslocamentos virtuais são relacionados por:
$$\delta x_1 + \delta x_2 = 0 \;\;\; \Longrightarrow  \;\;\; \delta x_2 = - \delta x_1$$
$$\delta \vec r_1 = \delta x_1 \hat \imath \;\;\;\;\; \delta \vec r_2 = \delta x_2 \hat \imath = - \delta x_1 \hat \imath$$
Pelo princípio de d'Alembert:
$$\sum_i^N (\dot{\vec P_i} - \vec F_i^{(a)}) \cdot \delta \vec r_i = 0$$
$$(\dot{\vec P_1} - \vec F_1^{(a)}) \cdot \delta \vec r_1 + (\dot{\vec P_2} - \vec F_2^{(a)}) \cdot \delta \vec r_2 = 0$$
$$(m_1 \ddot x_1 \hat \imath - m_1 g \hat \imath) \cdot \delta x_1 \hat \imath + (- m_2 \ddot x_1 \hat \imath - m_2 g \hat \imath) \cdot (-\delta x_1 \hat \imath) = 0$$
$$(m_1 \ddot x_1 \hat \imath - m_1 g \hat \imath) \cdot \delta x_1 \hat \imath = -(m_2 \ddot x_1 \hat \imath + m_2 g \hat \imath) \cdot \delta x_1 \hat \imath$$
$$(m_1 \ddot x_1 - m_1 g) \cdot \delta x_1 = -(m_2 \ddot x_1  + m_2 g) \cdot \delta x_1$$
$$(m_1 \ddot x_1 - m_1 g) = -(m_2 \ddot x_1 + m_2 g)$$
$$(m_1 \ddot x_1 - m_1 g) + (m_2 \ddot x_1 + m_2 g) = 0$$
$$(m_1 +m_2) \ddot x_1 + (m_2 -m_1) g = 0$$
$$\ddot x_1 = \dfrac{m_1 - m_2}{m_1 +m_2}g = - \ddot x_2$$
O resultado coincide com o resultado obtido pelo tratamento newtoniano elementar.


## Coordenadas Generalizadas

Em sistemas holônomos é possível introduzir um certo número de variáveis independentes $q_1, ..., q_n$ chamadas coordenadas generalizadas, de modo que:

$i)$ O vetor posição de cada partícula $(\vec r_1, ..., \vec r_N)$ é determinado univocamente pelos valores de  $q_1, ..., q_N$.

$ii)$ Os vínculos holônomos são satisfeitos quando expressos em termos de  $q_1, ..., q_N$.

**Exemplo**: Pêndulo Duplo no Plano.
![[Pasted image 20221001152657.png]]
Vínculos:
- $x_1^2 + y_1^2 = l_1^2$
- $(x_2 - x_1)^2 + (y_2 - y_1)^2 = l_2^2$

Fazendo $q_1 = \theta_1$ e $q_2 = \theta_2$, analisamos:

$i)$ 
$$x_1 = l_1 \; sin \theta_1, \;\;\;\;\; y_1 = l_1 \; cos \theta_1$$
$$x_2 = l_1 \; sin \theta_1 + l_2 \; sin \theta_2, \;\;\;\;\; y_2 = l_1 \; cos \theta_1 + l_2 \; cos \theta_2$$

$ii)$ Para o primeiro vínculo: 
$$x_1^2 + y_1^2 = l_1^2$$
$$(l_1 \; sin \theta_1)^2 + (l_1 \; cos \theta_1)^2 = l_1^2$$
$$l_1^2 \; sin^2 \theta_1 + l_1^2 \; cos^2 \theta_1 = l_1^2$$
$$l_1^2 (sin^2 \theta_1 + cos^2 \theta_1) = l_1^2$$
$$l_1^2 = l_1^2$$
Então para o segundo vínculo:
$$(x_2 - x_1)^2 + (y_2 - y_1)^2 = l_2^2$$
$$(l_1 \; sin \theta_1 + l_2 \; sin \theta_2 - l_1 \; sin \theta_1)^2 + (l_1 \; cos \theta_1 + l_2 \; cos \theta_2 - l_1 \; cos \theta_1)^2 = l_2^2$$
$$(l_2 \; sin \theta_2)^2 + (l_2 \; cos \theta_2)^2 = l_2^2$$
$$l_2^2 \; sin^2 \theta_2 + l_2^2 \; cos^2 \theta_2 = l_2^2$$
$$l_2^2 (sin^2 \theta_2 + cos^2 \theta_2) = l_2^2$$
$$l_2^2 = l_2^2$$

**Exemplo**: Uma partícula obrigada a permanecer sobre um círculo de raio R que se move uniformemente ($\vec u$).
![[Pasted image 20221002001053.png]]

Em $t=0$ o centro do disco está a origem

$$x = u_x t + R \; cos \theta, \;\;\;\;\; y = u_y t + R \; sin \theta $$
Fazendo $q_1 = \theta$, analisamos o vínculo:
$$(x - u_xt)^2+(y-u_yt)^2=R^2$$
$$(u_x t + R \; cos \theta - u_xt)^2+(u_y t + R \; sin \theta-u_yt)^2=R^2$$
$$(R \; cos \theta)^2+(R \; sin \theta)^2=R^2$$
$$R^2 \; cos^2 \theta + R^2 \; sin^2 \theta=R^2$$
$$R^2 (cos^2 \theta + sin^2 \theta) = R^2$$
$$R^2 = R^2$$

Então, um sistema de $N$ partículas pode ser descrito usando $n$ coordenadas generalizadas sedo $n = (\text{coordenadas necessárias para descrever as partículas}) - (\text{vínculos holônomos do sistema})$

Dizemos que o sistema possui $n$ graus de liberdade.

**Configuração do Sistema**: Determina as posições das partículas em função de $q_1, ..., q_n$.

**Espaço de Configuração**: Espaço cartesiano que tem como eivos coordenados as Coordenadas Generalizadas. 