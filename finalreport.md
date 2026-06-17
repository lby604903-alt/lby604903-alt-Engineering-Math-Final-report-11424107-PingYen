#  11424107:Signal and System Analysis

---

## Step 1: Establish the Differential Equation

The relationship between the input signal and the output voltage is

```math
RC\frac{dy(t)}{dt}+y(t)=f(t)
```

The input signal is

```math
f(t)=\left[\sin(10t)+0.5\sin(1000t)\right]u(t)
```

The initial condition is

```math
y(0)=0
```

---

## Step 2: Substitute the Given Circuit Parameters

Given

```math
R=1000\Omega
```

```math
C=1\times10^{-6}F
```

Then

```math
RC
=
1000\times10^{-6}
=
0.001
```

Substitute into the differential equation.

```math
0.001\frac{dy(t)}{dt}
+y(t)
=
\left[\sin(10t)+0.5\sin(1000t)\right]u(t)
```

---

## Step 3: Apply the Laplace Transform

By

```math
\mathcal L
\left\{
\frac{dy(t)}{dt}
\right\}
=
sY(s)-y(0)
```

and

```math
y(0)=0
```

we obtain

```math
0.001sY(s)+Y(s)
=
\frac{10}{s^2+100}
+
\frac{500}{s^2+1000000}
```

Factor out \(Y(s)\).

```math
Y(s)(0.001s+1)
=
\frac{10}{s^2+100}
+
\frac{500}{s^2+1000000}
```


So

```math
Y(s)
=
\frac{10}{(s^2+100)(0.001s+1)}
+
\frac{500}{(s^2+1000000)(0.001s+1)}
```

---

## Step 4: Solve the First Term

Let

```math
Y_1(s)
=
\frac{10}{(s^2+100)(0.001s+1)}
```

Rewrite

```math
0.001s+1
=
\frac{s+1000}{1000}
```

Then

```math
Y_1(s)
=
\frac{10000}
{(s^2+100)(s+1000)}
```

Use partial fractions.

```math
\frac{10000}
{(s^2+100)(s+1000)}
=
\frac{As+B}{s^2+100}
+
\frac{C}{s+1000}
```

Multiply by

```math
(s^2+100)(s+1000)
```

```math
10000
=
(As+B)(s+1000)
+
C(s^2+100)
```

Expand.

```math
(A+C)s^2
+
(1000A+B)s
+
1000B+100C
=
10000
```

Compare coefficients.

```math
A+C=0
```

```math
1000A+B=0
```

```math
1000B+100C=10000
```
---

## Step 5: Solve the Second Term

Let

```math
Y_2(s)
=
\frac{500}{(s^2+1000000)(0.001s+1)}
```

Rewrite

```math
0.001s+1
=
\frac{s+1000}{1000}
```

Then

```math
Y_2(s)
=
\frac{500000}
{(s^2+1000000)(s+1000)}
```

Use partial fractions.

```math
\frac{500000}
{(s^2+1000000)(s+1000)}
=
\frac{Ds+E}{s^2+1000000}
+
\frac{F}{s+1000}
```

Multiply both sides by

```math
(s^2+1000000)(s+1000)
```

```math
500000
=
(Ds+E)(s+1000)
+
F(s^2+1000000)
```

Expand.

```math
(D+F)s^2
+
(1000D+E)s
+
1000E
+
1000000F
=
500000
```

Compare coefficients.

```math
D+F=0
```

```math
1000D+E=0
```

```math
1000E+1000000F=500000
```

Solve the equations.
