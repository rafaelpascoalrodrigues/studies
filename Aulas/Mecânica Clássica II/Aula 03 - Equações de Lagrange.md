# Equações de Lagrange

Partindo do Princípio de d'Alembert:
$$\sum_{i=1}^N (\dot{\vec P_i} - \vec F_i^{(a)}) \cdot \delta \vec r_i = 0 $$
Assumindo vínculos ideais, logo $\vec f_i = 0, i=1, ..., N$, podemos abreviar a notação para das Forças Aplicadas para $\vec F_i^{(a)} \equiv \vec F_i$, então ficamos com:
$$\sum_{i=1}^N (\dot{\vec P_i} - \vec F_i) \cdot \delta \vec r_i = 0 $$$$\sum_{i=1}^N \dot{\vec P_i} \cdot \delta \vec r_i - \sum_{i=1}^N \vec F_i \cdot \delta \vec r_i = 0 $$
Consideramos então expressá-lo em Coordenadas Generalizadas $(q_1, ..., q_n)$ fazendo $\vec r_i = \vec r_i(q_1, ..., q_n, t)$.

Analisando, primeiramente, a somatória com relação às Forças Aplicadas:
$$\sum_{i=1}^N \vec F_i \cdot \delta \vec r_i$$
Para o deslocamento virtual temos:
$$\delta \vec r_i = \sum_{k=1}^n \dfrac{\partial \vec r_i}{\partial q_k} \delta q_k$$
Logo:
$$\sum_{i=1}^N \vec F_i \cdot \delta \vec r_i = \sum_{i=1}^N \vec F_i \cdot \sum_{k=1}^n \dfrac{\partial \vec r_i}{\partial q_k} \delta q_k = \sum_{k=1}^N \sum_{i=1}^n \vec F_i \cdot \dfrac{\partial \vec r_i}{\partial q_k} \delta q_k$$
Neste ponto temos $\sum_{i=1}^N \vec F_i \cdot \dfrac{\partial \vec r_i}{\partial q_k}$ que, por definição, é a $k$-ésima componente da ***Força Generalizada***, representada por $Q_k$, que não possuem necessariamente dimensão de força, visto que os $q_n$ não possuem necessariamente dimensão de comprimento, contudo $Q_k \delta q_k$ sempre possui dimensão de trabalho.

Logo:
$$ \sum_{k=1}^N \sum_{i=1}^n \vec F_i \cdot \dfrac{\partial \vec r_i}{\partial q_k} \delta q_k = \sum_{k=1}^n Q_k \; \delta q_k$$
Analisando então a somatória com relação ao momento:
$$\sum_{i=1}^N \dot{\vec P_i} \cdot \delta \vec r_i = \sum_{i=1}^N m_i \dot{\vec v_i} \cdot \delta \vec r_i = \sum_{i=1}^N m_i \dot{\vec v_i} \cdot \sum_{k=1}^n \dfrac{\partial \vec r_i}{\partial q_k} \delta q_k = \sum_{k=1}^n \sum_{i=1}^N m_i \dot{\vec v_i} \cdot  \dfrac{\partial \vec r_i}{\partial q_k} \delta q_k$$
Aplicamos então a seguinte identidade:
$$\dfrac{d}{dt} \left( m_i \vec v_i \cdot  \dfrac{\partial \vec r_i}{\partial q_k} \right) = \dfrac{d}{dt} (m_i \vec v_i) \cdot\dfrac{\partial \vec r_i}{\partial q_k} + m_i \vec v_i \cdot \dfrac{d}{dt} \left( \dfrac{\partial \vec r_i}{\partial q_k} \right)$$$$\dfrac{d}{dt} \left( m_i \vec v_i \cdot  \dfrac{\partial \vec r_i}{\partial q_k} \right) = m_i \dot{\vec v_i} \cdot\dfrac{\partial \vec r_i}{\partial q_k} + m_i \vec v_i \cdot \dfrac{d}{dt} \left( \dfrac{\partial \vec r_i}{\partial q_k} \right)$$$$m_i \dot{\vec v_i} \cdot\dfrac{\partial \vec r_i}{\partial q_k} = \dfrac{d}{dt} \left( m_i \vec v_i \cdot  \dfrac{\partial \vec r_i}{\partial q_k} \right) - m_i \vec v_i \cdot \dfrac{d}{dt} \left( \dfrac{\partial \vec r_i}{\partial q_k} \right)$$Logo:
$$\sum_{i=1}^N m_i \vec v_i \cdot  \dfrac{\partial \vec r_i}{\partial q_k} = \sum_{i=1}^N \left( \dfrac{d}{dt} \left( m_i \vec v_i \cdot  \dfrac{\partial \vec r_i}{\partial q_k} \right) - m_i \vec v_i \cdot \dfrac{d}{dt} \left( \dfrac{\partial \vec r_i}{\partial q_k} \right) \right)$$
Então:
$$\sum_{k=1}^n \sum_{i=1}^N m_i \dot{\vec v_i} \cdot  \dfrac{\partial \vec r_i}{\partial q_k} \delta q_k = \sum_{k=1}^n \sum_{i=1}^N \left( \dfrac{d}{dt} \left( m_i \vec v_i \cdot  \dfrac{\partial \vec r_i}{\partial q_k} \right) - m_i \vec v_i \cdot \dfrac{d}{dt} \left( \dfrac{\partial \vec r_i}{\partial q_k} \right) \right) \delta q_k$$
Isoladamente:
$$\dfrac{d}{dt} \left( \dfrac{\partial \vec r_i}{\partial q_k} \right) = \sum_{l=1}^n \dfrac{\partial}{\partial q_l} \left( \dfrac{\partial \vec r_i}{\partial q_k} \right) \dot q_l + \dfrac{\partial}{\partial t} \left( \dfrac{\partial \vec r_i}{\partial q_k} \right) = \dfrac{\partial}{\partial q_k} \left( \sum_{l=1}^n \dfrac{\partial \vec r_i}{\partial q_l} \dot q_i + \dfrac{\partial \vec r_i}{\partial t} \right)$$
Analisando então a velocidade das partículas:
$$\vec v_i= \dfrac{d \vec r_i}{dt} = \sum_{l=1}^n \dfrac{\partial \vec r_i}{\partial q_l} \dfrac{d q_l}{dt} + \dfrac{\partial \vec r_i}{\partial t} \dfrac{d t}{d t} = \sum_{l=1}^n \dfrac{\partial \vec r_i}{\partial q_l} \dot q_l + \dfrac{\partial \vec r_i}{\partial t}$$
Logo:
$$\dfrac{d}{dt} \left( \dfrac{\partial \vec r_i}{\partial q_k} \right) =\dfrac{\partial}{\partial q_k} \left( \sum_{l=1}^n \dfrac{\partial \vec r_i}{\partial q_l} \dot q_i + \dfrac{\partial \vec r_i}{\partial t} \right) = \dfrac{\partial \vec v_i}{\partial q_k}$$
Tratado as posições e velocidades como gradezas independentes, as derivadas parciais em relação aos $q_n$ tratam os $\dot q_n$ como constates, e vice-versa, então deduzimos:
$$\dfrac{\partial \vec v_i}{\partial \dot q_k} = \sum_{l=1}^n \dfrac{\partial \vec r_i}{\partial q_l} \dfrac{\partial \dot q_k}{\partial \dot q_k} = \dfrac{\partial \vec r_i}{\partial q_k}$$

Então: 
$$\sum_{k=1}^n \sum_{i=1}^N \left( \dfrac{d}{dt} \left( m_i \vec v_i \cdot  \dfrac{\partial \vec r_i}{\partial q_k} \right) - m_i \vec v_i \cdot \dfrac{d}{dt} \left( \dfrac{\partial \vec r_i}{\partial q_k} \right) \right) \delta q_k$$$$\sum_{k=1}^n \sum_{i=1}^N \left( \dfrac{d}{dt} \left( m_i \vec v_i \cdot  \dfrac{\partial \vec v_i}{\partial \dot q_k} \right) - m_i \vec v_i \cdot \dfrac{\partial \vec v_i}{\partial q_k} \right) \delta q_k$$
Usando a seguinte identidade:
$$\dfrac{\partial}{\partial \dot q_k} \left( \dfrac{1}{2} m_i \vec v_i \cdot \vec v_i \right) = \dfrac{1}{2} m_i \dfrac{\partial \vec v_i}{\partial \dot q_k} \cdot \vec v_i + \dfrac{1}{2} m_i \vec v_i \cdot \dfrac{\partial \vec v_i}{\partial \dot q_k} = m_i \vec v_i \cdot \dfrac{\partial \vec v_i}{\partial \dot q_k}$$
E analogamente:
$$\dfrac{\partial}{\partial q_k} \left( \dfrac{1}{2} m_i \vec v_i \cdot \vec v_i \right) = \dfrac{1}{2} m_i \dfrac{\partial \vec v_i}{\partial q_k} \cdot \vec v_i + \dfrac{1}{2} m_i \vec v_i \cdot \dfrac{\partial \vec v_i}{\partial q_k} = m_i \vec v_i \cdot \dfrac{\partial \vec v_i}{\partial q_k}$$
Então:
$$\sum_{k=1}^n \sum_{i=1}^N \left( \dfrac{d}{dt} \left( m_i \vec v_i \cdot  \dfrac{\partial \vec v_i}{\partial \dot q_k} \right) - m_i \vec v_i \cdot \dfrac{\partial \vec v_i}{\partial q_k} \right) \delta q_k$$
$$\sum_{k=1}^n \sum_{i=1}^N \left( \dfrac{d}{dt} \left( \dfrac{\partial}{\partial \dot q_k} \left( \dfrac{1}{2} m_i \vec v_i \cdot \vec v_i \right)\right) - \dfrac{\partial}{\partial q_k} \left( \dfrac{1}{2} m_i \vec v_i \cdot \vec v_i \right) \right) \delta q_k$$
$$\sum_{k=1}^n \sum_{i=1}^N \left( \dfrac{d}{dt} \left( \dfrac{\partial}{\partial \dot q_k} \left( \dfrac{1}{2} m_i v_i^2 \right)\right) - \dfrac{\partial}{\partial q_k} \left( \dfrac{1}{2} m_i  v_i^2 \right) \right) \delta q_k$$
Encontrando então um termo que remete à Energia Cinética da $i$-ésima partícula, que será denotado por $T_i$ e a Energia Cinética Total por $T = \sum_{i=1}^N = \dfrac{1}{2} m_i v_i^2$.
$$ \sum_{k=1}^n \sum_{i=1}^N \left( \dfrac{d}{dt} \left( \dfrac{\partial}{\partial \dot q_k} \left( \dfrac{1}{2} m_i v_i^2 \right)\right) - \dfrac{\partial}{\partial q_k} \left( \dfrac{1}{2} m_i  v_i^2 \right) \right) \delta q_k= \sum_{k=1}^n \sum_{i=1}^N \left( \dfrac{d}{dt} \left( \dfrac{\partial T_i}{\partial \dot q_k} \right) - \dfrac{\partial T_i}{\partial q_k} \right) \delta q_k$$$$\sum_{k=1}^n \left( \dfrac{d}{dt} \left( \dfrac{\partial T}{\partial \dot q_k} \right) - \dfrac{\partial T}{\partial q_k} \right) \delta q_k$$
Logo, temos que para o momento:
$$\sum_{i=1}^N \dot{\vec P_i} \cdot \delta \vec r_i = \sum_{k=1}^n \left( \dfrac{d}{dt} \left( \dfrac{\partial T}{\partial \dot q_k} \right) - \dfrac{\partial T}{\partial q_k} \right) \delta q_k$$
Retomando o resultado obtido para as Forças Aplicadas:
$$\sum_{i=1}^N \vec F_i \cdot \delta \vec r_i =  \sum_{k=1}^N \sum_{i=1}^n \vec F_i \cdot \dfrac{\partial \vec r_i}{\partial q_k} \delta q_k = \sum_{k=1}^n Q_k \; \delta q_k$$
Temos então que:
$$\sum_{i=1}^N \dot{\vec P_i} \cdot \delta \vec r_i - \sum_{i=1}^N \vec F_i \cdot \delta \vec r_i = 0 $$
$$\sum_{k=1}^n \left( \dfrac{d}{dt} \left( \dfrac{\partial T}{\partial \dot q_k} \right) - \dfrac{\partial T}{\partial q_k} \right) \delta q_k - \sum_{k=1}^n Q_k \; \delta q_k = 0$$
$$\sum_{k=1}^n \left( \dfrac{d}{dt} \left( \dfrac{\partial T}{\partial \dot q_k} \right) - \dfrac{\partial T}{\partial q_k} - Q_k\right) \delta q_k = 0$$
Como os $\delta q_n$ são mutualmente independentes e arbitrários, esta igualdade só poderá ser satisfeita se o coeficiente de cada  $\delta q_n$ for zero, então temos que:
$$\dfrac{d}{dt} \left( \dfrac{\partial T}{\partial \dot q_k} \right) - \dfrac{\partial T}{\partial q_k} = Q_k, \;\;\;\;\; k=1, ..., n$$

Caso as Forças Aplicadas sejam conservativas, isto significa que existe uma Energia Potencial no sistema, que será denotada por $V$, tal que:
$$V=V(\vec r_1, ..., \vec r_N, t)$$
Neste caso:
$$\vec F_i = -\nabla_i V = -\left( \dfrac{\partial V}{\partial x_i} \hat \imath + \dfrac{\partial V}{\partial y_i} \hat \jmath + \dfrac{\partial V}{\partial z_i} \hat k\right)$$
E as Forças Generalizadas serão:
$$Q_k = \sum_{i=1}^N \vec F_i \cdot \dfrac{\partial \vec r_i}{\partial q_k} = - \sum_{i=1}^N \left( \dfrac{\partial V}{\partial x_i} \hat \imath + \dfrac{\partial V}{\partial y_i} \hat \jmath + \dfrac{\partial V}{\partial z_i} \hat k\right) \cdot \left( \dfrac{\partial x_i}{\partial q_k} \hat \imath + \dfrac{\partial y_i}{\partial q_k} \hat \jmath + \dfrac{\partial z_i}{\partial q_k} \hat k\right)$$
$$Q_k = - \sum_{i=1}^N \left( \dfrac{\partial V}{\partial x_i} \dfrac{\partial x_i}{\partial q_k}  + \dfrac{\partial V}{\partial y_i} \dfrac{\partial y_i}{\partial q_k} + \dfrac{\partial V}{\partial z_i} \dfrac{\partial z_i}{\partial q_k} \right) = - \dfrac{\partial V}{\partial q_k}$$
Logo: 
$$\dfrac{d}{dt} \left( \dfrac{\partial T}{\partial \dot q_k} \right) - \dfrac{\partial T}{\partial q_k} = Q_k = - \dfrac{\partial V}{\partial q_k}$$
$$\dfrac{d}{dt} \left( \dfrac{\partial T}{\partial \dot q_k} \right) - \dfrac{\partial T}{\partial q_k} +\dfrac{\partial V}{\partial q_k} = 0$$
$$\dfrac{d}{dt} \left( \dfrac{\partial T}{\partial \dot q_k} \right) - \dfrac{\partial}{\partial q_k} (T - V) = 0$$
Dado que $V$ não depende de $\dot q_k$, $\dfrac{\partial V}{\partial \dot q_k} = 0$, a equação se torna:
$$\dfrac{d}{dt} \left( \dfrac{\partial}{\partial \dot q_k} (T-V) \right) - \dfrac{\partial}{\partial q_k} (T - V) = 0$$
Definimos a **Lagrangiana** por $L = T - V$, logo:
$$\dfrac{d}{dt} \left( \dfrac{\partial L}{\partial \dot q_k} \right) - \dfrac{\partial L}{\partial q_k} = 0, \;\;\;\;\; k = 1, ..., n$$

**Exemplo**: Obtenha a Lagrangiana e as equações de Lagrange para o sistema ilustrado abaixo. Considere que o comprimento natural da mola é $l$.
![[Pasted image 20221002183830.png]]
Vínculos:
- $x_1 + x_2 = l_0$ 

Graus de liberdade:
- $n = 3 \; \text{(coordenadas posicionais)} - 1 \; \text{(vínculo)} = 2$

*Arbitrariamente*, adotamos: $q_1 = x_2$ e $q_2 = x_3$, logo $x_1 = l_0 - x_2$ e $\dot x_1 = - \dot x_2$, $(\dot x_1)^2 = (\dot x_2)^2$.


Analisado a Energia Cinética $T$ do sistema:

$$T = \dfrac{1}{2} m_1 \dot x_1^2 + \dfrac{1}{2} m_2 \dot x_2^2 + \dfrac{1}{2} m_3 \dot x_3^2 = \dfrac{1}{2} m_1 \dot x2^2 + \dfrac{1}{2} m_2 \dot x_2^2 + \dfrac{1}{2} m_3 \dot x_3^2$$
$$ T = \dfrac{1}{2} (m_1 + m_2) \dot x_2^2 + \dfrac{1}{2} m_3 \dot x_3^2$$
Analisando então a Energia Potencial $V$, assumindo $V=0$ na linha horizontal do eixo da roldana:
$$V = -m_1 g x_1 -m_2 g x_2 - m_3 g x_3 + \dfrac{1}{2} k((x_3 - x_2) - l)^2$$
$$V = - m_1 g (l_0 - x_2) -m_2 g x_2 - m_3 g x_3 + \dfrac{1}{2} k(x_3 - x_2 - l)^2$$
$$V = - m_1 g l_0 + m_1 g x_2 -m_2 g x_2 - m_3 g x_3 + \dfrac{1}{2} k(x_3 - x_2 - l)^2$$
$$V = - m_1 g l_0 - (m_2 - m_1) g x_2 - m_3 g x_3 + \dfrac{1}{2} k(x_3 - x_2 - l)^2$$
Então a Lagrangiana:
$$L=T-V$$
$$L= \dfrac{1}{2} (m_1 + m_2) \dot x_2^2 + \dfrac{1}{2} m_3 \dot x_3^2 + m_1 g l_0 + (m_2 - m_1) g x_2 + m_3 g x_3 - \dfrac{1}{2} k(x_3 - x_2 - l)^2$$
Logo e com isso as derivadas parciais serão:

$$\dfrac{\partial L}{\partial \dot x_2} = (m_1 + m_2) \dot x_2 $$
$$\dfrac{\partial L}{\partial \dot x_3} = m_3 \dot x_3 $$
$$\dfrac{\partial L}{\partial x_2} = (m_2 - m_1)g + k(x_3 - x_2 - l)  $$
$$\dfrac{\partial L}{\partial x_3} = m_3 g - k(x_3 - x_2 - l)  $$
E com isso, as Equações de Lagrange serão:

Para $x_2$: 
$$\dfrac{d}{dt} \left( \dfrac{\partial L}{\partial \dot x_2} \right) - \dfrac{\partial L}{\partial x_2} = 0$$
$$\dfrac{d}{dt} \left( (m_1 + m_2) \dot x_2 \right) - (m_2 - m_1)g - k(x_3 - x_2 - l) = 0$$
$$(m_1 + m_2) \ddot x_2 - (m_2 - m_1)g - k(x_3 - x_2 - l) = 0$$

Para $x_3$:
$$\dfrac{d}{dt} \left( \dfrac{\partial L}{\partial \dot x_3} \right) - \dfrac{\partial L}{\partial x_3} = 0$$
$$\dfrac{d}{dt} \left( m_3 \dot x_3 \right) - m_3 g + k(x_3 - x_2 - l) = 0$$
$$m_3 \ddot x_3 - m_3 g + k(x_3 - x_2 - l) = 0$$


Supondo que a mola não exista, $k=0$, temos que:
$$(m_1 + m_2) \ddot x_2 - (m_2 - m_1)g - k(x_3 - x_2 - l) = 0$$
$$(m_1 + m_2) \ddot x_2 - (m_2 - m_1)g = 0$$
$$ \ddot x_2 = \dfrac{(m_2 - m_1)}{(m_1 + m_2)}g \;\;\;\;\; \text{(máquina de Atwood)}$$

$$m_3 \ddot x_3 - m_3 g + k(x_3 - x_2 - l) = 0$$
$$m_3 \ddot x_3 - m_3 g = 0$$
$$m_3 \ddot x_3 = m_3 g $$
$$\ddot x_3 = g \;\;\;\;\; \text{(queda livre)} $$
