### Exemplos de Aplicações das Equações de Lagrange

**Exemplo**: Aplicar o formalismo lagrangiano para encontrar as equações de movimento em um pêndulo duplo.
![[Pasted image 20221001152657.png]]

Vínculos:
- $x_1^2 + y_1^2 = l_1^2$
- $(x_2 - x_1)^2 + (y_2 - y_1)^2 = l_2^2$

Graus de liberdade:
- $n = 4 \; \text{(coordenadas posicionais)} - 2 \; \text{(vínculo)} = 2$

*Arbitrariamente*, adotamos: $q_1 = \theta_1$ e $q_2 = \theta_1$.

Temos então que:
- $x_1 = l_1 sin \theta_1$,                           $\dot x_1 = l_1 \dot \theta_1 cos \theta_1$
- $y_1 = l_1 cos \theta_1$,                           $\dot y_1 = - l_1 \dot \theta_1 sin \theta_1$
- $x_2 = l_1 sin \theta_1 + l_2 sin \theta_2$,           $\dot x_2 = l_1 \dot \theta_1 cos \theta_1 - l_2 \dot \theta_2 cos \theta_2$
- $x_2 = l_1 cos \theta_1 + cos \theta_2$,              $\dot y_2 = -l_1 \dot \theta_1 sin \theta_1 + l_2 \dot \theta_2 sin \theta_2$

Analisado a Energia Cinética $T$ do sistema:

$$T = \dfrac{1}{2} m_1 (\dot x_1^2 + \dot y_1^2) + \dfrac{1}{2} m_2 (\dot x_2^2 + \dot y_2^2) $$
$$\begin{array}{ll}
T = & \dfrac{1}{2} m_1 (l_1^2 \dot \theta_1^2 cos^2 \theta_1 + l_1^2 \dot \theta_1^2 sin^2 \theta_1) + 
\dfrac{1}{2} m_2 (l_1^2 \dot \theta_1^2 cos^2 \theta_1 + l_2^2 \dot \theta_2^2 cos^2 \theta_2 +
\\
& + l_1^2 \dot \theta_1^2 sin^2 \theta_1 + l_2^2 \dot \theta_2^2 sin^2 \theta_2 + 2 l_1 l2 \dot \theta_1 \dot \theta_2 cos \theta_1 cos \theta_2 + 2 l_1 l2 \dot \theta_1 \dot \theta_2 sin \theta_1 sin \theta_2)
\end{array}$$
$$\begin{array}{ll}
T = & \dfrac{1}{2} m_1 (l_1^2 \dot \theta_1^2 (cos^2 \theta_1 + sin^2 \theta_1)) + 
\dfrac{1}{2} m_2 (l_1^2 \dot \theta_1^2 (cos^2 \theta_1 + sin^2 \theta_1) +
\\
& + l_2^2 \dot \theta_2^2 (cos^2 \theta_2 + sin^2 \theta_2) + 2 l_1 l_2 \dot \theta_1 \dot \theta_2 (cos \theta_1 cos \theta_2 + sin \theta_1 sin \theta_2))
\end{array}$$
$$
T = \dfrac{1}{2} m_1 l_1^2 \dot \theta_1^2 + 
\dfrac{1}{2} m_2 l_1^2 \dot \theta_1^2 + \dfrac{1}{2} m_2 l_2^2 \dot \theta_2^2  + m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 cos (\theta_1  - \theta_2)
$$
Analisando então a Energia Potencial $V$, assumindo $V=0$ em $y=0$.

$$V = -m_1 g l_1 cos \theta_1 - m_2 g (l_1 cos \theta_1 + l_2 cos \theta_2)$$

Então a Lagrangiana:

$$L=T-V$$
$$\begin{array}{ll}
L = & \dfrac{1}{2} m_1 l_1^2 \dot \theta_1^2 + 
\dfrac{1}{2} m_2 l_1^2 \dot \theta_1^2 + \dfrac{1}{2} m_2 l_2^2 \dot \theta_2^2  + m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 cos (\theta_1  - \theta_2) +
\\
& + m_1 g l_1 cos \theta_1 + m_2 g (l_1 cos \theta_1 + l_2 cos \theta_2)
\end{array}$$

Logo e com isso as derivadas parciais serão:

$$\dfrac{\partial L}{\partial \dot \theta_1} = (m_1 + m_2) l_1^2 \dot \theta_1 + m_2 l_1 l_2 \dot \theta_2 cos (\theta_1  - \theta_2)  $$
$$\dfrac{\partial L}{\partial \theta_1} = - m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 sin (\theta_1  - \theta_2) - m_1 g l_1 sin \theta_1 - m_2 g l_1 sin \theta_1 $$
$$\dfrac{\partial L}{\partial \theta_1} = - m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 sin (\theta_1  - \theta_2) - (m_1 + m_2) g l_1 sin \theta_1$$

$$\dfrac{\partial L}{\partial \dot \theta_2} = m_2 l_2^2 \dot \theta_2 + m_2 l_11 l_2 \dot \theta_1 cos(\theta_1 - \theta_2)  $$
$$\dfrac{\partial L}{\partial \theta_2} = m_2 l_1 l_2 \dot \theta_1  sin (\theta_1  - \theta_2) - m_2gl_2 sin \theta_2 $$
E com isso, as Equações de Lagrange serão:

Para $\theta_1$:
$$\dfrac{d}{dt} \left( \dfrac{\partial L}{\partial \dot \theta_1} \right) - \dfrac{\partial L}{\partial \theta_1} = 0$$
$$\dfrac{d}{dt} \left( (m_1 + m_2) l_1^2 \dot \theta_1 + m_2 l_1 l_2 \dot \theta_2 cos (\theta_1  - \theta_2) \right) + m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 sin (\theta_1  - \theta_2) + (m_1 + m_2) g l_1 sin \theta_1 = 0$$
$$
\begin{array}{}
(m_1 + m_2) l_1^2 \ddot \theta_1

+ m_2 l_1 l_2 (
  \ddot \theta_2 cos (\theta_1  - \theta_2) 
- \dot \theta_2 sin (\theta_1  - \theta_2)(\dot \theta_1  - \dot \theta_2) ) +
\\

+ m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 sin (\theta_1  - \theta_2) + (m_1 + m_2) g l_1 sin \theta_1 = 0
\end{array}$$
$$
\begin{array}{}
(m_1 + m_2) l_1^2 \ddot \theta_1

+ m_2 l_1 l_2 
  \ddot \theta_2 cos (\theta_1  - \theta_2) 
- m_2 l_1 l_2 \dot \theta_2 sin (\theta_1  - \theta_2)(\dot \theta_1  - \dot \theta_2)  +
\\

+ m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 sin (\theta_1  - \theta_2) + (m_1 + m_2) g l_1 sin \theta_1 = 0
\end{array}$$
$$
\begin{array}{}
(m_1 + m_2) l_1^2 \ddot \theta_1

+ m_2 l_1 l_2 
  \ddot \theta_2 cos (\theta_1  - \theta_2) 
- m_2 l_1 l_2 \dot \theta_2 sin (\theta_1  - \theta_2)(\dot \theta_1  - \dot \theta_2)  +
\\

+ m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 sin (\theta_1  - \theta_2) + (m_1 + m_2) g l_1 sin \theta_1 = 0
\end{array}$$
$$
\begin{array}{}
(m_1 + m_2) l_1^2 \ddot \theta_1

+ m_2 l_1 l_2 
  \ddot \theta_2 cos (\theta_1  - \theta_2) 
- m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 sin (\theta_1  - \theta_2)  +
\\
+ m_2 l_1 l_2 \dot \theta_2^2 sin (\theta_1  - \theta_2)
+ m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 sin (\theta_1  - \theta_2) + (m_1 + m_2) g l_1 sin \theta_1 = 0
\end{array}$$
$$
(m_1 + m_2) l_1^2 \ddot \theta_1

+ m_2 l_1 l_2 
  \ddot \theta_2 cos (\theta_1  - \theta_2) 
+ m_2 l_1 l_2 \dot \theta_2^2 sin (\theta_1  - \theta_2)
+ (m_1 + m_2) g l_1 sin \theta_1 = 0
$$

Para $\theta_2$:

$$\dfrac{d}{dt} \left( \dfrac{\partial L}{\partial \dot \theta_2} \right) - \dfrac{\partial L}{\partial \theta_2} = 0$$
$$\dfrac{d}{dt} \left( m_2 l_2^2 \dot \theta_2 + m_2 l_11 l_2 \dot \theta_1 cos(\theta_1 - \theta_2) \right) 

- m_2 l_1 l_2 \dot \theta_1\dot \theta_2  sin (\theta_1  - \theta_2)

+ m_2gl_2 sin \theta_2
= 0$$
$$
\begin{array}{c}
m_2 l_2^2 \ddot \theta_2

+ m_2 l_11 l_2 (\ddot \theta_1 cos(\theta_1 - \theta_2)
- \dot \theta_1 sin(\theta_1 - \theta_2)(\dot \theta_1 - \dot \theta_2) ) 
-
\\
- m_2 l_1 l_2 \dot \theta_1 \dot \theta_2  sin (\theta_1  - \theta_2)

+ m_2gl_2 sin \theta_2
= 0
\end{array}$$
$$
\begin{array}{c}
m_2 l_2^2 \ddot \theta_2 +
m_2 l_1 l_2 \ddot \theta_1 cos(\theta_1 - \theta_2)-
m_2 l_1 l_2 \dot \theta_1^2 sin(\theta_1 - \theta_2) +
\\
+ m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 sin(\theta_1 - \theta_2)

- m_2 l_1 l_2 \dot \theta_1 \dot \theta_2  sin (\theta_1  - \theta_2)

+ m_2gl_2 sin \theta_2
= 0
\end{array}$$
$$
\begin{array}{c}
m_2 l_2^2 \ddot \theta_2 +
m_2 l_1 l_2 \ddot \theta_1 cos(\theta_1 - \theta_2)-
m_2 l_1 l_2 \dot \theta_1^2 sin(\theta_1 - \theta_2) +
\\
+ m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 sin(\theta_1 - \theta_2)

- m_2 l_1 l_2 \dot \theta_1 \dot \theta_2 sin (\theta_1  - \theta_2)

+ m_2gl_2 sin \theta_2
= 0
\end{array}$$

$$

m_2 l_2^2 \ddot \theta_2 +
m_2 l_1 l_2 \ddot \theta_1 cos(\theta_1 - \theta_2)-
m_2 l_1 l_2 \dot \theta_1^2 sin(\theta_1 - \theta_2) +
m_2gl_2 sin \theta_2
= 0
$$

**Exemplo**: Encontre as equações de movimento para um pêndulo simples cujo ponto de sustentação move-se com aceleração constante e igual a $a$ na direção horizontal. Então encontre a nova posição de equilíbrio e a frequência angular para pequenas oscilações em torno da nova posição de equilíbrio.
![[Pasted image 20221003140405.png]]


Vínculos:
- $(x -\dfrac{1}{2} a t^2)^2 + y^2 = l^2$

Graus de liberdade:
- $n = 2 \; \text{(coordenadas posicionais)} - 1 \; \text{(vínculo)} = 1$

Adotamos: $q_1 = \theta$.

Temos então que:
- $x = \dfrac{1}{2} a t^2 + l sin \theta$,            $\dot x = at + l \dot \theta cos \theta$
- $y = -l cos \theta$,                      $\dot y = l \dot \theta sin \theta$

Analisado a Energia Cinética $T$ do sistema:

$$T = \dfrac{1}{2} m (\dot x^2 + \dot y^2)$$
$$T = \dfrac{1}{2} m (a^2 t^2 + l^2 \dot \theta^2 cos^2 \theta
+ 2alt \dot \theta \;cos \theta
+ l^2 \dot \theta^2  sin^2 \theta)$$
$$T = \dfrac{1}{2} m (a^2 t^2 + l^2 \dot \theta^2 (cos^2 \theta + sin^2 \theta)
+ 2alt \dot \theta \; cos \theta)$$
$$T = \dfrac{1}{2} m (a^2 t^2 + l^2 \dot \theta^2 + 2alt \dot \theta \; cos \theta)$$

Analisando então a Energia Potencial $V$, assumindo $V=0$ em $y=0$.
$$V = mgy = mg (-l cos \theta) = -m g l \; cos \theta$$
Então a Lagrangiana:

$$L=\dfrac{1}{2} m (a^2 t^2 + l^2 \dot \theta^2 + 2alt \dot \theta \; cos \theta) + m g l \; cos \theta$$

Logo e com isso as derivadas parciais serão:

$$\dfrac{\partial L}{\partial \dot \theta} = m l^2 \dot \theta + m a l t \; cos \theta $$

$$\dfrac{\partial L}{\partial \theta} = - m a l t \dot \theta \; sin \theta \; - m g l \; sin \theta $$

E com isso, as Equações de Lagrange serão:

$$\dfrac{d}{dt} \left( \dfrac{\partial L}{\partial \dot \theta}  \right) - \dfrac{\partial L}{\partial \theta} = 0$$
$$\dfrac{d}{dt} \left( m l^2 \dot \theta + m a l t \; cos \theta \right) 

+ m a l t \dot \theta \; sin \theta \; + m g l \; sin \theta
= 0$$
$$ m l^2 \ddot \theta + m a l (cos \theta - t \dot \theta \; sin \theta)

+ m a l t \dot \theta \; sin \theta \; + m g l \; sin \theta
= 0$$
$$ m l^2 \ddot \theta + m a l \; cos \theta - m a l t  \dot \theta \; sin \theta

+ m a l t \dot \theta \; sin \theta \; + m g l \; sin \theta
= 0$$
$$ m l^2 \ddot \theta + m a l \; cos \theta + m g l \; sin \theta
= 0$$

Então a aceleração será:
$$ m l^2 \ddot \theta + m a l \; cos \theta + m g l \; sin \theta
= 0$$
$$ m l^2 \ddot \theta = - m a l \; cos \theta - m g l \; sin \theta$$
$$ l \ddot \theta = - a \; cos \theta - g \; sin \theta$$
$$ \ddot \theta = - \dfrac{a}{l} \; cos \theta - \dfrac{g}{l} \; sin \theta$$

Notamos que quando a aceleração é 0, recuperamos a Equação do Movimento do pêndulo simples.

O equilíbrio ocorre quando $\ddot \theta = 0$, então
$$ \ddot \theta = - \dfrac{a}{l} \; cos \theta - \dfrac{g}{l} \; sin \theta$$
$$ 0 = - \dfrac{a}{l} \; cos \theta - \dfrac{g}{l} \; sin \theta$$
$$ \dfrac{a}{l} \; cos \theta = - \dfrac{g}{l} \; sin \theta$$
$$ \dfrac{a}{l} \; cos \theta \dfrac{1}{cos \theta} = - \dfrac{g}{l} \; sin \theta \dfrac{1}{cos \theta}$$
$$ a  = - \dfrac{sin \theta}{cos \theta} g$$
$$ a  = -g \; tan \theta $$
$$ tan \theta = - \dfrac{a}{g} $$
Definimos a notação que de $\theta_e$ quando $\theta$ está na posição de equilíbrio. 

Para pequenas variações em torno do ponto de equilíbrio onde $\theta = \theta_e$, $\theta(t) = \theta_e + \varepsilon(t)$ onde $|\varepsilon| << 1$.

Se  $\theta(t) = \theta_e + \varepsilon(t)$, então $\ddot \theta(t) = \ddot \varepsilon(t)$, logo:

$$\ddot \theta = \ddot \varepsilon = -\dfrac{a}{l} \; cos \theta - \dfrac{g}{l} \; sin \theta$$
$$\ddot \theta = \ddot \varepsilon = -\dfrac{a}{l} \; cos (\theta_e + \varepsilon) - \dfrac{g}{l} \; sin (\theta_e + \varepsilon)$$
$$\ddot \theta = \ddot \varepsilon = -\dfrac{a}{l} \; (cos \theta_e \; cos( \varepsilon) - sin \theta_e \; sin( \varepsilon)) - \dfrac{g}{l} \; (sin \theta_e \; cos( \varepsilon) + cos \theta_e \; sin( \varepsilon))$$
Como $|\varepsilon| << 1$, $cos(\varepsilon) \approx 1$ e $sin(\epsilon) \approx \varepsilon$, logo:   
$$\ddot \theta = \ddot \varepsilon = -\dfrac{a}{l} \; (cos \theta_e \; cos( \varepsilon) - sin \theta_e \; sin( \varepsilon)) - \dfrac{g}{l} \; (sin \theta_e \; cos( \varepsilon) + cos \theta_e \; sin( \varepsilon))$$
$$\ddot \theta = \ddot \varepsilon = -\dfrac{a}{l} \; (cos \theta_e - \varepsilon \; sin \theta_e \; ) - \dfrac{g}{l} \; (sin \theta_e \;  + \varepsilon \; cos \theta_e )$$
$$\ddot \theta = \ddot \varepsilon = -\dfrac{a}{l} cos \theta_e +\dfrac{a}{l} \varepsilon \; sin \theta_e - \dfrac{g}{l} sin \theta_e   -\dfrac{g}{l} \varepsilon \; cos \theta_e $$
$$\ddot \theta = \ddot \varepsilon = -\dfrac{a}{l} cos \theta_e  - \dfrac{g}{l} sin \theta_e   - \left( \dfrac{g}{l} cos \theta_e - \dfrac{a}{l} sin \theta_e \right) \varepsilon$$
Onde temos que $-\dfrac{a}{l} cos \theta_e  - \dfrac{g}{l} sin \theta_e = 0$ no equilíbrio e $\left( \dfrac{g}{l} cos \theta_e - \dfrac{a}{l} sin \theta_e \right) \varepsilon$ é constante e maior que zero, logo:
$$\ddot \varepsilon = - \left( \dfrac{g}{l} cos \theta_e - \dfrac{a}{l} sin \theta_e \right) \varepsilon$$
$$\ddot \varepsilon = - \omega^2 \varepsilon, \;\;\;\;\;\;\;\; \text{onde} \; \omega^2 = \left( \dfrac{g}{l} cos \theta_e - \dfrac{a}{l} sin \theta_e \right)$$
Adotando $\varepsilon(t) = A \; sin(\omega t + \phi)$ como solução para $\varepsilon$ e sabendo que $tan \theta = - \dfrac{a}{g}$:
![[Pasted image 20221003153758.png]]

$$sin \theta_e = \dfrac{-a}{\sqrt{a^2+g^g}}, \;\;\;\;\;\;\; cos \theta_e = \dfrac{g}{\sqrt{a^2+g^g}}$$
$$\omega^2 = \left( \dfrac{g}{l} cos \theta_e - \dfrac{a}{l} sin \theta_e \right)$$
$$\omega^2 = \left( \dfrac{g}{l} \dfrac{g}{\sqrt{a^2+g^g}} - \dfrac{a}{l} \dfrac{-a}{\sqrt{a^2+g^g}} \right)$$
$$\omega^2 = \dfrac{1}{l} \left( \dfrac{g^2}{\sqrt{a^2+g^g}} +  \dfrac{a^2}{\sqrt{a^2+g^g}} \right)$$
$$\omega^2 = \dfrac{1}{l} \left( \dfrac{a^2 + g^2}{\sqrt{a^2+g^g}}  \right)$$
$$\omega^2 = \dfrac{1}{l} \sqrt{a^2+g^g}$$
