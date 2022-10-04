# Vínculos

**Definicão:** Limitações impostas às possíveis posições e velocidades das partículas em um sistema mecânico, restringindo seu movimeto.

As limitações são de *ordem cienemática* e precisam ser levadas em conta na formulação das equações de movimeto do sistema.

Restrições de natureza dinâmica, decorentes das equações de movimento, não são vínculos!

**Exemplo**: Pêndulo Duplo.
![[Pasted image 20221001152657.png]]
***Vínculos***:
- $x_1^2 + y_1^2 =l_1^2$
- $(x_2 - x_1)^2 + (y_2 - y_1)^2 = l_2^2$

Note que $x_1$, $x_2$, $y_1$ e $y_3$ *não são independentes*, pois só podem assumir valores que respeitem os vínculos.

## Vínculos Holônomos

Se $\xi_1$, ..., $\xi_m$ são coordenadas arbitrárias usadas para descrever a ***configuração*** de um sistema mecânico e o sistema pode ser descrito exclusivamente por estas coordenadas, podendo envolver o tempo, seus vínculos são ditos vínculos holônomos.
$$f(\xi_1, ..., \xi_M, t) = 0$$
***Configuração*** é a posição de cada uma das partículas de um sistema mecânico num dado instante.

Podem ocorrer, principalmente na dinâmica de corpos rígidos, vínculos representáveis por equações envolvendo velocidades.
$$g(\xi_1, ..., \xi_M, \dot\xi_1, ..., \dot\xi_M, t) = 0$$
Em geral, estes vínculos não são holônomos, porém se um vínculo expresso em termos também das velocidades puder ser reduzido por uma integração à forma que dependa apenas das coordenadas, e talvez também do tempo, ele será digo holônomo.

**Exemplo**: Considere o rolamento sem deslizar de um disco de raio R.

![[Pasted image 20221001155952.png]]

O Vínculo de rolamento sem deslizar será $\dot x_{CM} = R \dot \theta$.

Apesar de envolver velocidades, este vínculo ainda é holônomo pois:

$$\dot x_{CM} = R \dot \theta, \;\;\;\;\; \dfrac{d}{dt} x_{CM} = R \dfrac{d}{dt} \theta, \;\;\;\;\; dx_{CM} = R \; d \theta$$
$$\int dx_{CM} = \int R \; d \theta, \;\;\;\;\; x_{CM} + C_1= R \theta 
+ C_2, \;\;\;\;\; x_{CM} = R \theta + C$$

**Exemplo**: Um disco vertical de raio R rola sem deslizar em um plano horizontal.
![[Pasted image 20221001163948.png]]
Vínculos:
- $\dot x_{CM} - R \; \dot \phi \; cos \theta = 0$
- $\dot y_{CM} - R \; \dot \phi \; sin \theta = 0$

Para que os vínculos sejam integráveis, deve existir um fator integrante não-nulo $h(x, y, \theta, \phi, t)$, logo, para o primeiro vínculo devemos ter que:
$$h(x, y, \theta, \phi, t) \cdot (\dot x_{CM} - R \; \dot \phi \; cos \theta) = \dfrac{d}{dt} G(x, y, \theta, \phi, t) = \dfrac{\partial G}{\partial x} \dot x + \dfrac{\partial G}{\partial y} \dot y + \dfrac{\partial G}{\partial \theta} \dot \theta + \dfrac{\partial G}{\partial \phi} \dot \phi + \dfrac{\partial G}{\partial t} $$
onde G será equivalente a uma constante arbitrária $G(x, y, \theta, \phi, t) - C = 0$ que tem a forma $f(x, y, \theta, \phi, t)$.

Assumindo que o vínculo é integrável, comparando os coeficientes temos que:
$$h \; \dot x - h \; R \; \dot \phi \; cos \theta =  \dfrac{\partial G}{\partial x} \dot x + \dfrac{\partial G}{\partial y} \dot y + \dfrac{\partial G}{\partial \theta} \dot \theta + \dfrac{\partial G}{\partial \phi} \dot \phi + \dfrac{\partial G}{\partial t} $$$$\dfrac{\partial G}{\partial x} = h, \;\;\; \dfrac{\partial G}{\partial y} = 0, \;\;\; \dfrac{\partial G}{\partial \theta} = 0, \;\;\; \dfrac{\partial G}{\partial \phi} = -h \; R \; cos \theta $$Assumido, também, funções *bem comportadas*, contínuas e que possuem derivadas contínuas, temos que a ordem de diferenciação uma segunda derivada é irrelevante, então:
$$\dfrac{\partial^2 G}{\partial y \partial x} = \dfrac{\partial^2 G}{\partial x \partial y} \Longrightarrow \dfrac{\partial G}{\partial y} h = \dfrac{\partial G}{\partial x} 0 \Longrightarrow h = h(x, \theta, \phi, t)$$
$$\dfrac{\partial^2 G}{\partial \theta \partial x} = \dfrac{\partial^2 G}{\partial x \partial \theta} \Longrightarrow \dfrac{\partial G}{\partial \theta} h = \dfrac{\partial G}{\partial x} 0 \Longrightarrow h = h(x, \phi, t)$$
$$\dfrac{\partial^2 G}{\partial \theta \partial \phi} = \dfrac{\partial^2 G}{\partial \phi \partial \theta} \Longrightarrow \dfrac{\partial G}{\partial \theta} (-h \; R \; cos \theta) = \dfrac{\partial G}{\partial \phi} 0 \Longrightarrow  h \; R \; sin \theta = 0$$
Temos então que $h \; R \; sin \theta = 0$ e que $h$ não depende de $\theta$, logo $h \; R \; sin \theta = 0$ é válido para qualquer $\theta$, e isso somente é possível para $h = 0$, logo não existe $h$ não nulo, sendo então o vínculo não-holônomo.


A ideia de vínculo leva ao conceito de ***deslocamento infinitesimal virtual*** $\delta \vec r$ caracterizado por uma mudança de coordenadas (configuração) consistente com os vínculos num instante *fixo* de tempo.

Considerando um sistema de $N$ partículas, podemos dizer que a força total na $i$-ésima partícula tem a forma:
$$\vec F_i = \vec F_i^{(a)} + \vec f_i$$
onde $\vec F_i^{(a)}$ são as Forças Aplicadas e $\vec f_i$ são as Forças de vínculo.

No exemplo do pêndulo duplo, $\vec F_1^{(a)}$ e $\vec F_2^{(a)}$ são as forças peso em $m_1$ e $m_2$ enquanto $\vec f_1$ e $\vec f_2$ são as tensões nos fios $l_1$ e $l_2$.

Com isso podemos chegar a uma formulação que lide diretamente com as Forças Aplicadas e com um número reduzido de coordenadas independentes.
