# Up For A Little Challenge

I began by downloading the original image:

![Begin Hack](assets/Begin%20Hack.jpg "BBegin Hack.jpg")

My first step was to try extracting any hidden text from it. I started with Aperi'Solve to check the image metadata, but it didn’t reveal anything particularly useful. Next, I switched to WSL and ran the following command:

```sh
strings "Begin Hack.jpg"
```

This produced a long output:

```
JFIF
Exif
8Photoshop 3.0
8BIM
8BIM
S@%c
&T6d
'E7e
()*89:HIJWXYZghijwxyz
0"2Q
3#aB
c6p&ET
()*789:FGHIJUVWXYZdefghijstuvwxyz
mQ15
TLMm
[m[mQ15
*tMD
"k4J
Rs]n
<zbpM
;ELN
*gEN
=a?6m
bj'j
:5LN
[m[m[mZ4
_|RW
zgm19
-{{?_
:UWXV
A_~{
[mRQ.
MtMm
_b|g
)bum
Q;TLMm
j&5i
\_s5sH
mQ:j6
mQ15
[mFw\j
y0X,
Yyrx
        iKJ
DC(jC)dwC
?HxC
Cl|G
/sPj
MJ,h`
550]
4KvwUp
QYj,
n7~$N[$
-g0L
Gmu5
i*iSJ
]ZIsk
g<W1M
LE4l^\
wdc.)
:}^Xs
ML      ~
1bdM;V
Lub
%)p_
d(3D
gqm6
[y|7
Qoq-
)kAO
j.YJ
t)9m
U>iy
}p.<E1
.Xm5
Yu>6p
_f;>Yd$W
&MBo
X?$6
bjCL
k)p$
W&YL
19b$
^8/_
l',r
%pRG
H4\p
R/C,^
7l#Y
Oi?h
w       +V
|^7V*
QXmG5_?
/E'C
.$%er
o%))
:?ab
y+q\
5O9e?%j?
_&j"
1,G$+
CS@?
*zHr
Z#8CLQ_$#
1exh
1yjyw(
'Trj
`- https://mega.nz/#!z8hACJbb!vQB569ptyQjNEoxIwHrUhwWu5WCj1JWmU-OFjf90Prg -N17hGnFBfJliykJxXu8 -
=u}B
{Y4B
R_:/
/bTK
T8(w
}SPF*
.YRi,
m%<p
7<S:
CdRR
5Ol=
7Ge'
!1AQaq
 0@P`p
rK2*
=611y
*E%9
M`H0X_
_W]y
!{u~
        $V/
r%LL
;3;;
vj54
=}pW
5p^-
?s$X0?]
4@a4
=reg#
9*fL'
Mp real_unlock_key: Nothing Is As It SeemsU
~t>?
pb}X8a
;>)I$
A16hM
O9]F
K_Es
OQcc
{8OI
<T|pF
t<?EK*
)#0=n
b_74
^x<sN
1u{k
Nitr
b9R6
(Q{T
 F>_
bK(1
c       <AI<a
JxAD
AQa q
0@P`p
]!ql>
-L_Q
c<gg
c='I
_l2A5
5~Fh
89]M}+
^Jx(
)_4b
LQ")
zy=>
n66k
NuHPO
;(hO
+vU8*
+CL@
NiiJo
"Y#).3
kw]}
1|yq
UB!1/OV1
nt }
0+<$<
:Rgh
Qo"P
?a>^
)gN0e&W
Xzbg
T       7JA
        bZ<R
N: r@
%r",r
 #=#
U@!e
H/ga
8HK/
iPi5
|XPr
yJ6P
KeMLx
bQvs
MSU}
"*OL
Y@dmf
J\yE
%PEuW
yDYUE
 password: Really? Again
3oC=
S MWX
lwPBj
XR0W'
@t-%
flag{Not_So_Simple...}
?@};
7b,,*
W*)^
#zZ&
 Oqq
uS%f
yB1+!
w)%     >
y:O     @
tt'8
1F?jn
;'"K
|q=_
=U$a
FS      `
8nzo    a~
Trqe@
(~CK9&
Jq$?
@a:O>
ea!%!
e$Ef
yQ(u$65
4"<
s^)V
```

Among all the noise, one thing immediately stood out, the [link](https://mega.nz/#!z8hACJbb!vQB569ptyQjNEoxIwHrUhwWu5WCj1JWmU-OFjf90Prg-N17hGnFBfJliykJxXu8). Following the link downloaded a ZIP archive named `Up For A Little Challenge.zip`.

I extracted the archive using WinRAR and viewed all contents, including hidden files in File Explorer. Inside, I found a folder named `Did I Forget Again_` containing two files:

- `.Processing.cerb4`

- `Loo Nothing Becomes Useless ack.jpg`

The `.jpg` file didn’t seem significant, but the `.Processing.cerb4` file caught my attention. Inspecting its raw content revealed a reference to `skycoder.jpg`, suggesting it was actually a compressed file.

![Loo Nothing Become Useless ack.jpg](assets/Did%20I%20Forget%20Again_/Loo%20Nothing%20Becomes%20Useless%20ack.jpg "Loo Nothing Becomes Useless ack.jpg")

I then renamed the file to .zip, entered the password: `Nothing Is As It Seems`, and extracted it again using WinRAR. Inside was `skycoder.jpg`, and in the bottom-right corner of the image, the text `flag{hack_complete}` was clearly visible.

![skycoder.jpg](assets/Did%20I%20Forget%20Again_/.Processing/skycoder.jpg "skycoder.jpg")

