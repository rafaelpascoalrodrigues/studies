# Trabalho e Energia na Eletrostática

Uma carga colocada em um Campo Elétrico recebe uma Força do Campo Elétrico, logo, ao realizar um deslocamento desta carga o Campo Elétrico irá realizar um Trabalho sobre esta carga. 

Ao fazer uma movimentação de cargas, trazendo cargas para uma região onde originalmente não haviam cargas e construindo assim um objeto carregado, Trabalho é realizado sobre estas cargas, gerando então a Energia do Campo Elétrico.

$$W = \int_{\vec a}^{\vec b} \vec F \cdot d \vec l \ \ \ : \text{Trabalho Mecânico}$$
Na eletrostática, a Força Elétrica é definida por:
$$\vec F = Q \ \vec E, \ \ \ \ \text{logo: } W = Q \int_{\vec a}^{\vec b} \vec E \cdot d \vec l$$
Este é o Trabalho realizado pelo Campo Elétrico sobre a Carga.

O Trabalho sobre o Campo é o Trabalho necessário para levar uma carga $Q$ do ponto $\vec a$ ao ponto $\vec B$ em um Campo Elétrico $\vec E$:
$$W_{\text{pelo o campo}} = -W_{\text{sobre o campo}}$$
Neste conteúdo trabalharemos majoritariamente com o Trabalho realizado sobre o campo, então definimos:
$$W_{\text{sobre o campo}} = W = -Q \int_{\vec a}^{\vec b} \vec E \cdot d \vec l$$
Lembrando que:
$$\Delta V = V(\vec a) - V(\vec b) = - \int_{\vec a}^{\vec b} \vec E \cdot d \vec l $$
Logo:
$$W = Q \ \Delta V$$

Analisando então o Trabalho para trazer uma carga do infinito até o ponto $\vec r$:
$$W = Q \ \Delta V = V(\vec r) - V(\infty) = \dfrac{W}{Q}$$
Escolhendo o referencial onde $V(\infty) =0$:
$$V(\vec r) = \dfrac{W}{Q} \equiv [V] \equiv [J/C]$$

Ao trazer uma carga $q_1$ do infinito para um ponto $\vec r_1$ onde não há cargas ou Campo Elétrico, o Trabalho é nulo.

Então, ao trazer uma segunda carga $q_2$ do infinito para uma posição $\vec r_2$ teremos um Trabalho $W_{12}$ para trazer a carga $q_2$ para a posição $\vec r_2$ na presença de $q_1$ em $\vec r_1$.

![[Pasted image 20221014162813.png]]

Pela presença da carga $q_1$, temos então um Potencial Elétrico sobre o ponto $\vec r_2$:
$$V_{12} = \frac{1}{4 \pi \epsilon_0} \frac{q_1}{r_{12}}$$
Logo o Trabalho para trazer a carga $q_2$ para a posição $\vec r_2$ será:
$$W_2 = q_2 \ V_{12} =\frac{1}{4 \pi \epsilon_0} \frac{q_1 q_2}{r_{12}} $$
Agora, para trazer uma carga $q_3$ do infinito para uma posição $\vec r_3$ teremos na posição $\vec r_3$ teremos os Potenciais Elétricos $V_{13}$ devido à carga $q_1$ e $V_{12}$ devido à carga $q_2$:
$$V_{13} = \frac{1}{4 \pi \epsilon_0} \frac{q_1}{r_{13}}, \ \ \ \ V_{23} = \frac{1}{4 \pi \epsilon_0} \frac{q_2}{r_{23}}$$
![[Pasted image 20221014163943.png]]
Logo o Trabalho para trazer a carga $q_3$ para a posição $\vec r_3$ será:

$$W_3 = q_3 \ (V_{13} + V_{23}) =\frac{1}{4 \pi \epsilon_0} \left( \frac{q_1 q_3}{r_{13}} + \frac{q_2 q_3}{r_{23}} \right)$$
Ao adicionar uma quarta carga $q_4$ na posição $\vec r_4$ o processo é similar:
$$V_{14} = \frac{1}{4 \pi \epsilon_0} \frac{q_1}{r_{14}}, \ \ \ \ V_{24} = \frac{1}{4 \pi \epsilon_0} \frac{q_2}{r_{24}}, \ \ \ \ V_{34} = \frac{1}{4 \pi \epsilon_0} \frac{q_3}{r_{34}}$$
Então o Trabalho para trazer a carga $q_4$ para a posição $\vec r_4$ será:
$$W_4 = q_4 \ (V_{14} + V_{24} + V_{34}) =c$$

E o Trabalho total para trazer as 4 cargas do infinito para suas respectivas posições será a soma dos Trabalhos:
$$W_T = W_1 +W_2+W_3+W_4$$
$$W_T = 0 + \frac{1}{4 \pi \epsilon_0} \frac{q_1 q_2}{r_{12}}+\frac{1}{4 \pi \epsilon_0} \left( \frac{q_1 q_3}{r_{13}} + \frac{q_2 q_3}{r_{23}} \right)+\frac{1}{4 \pi \epsilon_0} \left( \frac{q_1 q_4}{r_{14}} + \frac{q_2 q_4}{r_{24}} + \frac{q_4 q_4}{r_{34}} \right)$$
$$W_T = \frac{1}{4 \pi \epsilon_0}  \left(\frac{q_1 q_2}{r_{12}}+ \frac{q_1 q_3}{r_{13}} + \frac{q_2 q_3}{r_{23}} + \frac{q_1 q_4}{r_{14}} + \frac{q_2 q_4}{r_{24}} + \frac{q_4 q_4}{r_{34}}\right)$$

Generalizando para $n$ cargas trazidas do infinito para suas respectivas $\vec r_i$ posições:
$$W_T^{(n)} = \frac{1}{4 \pi \epsilon_0}  \sum_{\substack{i=1 \\ i \neq j}}^n \sum_{j=1}^n \dfrac{q_i q_j}{r_{ij}}$$
Separando os dois somatórios deste modo iremos somar o potencial de uma carga com outra e novamente desta outra com a primeira, então precisamos dividir o valor pela metade:
$$W_T^{(n)} = \dfrac{1}{2} \sum_{\substack{i=1 \\ i \neq j}}^n q_i \left( \sum_{j=1}^n \frac{1}{4 \pi \epsilon_0} \dfrac{q_j}{r_{ij}} \right)$$
Reconhecemos $\sum_{j=1}^n \frac{1}{4 \pi \epsilon_0} \dfrac{q_j}{r_{ij}}$ como sendo o Potencial Elétrico total de cada carga sobre um ponto $\vec r_i$:
$$V(\vec r_i) = \sum_{j=1}^n \frac{1}{4 \pi \epsilon_0} \dfrac{q_j}{|r_{i} - r_j|}$$
Logo:
$$W_T^{(n)} = \dfrac{1}{2} \sum_{i=1}^n q_i \ V(\vec r_i) $$

Partindo para uma distribuição contínua de cargas em um volume $V'$, teremos $n \rightarrow \infty$ e $q \rightarrow dq$:

$$W = \dfrac{1}{2} \int_{V'} \rho(\vec r) \ V(\vec r)\ dV' $$
Pela Lei de Gauss na forma diferencial:
$$\vec \nabla \cdot \vec E = \dfrac{\rho}{\epsilon_0}, \ \ \ \ \  \rho = \epsilon_0 \ \vec \nabla \cdot \vec E$$$$W = \dfrac{1}{2} \int_{V'} \epsilon_0 \ ( \vec \nabla \cdot \vec E) \ V(\vec r)\ dV' $$
Pela identidade:
$$\vec \nabla \cdot(\vec A \ B) = (\vec \nabla \cdot \vec A) B + \vec A \cdot (\vec \nabla B), \ \ \ \ \ (\vec \nabla \cdot \vec A) B = \vec \nabla \cdot(\vec A \ B) - \vec A \cdot(\vec \nabla B) $$
$$(\vec \nabla \cdot \vec E) V = \vec \nabla \cdot(\vec E \ V) - \vec E \cdot (\vec \nabla V)$$
$$W = \dfrac{1}{2} \int_{V'} \epsilon_0 (\vec \nabla \cdot(\vec E \ V) - \vec E \cdot (\vec \nabla V)) \ dV' $$
$$W = \dfrac{1}{2}  \epsilon_0 \left( \int_{V'} (\vec \nabla \cdot(\vec E \ V) \ dV' - \int_{V'}\vec E \cdot (\vec \nabla V) \ dV' \right) $$
Pelo Teorema de Gauss:
$$\int_V \vec \nabla \cdot \vec f \ dV - \oint_S \vec f \cdot d \vec a$$
$$W = \dfrac{1}{2}  \epsilon_0 \left( \oint_{S'} (\vec E \ V) \cdot d  \vec a - \int_{V'}\vec E \cdot (\vec \nabla V) \ dV' \right) $$
E também como $\vec E = - \vec \nabla V$:
$$W = \dfrac{1}{2}  \epsilon_0 \left( \oint_{S'} (\vec E \ V) \cdot d  \vec a - \int_{V'}\vec E \cdot (-\vec E) \ dV' \right) $$
$$W = \dfrac{1}{2}  \epsilon_0 \left( \oint_{S'} (\vec E \ V) \cdot d  \vec a + \int_{V'} E^2  \ dV' \right) $$
Assim temos a relação do trabalho com o Campo Elétrico.

Considerando uma distância muito grande da distribuição de cargas, grande o suficiente para podermos considerar toda a distribuição como uma carga pontual, temos que:
$$V \simeq \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{r},\ \ \ \ \ \ \ \ \ \vec E \simeq \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{r^2} \ \hat r $$

Podemos então analisar isoladamente a parte que depende do Potencial Elétrico:

$$\oint_{S'} (\vec E \ V) \cdot d  \vec a = \oint_{S'}  \left( \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{r^2} \ \hat r \ \ \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{r} \right) \cdot d  \vec a $$
$$\oint_{S'} (\vec E \ V) \cdot d  \vec a = \dfrac{Q^2}{(4 \pi \epsilon_0)^2} \oint_{S'}  \left(  \dfrac{1}{r^3} \ \hat r \right) \cdot d  \vec a $$
Sedo $d \vec a = r^2 \ sin \theta \ d \theta \ d \varphi \ \hat r$ em Coordenadas Esféricas:
$$\oint_{S'} (\vec E \ V) \cdot d  \vec a = \dfrac{Q^2}{(4 \pi \epsilon_0)^2} \oint_{S'}  \left(  \dfrac{1}{r^3} \ \hat r \right) \cdot (r^2 \ sin \theta \ d \theta \ d \varphi \ \hat r)$$
$$\oint_{S'} (\vec E \ V) \cdot d  \vec a = \dfrac{Q^2}{(4 \pi \epsilon_0)^2} \oint_{S'}  \left(  \dfrac{1}{r}  \right) \cdot (sin \theta \ d \theta \ d \varphi)$$
$$\oint_{S'} (\vec E \ V) \cdot d  \vec a = \dfrac{1}{(4 \pi \epsilon_0)^2} \dfrac{Q^2}{r}\oint_{S'}  sin \theta \ d \theta \ d \varphi$$
$$\oint_{S'} (\vec E \ V) \cdot d  \vec a = \dfrac{1}{(4 \pi \epsilon_0)^2} \dfrac{Q^2}{r} \int_0^{2\pi} d \varphi \int_0^{\pi} sin \theta \ d \theta$$
$$\oint_{S'} (\vec E \ V) \cdot d  \vec a = \dfrac{1}{(4 \pi \epsilon_0)^2} \dfrac{Q^2}{r} [2 \pi] [cos \theta]^0_{\pi}$$
$$\oint_{S'} (\vec E \ V) \cdot d  \vec a = \dfrac{1}{(4 \pi \epsilon_0)^2} \dfrac{Q^2}{r} [2 \pi] [1 - (-1)]$$
$$\oint_{S'} (\vec E \ V) \cdot d  \vec a = \dfrac{4 \pi}{(4 \pi \epsilon_0)^2} \dfrac{Q^2}{r}$$
$$\oint_{S'} (\vec E \ V) \cdot d  \vec a = \dfrac{1}{4 \pi (\epsilon_0)^2} \dfrac{Q^2}{r}$$
Como a distância considerada é muito grande, $\vec r \rightarrow \infty$, logo $\frac{1}{r} \rightarrow 0$, então $\oint_{S'} (\vec E \ V) \rightarrow 0$.

Temos então, nesta condição:

$$W = \dfrac{1}{2}  \epsilon_0 \left( \oint_{S'} (\vec E \ V) \cdot d  \vec a + \int_{V'} E^2  \ dV' \right) $$
$$W = \dfrac{1}{2}  \epsilon_0 \left( 0 + \int_{V'} E^2  \ dV' \right) $$
$$W = \dfrac{  \epsilon_0 }{2}\int_{V'} E^2  \ dV'$$
Temos então a Densidade de Energia do Campo Elétrico, Energia do Campo Elétrico por unidade de volume:
$$\rho_E = \dfrac{  \epsilon_0 }{2} E^2$$
$$W = \int_{V'} \rho_E  \ dV'$$

Novamente considerando uma distância muito grande da densidade de carga, podendo então considerá-la como uma carga pontual:
$$W = \dfrac{  \epsilon_0 }{2}\int_{V'} E^2  \ dV' = \dfrac{  \epsilon_0 }{2} \int_{V'}\dfrac{1}{(4 \pi\epsilon_0)^2} \dfrac{Q^2}{r^4}  \ dV'$$
$$W = \dfrac{\epsilon_0}{2} \int_{V'}\dfrac{1}{(4 \pi\epsilon_0)^2} \dfrac{Q^2}{r^4}  \ (r^2 \ sin \theta \ d \theta \ d \varphi \ dr)$$
$$W = \dfrac{\epsilon_0}{2} \dfrac{Q^2}{(4 \pi\epsilon_0)^2} \int_{V'}\dfrac{1}{r^2}  \ (\ sin \theta \ d \theta \ d \varphi \ dr)$$
$$W = \dfrac{\epsilon_0}{2} \dfrac{Q^2}{(4 \pi\epsilon_0)^2} \int_0^{2 \pi}d \varphi \int_0^\pi sin \theta \ d \theta \int_a^b  \dfrac{1}{r^2} dr$$
$$W = \dfrac{\epsilon_0}{2} \dfrac{Q^2}{(4 \pi\epsilon_0)^2} [4 \pi] \left[ \dfrac{1}{r}\right]_b^a$$
$$W = \dfrac{Q^2}{8 \pi \epsilon_0} \left[ \dfrac{1}{a} - \dfrac{1}{b} \right]$$
Para todo o espaço, muito distante da distribuição de cargas $b \rightarrow \infty$, $\frac{1}{b} \rightarrow 0$, logo:
$$W = \dfrac{Q^2}{8 \pi \epsilon_0}  \dfrac{1}{a}$$
Por outro lado, não podemos calcular no ponto na origem da carga, pois quando $a \rightarrow 0$,$\frac{1}{a} \rightarrow \infty$, logo a Energia $W \rightarrow \infty$.

**Exemplo**: Energia de uma Casca Esférica carregada de raio $R$ e carga total $Q$.

Podemos calcular a Energia acumulada:

$$W = \dfrac{1}{2} \int_S \sigma \ V\ da $$
$$W = \dfrac{1}{2} \int_S \dfrac{Q}{4 \pi R^2}  \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{R}da $$
$$W = \dfrac{1}{2} \dfrac{Q^2}{4 \pi R^3}\dfrac{1}{4 \pi \epsilon_0} \int_S da $$
$$W = \dfrac{1}{2} \dfrac{Q^2}{4 \pi R^3}\dfrac{1}{4 \pi \epsilon_0} [4 \pi \ R^2] $$
$$W = \dfrac{1}{8 \pi \epsilon_0}\dfrac{Q^2}{R} $$

Podemos também analisar o Campo Elétrico gerado ela distribuição de cargas:
$$W = \dfrac{  \epsilon_0 }{2}\int_{V'} E^2  \ dV'$$
Pela lei de Gauss sabemos que o Campo Elétrico é nulo dentro da Casca Esférica, mas não fora dela:
$$\left\{
\begin{array}{l}
E(r > R) = \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{r^2}\\
E(r < R) = 0
\end{array}
\right.$$
Logo:
$$W = \dfrac{  \epsilon_0 }{2}\int_{V'} (\dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{r^2})^2  \ dV'$$
$$W = \dfrac{  \epsilon_0 }{2} \dfrac{Q^2}{(4 \pi \epsilon_0)^2} \int_{V'} \dfrac{1}{r^4} \ dV'$$
$$W = \dfrac{  \epsilon_0 }{2} \dfrac{Q^2}{(4 \pi \epsilon_0)^2} \int_{V'} \dfrac{1}{r^4} \ (r^2 \ sin \theta \ d \theta \ d \varphi \ dr)$$
$$W = \dfrac{  \epsilon_0 }{2} \dfrac{Q^2}{(4 \pi \epsilon_0)^2} \int_0^{2 \pi}d \varphi \int_0^\pi sin \theta \ d \theta \int_R^\infty \dfrac{1}{r^2} dr$$
$$W = \dfrac{ 1 }{2} \dfrac{Q^2}{4 \pi \epsilon_0}  \left[  \dfrac{1}{r} \right]^R_\infty$$
$$W = \dfrac{Q^2}{8 \pi \epsilon_0} \left[ \dfrac{1}{R} - \dfrac{1}{\infty} \right]$$
$$W = \dfrac{Q^2}{8 \pi \epsilon_0} \left[ \dfrac{1}{R} - 0 \right]$$
$$W = \dfrac{1}{8 \pi \epsilon_0}  \dfrac{Q^2}{R}$$
