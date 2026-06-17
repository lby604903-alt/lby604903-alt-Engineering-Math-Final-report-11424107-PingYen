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
