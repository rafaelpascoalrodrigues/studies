## Campo Elétrico

**Exemplo**: Calcular o campo elétrico gerado por uma barra carregada:

![[Pasted image 20221005203730.png]]

Temos que:

$dq = \lambda \ dx$
$\lambda = \dfrac{Q}{L}$

$\vec r = h \ \hat \jmath$
$\vec r' = x \ \hat \imath$
$\vec r_p = \vec r - \vec r' = - x \ \hat \imath + h \ \hat \jmath$ 

Analisando o infinitesimal do Campo Elétrico em suas componentes:

$$d \vec E = dE_x \ \hat \imath + dE_y \ \hat \jmath$$
$$d \vec E = dE \ cos \theta \ \hat \imath + dE \ sin \theta \ \hat \jmath$$
$$d \vec E = dE \ ( cos \theta \ \hat \imath + \ sin \theta \ \hat \jmath)$$
$$d \vec E = \dfrac{1}{4 \pi \epsilon_0} \dfrac{dq}{(\vec r_p)^2}  \ ( cos \theta \ \hat \imath + \ sin \theta \ \hat \jmath) = \dfrac{1}{4 \pi \epsilon_0} \dfrac{\lambda \ dx}{(\vec r_p)^2}  \ ( cos \theta \ \hat \imath + \ sin \theta \ \hat \jmath)$$

$$\vec E = \int d \vec E \ \ \ \Longrightarrow \ \ \ \vec E(\vec r) = \int \dfrac{1}{4 \pi \epsilon_0} \dfrac{\lambda \ dx}{(\vec r_p)^2}  \ ( cos \theta \ \hat \imath + \ sin \theta \ \hat \jmath)$$

$$\vec E(\vec r) = \dfrac{\lambda}{4 \pi \epsilon_0} \int_{-\frac{L}{2}}^{\frac{L}{2}} \dfrac{dx}{(\vec r_p)^2}  \ ( cos \theta \ \hat \imath + \ sin \theta \ \hat \jmath)$$
$$\vec E(\vec r) = \dfrac{\lambda}{4 \pi \epsilon_0} \left( \int_{-\frac{L}{2}}^{\frac{L}{2}} \dfrac{cos \theta}{(\vec r_p)^2} dx \ \hat \imath + \int_{-\frac{L}{2}}^{\frac{L}{2}} \ \dfrac{sin \theta}{(\vec r_p)^2} dx \ \hat \jmath \right)$$

![[Pasted image 20221011155231.png]]
$$r_p = \sqrt{x^2 + h ^2}, \ \ \ \ cos \theta = \dfrac{-x}{r_p} = \dfrac{-x}{\sqrt{x^2 + h ^2}}, \ \ \ \ \ sin \theta = \dfrac{h}{r_p} = \dfrac{h}{\sqrt{x^2 + h ^2}}$$
Note que $x$ é negativo, pois pelo diagrama anterior $x$ é negativo e $tetha$ positivo. 
$$\vec E(\vec r) = \dfrac{\lambda}{4 \pi \epsilon_0} \left( \int_{-\frac{L}{2}}^{\frac{L}{2}} \dfrac{cos \theta}{(\vec r_p)^2} dx \ \hat \imath + \int_{-\frac{L}{2}}^{\frac{L}{2}} \ \dfrac{sin \theta}{(\vec r_p)^2} dx \ \hat \jmath \right)$$
$$\vec E(\vec r) = \dfrac{\lambda}{4 \pi \epsilon_0} \left( \int_{-\frac{L}{2}}^{\frac{L}{2}} \dfrac{-x}{(\vec r_p)^3} dx \ \hat \imath + \int_{-\frac{L}{2}}^{\frac{L}{2}} \ \dfrac{h}{(\vec r_p)^3} dx \ \hat \jmath \right)$$
$$\vec E(\vec r) = \dfrac{\lambda}{4 \pi \epsilon_0} \left( \int_{-\frac{L}{2}}^{\frac{L}{2}} \dfrac{-x}{(x^2 + h^2)^\frac{3}{2}} dx \ \hat \imath + \int_{-\frac{L}{2}}^{\frac{L}{2}} \ \dfrac{h}{(x^2 + h^2)^\frac{3}{2}} dx \ \hat \jmath \right)$$
Notamos que $f(x) = -\dfrac{x}{(x^2 + h^2)^\frac{3}{2}}$ é uma função ímpar, e uma função ímpar integrada em um intervalo simétrico é igual a $0$.

Notamos também que $f(x) = \dfrac{h}{(x^2 + h^2)^\frac{3}{2}}$ é uma função par, uma função par integrada em um intervalo simétrico é igual ao dobro da integral da função par de $0$ até o intervalo final.

Temos então:
$$\vec E(\vec r) = \dfrac{\lambda}{4 \pi \epsilon_0} \left( 0+ 2\int_{0}^{\frac{L}{2}} \ \dfrac{h}{(x^2 + h^2)^\frac{3}{2}} dx \ \hat \jmath \right) = \dfrac{\lambda \ h}{2 \pi \epsilon_0} \int_{0}^{\frac{L}{2}} \ \dfrac{1}{(x^2 + h^2)^\frac{3}{2}} dx \ \hat \jmath $$
$$\vec E(\vec r) = \dfrac{\lambda \ h}{2 \pi \epsilon_0} \int_{0}^{\frac{L}{2}} \ \dfrac{1}{(\frac{h^2}{h^2}(x^2 + h^2))^\frac{3}{2}} dx \ \hat \jmath $$
$$\vec E(\vec r) = \dfrac{\lambda \ h}{2 \pi \epsilon_0} \int_{0}^{\frac{L}{2}} \ \dfrac{1}{(h^2(\frac{x^2}{h^2} + 1))^\frac{3}{2}} dx \ \hat \jmath $$
$$\vec E(\vec r) = \dfrac{\lambda \ h}{2 \pi \epsilon_0} \int_{0}^{\frac{L}{2}} \ \dfrac{1}{h^3(\frac{x^2}{h^2} + 1)^\frac{3}{2}} dx \ \hat \jmath $$
$$\vec E(\vec r) = \dfrac{\lambda}{2 \pi \epsilon_0 \ h^2} \int_{0}^{\frac{L}{2}} \ \dfrac{1}{(\frac{x^2}{h^2} + 1)^\frac{3}{2}} dx \ \hat \jmath $$
Se fizermos $u = \dfrac{x}{h}$, $du = \dfrac{1}{h} dx$, $u(0) = \dfrac{0}{h}=0$ e $u(\frac{L}{2}) = \dfrac{\frac{L}{2}}{h}=\dfrac{L}{2h}$:
$$\vec E(\vec r) = \dfrac{\lambda}{2 \pi \epsilon_0 \ h^2} \int_{0}^{\frac{L}{h2}} \ \dfrac{1}{(u^2 + 1)^\frac{3}{2}} \ h \  du \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{\lambda}{2 \pi \epsilon_0 \ h} \int_{0}^{\frac{L}{h2}} \ \dfrac{1}{(u^2 + 1)^\frac{3}{2}} \  du \ \hat \jmath$$
Se $u = tan \alpha$, $du = \dfrac{du}{d \alpha} d \alpha = sec^2 \alpha \ d \alpha = (tan^2 \alpha +1) \ d \alpha$,

Quando $u = 0 = tan \alpha$ quando $\alpha = 0$ e $u = \dfrac{L}{2h} = tan \alpha$ quando $alpha = tan^{-1} (\frac{L}{2h})$.

Logo:
$$\vec E(\vec r) = \dfrac{\lambda}{2 \pi \epsilon_0 \ h} \int_{0}^{\frac{L}{h2}} \ \dfrac{1}{(u^2 + 1)^\frac{3}{2}} \  du \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{\lambda}{2 \pi \epsilon_0 \ h} \int_{0}^{tan^{-1} (\frac{L}{2h})} \ \dfrac{(tan^2 \alpha + 1)}{(tan^2 \alpha + 1)^\frac{3}{2}} \  d \alpha \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{\lambda}{2 \pi \epsilon_0 \ h} \int_{0}^{tan^{-1} (\frac{L}{2h})} \ \dfrac{1}{(tan^2 \alpha + 1)^\frac{1}{2}} \  d \alpha \ \hat \jmath$$
Sendo $tan^2 \alpha + 1 = \dfrac{sin^2 \alpha}{cos^2 \alpha} + 1 = \dfrac{sin^2 \alpha}{cos^2 \alpha} + \dfrac{cos^2 \alpha}{cos^2 \alpha} = \dfrac{sin^2 \alpha + cos^2 \alpha}{cos^2 \alpha} = \dfrac{1}{cos^2 \alpha}$ 
$$\vec E(\vec r) = \dfrac{\lambda}{2 \pi \epsilon_0 \ h} \int_{0}^{tan^{-1} (\frac{L}{2h})} \ \dfrac{1}{(\frac{1}{cos^2 \alpha})^\frac{1}{2}} \  d \alpha \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{\lambda}{2 \pi \epsilon_0 \ h} \int_{0}^{tan^{-1} (\frac{L}{2h})} \ cos \alpha \  d \alpha \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{\lambda}{2 \pi \epsilon_0 \ h}  \ \left [sin \alpha \right]_0^{tan^{-1} (\frac{L}{2h})} \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{\lambda}{2 \pi \epsilon_0 \ h}  \ sin \left( tan^{-1} \left( \frac{L}{2h} \right) \right) \ \hat \jmath$$

Como $sin (tan^{-1} \alpha) = \dfrac{\alpha}{\sqrt{\alpha^2 + 1}}$, então:
$$\vec E(\vec r) = \dfrac{\lambda}{2 \pi \epsilon_0 \ h}  \ \dfrac{\frac{L}{2h}}{\sqrt{(\frac{L}{2h})^2 + 1}} \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{\lambda \ L}{4 \pi \epsilon_0 \ h}  \ \dfrac{1}{h\sqrt{(\frac{L}{2h})^2 + 1}} \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{\lambda \ L}{4 \pi \epsilon_0 \ h}  \ \dfrac{1}{\sqrt{(\frac{L}{2})^2 + h^2}} \ \hat \jmath$$
Como $\lambda = \frac{Q}{L}$: 
$$\vec E(\vec r) = \dfrac{Q}{4 \pi \epsilon_0} \dfrac{1}{h}  \ \dfrac{1}{((\frac{L}{2})^2 + h^2)^{\frac{1}{2}}} \ \hat \jmath$$

Com isso, quando $h >> L$, podemos considerar que a barra está tão distante do ponto que ela pode ser considerada uma carga pontual.

Podemos fazer:
$$\vec E(\vec r) = \dfrac{Q}{4 \pi \epsilon_0} \dfrac{1}{h}  \ \dfrac{1}{((\frac{L}{2})^2 + h^2)^{\frac{1}{2}}} \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{Q}{4 \pi \epsilon_0} \dfrac{1}{h}  \ \dfrac{1}{h((\frac{L}{2h})^2 + 1)^{\frac{1}{2}}} \ \hat \jmath$$
Como $h >> L$, $\frac{L}{2h} \longrightarrow 0$ :
$$\vec E(\vec r) = \dfrac{Q}{4 \pi \epsilon_0} \dfrac{1}{h}  \ \dfrac{1}{h(0^2 + 1)^{\frac{1}{2}}} \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{Q}{4 \pi \epsilon_0} \dfrac{1}{h^2} \ \hat \jmath$$
Logo, realmente atua como uma carga pontual.

No caso de  $h << L$, o ponto está tão próximo que é como se a barra fosse infinita.

Logo:
$$\vec E(\vec r) = \dfrac{Q}{4 \pi \epsilon_0} \dfrac{1}{h}  \ \dfrac{1}{((\frac{L}{2})^2 + h^2)^{\frac{1}{2}}} \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{Q}{4 \pi \epsilon_0} \dfrac{1}{h}  \ \dfrac{1}{\frac{L}{2}(1 + (\frac{2h}{L})^2)^{\frac{1}{2}}} \ \hat \jmath$$
Neste caso de $h << L$, $\frac{2h}{L} \longrightarrow 0$:
$$\vec E(\vec r) = \dfrac{Q}{4 \pi \epsilon_0} \dfrac{1}{h}  \ \dfrac{2}{L} \dfrac{1}{(1 + 0^2)^{\frac{1}{2}}} \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{Q}{4 \pi \epsilon_0} \dfrac{1}{h}  \ \dfrac{2}{L} \ \hat \jmath$$
Como $\lambda = \frac{Q}{L}$:
$$\vec E(\vec r) = \dfrac{\lambda L}{4 \pi \epsilon_0} \dfrac{1}{h}  \ \dfrac{2}{L} \ \hat \jmath$$
$$\vec E(\vec r) = \dfrac{1}{4 \pi \epsilon_0} \dfrac{2 \ \lambda}{h} \ \hat \jmath$$
  Em coordenadas cilíndricas:
  
![[Pasted image 20221012181746.png]]
$$\vec E(\vec r) = \dfrac{1}{4 \pi \epsilon_0} \dfrac{2 \ \lambda}{r} \ \hat r$$


# Divergente do Campo Elétrico

Com o campo elétrico gerado por uma carga pontual:
$$\vec E(\vec r) = \dfrac{1}{4 \pi \epsilon_0} \dfrac{q}{r^2} \ \hat r$$
Verificamos o Campo Elétrico gerado por esta carga pontual sobre uma superfície esférica $S$ de raio $R$:

 ![[Pasted image 20221012190657.png]]
 
Pela Lei de Gauss:
  $$\oint_S \vec E \cdot d \vec a = \dfrac{q}{4 \pi \epsilon_0} \oint_S \dfrac{\hat r}{r^2} \ d \vec a, \ \ \ \ \ d \vec a = r^2 sin \theta \ d \theta \ d \varphi \ \hat r$$
$$\dfrac{q}{4 \pi \epsilon_0} \oint_S \dfrac{\hat r}{r^2} \  r^2 \ sin \theta \ d \theta \ d \varphi \ \hat r$$
$$ \dfrac{q}{4 \pi \epsilon_0} \int_0^{2 \pi} d \varphi \int_0^\pi  sin \theta \ d \theta $$
$$ \dfrac{q}{4 \pi \epsilon_0} [2 \pi]  [ cos \theta ]_\pi^0 $$
$$ \dfrac{q}{4 \pi \epsilon_0} [2 \pi]  [ cos 0 - cos \pi ]_\pi^0 $$
$$ \dfrac{q}{2 \epsilon_0}  [ 1 - (-1) ] \ \hat r = \dfrac{q}{\epsilon_0} $$
Logo, $\oint_S \vec E \cdot d \vec a = \dfrac{q}{\epsilon_0}$ não depende do raio da esfera, então não depende da superfície ser uma esfera, sendo a formulação válida para qualquer forma.

Temos então que o Fluxo do Campo elétrico não depende do formato da superfície fechada, apenas da carga.
  $$\Phi_E = \oint_S \vec E \cdot d \vec a = \dfrac{q}{\epsilon_0}  $$
  Para múltiplas cargas, o mesmo é válido e sendo o Campo Elétrico aditivo, a carga total será a soma das cargas, independente da sua posição dentro da superfície.
  $$ \vec E = \sum_{i=1}^n \vec E_i, \ \ \ \ \ \Phi_E = \oint_S \vec E \cdot d \vec a = \oint_S \left( \sum_{i=1}^n \vec E_i \right) \cdot d \vec a = \dfrac{1}{\epsilon_0} \sum_{i=1}^n q_i$$

Pelo Teorema e Gauss, a integral sobre uma superfície fechada de uma função vetorial é igual à integral sobre o volume contido nesta superfície do divergente desta mesma função vetorial.
$$\oint_S \vec f \cdot d \vec a = \int_V(\vec \nabla \cdot \vec f) \ dV$$
Logo:
$$\oint_S \vec E \cdot d \vec a = \int_V(\vec \nabla \cdot \vec E) \ dV$$
$$\dfrac{Q}{\epsilon_0} = \int_V(\vec \nabla \cdot \vec E) \ dV$$
Se $Q$ for uma distribuição contínua de carga, então $Q = \int_V \rho \ dV$, então:
$$\int_V\dfrac{\rho}{\epsilon_0} \ dV = \int_V(\vec \nabla \cdot \vec E) \ dV$$
Deste modo, como sabemos que a formulação é válida para qualquer superfície, ela também é valida para o volume contido em qualquer superfície, então temos que:
$$\vec \nabla \cdot \vec E = \dfrac{\rho}{\epsilon_0} \ \ \ \ \ \ \ \ \ \ \text{Lei de Gauss na forma Diferencial}$$

Para uma distribuição qualquer de carga $\rho$ sobre um volume $V'$:
$$\vec \nabla \cdot \vec E = \vec \nabla \cdot \left( \int_{V'} \dfrac{1}{4 \pi \epsilon_0} \dfrac{\hat r_p}{(r_p)^2} \rho(\vec r') \ dV'\right) = \dfrac{1}{4 \pi \epsilon_0}  \int_{V'} \vec \nabla \cdot \left( \dfrac{\hat r_p}{(r_p)^2} \right) \rho(\vec r') \ dV' $$

Tendo o Divergente em coordenadas esféricas:
$$\vec \nabla \cdot \vec f = \dfrac{1}{r^2} \dfrac{\partial}{\partial r}(r^2 \ f_r) + \dfrac{1}{r \ sin \theta} \dfrac{\partial}{\partial \theta} (sin \theta \ f_\theta) + \dfrac{1}{r \ sin \theta} \dfrac{\partial}{\partial \varphi} f_\varphi $$
Sendo que $\vec \nabla \cdot \left( \dfrac{\hat r}{r^2} \right)$ possui componente apenas na direção radial ($\hat r$) temos então:
$$\vec \nabla \cdot \left( \dfrac{\hat r}{r^2} \right) = \dfrac{1}{r^2} \dfrac{\partial}{\partial r}\left(r^2 \ \dfrac{1}{r^2}\right) = \dfrac{1}{r^2} \dfrac{\partial}{\partial r}\left(1\right) = 0$$
Aplicando o Teorema de Gauss neste resultado:
$$\oint_S \left( \dfrac{\hat r}{r^2} \right) \cdot d \vec a = \int_V \left(\vec \nabla \cdot \left( \dfrac{\hat r}{r^2} \right) \right) \ dV$$
Analisando a integral de superfície:
$$\oint_S \left( \dfrac{\hat r}{r^2} \right) (r^2 \ sin \theta \ d \theta \ d \varphi \ \hat r)$$
$$\oint_S sin \theta \ d \theta \ d \varphi = \int_0^{2 \pi} d \varphi \ \int_0^\pi sin \theta \ d \theta = 2\pi \cdot 2 = 4 \pi$$
Logo:
$$\oint_S \left( \dfrac{\hat r}{r^2} \right) \cdot d \vec a = \int_V \left(\vec \nabla \cdot \left( \dfrac{\hat r}{r^2} \right) \right) \ dV$$
$$ 4 \pi = \int_V \left(0 \right) \ dV$$
Pelo Teorema de Gauss era esperado então que $\int_V \left(\vec \nabla \cdot \left( \dfrac{\hat r}{r^2} \right) \right) \ dV = 4 \pi$ mas como  $\vec \nabla \cdot \left( \dfrac{\hat r}{r^2} \right) = 0$ isso parece impossível, mas isso se deve ao fato de que $\vec \nabla \cdot \left( \dfrac{\hat r}{r^2} \right)$ não incluir a origem, pois  $\dfrac{\hat r}{r^2}$ não está definido quando $r = 0$.


Para resolver esta questão, utilizamos o **Delta de Dirac** onde:
$$\delta(x) = \left\{ 
\begin{array}{ll}
0 & x \neq 0 \\
\infty & x = 0
\end{array}
\right.
\ \ \ \ \ \text{tal que:} \int_{- \infty}^{+\infty} \delta(x) 
 \ dx = 1$$
Logo, se tivermos $\delta(x - x_0)$, o resultado será $\infty$ se $x = x_0$ e $0$ quando $x \neq x_0$, então temos que $f(x) \delta (x)$ será $0$ para qualquer ponto exceto em $x=0$, nos possibilitando analisar a origem.

O $\delta (x)$ é válido para uma única dimensão. Para representar em três dimensões fazemos $\delta^3(\vec r)$.
$$\delta^3(\vec r) = \delta(x)\delta(y)\delta(z) = \int_{- \infty}^{+\infty} \int_{- \infty}^{+\infty} \int_{- \infty}^{+\infty} \delta(x) \delta(y) \delta(z) 
 \ dx \ dy \ dz = 1 $$
 
Tendo que:
$$ \vec \nabla \cdot \left( \dfrac{\hat r}{r^2} \right) = 4 \pi \ \delta^3(\vec r) $$
Logo:
$$ \int_V \vec \nabla \cdot \left( \dfrac{\hat r}{r^2} \right) \ dV = \int_V (4 \pi \ \delta^3(\vec r) ) \ dV = 4 \pi \int_V  \ \delta^3(\vec r) \ dV = 4 \pi \ (1) = 4 \pi$$
Temos agora que:
$$\oint_S \left( \dfrac{\hat r}{r^2} \right) \cdot d \vec a = \int_V \left(\vec \nabla \cdot \left( \dfrac{\hat r}{r^2} \right) \right) \ dV$$
$$\oint_S \left( \dfrac{\hat r}{r^2} \right) \cdot d \vec a = \int_V (4 \pi \ \delta^3(\vec r) ) \ dV$$
$$4 \pi = 4 \pi$$
Logo, para o campo elétrico:

$$\vec \nabla \cdot \vec E(\vec r) =  \dfrac{1}{4 \pi \epsilon_0} \int_{V'} (4 \pi \delta^3(\vec r - \vec r')) \ \rho(\vec r') \ 
dV'$$
Podemos então resolver p  ara quando $\vec r' = \vec r$, sendo:
$$\vec \nabla \cdot \vec E(\vec r) = \dfrac{1}{4 \pi \epsilon_0} 4 \pi \ \rho(\vec r) = \dfrac{\rho(\vec r)}{\epsilon_0}$$

**Exemplo**: Campo Elétrico de uma casca esférica carregada de raio $R$ em um ponto $P$ externo à esfera.

![[Pasted image 20221013144028.png]]

$$\oint \vec E \cdot d \vec a = \dfrac{Q}{\epsilon_0}$$
Como o Campo Elétrico tem a mesma direção de $\vec r$, então $\vec E \cdot d \vec a = E \ da$:
$$\oint \vec E \cdot d \vec a = \oint E \ da = E \ a = E \ (4 \pi \ r^2)$$
Logo:
$$\oint \vec E \cdot d \vec a = \dfrac{Q}{\epsilon_0}$$
$$E \ (4 \pi \ r^2) = \dfrac{Q}{\epsilon_0}$$
$$E = \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{r^2}$$

No interior da Casca Esférica $Q = 0$, logo $E = \dfrac{1}{4 \pi \epsilon_0} \dfrac{0}{r^2} = 0$.

Na superfície da Casta Esférica $r = R$ e como $Q = \sigma \ A =  4 \pi \ \sigma \ R^2$, logo:

$$E = \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{r^2} = \dfrac{1}{4 \pi \epsilon_0} \dfrac{4 \pi \ \sigma \ R^2}{R^2} = \dfrac{\sigma}{\epsilon_0}$$




