- [ジョーンズベクトル](#ジョーンズベクトル)
- [ジョーンズベクトルの見方](#ジョーンズベクトルの見方)
- [直線偏光](#直線偏光)
- [円偏光](#円偏光)
- [ジョーンズ行列](#ジョーンズ行列)
  - [補足](#補足)
- [1/2波長板](#12波長板)
- [1/4波長板](#14波長板)
- [直線偏光子](#直線偏光子)
- [具体的な使い道](#具体的な使い道)
  - [HWPをPBSの前に置く](#hwpをpbsの前に置く)
  - [表から透過させたあとに裏から透過させる](#表から透過させたあとに裏から透過させる)
- [SLM](#slm)


## ジョーンズベクトル

電場を $x$ 軸(水平方向), $y$ 軸(垂直方向)に分けて考えてみます.

ベクトルで表すと

$$
\vec{E} = 
\begin{bmatrix}
E_{x0} e^{i\phi_x} \newline
E_{y0} e^{i\phi_y}
\end{bmatrix} \quad (1.1)
$$

と書けます.

これは1941年にアメリカの物理学者ジョーンズ(R. Clark Jones)によって考案されたもので **ジョーンズベクトル** と言い,上式のように書くことで偏光状態を **複素ベクトル** によって表すことができます. $x,y$ 成分の振幅や位相の違いによって色々な偏光状態が表されます.

ここで **※全体にかかる振幅の大きさや位相は偏光の状態に影響しない** ことに注意してくださいこれは

- 全体にかかる振幅とは、例えば水平方向に振動している電場の振動の幅が変わるだけで水平であるという形は変わらない.
- 全体にかかる位相とは、例えば水平方向に振動している電場をどの瞬間から観測するのか(右に一番振れているところから観測するのか,左に一番振れているところから観測するのか)の違いであり物理的にはどちらも同じ電場を表している.

ということに対応しています.つまり $(1.1)$ 式は

$$
\vec{E}=E _ {x0} e^{i\phi _ x}
\begin{bmatrix}
1 \newline
\frac{E _ {y0}}{E _ {x0}} e^{i(\phi _ y-\phi _ x)}
\end{bmatrix}\propto
\begin{bmatrix}
1 \newline
a e^{i\delta}
\end{bmatrix}
$$

- $a = \frac{E _ {y0}}{E _ {x0}}$
- $\delta = \phi _ y-\phi _ x$

としても **同じ偏光状態** を表しているということです.

<div style="page-break-before:always"></div>

## ジョーンズベクトルの見方

ジョーンズベクトルは複素ベクトルであるので成分だけで見るとどのような偏光状態を表しているかは一目ではわからないです.そこでこのベクトルが時間変化したときにどのような形になるかを考えます.時間変化を見たいので $e^{i\omega t}$ をかけます.

$$
\vec{E}=e^{i\omega t}
\begin{bmatrix}
E_{x0} e^{i\phi_x} \newline
E_{y0} e^{i\phi_y}
\end{bmatrix}
$$

次にこのベクトルを実部と虚部に分けます.

$$
\vec{E}=
\begin{bmatrix}
E_{x0}[\cos{\omega t}\cos{\phi _ x}-\sin{\omega t}\sin{\phi _ x}+i(\cos{\omega t}\sin{\phi _ x}+\sin{\omega t}\cos{\phi _ x})] \newline
E_{y0}[\cos{\omega t}\cos{\phi _ y}-\sin{\omega t}\sin{\phi _ y}+i(\cos{\omega t}\sin{\phi _ y}+\sin{\omega t}\cos{\phi _ y})] 
\end{bmatrix}
$$

最後に実部をとり $t$ を変化させたときのベクトルの軌跡を見れば良いです.つまり

$$
Re(\vec{E})=
\begin{bmatrix}
E_{x0}(\cos{\omega t}\cos{\phi _ x}-\sin{\omega t}\sin{\phi _ x}) \newline
E_{y0}(\cos{\omega t}\cos{\phi _ y}-\sin{\omega t}\sin{\phi _ y}) 
\end{bmatrix} \quad (2.1)
$$

の軌跡を考えます.

そもそも波を複素数で表現するのは実部だけ( $\cos$ だけ)で考えると計算が面倒になるという問題を解決するためだったので最終的には実部を取るというのは理にかなっています.

次の項からは代表的な偏光状態について考えます.

<div style="page-break-before:always"></div>

## 直線偏光

$(1.1)$ 式において $x,y$ 成分の位相が共に等しいとき,つまり

$$
\phi_y = \phi_x
$$

の場合を考えます.軌跡を考えるベクトルは

$$
\begin{aligned}
Re(\vec{E})
&=
\begin{bmatrix}
E_{x0}(\cos{\omega t}\cos{\phi _ x}-\sin{\omega t}\sin{\phi _ x}) \newline
E_{y0}(\cos{\omega t}\cos{\phi _ x}-\sin{\omega t}\sin{\phi _ x}) 
\end{bmatrix} \newline
&=
\begin{bmatrix}
E_{x0}\cos{(\omega t+\phi _ x)} \newline
E_{y0}\cos{(\omega t+\phi _ x)}
\end{bmatrix} \newline
\therefore Re(\vec{E})
&=
\cos{(\omega t+\phi _ x)}
\begin{bmatrix}
E_{x0} \newline
E_{y0}
\end{bmatrix}
\end{aligned}
$$

$x,y$ 成分に位相差はないので振幅の比によって偏光状態が決まります.また, $t$ を変化させてこのベクトルの軌道を見てもこれらの成分の比は変わらないので直線に変化します.この偏光状態を直線偏光と言います.

## 円偏光

次に振幅が等しく,x成分の位相 $\delta _ x$ ,y成分の位相 $\delta _ y$ が $\delta = \delta _ y - \delta _ x$ だけ遅れている場合を考えます.まず

$$
\delta = \frac{\pi}{2}
$$

の場合を考えます.

$$
\phi_y = \phi_x + \frac{\pi}{2}
$$

であるのでこれを(2.1)に代入すると

$$
\begin{aligned}
  Re(\vec{E})&=
  \begin{bmatrix}
    E_{x0}(\cos{\omega t}\cos{\phi _ x}-\sin{\omega t}\sin{\phi _ x}) \newline
    E_{y0}(\cos{\omega t}\cos{\phi _ y}-\sin{\omega t}\sin{\phi _ y}) 
  \end{bmatrix} \newline
    &=E _ {x0}
  \begin{bmatrix}
    \cos{\omega t}\cos{\phi _ x}-\sin{\omega t}\sin{\phi _ x} \newline
    \cos{\omega t}\cos{(\phi _ x+\frac{\pi}{2})}-\sin{\omega t}\sin{(\phi _ x+\frac{\pi}{2})}
  \end{bmatrix} \newline
    &=E _ {x0}
  \begin{bmatrix}
    \cos{\omega t}\cos{\phi _ x}-\sin{\omega t}\sin{\phi _ x} \newline
    -\cos{\omega t}\sin{\phi _ x}-\sin{\omega t}\cos{\phi _ x}
  \end{bmatrix} \newline
    \therefore Re(\vec{E})&=
    E _ {x0}
  \begin{bmatrix}
    \cos{\omega t} \newline
    -\sin{\omega t}
  \end{bmatrix}
\end{aligned}
$$

任意の $\phi _ x$ について成り立つので $\phi _ x=0$ としました.この軌道は右回りの円になるのでこれは **右回り円偏光** となります.

また(1.1)に代入するとジョーンズベクトルは

$$
\begin{aligned}
  \vec{E}
    &=E_{x0}
  \begin{bmatrix}
    e^{i \varphi_x} \newline
    e^{i (\varphi_x + \frac{\pi}{2})}
  \end{bmatrix} \newline
    &= E_{x0} e^{i\varphi_x}
  \begin{bmatrix}
    1 \newline
    e^{i\frac{\pi}{2}}
  \end{bmatrix} \newline
    &= E_{x0} e^{i\varphi_x} \newline
  \therefore \vec{E} &=E_{x0} e^{i\varphi_x}
  \begin{bmatrix}
    1 \newline
    i
  \end{bmatrix} \newline
\end{aligned}
$$

となるのでこのジョーンズベクトルは右回り円偏光を表していることが分かりました.

次に

$$
\delta = -\frac{\pi}{2}
$$

の場合を考えます.同様に計算すると

$$
\begin{aligned}
  Re(\vec{E})&=
  \begin{bmatrix}
    E_{x0}(\cos{\omega t}\cos{\phi _ x}-\sin{\omega t}\sin{\phi _ x}) \newline
    E_{y0}(\cos{\omega t}\cos{\phi _ y}-\sin{\omega t}\sin{\phi _ y}) 
  \end{bmatrix} \newline
    &=E _ {x0}
  \begin{bmatrix}
    \cos{\omega t}\cos{\phi _ x}-\sin{\omega t}\sin{\phi _ x} \newline
    \cos{\omega t}\cos{(\phi _ x-\frac{\pi}{2})}-\sin{\omega t}\sin{(\phi _ x-\frac{\pi}{2})}
  \end{bmatrix} \newline
    &=E _ {x0}
  \begin{bmatrix}
    \cos{\omega t}\cos{\phi _ x}-\sin{\omega t}\sin{\phi _ x} \newline
    \cos{\omega t}\sin{\phi _ x}+\sin{\omega t}\cos{\phi _ x}
  \end{bmatrix} \newline
    \therefore Re(\vec{E})&=
    E _ {x0}
  \begin{bmatrix}
    \cos{\omega t} \newline
    \sin{\omega t}
  \end{bmatrix}
\end{aligned}
$$

となりこれは **左回り円偏光** となります.

$$
\begin{aligned}
  \vec{E}
    &=E_{x0}
  \begin{bmatrix}
    e^{i \varphi_x} \newline
    e^{i (\varphi_x - \frac{\pi}{2})}
  \end{bmatrix} \newline
    &= E_{x0} e^{i\varphi_x}
  \begin{bmatrix}
    1 \newline
    e^{-i\frac{\pi}{2}}
  \end{bmatrix} \newline
    &= E_{x0} e^{i\varphi_x} \newline
  \therefore \vec{E}&=E_{x0} e^{i\varphi_x}
  \begin{bmatrix}
    1 \newline
    -i
  \end{bmatrix} \newline
\end{aligned}
$$

となりこのジョーンズベクトルは左回り円偏光を表していることが分かりました.

## ジョーンズ行列

偏光状態を変えるということはジョーンズベクトルを異なるジョーンズベクトルに変換することだと言えます.

この変換を実現させる方法として **波長板** というものがあります.

2成分ベクトルを変換させるということはこの波長板という素子は $2 \times 2$ の行列であると予想されます.この行列を**ジョーンズ行列**と言います.

また,波長板は遅相子(retardar)と呼ばれ,2つの直交する電場の一方の位相を変化させます.以下の説明では

y成分の位相が遅れるように(x成分の位相が進むように)方向を選びます.このときyを遅相軸,xを進相軸と呼びます.

それぞれの位相を独立に変化させるので行列の非対角成分は0になると予想できます.つまり

$$
\begin{aligned}
J &=
\begin{bmatrix}
e^{i\varphi_x} & 0 \newline
0 & e^{i\varphi_y}
\end{bmatrix} \newline
&= e^{i\varphi_x}
\begin{bmatrix}
1 & 0 \newline
0 & e^{i(\varphi_y - \varphi_x)}
\end{bmatrix} \newline
\therefore J &= e^{i\varphi_x}
\begin{bmatrix}
1 & 0 \newline
0 & e^{i\delta}
\end{bmatrix} \newline
\end{aligned}
$$

となります.

偏光素子では位相差をどのくらい与えるのだけが重要なのであると述べたのでこれを全体にかかる係数を省略して

$$
J =
\begin{bmatrix}
1 & 0 \newline
0 & e^{i\delta}
\end{bmatrix}
$$

とします.また,偏光子はx-y平面で $\theta$ 傾けるという自由度があり,$\theta$ だけ回転させるとジョーンズ行列は

$$
\begin{aligned}
J &=
\begin{bmatrix}
\cos{\theta} & -\sin{\theta} \newline
\sin{\theta} & \cos{\theta}
\end{bmatrix}
\begin{bmatrix}
1 & 0 \newline
0 & e^{i\delta}
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \newline
-\sin{\theta} & \cos{\theta}
\end{bmatrix} \newline
&= 
\begin{bmatrix}
\cos{\theta} & -e^{i\delta} \sin{\theta} \newline
\sin{\theta} & e^{i\delta} \cos{\theta}
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \newline
-\sin{\theta} & \cos{\theta}
\end{bmatrix} \newline
\therefore J &= 
\begin{bmatrix}
e^{i\delta} \sin^2{\theta} + \cos^2{\theta} & \sin{\theta} \cos{\theta} (1 - e^{i\delta}) \newline
\sin{\theta} \cos{\theta} (1 - e^{i\delta}) & \sin^2{\theta} + e^{i\delta} \cos^2{\theta}
\end{bmatrix} \quad (5.1) \newline
\end{aligned}
$$

となります.この $\delta$ の違いによって波長板の種類が変わっていきます.

### 補足

ここでこの行列の転置をとって複素共役をとったものと元の行列を掛けてみると

$$
J \cdot J ^{\dagger }=
\begin{bmatrix}
1 & 0 \newline
0 & e^{i\delta}
\end{bmatrix}
\begin{bmatrix}
1 & 0 \newline
0 & e^{-i\delta}
\end{bmatrix}=
\begin{bmatrix}
1 & 0 \newline
0 & 1
\end{bmatrix}
$$

となり,これは単位行列になります.

つまり偏光素子を行列で表したものは**ユニタリー行列**であることが分かります.

## 1/2波長板

位相差を $\delta=\pi$ 与えるものを **1/2波長板(HWP:Half Wave Plate)** と言います.

前項で導出した(5.1)式に代入してみると

$$
\begin{aligned}
J_{HWP(\theta)} &=
\begin{bmatrix}
-\sin^2{\theta} + \cos^2{\theta} & 2\sin{\theta} \cos{\theta} \newline
2\sin{\theta} \cos{\theta} & \sin^2{\theta} - \cos^2{\theta}
\end{bmatrix} \newline
\therefore J_{HWP(\theta)} &= 
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix}
\end{aligned}
$$

となります.

例えば $\theta = 0$ のときは

$$
J_{HPW(\theta=0)} =
\begin{bmatrix}
1 & 0 \newline
0 & -1
\end{bmatrix}
$$

というジョーンズ行列になります.非対角成分は0で1行1列成分は1,2行2列成分は-1であるのでこれはy成分を反転する働きをします.

例えば $\frac{\pi}{4}$ だけ傾いた直線偏光

$$
\vec{E}_{in} = 
\begin{bmatrix}
1 \newline
1
\end{bmatrix}
$$

を入射させると

$$
\vec{E}_{out} = 
\begin{bmatrix}
1 \newline
-1
\end{bmatrix}
$$

となり, $-\frac{\pi}{4}$ だけ傾いた直線偏光に変化します.

元の状態から時計回りに $2 \times \frac{\pi}{4}$ だけ回転している。

となる。

また, $\theta = \frac{\pi}{4}$ だけ回転させると

$$
J_{HWP(\theta=\frac{\pi}{4})} =
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}
$$

となり **x,y成分を交換する** という働きをします.

## 1/4波長板

位相差を $\delta=\frac{\pi}{2}$ 与えるものを **1/4波長板(HWP:Quarter Wave Plate)** と言います.先ほどと同様に計算すると

$$
\begin{aligned}
J_{QWP(\theta)} &=
\begin{bmatrix}
e^{i \frac{\pi}{2}} \sin^2{\theta} + \cos^2{\theta} & \sin{\theta} \cos{\theta} (1 - e^{i \frac{\pi}{2}}) \newline
\sin{\theta} \cos{\theta} (1 - e^{i \frac{\pi}{2}}) & \sin^2{\theta} + e^{i \frac{\pi}{2}} \cos^2{\theta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
i \sin^2{\theta} + \cos^2{\theta} & \sin{\theta} \cos{\theta} (1 - i) \\
\sin{\theta} \cos{\theta} (1 - i) & \sin^2{\theta} + i \cos^2{\theta}
\end{bmatrix} \newline
\therefore J_{QWP(\theta)}
&=
\begin{bmatrix}
1 - i\cos{2\theta} & -i\sin{2\theta} \newline
-i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix}
\end{aligned}
$$

となります.

 $\theta = 0$ のときは

$$
J_{QWP(\theta=0)} =
\begin{bmatrix}
1 & 0 \newline
0 & i
\end{bmatrix}
$$

となります.x成分はそのままでy成分を $\frac{\pi}{2}(e^{\frac{\pi}{2}}=i)$ 遅らせる働きをします.

例えばここに $\frac{\pi}{4}$ 傾いた直線偏光

$$
\vec{E}_{in} = 
\begin{bmatrix}
1 \newline
1
\end{bmatrix}
$$

を入射させると

$$
\vec{E}_{out} = 
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
$$

となり右回り円偏光に変化します.

## 直線偏光子

任意の角度の直線偏光のみを通す光学素子を直線偏光子と言います.x成分のみを押す時を $\theta=0$ とすると

$$
\begin{aligned}
J _ {LP(\theta)} &=
\begin{bmatrix}
\cos{\theta} & -\sin{\theta} \newline
\sin{\theta} & \cos{\theta}
\end{bmatrix}
\begin{bmatrix}
1 & 0 \newline
0 & 0
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \newline
-\sin{\theta} & \cos{\theta}
\end{bmatrix} \newline
&= 
\begin{bmatrix}
\cos{\theta} & 0 \newline
\sin{\theta} & 0
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \newline
-\sin{\theta} & \cos{\theta}
\end{bmatrix} \newline
\therefore J _ {LP(\theta)} &= 
\begin{bmatrix}
\cos^2{\theta} & \sin{\theta} \cos{\theta} \newline
\sin{\theta} \cos{\theta} & \sin^2{\theta}
\end{bmatrix} \newline
\end{aligned}
$$

となります.
$\frac{\pi}{4}$ 傾ければ

$$
J _ {LP(\theta = \frac{\pi}{4})}=
\begin{bmatrix}
1 & 1 \newline
1 & 1
\end{bmatrix}
$$

となりx,y成分をそれぞれ足したものが新たなx,y成分になります.

<div style="page-break-before:always"></div>

## 具体的な使い道

ここでは先ほど紹介した光学素子の具体的な使い方を見ていきます.

### HWPをPBSの前に置く

$\theta$ 回転している1/2波長板のジョーンズ行列は

$$
\begin{aligned}
J_{HWP(\theta)} &=
\begin{bmatrix}
-\sin^2{\theta} + \cos^2{\theta} & 2\sin{\theta} \cos{\theta} \newline
2\sin{\theta} \cos{\theta} & \sin^2{\theta} - \cos^2{\theta}
\end{bmatrix} \newline
\therefore J_{HWP(\theta)} &= 
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix}
\end{aligned}
$$

だったので例えばここに45度傾いた直線偏光を入射させると

$$
\begin{aligned}
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
&=
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix}
\begin{bmatrix}
1 \newline
1
\end{bmatrix}
\end{aligned}
$$

となります.例えばHWPの角度 $\theta$ を22.5度傾けたとすると

$$
J _ {HWP(\frac{\pi}{8})}=\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 & 1 \newline
1 & -1
\end{bmatrix}
$$

というジョーンズ行列になるので

$$
\begin{aligned}
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
&=
\begin{bmatrix}
1 & 1 \newline
1 & -1
\end{bmatrix}
\begin{bmatrix}
1 \newline
1
\end{bmatrix} \newline
\therefore
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
&=
\begin{bmatrix}
2 \newline
0
\end{bmatrix}
=2
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
\end{aligned}
$$

となり時計回りに $2\theta=45$ 度傾くので $x$ 偏光成分のみになります.このように任意の角度の直線偏光を任意の角度の直線偏光に変化させることができます.

### 表から透過させたあとに裏から透過させる

次に $\theta$ 回転させた1/2波長板,1/4波長板に光を透過させたあとすぐに後ろから透過させます.表で透過した後,ミラーで反射して今度は裏から透過させます.裏から透過させるときは回転角が $\pi-\theta$ となるので

1/2波長板は

$$
\begin{aligned}
J _ {HWP} &=
\begin{bmatrix}
\cos{2(\pi-\theta)} & \sin{2(\pi-\theta)} \newline
\sin{2(\pi-\theta)} & -\cos{2(\pi-\theta)}
\end{bmatrix}
\begin{bmatrix}
-1 & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
-\cos{2\theta} & -\sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix}
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
-\cos^2{2\theta}-\sin^2{2\theta} & 0 \newline
0 & \sin^2{2\theta}+\cos^2{2\theta}
\end{bmatrix} \newline
\therefore J _ {HWP} &=
\begin{bmatrix}
-1 & 0 \newline
0 & 1
\end{bmatrix}
\end{aligned}
$$

のように回転角 $\theta$ に依存せずx成分を反転する働きをすることが分かります.見る方向が変わった(x成分が反転した)だけなので,ミラーを抜きにすれば偏光状態をなにも変えないという働きをします.

次に1/4波長板について考えます.

$$
\begin{aligned}
J _ {QWP(\theta)}&=
\begin{bmatrix}
1 - i\cos{2(\pi-\theta)} & -i\sin{2(\pi-\theta)} \newline
-i\sin{2(\pi-\theta)} & 1 + i\cos{2(\pi-\theta)}
\end{bmatrix}
\begin{bmatrix}
-1 & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 - i\cos{2\theta} & -i\sin{2\theta} \newline
-i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
-1+i\cos{2\theta} & i\sin{2\theta} \newline
-i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix}
\begin{bmatrix}
1 - i\cos{2\theta} & -i\sin{2\theta} \newline
-i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos^2{2\theta}-1+2i\cos{2\theta}+\sin^2{2\theta} & i\sin{2\theta}+\sin{2\theta}\cos{2\theta}-\sin{2\theta}\cos{2\theta} \newline
-i\sin{2\theta}-\sin{2\theta}\cos{2\theta}-i\sin{2\theta}+\sin{2\theta}\cos{2\theta} & -\sin^2{2\theta}+1+2i\cos{2\theta}\cos^2{2\theta}
\end{bmatrix} \newline
\therefore J _ {QWP(\theta)} &= 2i
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
-\sin{2\theta} & \cos{2\theta}
\end{bmatrix}
\end{aligned}
$$

となります.例えば $\theta = \frac{\pi}{4}$ では

$$
J _ {1/4} \propto
\begin{bmatrix}
0 & 1 \newline
-1 & 0
\end{bmatrix}
$$

となりx,y成分を交換後y成分を反転させる働きをします.

## SLM

メーカーによって異なりますがここではx成分のみ変調(遅らせる)反射型のSLMを考えます.ジョーンズ行列は

$$
J _ {SLM}=
\begin{bmatrix}
-e^{i\delta(x, y)} & 0 \newline
0 & 1
\end{bmatrix}
$$

となります.(1,1)成分にマイナスがつきますがこれは反射型であるためです.光を迎える側から光の振動方向を考えるので反射する前と後で水平方向の軸が反転します.

また $\delta(x,y)$ についてですが,SLMは $[0, 2\pi]$ までを諧調数(大体1024)で割った値で位相を与えることができます.つまり1024諧調なら $0rad, 0.00614rad, \cdots$ のように変化させることができるということです.さらに1ピクセルごとにその変調量を変えることができます. 

次にSLMによってジョーンズベクトルがどのように変わるかを考えます.

<!-- 通常,SLM自体は回転させずにビームの偏光状態を調節するので波長板と違って $\theta$ の自由度はないです. -->

$$
\begin{aligned}
  \begin{bmatrix}
    \alpha' \newline
    \beta'
  \end{bmatrix}
  &=
  \begin{bmatrix}
    -e^{i\delta(x,y)} & 0 \newline
    0 & 1
  \end{bmatrix}
  \begin{bmatrix}
    \alpha \newline
    \beta
  \end{bmatrix} \newline
  &=
  \begin{bmatrix}
    -\alpha e^{i\delta(x,y)} \newline
    \beta
  \end{bmatrix}\newline
\end{aligned}
$$

$$
\therefore
\begin{bmatrix}
  \alpha' \newline
  \beta'
\end{bmatrix}
=\begin{bmatrix}
  -(Re(\alpha)\cos{\delta(x,y)}-Im(\alpha)\sin{\delta(x,y)}+i(Re(\alpha)\sin{\delta(x,y)}+Im(\alpha)\cos{\delta(x,y)})) \\
  Re(\beta)+iIm(\beta)
\end{bmatrix}
$$

となります.

ここで先ほどの波長板や直線偏光子と比べてみます.ピクセルごとに位相を変調できるのはSLMだけですが1024諧調の位相を変調できるとはどういうことでしょうか？

$\theta$ 回転させた波長板のジョーンズ行列は(5.1)式より

$$
J=\begin{bmatrix}
e^{i\delta} \sin^2{\theta} + \cos^2{\theta} & \sin{\theta} \cos{\theta} (1 - e^{i\delta}) \newline
\sin{\theta} \cos{\theta} (1 - e^{i\delta}) & \sin^2{\theta} + e^{i\delta} \cos^2{\theta}
\end{bmatrix}
$$

であったので $\theta=\frac{\pi}{2}$ を代入すると

$$
J=\begin{bmatrix}
e^{i\delta} & 0 \newline
0 & 1
\end{bmatrix}
$$

となります. $\theta=\frac{\pi}{2}$ とは進相軸(ここではx軸)と遅相軸(ここではy軸)を入れ替えることに相当するので反射のことを考えなければSLMも1ピクセルごとに波長板が埋められている素子と考えることができます.例えば先ほど書いたように諧調数が1024の場合, $\frac{n}{1024} (n=1, 2, \cdots, 1024)$ 波長板と解釈することができます.例えば $n=512$ なら1/2波長板ですし $n=256$ なら1/4波長板です.radで表すならこれに $2\pi$ をかければよく $\frac{2\pi n}{1024}rad$ 変調させる素子と言えます.
