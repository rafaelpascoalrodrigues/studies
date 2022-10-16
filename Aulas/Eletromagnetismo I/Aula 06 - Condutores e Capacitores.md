# Condutores

Na Eletrostática, os materiais são divididos, a grosso modo, em dois tipos:

- **Isolantes**: as cargas não se movimentam no material
- **Condutores**: as cargas no material possuem liberdade para se movimentar

## Propriedades dos Condutores


**1.** Dentro de um condutor, em um estado estacionário, temos $\vec E = 0$.

Nesta situação $\vec F = q \vec E = 0$, logo não há Força atuando sobre as cargas, logo elas estão em estado estacionário.

**2.** Deste modo, $\rho = 0$ dentro do condutor, pois:
$$\oint \vec E \cdot d \vec a = \dfrac{\rho}{\epsilon_0}, \ \ \ \ \ \vec E = 0 \longrightarrow \rho = 0 $$

**3.** Assim cargas livres estarão na superfície do condutor, de modo que o Campo Elétrico dentro do condutor seja igual a $0$ devido ao Campos Elétricos gerados pelas cargas se anulem dentro do material.


Energia da distribuição volumétrica de cargas em uma Esfera:

$$W_V = \dfrac{1}{2} \int_{V'} V(\vec r) \ \rho (\vec r) \ dV'$$
Para dentro da Esfera, temos:
$$V(\vec r) = \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{2R}\left( 3 -\dfrac{r^2}{R^2} \right)$$
$$\rho = \dfrac{Q}{V} = \dfrac{3Q}{4 \pi R^3}$$
Logo:
$$W_V = \dfrac{1}{2} \int_{V'} V(\vec r) \ \rho (\vec r) \ dV'$$
$$W_V = \dfrac{1}{2} \int_{V'} \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{2R}\left( 3 -\dfrac{r^2}{R^2} \right) \ \dfrac{3Q}{4 \pi R^3} \ (r^2 \ sin \theta \ d \theta \ d \varphi \ dr)$$
$$W_V = \dfrac{1}{2} \dfrac{1}{4 \pi \epsilon_0} \dfrac{3Q}{4 \pi R^3} \dfrac{Q}{2R} \int_0^{2 \pi} d \varphi \int_0^{pi} sin \theta \ d \theta \int_0^{R} \left( 3 -\dfrac{r^2}{R^2} \right) \ r^2 \ dr$$
$$W_V = \dfrac{1}{2} \dfrac{1}{4 \pi \epsilon_0} \dfrac{3Q^2}{8 \pi R^4}  [4 \pi] \int_0^{R} \left( 3 -\dfrac{r^2}{R^2} \right) \  \ dr$$
$$W_V = \dfrac{1}{4 \pi \epsilon_0} \dfrac{3Q^2}{4 R^4}   \int_0^{R} \left( 3r^2 -\dfrac{r^4}{R^2} \right) \ dr$$
$$W_V = \dfrac{1}{4 \pi \epsilon_0} \dfrac{3Q^2}{4 R^4} \left( \left[ r^3  \right]_0^{R} + \left[\dfrac{1}{5R^2} r^5 \right]^0_{R} \right)$$
$$W_V = \dfrac{1}{4 \pi \epsilon_0} \dfrac{3Q^2}{4 R^4} \left(  R^3   - \dfrac{R^5}{5R^2}   \right)$$
$$W_V = \dfrac{1}{4 \pi \epsilon_0} \dfrac{3Q^2}{4 R^4} \left(  \dfrac{5R^3}{5}   - \dfrac{R^3}{5}   \right)$$
$$W_V = \dfrac{1}{4 \pi \epsilon_0} \dfrac{3Q^2}{4 R^4}   \dfrac{4R^3}{5}$$
$$W_V = \dfrac{1}{4 \pi \epsilon_0} \dfrac{3Q^2}{R}   \dfrac{1}{5}$$
$$W_V = \dfrac{3}{20 \pi}\dfrac{Q^2}{R \epsilon_0} $$

Sabemos que a distribuição de cargas em uma Casca Esférica é: 
$$W = \dfrac{1}{8 \pi \epsilon_0}\dfrac{Q^2}{R} $$
Que é similar a dizermos que toda a distribuição de cargas dentro de uma esfera está localizada em sua superfície, logo:
$$W_S = \dfrac{1}{8 \pi \epsilon_0}\dfrac{Q^2}{R} $$

Temos então:
$$\dfrac{W_V}{W_S} = \dfrac{\dfrac{3}{20 \pi}\dfrac{Q^2}{R \epsilon_0}}{\dfrac{1}{8 \pi \epsilon_0}\dfrac{Q^2}{R}} = \dfrac{\dfrac{3}{20}}{\dfrac{1}{8}}=\dfrac{24}{20} = \dfrac{6}{5} = 1,2$$
$$W_v = 1.2 \ W_S$$
Logo, a configuração de menor energia será aquela com as cargas na superfície.


**4.** No interior do condutor o Potencial Elétrico é constante.

Como dentro do condutor $\vec E = 0$, $\vec E = -\vec \nabla V \Rightarrow 0 = -\vec \nabla V  \Rightarrow V \text{ é constante}$ (equipotencial).


**5.** Imediatamente após a superfície do material condutor, o Campo Elétrico estará perpendicular à superfície.
$$\vec E \parallel \vec n \text{ : nas paredes exteriores ao material condutor}$$
$$\vec E \perp \vec n \text{ : implica movimento de cargas sobre a parede (estado não estacionário)}$$
 Logo, se o Campo Elétrico é perpendicular à direção normal à superfície for nulo, $\vec E_\perp = 0$, então todo o Campo Elétrico estará na direção normal à parede $\vec E = E \ \hat n$.  
 
## Cargas Induzidas

Ao expor um condutor neutro a um Campo Elétrico externo, a distribuição de cargas no condutor irá se organizar para anular o Campo Elétrico externo, formando um Campo Elétrico inverso.

Nesta situação existe uma Força atuando o condutor que cria esta distribuição induzida de cargas, esta Força atuando sobre o condutor gera a chamada **Pressão Eletrostática**. 

![[Pasted image 20221015194726.png]]

Um pequeno pedaço da superfície que onde temos uma carga $q$ está sujeito a uma Força  $F=q \ E$, logo, nesta pequena área da superfície temos uma Pressão Eletrostática de:
$$P = \dfrac{F}{A} = \dfrac{q}{A}\ E = \sigma E  $$
Contudo, o Campo Elétrico gerado por uma carga não exerce Força sobre ela mesma, logo a Força sobre ela é devido ao Campo Elétrico gerado por todas as outras cargas, e a disposição das cargas mais próximas fazem com que as componentes perpendiculares à normal da superfície se anule, sobrando apenas o componente paralelo à normal.

![[Pasted image 20221015200908.png]]

A carga, em uma pequena área, irá gerar um Campo Elétrico $\frac{\sigma}{2 \epsilon_0}$ acima e um Campo Elétrico abaixo igual, $\frac{\sigma}{2 \epsilon_0}$.

![[Pasted image 20221015205439.png]]

Sabendo que o Campo Elétrico dentro de um material condutor é igual a $0$ e que logo após superfície do material condutor o Campo Elétrico é igual a $\frac{\sigma}{\epsilon_0}$, logo o Campo Elétrico que irá exercer força sobre a carga é a diferença entre o Campo Elétrico na superfície e o gerado pela própria carga.

![[Pasted image 20221015205455.png]]

$$E = E_s - E_q = \dfrac{\sigma}{\epsilon_0} - \dfrac{2 \sigma}{\epsilon_0} = \dfrac{\sigma}{2\epsilon_0}$$
Logo, a Pressão Eletrostática será:
$$P = \sigma E = \sigma \dfrac{\sigma}{2\epsilon_0} = \dfrac{\sigma^2}{2\epsilon_0}$$
Como $E = \dfrac{\sigma}{\epsilon_0}$, $\sigma = E \ \epsilon_0$, então:
$$P = \dfrac{\sigma^2}{2\epsilon_0} = \dfrac{(E \ \epsilon_0)^2}{2\epsilon_0} = \dfrac{\epsilon_0}{2} \ E^2$$

## Potencial na Superfície de um Condutor

Sendo o Campo Elétrico imediatamente após superfície de um condutor é:
$$E = \frac{\sigma}{\epsilon_0}, \ \ \ \ \vec E = E \ \hat n = \frac{\sigma}{\epsilon_0} \ \hat n $$
$$\sigma \ \hat n = 
\vec E \ \epsilon_0, \ \ \ \ \ \ \vec E = - 
\vec \nabla V$$
$$\sigma \ \hat n = - (\vec \nabla V) \ \epsilon_0$$
$$\hat n \cdot \sigma \ \hat n = - \hat n \cdot (\vec \nabla V) \ \epsilon_0$$
$$\sigma = -\epsilon_0 \ \dfrac{\partial V}{\partial n} \ $$
Lembrando que a derivada parcial do Potencial acima da superfície na direção normal subtraindo da derivada parcial do Potencial abaixo da superfície na direção normal era:
$$\dfrac{\partial V_+}{\partial n} - \dfrac{\partial V_-}{\partial n} = - \dfrac{\sigma}{\epsilon_0}$$
Como de vimos que o Potencial dentro de uma superfície condutora é constante, então:
$$\dfrac{\partial V_- }{\partial n} = 0$$
Logo:
$$\dfrac{\partial V_+}{\partial n}  - \dfrac{\partial V_-}{\partial n} = - \dfrac{\sigma}{\epsilon_0}$$
$$\dfrac{\partial V_+}{\partial n} - 0 = - \dfrac{\sigma}{\epsilon_0}$$
$$\dfrac{\partial V_+}{\partial n} = - \dfrac{\sigma}{\epsilon_0}$$
$$\sigma = \epsilon_0 \ \dfrac{\partial V_+}{\partial n} $$
# Capacitores

A Capacitância é a relação entre a diferença de Potencial e as cargas no material.
$$\Delta V = V(b) - V(a) = - \int_a^b \vec E \cdot d \vec l$$
E também o Campo Elétrico é proporcional à distribuição de Cargas, assim como a diferença de Potencial também será proporcional à distribuição de Cargas.
$$
\vec E \propto Q \Longrightarrow \Delta V \propto Q$$
Logo, a capacitância será:
$$C \ \Delta V = Q \Longrightarrow C = \dfrac{|Q|}{|\Delta V|}$$
A capacitância é medita em Farad [F] e é sempre positiva.

**Exemplo**: Capacitor de Placas paralelas.

![[Pasted image 20221015215208.png]]

Temos que na região entre as placas temos a soma dos Campos, enquanto na parte de fora os campos se anulam.

Então, entre as placas temos:
$$E = \dfrac{\sigma}{2 \epsilon_0} +  \dfrac{\sigma}{2 \epsilon_0} =  \dfrac{\sigma}{\epsilon_0}$$
Sendo $\sigma = \dfrac{Q}{A}$:
$$E = \dfrac{\sigma}{\epsilon_0} = \dfrac{Q}{A \ \epsilon_0}$$
Logo, a diferença de Potencial será:
$$\Delta V =  - \int_0^d \vec E \cdot d \vec l = - \int_0^d \dfrac{Q}{A \ \epsilon_0} \ dl = - \dfrac{Q}{A \ \epsilon_0} d $$
Então:
$$C = \dfrac{|Q|}{|\Delta V|} = \dfrac{|Q|}{\left|- \dfrac{Q}{A \ \epsilon_0} d \right|} = \dfrac{A}{d} \epsilon_0$$
Logo a Capacitância não depende da quantidade de cargas, mas da área dos materiais condutores e da distância entre eles.

**Exemplo**: Duas Cascas Esféricas concêntricas.

![[Pasted image 20221015225236.png]]

Fazendo a casca interna de raio $a$ e com distribuição de cargas $Q_-$ e a casca externa de raio $b$ e com distribuição de cargas $Q_+$:

$$\vec E = \dfrac{1}{4 \pi \epsilon 0} \dfrac{Q}{r^2} \ \hat r$$
$$\Delta V = - \int_a^b \vec E \cdot d \vec l = - \int_a^b \dfrac{1}{4 \pi \epsilon 0} \dfrac{Q}{r^2} \ \hat r \cdot (dr \ \hat r)  $$
$$\Delta V = - \dfrac{Q}{4 \pi \epsilon 0} \int_a^b  \dfrac{1}{r^2} \  dr  = \dfrac{Q}{4 \pi \epsilon 0} \left [ \dfrac{1}{r} \right]_a^b = \dfrac{Q}{4 \pi \epsilon 0} \left [ \dfrac{1}{b} - \dfrac{1}{a}  \right] = \dfrac{Q}{4 \pi \epsilon 0} \left [ \dfrac{1}{b} - \dfrac{1}{a}  \right] $$
$$\Delta V = \dfrac{Q}{4 \pi \epsilon 0}  \dfrac{a-b}{ab} $$
Como $b > a$:
$$\left|\dfrac{Q}{4 \pi \epsilon 0}  \dfrac{a-b}{ab} \right| = \left(\dfrac{Q}{4 \pi \epsilon 0}  \dfrac{b-a}{ab} \right)$$
$$C = \dfrac{|Q|}{|\Delta V|} = \dfrac{|Q|}{\left|\dfrac{Q}{4 \pi \epsilon 0}  \dfrac{a-b}{ab} \right|} = \dfrac{4 \pi \epsilon 0 \ ab}{b-a }$$

Se fizermos $b \rightarrow \infty$, seria como se apenas existisse a casca esférica interna:

$$C = \dfrac{4 \pi \epsilon 0 \ ab}{b-a} = \dfrac{4 \pi \epsilon 0 \ ab}{b(1-\frac{a}{b})}=\dfrac{4 \pi \epsilon 0 \ a}{(1-\frac{a}{b})} = \dfrac{4 \pi \epsilon 0 \ a}{(1-\frac{a}{\infty})} =  4 \pi \epsilon 0 \ a =   4 \pi \epsilon 0 \ R$$

## Energia armazenada no Capacitor

$$W = q \ \Delta V$$
Onde $W$ é o trabalho para movimentar uma carga através de uma diferença de potencial $\Delta V$, sendo $\Delta V = \frac{q}{C}$.

Logo:
$$W = \int dW = \int_0^Q dq \ \Delta V \ = \int_0^Q dq \ \dfrac{q}{C}= \dfrac{1}{C} \int_0^Q q \ dq = \dfrac{1}{C} \left[ \dfrac{1}{2} q^2\right]_0^Q = \dfrac{1}{2} \dfrac{Q^2}{C} $$

Como $Q = C \ \Delta V$:
$$W = \dfrac{1}{2} \dfrac{Q^2}{C} = \dfrac{1}{2} \dfrac{(C \ \Delta V)^2}{C}= \dfrac{1}{2} C \ (\Delta V)^2$$