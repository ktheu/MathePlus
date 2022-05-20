## Gleichungen

Die entsprechenden Code-Schnipsel in die Sagemath-Zelle einfügen

[Sagemath-Zelle](https://sagecell.sagemath.org/)

### Gleichungen lösen

```
var('x')
eq = x^3-10*x^2+31*x-30            # Nullstellen
solve(eq,x)
```

### Ungleichungen lösen

```
var('x')
eq = 2/(x-1) > 1/x
solve(eq,x)
```

### Polynomdivision

```
var('x')
f(x) =2 *x^3+4*x^2-2*x-4
g(x) = (x-1)
f.maxima_methods().divide(g)

Output:
[2*x^2 + 6*x + 4, 0]      # die 0 bedeutet: die Polynomdivision geht auf

```

```
var('x')
f(x) = x^3-x^2+3*x-3
g(x) = x-2
f.maxima_methods().divide(g)

Output:
[x^2 + x + 5, 7]         # die 7 ist der Rest bei der Polynomdivision

```

### Funktionen plotten

```
var('x')
f(x) = (x-2)^2+3
plot(f(x),(x,-2,6),ymin=0,ymax=20)
```

Mehrere Funktionen plotten

```
var('x')
f(x) = x/(x+3)
g(x) = (5*x+1)/(2*x)
plot([f(x),g(x)],(x,-10,10),ymin=-5,ymax=5)
```
