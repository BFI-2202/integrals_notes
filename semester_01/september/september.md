# Лекция — 05.09.2023
## Двойные интегралы

$z = f(x, y)$
$V = \lim\limits_{diam S_{i}\to 0} \sum\limits_{i = 1}^{n} f(P_{i)}\Delta S_i$
Если $f(x, y)$ непрерывна в замкнутой области $D$ и существует предел последовательности интегральных сумм, который не зависит от способа разбиения области на $\Delta S_i$ и от выбора точек $P_i$ при условии, что диаметр $\Delta S_i$ стремится к нулю, то этот предел мы и будем называть двойным интегралом функции $f(x, y)$ по области $D$
$V = \int \int f(x, y) d x d y$ = $\lim \limits_{diam S_{i}\to 0} \sum\limits_{i = 1}^{n} f(P_{i)}\Delta S_i$
### Свойства интегралов

1. $\int \int\limits_{D} (f_{1}+ f_{2)}d x d y = \int \int\limits_{D} f_{1} dx dy + \int\int\limits_{D} f_{2}dx dy$
2. $\int\int\limits_{D} \alpha f(x, y) d x d y = \alpha \int\int\limits_{D} f(x, y) d x dy$
3. $D = D_{1}+ D_{2}+ \dots + D_n$ (конечное число областей), $\int\int\limits_{D} = \int\int\limits_{D_{1}}+ \int\int\limits_{D_{2}}+\dots+\int\int\limits_{D_n}$
### Вычисление двойного интеграла, переход к повторными интегралам

Пусть $y = \phi_1(x)$, $y=\phi_2(x)$ — некоторые кривые, ограничивающие область.
Ее двойной интеграл: $\int\int\limits_{D} f(x, y) d x d y = \int\limits_{a}^{b} (\int\limits_{\phi_{1}(x)}^{\phi_{2}(x)} f(x, y) d y)dx = \int\limits_{\alpha}^{\beta} d x \int\limits_{\phi_{1}(x)}^{\phi_{2}(x)} f(x, y) d y$
#### Примеры
##### Пример №1

$y = x^2$, $1 \le x \le 2$
$\int\limits_{1}^{2} d x \int\limits_{0}^{x^2} f(x, y) d y$
##### Пример №2

$x^{2}+ y^{2}= 4$, $-2 \le x \le 2$
 $\int\limits_{-2}^{2} d x \int\limits_{0}^{\sqrt{4 - x^2}} f(x, y) d y$
##### Пример №3

$x^{2}+ y^{2}= 4$, $0 \le x \le 2$
$\int\limits_{0}^{2} d x \int\limits_{-\sqrt{4-x^{2}}}^{\sqrt{4-x^{2}}} f(x, y) d x$
##### Пример №4

$y = x + 2$, $-2 \le x \le 0$; $y = \sqrt{4 - x^2}$, $0 \le x \le 2$
$\int\limits_{-2}^{0} d x \int\limits_{0}^{x + 2} f(x, y) d y + \int\limits_{0}^{2} d x \int\limits_{0}^{\sqrt{4 - x^{2}}} f(x, y) d y$
##### Пример №5

$y = 4 - x^2$, $0 \le x \ 2$
$\int\limits_{0}^{2} d x + \int\limits_{0}^{4-x^{2}} f d y = \int\limits_{0}^{4} d y \int\limits_{0}^{\sqrt{4-y}} f(x, y) d x$ (сменили порядок интегрирования)
##### Пример №6

$\int\limits_{2}^{4} d x \int\limits_{x}^{2x} \frac{y}{x} d y = \int\limits_{2}^{4} \frac{3}{2} x d x = \frac{3}{2} * \frac{x^{2}}{2} \bigg|^{4}_{2} = \frac{3}{4}(16-4)=9$
$\frac{1}{x} \frac{y^{2}}{x} \bigg|^{y = 2x} = \frac{4x^{2}-x^{2}}{2x} = \frac{3x^{2}}{2x} = \frac{3}{2}x$
##### Пример №7

$$
y = x, y = 2 - x
$$
$$
\int\limits_{0}^{1} d x \int\limits_{0}^{x} f(x, y) d y + \int\limits_{1}^{2} d x \int\limits_{0}^{2 - x} f(x, y) dy 
$$
$$
\int\limits_{0}^{1} d y \int\limits_{2 - y}^{y} f(x, y) d x
$$
### Замена переменных в двойном интеграле, полярные координаты

Каждая точка в декартовой системе координат характеризуется $x$и $y$. C другой стороны, если мы направим полярную ось, то эта же точка может характеризоваться $\rho$ — длина радиус-вектора, $\phi$ — угол поворота относительно положительного направления оси $OX$

$x = \rho \cos \phi$
$y = \rho \sin \phi$

Иногда двойной интеграл удобно вычислять не в декартовых координатах, а каких-нибудь других: может, в этих новых координатах может быть что-нибудь более удобно записано, например, $\rho = 2$ симпатичней, нежели $x^{2}+ y^{2}= 4$.

$\int\int f(x, y) d x d y = \int \int f(x(u; v), y(u; v)) |J| d x d y$

**Якобиан перехода к полярным координатам**:

$$
J = \begin{pmatrix}
\frac{\delta x}{\delta u} & \frac{\delta x}{\delta v} \\ 
\frac{\delta y}{\delta u} & \frac{\delta y}{\delta v}
\end{pmatrix} = \begin{pmatrix}
\cos \phi & -\rho \sin \phi \\ 
\sin \phi & \rho \cos \phi
\end{pmatrix} = \rho
$$
#### Примеры
##### Пример №1

$S: \begin{cases}x^{2} + y^{2}- 6y = 0 \\ y = x \\ y = \sqrt{3} x \end{cases}$

$\rho^2 \cos^2 + \rho^ 2\sin^2 \phi = 6 \rho \sin \phi \Longleftrightarrow \rho = 6 \sin \phi$
$S = \displaylines{\int\int d x d y = \int\int \rho d \rho d \phi = \int\limits_{\pi/4}^{\pi/3} d \phi \int\limits_{0}^{6 \sin \phi} \rho d \rho = 6 \int\limits_{\pi/4}^{\pi/3} 2 \sin^2 \phi d \phi = 9 \int\limits_{\pi/4}^{\pi/3} (1 - \cos 2 \phi) d \phi = 9 (\phi - \frac{1}{2} \sin \phi) = \bigg|_{\pi/4}^{\pi/3} = \\ = 9 (\frac{\pi}{3} - \frac{\pi}{4} - \frac{1}{2} (\sin \frac{2\pi}{3} - \sin \frac{\pi}{2}) = 9 (\frac{\pi}{12} + \frac{1}{2} - \frac{\sqrt{3}}{4})}$
### Геометрические приложения двойного интеграла

1. $S = \int\int\limits_{S} d x \ d y$
2. $V = \int\int\limits_{D} (f_1(x, y) - f_2(x, y)) d x \ d y$
## Тройные интегралы

$$\int\int\limits_{V}\int f(x, y, z) d x \ d y \ d z =$$ $$ = \int\limits_{a}^{b} d x \int\limits_{\phi_1(x)}^{\phi_2(x)} d y \int\limits_{\xi_1(x, y)}^{\xi_2(x, y)} f(x, y, z) \ d z$$
### Примеры
#### Пример №1

$z = x^2 + y^2$
$z = 2(x^2 + y^2)$
$y = x^2$, $y = x$

 $$\int\limits_{0}^{1} d x \int\limits_{x^2}^{x} d y \int\limits_{x^2+y^2}^{2(x^2+y^2)} f(x, y, z) \ d z$$
# Практическое занятие — 07.09.2023
## Методы решения неопределенных интегралов
### Метод подстановки

$\int \sqrt{1 - x^2} dx = \dots$
$x = \sin t$
$d x = \cos t d t$  
$\dots = \int \sqrt{1 - \sin^2 t} \cos t d t = \int \cos^2 t d t = \frac{1}{2} \int (1 + \cos 2 t) d t = \frac{1}{2} (t + \frac{1}{2} \sin 2t) = \frac{1}{2} (t + \sin t \cos t) = \dots$
Выполним обратную подстановку:
$\dots = \frac{1}{2} (\arcsin x + x\sqrt{1 - x^2}) + C$

Этот пример можно решить и интегрированием по частям: $u = \sqrt{1 - x^2}$, $du = \frac{-2 x dx}{2\sqrt{1 - x^2}}$, $dv = d x$, $v x$

$\dots = x\sqrt{1-x^2} - \int \frac{1-x^2 d x}{\sqrt{1-x^2}}=x\sqrt{1-x^2}-\int\sqrt{1-x^2}dx+\int\frac{dx}{\sqrt{1-x^2}} = \dots$

---

$\int \frac{d x}{x \sqrt{1 + 9x^2}} = \dots$
$t = \frac{1}{x}$, $x = \frac{1}{t}$
$dx = \frac{1}{t^2} dt$
$\dots = \int \frac{-\frac{1}{t^2} d t}{\frac{1}{t} \sqrt{1 + \frac{9}{t^2}}} dt = -\int \frac{\frac{t}{t^2} d t}{\sqrt{t^2 + 3^2}} = -\ln |t + \sqrt{t^2 + 9}| + C = -\ln |\frac{1}{x} + \sqrt{\frac{1}{x^2} + 9}| + C$
### Интегрирование по частям

$\int u d v = u v - \int v d u$

1. Многочлен * тригонометрическую или показательную функцию, $u$ — многочлен, $dv$ — остальное
2. Многочлен * логарифмическую функцию или обратную тригонометрическую функцию, $u$ — функция, $dv$ — остальное

$\int (x^2 + x) \ln x d x = \dots$
$ln x = u$, $(x^2 + x) d x = dv$
$du = \frac{dx}{x}$, $v = \int (x^2 + x) d x = \frac{x^3}{3} + \frac{x^2}{2}$

$\dots = (\frac{x^3}{3} + \frac{x^2}{2}) \ln x - \int (\frac{x^3}{3} + \frac{x^2}{2}) \frac{d x}{x} = (\frac{x^3}{3} + \frac{x^2}{2}) \ln x - \frac{x^3}{9} - \frac{x^2}{4} + C$

---

$\int (2x + 1) \sin x d x = \dots$ 
$u = 2 x + 1$, $dv = \sin x dx$
$d u = 2 d v$, $v = -\cos x$

$\dots = (2x + 1)(- \cos x) + 2 \int \cos x dx = (2x + 1)(-\cos x) + 2 \sin x + C$
### Интегрирование дробей

Можем интегрировать только правильные дроби: $\int \frac{\sqrt{x^3-x+5}}{x^2 + 1} = \int x - \int \frac{2x}{x^2 + 1} + \int \frac{5}{x^2 + 1} = \dots$
Главное: выделить целую часть. Получили отдельные интегралы, которые уже табличные или почти табличные.
$\dots = \frac{x^2}{2} - \ln|x^2 + 1| + 5 \arctan x + C$

Кроме того, можем выделять полный квадрат в знаменателе: $\int \frac{d x}{x^2 + 2x + 5} = \int \frac{d x}{x^2 + 2x + 1 + 4} = \int \frac{d (x + 1)}{(x+1)^2 + 2^2} = \frac{1}{2} \arctan \frac{x + 1}{2} + C$

1. Действительные различные корни у знаменателя
   $\int \frac{(7x + 8) dx}{(x - 3)}{x + 5} = \dots$
   Разбиваем эту дробь на две отдельные дроби и подбираем коэффициенты
   $\frac{A}{x - 3} + \frac{B}{x + 5} = \frac{A(x + 5) + B(x - 3)}{(x-3)(x+5)}$
   При x: $A + B = 7$
   Свободный член: $5A - 3B = 8$
   $A = \frac{29}{8}$, $B = \frac{27}{8}$
   $\dots = \int \frac{\frac{29}{8} dx}{x - 3} + \int \frac{\frac{27}{8} dx}{x + 5} = \frac{29}{8} \ln |x - 3| + \frac{27}{8} \ln |x + 5| + C$
2. Действительные кратные корни
   $\int \frac{(7x + 8) dx}{(x-3)^2 (x + 5)^3} = \int \frac{A dx}{x - 3} + \int \frac{B dx}{(x-3)^2} + \int \frac{C dx}{x = 5} + \int \frac{D dx}{(x+5)^2} + \int \frac{\xi dx}{(x+5)^3} = \dots$
   $\dots = A \ln |x - 3| + \frac{B(x - 3)^{-1}}{-1} + C \ln |x + 5| + \frac{D (x + 5)^{-1}}{-1} + \frac{\xi (x+5)^{-2}}{-2}  + C$
3. Комплексные корни
   $\frac{2x+5}{(x^2+1)(x^2+3)}=\frac{A x + B}{x^2 + 1} + \frac{C x + D}{x^2 + 3}$
   $\int\frac{(2x + 5) d x}{(\dots)(\dots)} = A \int\frac{x d x}{x^2 + 1} + B\int\frac{d x}{x^2 + 1} + C \int\frac{2x dx}{x^2 + 3} + D \int\frac{dx}{x^2 + 3} = \dots$

Бывают комбинированные случаи: $\frac{2 x + 9}{x^2 (x - 1)(x^2 + 4)} = \frac{A}{x} + \frac{B}{x^2} + \frac{C}{x - 1} + \frac{F x}{x^2 + 4} + \frac{D}{x^2 + 4}$
### Интегрирование тригонометрических штук

$\int \sin \alpha x * \cos \beta x d x$, $m$, $n$ — степени $\sin x$ и $\cos x$
1. $m$ и $n$ — четные
   $\cos^2 x =\frac{1 + \cos 2x}{2}$
   $\sin^2 x = \frac{1 - \cos 2x}{2}$
2. $m$ или $n$ — нечетное
   Например, $\int \sin^6 x * \cos^3 x d x = \int \sin^6 x \cos^2 \cos dx = \int \sin^6 x (1 - \sin^2 x) d \sin x = \dots$
   $\dots = \frac{\sin^7 x}{7} - \frac{\sin^9 x}{9} + C$

### Универсальная тригонометрическая подстановка

$\tan \frac{x}{2} = t$
$x = 2 \arctan t$, $d x = \frac{2 d t}{1 + t^2}$
$\sin x = \frac{2 t}{1 + t^2}$, $\cos x = \frac{1 - t^2}{1 + t^2}$

$\int \frac{dx}{5 + 4 \sin x} = \int\frac{\frac{2dt}{1+t^2}}{5 + 4 * \frac{2t}{1+t^2}} = \int\frac{\frac{2dt}{1+t^2}}{\frac{5+5t^2+8t}{1+t^2}} = 2\int\frac{dt}{5t^2+8t+5} = \frac{2}{t} \int\frac{d t}{t^2 + 2 * \frac{4}{5} t + 1} = \dots$
$\dots = \frac{2}{t} \int\frac{d t}{t^2 + 2 * \frac{4}{5} t + \frac{16}{25} - \frac{16}{25} +1} = \frac{2}{5} \int\frac{d(t+\frac{4}{5})}{(t+\frac{4}{5})^2 + (\frac{3}{5})^2} = \frac{2}{3} \arctan \frac{(1 + \frac{4}{5})}{3/5} + C = \dots$
$\dots = \frac{2}{3} \arctan (\frac{5 \tan \frac{x}{2} + 4}{3}) + C$
## Решение определенных интегралов

Не забываем про пределы интегрирования — это критически важно. Если мы их не меняем — мы должны выполнить обратную подстановку обязательно. Если не выполняем обратную подстановку — их поменять обязательно.

## Решение задач

### 1714

$\int x^2 \sqrt[5]{x^3 + 2} dx = \dots$
$d(x^3+2) = 3x^2 d x$
$\dots = \frac{1}{3} \int 3x^2 \sqrt{x^3 + 2} dx = \frac{1}{3} \int (x^3 + 2)^{1/5} d(x^3 + 2) = \frac{1}{3} \frac{(x^3 + 2)^{6/5}}{6/5} + C = \dots$
$\dots = \frac{5(x^3 + 2)^{6/5}}{18} + C$
### 1718

$\int \frac{(6x-5) dx}{2 \sqrt{3x^2-5x+6}} = \dots$
$d(3x^2-5x+6) = (6x-5)dx$
$\dots = \frac{1}{2} \int \frac{d(3x^2-5x+6)}{\sqrt{3x^2-5x+6}} = \frac{1}{2} \int (3x^2-5x+6)^{-\frac{1}{2}} \ d(3x^2-5x+6) = \frac{1}{2} \frac{\sqrt{3x^2-5x+6}}{\frac{1}{2}} + C = \dots$$\dots = \sqrt{3x^2-5x+6} + C$
### 1768

$\int \frac{e^{x} dx}{e^{2x} + 4} = \dots$
$d(e^x) = e^x dx$
$\dots = \int \frac{d(e^x)}{(e^x)^2 + 2^2} = \frac{1}{2} \arctan \frac{e^x}{2} + C$
### 1782

$\int \frac{x dx}{2x + 1} = \frac{1}{2} \int\frac{2x + 1 - 1}{2x + 1} dx = \frac{1}{2} (\int dx - \int\frac{dx}{2x+1}) = \dots$
$\dots = \frac{1}{2} (x - \frac{1}{2} \ln (2x+1)) = \frac{1}{2}x - \frac{1}{4} \ln (2x + 1) + C$

### 1792

$\int \frac{dx}{x(x+1)} = \dots$
$\frac{1}{x(x + 1)} = \frac{A}{x} + \frac{B}{x + 1} = \frac{A}{x(x + 1)}$
$\dots = \int \frac{d x}{x} - \int\frac{d x}{x + 1} = \ln |x| - \ln |x + 1| + C = \ln |\frac{x}{x+1}| + C$
### 1933

$\int x \cos x = \dots$
$u = x$, $d v = dx$
$v = \sin x$, $v = x$
### 1729

$\int \arctan \sqrt{x} d x = \dots$

$t = \sqrt{x}$, $x = t^2$, $d x = 2 t dt$
$\dots = 2 \int \arctan t * t d t = \dots$
$u = \arctan t$, $d v = t d t$
$du = \frac{dt}{1 + t^2}$, $v = \frac{t^2}{2}$

$\dots = 2 (\frac{t^2 \arctan t}{2} - \frac{1}{2} \int \frac{t^2 d t}{1 + t^2}) = t^2 \arctan t - \int \frac{t^2 d t}{1 + t^2} = \dots$
$\dots = t^2 \arctan t - \int \frac{t^2 + t - 1}{t^2 + t} d t = t^2 \arctan t - t + \arctan t + C$
### 2012

$\int \frac{x d x}{(x + 1)(2 x + 1)} = \dots$
$\frac{A}{x + 1} + \frac{B}{2x + 1} = \frac{A(2x + 1) + B(x + 1)}{(x + 1)(2x + 1)} = \frac{2Ax + A + Bx + B}{(x+1)(2x+1)}$
При $x$: $2A + B = 1$
Свободный член: $A + B = 0$
$A = 1$, $B= -1$

$\dots = \int \frac{dx}{x+1} - \int\frac{dx}{2x + 1} = ln |x + 1| - \frac{1}{2} \ln |2x + 1| + C$
### 2013
$\int \frac{x dx}{2x^2-3x-2} = \dots$
$D = 9 + 16 = 25$
$x_{1} = \frac{3 + 5}{4} = 2$
$x_2 = -\frac{2}{4} = -\frac{1}{2}$

$\dots = \int \frac{x d x}{2(x-2)(x+\frac{1}{2})} = \frac{1}{2} \int \frac{x d x}{(x-2)(x+\frac{1}{2})} = \dots$
$\frac{A}{x-2} + \frac{B}{x + \frac{1}{5}} = \frac{A(x+\frac{1}{2})+B(x-2)}{(x-2)(x+\frac{1}{2})} = \frac{Ax + \frac{A}{2} + Bx - 2B}{(x-2)(x+\frac{1}{2})}$
При $x$: $A + B = 1$
Свободный член: $\frac{A}{2} - 2B = 0$
$A = \frac{4}{5}$, $B= \frac{1}{5}$

$\dots = \frac{1}{2} (\int \frac{\frac{4}{5} d x}{x-2} + \int \frac{\frac{1}{2} dx}{x + \frac{1}{2}}) = \frac{1}{2} (\frac{4}{5} * \int \frac{dx}{x-2} + \frac{1}{5} * \int \frac{dx}{x+\frac{1}{2}}) = \dots$
$\dots = \frac{4}{10} \ln |x - 2| + \frac{1}{10} \ln |x + \frac{1}{2}| + C$
### 2022

$\int \frac{(x^2-3x+2)d x}{x(x^2+2x+1)}$
### 2036

$\int \frac{d x}{x(x^2+1)} = \dots$
$\frac{A}{x} + \frac{Bx + C}{x^2 + 1} = \frac{(A + B)x^2 + Cx + A}{x(x^2 + 1)}$
$A = 1$, $B = -1$, $C = 0$

$\dots = \int \frac{d x}{x} + \int \frac{dx}{x^2+1} = \ln |x| - \frac{1}{2} \ln |x^2 + 1| + C$
### 2090 

$\int \sin^3 x \cos^2 x \ d x = \int (1 - \cos^2 x) \sin x \cos^2 x \ dx = \dots$
$t = \cos x$, $dt = - \sin x d x$
$\dots = - \int (1-t^2) t^2 \ dt = - \int (t^2 - t^4) \ dt = - \int t^2 dt + \int t^4 dt = \dots$
$\dots = -\frac{t^3}{3} + \frac{t^5}{5} = \frac{-\cos^3 x}{3} + \frac{\cos^5 x}{5} + C$
### 2091

$\int \frac{\sin^3 x}{\cos^4 x} dx = \int \frac{\sin^2 x}{\cos^4 x} \sin x \ dx = - \int \frac{1 - \cos^2 x}{\cos^4 x} d(\cos x) = \dots$
$\dots = - \int \frac{d \cos x}{\cos^4 x} + \int \frac{d \cos x}{\cos^2 x} = -\frac{\cos^{-3} x}{-3} + \frac{\cos^{-1} x}{-1} = \dots$
$\dots = \frac{1}{3 \cos^3 x} - \frac{1}{\cos x}$
### 2100

$\int \tan^5 x \ dx = \int \frac{\sin^5 x}{\cos^5 x} \ dx = \frac{(1 - cos^2 x)^2 \sin x}{\cos^5 x} dx = \dots$
$t = \cos x$, $d t = -\sin x dx$
$\dots = \int \frac{-(1 - t^2)^2 d t}{t^5} = - \int \frac{t^4 - 2t^2 + 1}{t^5} dt = - \int \frac{dt}{t^5} + \int \frac{2 \ dt}{t^3} - \int \frac{dt}{t} = \dots$
$\dots = \frac{1 - 4\cos x}{4\cos^4 x} - \ln |\cos x|$
### 2110

$\int \frac{d x}{5 - 3 \cos x} = \dots$
$t = \tan \frac{x}{2}$, $x = 2 \arctan t$
$d x = \frac{2 d t}{1 + t^2}$, $\cos x = \frac{1 - t^2}{1 + t^2}$

$\dots = \int \frac{\frac{2 d t}{1 + t^2}}{5 - 3 \frac{1 - t^2}{1+t^2}} = \int \frac{2 d t}{5 + 5t^2 - 3 + 3t^2} = \frac{1}{2} \int \frac{2 d t}{8t^2 + 2} = \frac{1}{2} \int \frac{d t}{4t^2 + 1} = \dots$
$\dots = \frac{1}{2} \int \frac{d(2t)}{(2t)^2+1)} = \frac{1}{2} \arctan (2 \tan \frac{x}{2}) + C$
### 2116

$\int \frac{d x}{5 - 4 \sin x + 3 \cos x} = \dots$
$t = \tan \frac{x}{2}$, $x = 2 \arctan t$
$d x = \frac{2 d t}{1 + t^2}$, $\cos x = \frac{1 - t^2}{1 + t^2}, \sin x = \frac{2 t}{1 + t^2}$

$\dots = \int \frac{\frac{2 dt}{1 + t^2}}{5 - \frac{8 t}{1 + t^2} + \frac{3(1 - t^2)}{1 + t^2}} = \int \frac{\frac{2 d t}{1 + t^2}}{\frac{5 + 5t^2 - 8t + 3 - 3t^2}{1 + t^2}} = \int \frac{d t}{t^2 - 4t + 4} = - \frac{1}{\tan \frac{x}{2} - 2} + C$
## Двойные интегралы

$\int\limits_{D}\int f(x, y) \ d x \ d y = \int\limits_{a}^{b} \ d x (\int\limits_{\phi_2(x)}^{\phi_1(x)} f(x, y) \ dy)$

### Расставляем пределы
#### 3486

$x = 0$, $y = 0$, $x + y = 2$

Рисунок:
![[Pasted image 20230907141127.png]]

$\int\limits_{0}^{2} dx (\int\limits_{0}^{2 - x} f(x, y) \ d y)$

$\int\limits_{0}^{2} d y (\int\limits_{0}^{2 - y} f(x, y) dx)$

#### 3487

$x^2 + y^2 \le 1$, $x \ge 0$, $y \ge 0$

Рисунок:
![[Pasted image 20230907141601.png]]

$\int\limits_{0}^{1} dx (\int\limits_{0}^{\sqrt{1 - x^2}} f(x, y) \ d y)$

$\int\limits_{0}^{1} d y (\int\limits_{0}^{\sqrt{1-y^2}} f(x, y) dx)$
#### 3488

$x + y \le 1$, $x - y \le 1$, $x \ge 0$

Рисунок:
![[Pasted image 20230907142028.png]]

$\int\limits_{0}^{1} dx (\int\limits_{x-1}^{1-x} f(x, y) \ d y)$

$\int\limits_{-1}^{0} d y (\int\limits_{0}^{y+1} f(x, y) dx)$ + $\int\limits_{0}^{1} d y (\int\limits_{0}^{1-y} f(x, y) dx)$
#### 3489

$y \ge x^2$, $y \le 4 - x^2$

Рисунок:
![[Pasted image 20230907142452.png]]

$\int\limits_{-\sqrt{2}}^{\sqrt{2}} dx (\int\limits_{x^2}^{4-x^2} f(x, y) \ d y)$

$\int\limits_{0}^{2} d y (\int\limits_{-\sqrt{y}}^{\sqrt{y}} f(x, y) dx)$ + $\int\limits_{2}^{4} d y (\int\limits_{-\sqrt{4-y}}^{\sqrt{4-y}} f(x, y) dx)$
#### 3485

$x = 3$, $x = 5$, $3x - 2y + 4 = 0$, $3x - 2y + 1 = 0$

Рисунок:
![[Pasted image 20230907143108.png]]

$\int\limits_{3}^{5} dx (\int\limits_{\frac{3x + 1}{2}}^{\frac{3x + 4}{2}} f(x, y) \ d y)$
$3x - 2y + 4 = 0$, $2y = 3x + 4$, $y = \frac{3x + 4}{2}$
$3x - 2y + 1 = 0$, $2y = 3x + 1$, $y = \frac{3x + 1}{2}$

$\int\limits_{5}^{6.5} d y (\int\limits_{3}^{\frac{2y-4}{3}} f(x, y) dx) + \int\limits_{6.5}^{8} d y (\int\limits_{\frac{2y-1}{3}}^{\frac{2y-4}{3}} f(x, y) dx) + \int\limits_{8}^{9.5} d y (\int\limits_{\frac{2y-1}{3}}^{5} f(x, y) dx)$
$3x - 2y + 4 = 0$, $3x = 2y - 4$, $x = \frac{2y-4}{3}$
$3x - 2y + 1 = 0$, $3x = 2y - 1$, $x = \frac{2y-1}{3}$
## Домашнее задание, Берман

3492, 3493, 3494, 3506 (1, 2, 3), 3508
