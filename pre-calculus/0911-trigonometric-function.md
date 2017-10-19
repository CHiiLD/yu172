# 삼각함수

## 60분법과 호도법의 정의

- 60분법 - 각의 크기를 360등분 한 것을 1도로 한다.
- 호도법 - 반지름이 $r$인 원에서 어떤 호의 길이가 $r$일 때의 각의 크기를 $1rad$라 한다.

## 부채꼴의 둘레와 넓이

1. $l = r\theta$
2. $A = \frac{1}{2}rl = \frac{1}{2}r^2\theta$


## 삼각함수의 정의

삼각함수가 $x^2 + y^2 = r^2$ 임을 만족할 때,

- $\sin\theta = \dfrac{y}{r}$


- $\cos\theta = \dfrac{y}{r}$


- $\tan\theta = \dfrac{y}{x}$

|              | $\theta = 0$ |     $\theta = 30$     |     $\theta = 45$     |     $\theta = 60$     |  $\theta = 90$   |
| :----------: | :----------: | :-------------------: | :-------------------: | :-------------------: | :--------------: |
| $\sin\theta$ |     $0$      |    $\dfrac{1}{2}$     | $\dfrac{1}{\sqrt{2}}$ | $\dfrac{\sqrt{3}}{2}$ |        1         |
| $\cos\theta$ |     $1$      | $\dfrac{\sqrt{3}}{2}$ | $\dfrac{1}{\sqrt{2}}$ |    $\dfrac{1}{2}$     |        0         |
| $\tan\theta$ |     $0$      | $\dfrac{1}{\sqrt{3}}$ |           1           |      $\sqrt{3}$       | $\dfrac{\pi}{2}$ |

## 삼각함수의 성질

### 사분면의 양수

각각 1사분면부터 $\text{all}, \sin, \tan, \cos$

### 정리 1

- 
  $\sin(\dfrac{\pi}{2} - \theta) = \cos\theta$

- $\cos(\dfrac{\pi}{2} - \theta) = \sin\theta$
- $\tan(\dfrac{\pi}{2} - \theta) = \cot\theta$


### 정리 2

- 
  $\sin^2\theta + cos^2\theta = 1$ 

- $1 + \tan^2\theta = \sec^2\theta$ 
- $1 + \cot^2\theta = csc^2\theta$


## 주기함수

$$
Def. f(x + p) = f(x) for all x \\
\leftrightharpoons f:\text{preodic function} \\
\text{이 때, 주기함수를 만족하는 P를 기본주기라고 한다.}
$$

- 
  $\dfrac{\cos(\pi + \theta)}{\sin(\pi + \theta)} = \dfrac{-\sin\theta}{-\cos\theta} = \tan\theta$ 

- $\sin(n\pi + \theta) = (-1)^n\sin\theta$ 
- $\cos(n\pi + \theta) = (-1)^n\cos\theta$ 
- $\tan(n\pi + \theta) = \tan\theta$ 
- $\sin(\dfrac{(2n-1)\pi}{2}) = (-1)^n\cos\theta$ 
- $\cos(\dfrac{(2n-1)\pi}{2}) = (-1)^n\sin\theta$
- $\tan(\dfrac{(2n-1)\pi}{2}) = \cot\theta$

## $y = \sin x$ 의 그래프

1. 기본주기: 2$\pi$
2. $-1 \le \sin x \le 1$
3. 기함수
4. x 절편: $\{n\pi | n \in \mathbb{N}\}$
5. y 절편: 0


## 역삼각함수

- $y=\sin^{-1}x$

$$
\begin{aligned}
&y=\sin{x}:[-\dfrac{\pi}{2}, \dfrac{\pi}{2}] \to [-1, 1]\\
&y=\sin^{-1}x:[-1, 1] \to [-\dfrac{\pi}{2}, \dfrac{\pi}{2}]
\end{aligned}
$$



- $y=\cos^{-1}x$

$$
\begin{aligned}
&y=\cos{x}:[0, 2\pi] \to [-1, 1]\\
&y=\cos^{-1}x:[-1, 1] \to [0, 2\pi]
\end{aligned}
$$



- $y=\tan^{-1}x$

$$
\begin{aligned}
&y=\tan{x}:[-\dfrac{\pi}{2}, \dfrac{\pi}{2}] \to \mathbb{R}\\
&y=\tan^{-1}x:\mathbb{R} \to [-\dfrac{\pi}{2}, \dfrac{\pi}{2}]
\end{aligned}
$$

# 해석적 삼각함수와 삼각법의 응용

## 합과 차의 공식

### 오일러의 공식

$$
e^{i\theta} = \cos\theta + i\sin\theta
$$

### 합과 차의 공식

$$
\begin{aligned}
&Thm. \\
&\sin(\alpha \pm \beta) = \sin\alpha\cos\beta \pm \cos\alpha\sin\beta \\
&\cos(\alpha \pm \beta) = \cos\alpha\cos\beta \mp \sin\alpha\sin\beta \\
&\tan(\alpha \pm \beta) = \dfrac{\tan\alpha \pm \tan\beta}{1 \mp \tan\alpha\tan\beta}
\end{aligned}
$$

### 합과 차의 공식 유도

$$
\begin{aligned}
&Def. \\
&e^{i(\alpha + \beta)} = \cos(\alpha + \beta) + i\sin(\alpha + \beta) \\
&= e^{i\alpha}  e^{i\beta} \\
&= (\cos\alpha + i\sin\alpha)(\cos\beta + i\sin\beta) \\
&= (\cos\alpha\cos\beta - \sin\alpha\sin\beta) + i(\sin\alpha\cos\beta + \cos\alpha\sin\beta)
\end{aligned}
$$

$$
\begin{aligned}
Def. \\
&\tan(\alpha + \beta) =\dfrac{\sin(\alpha + \beta)}{\cos(\alpha + \beta)} \\
&= \dfrac{\sin\alpha\cos\beta + \cos\alpha\sin\beta}{\cos\alpha\cos\beta - \sin\alpha\sin\beta} \\
&= \dfrac{\dfrac{\sin\alpha\cos\beta}{\cos\alpha\cos\beta} + \dfrac{\cos\alpha\sin\beta}{\cos\alpha\cos\beta}}{1 - \dfrac{\sin\alpha\sin\beta}{\cos\alpha\cos\beta}} \\
&= \dfrac{\tan\alpha + \tan\beta}{1 - \tan\alpha\tan\beta}
\end{aligned}
$$

## 배각 공식

- $\sin(2\theta) = 2\sin\theta\cos\theta$
- $\cos(2\theta) = \cos^2\theta-\sin^2\theta = 1 - 2\sin^2\theta = 2\cos^2\theta - 1$
- $\tan(2\theta) = \dfrac{2\tan\theta}{1 + \tan^2\theta}$


## 반각 공식

- $\sin\dfrac{\theta}{2} = \pm\sqrt{\dfrac{1- \cos\theta}{2}}$
- $\cos\dfrac{\theta}{2} = \pm\sqrt{\dfrac{1+ \cos\theta}{2}}$
- $\tan\dfrac{\theta}{2} = \pm\sqrt{\dfrac{1- \cos\theta}{1+ \cos\theta}}$

$\pm$ 은 $\dfrac{\theta}{2}$가 몇 사분면인지에 따라 결정된다.



- $\cos^2\theta = \dfrac{1 + \cos(2\theta)}{2}$
- $\sin^2\theta = \dfrac{1 - \cos(2\theta)}{2}$
- $\tan^2\theta = \dfrac{1 - \cos^2\theta}{1 + \cos^2\theta}$

## 사인법칙과 코사인법칙

### 사인법칙

$$
\dfrac{\sin A}{a} = \dfrac{\sin B}{b} = \dfrac{\sin C}{c}
$$

### 코사인법칙

$$
a^2 = b^2 + c^2 - 2bc\cos A\\
b^2 = a^2 + c^2 - 2ac\cos B\\
c^2 = a^2 + b^2 - 2ab\cos C
$$

