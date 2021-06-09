## Lineare Algebra

Die entsprechenden Code-Schnipsel in die Sagemath-Zelle einfügen

[Sagemath-Zelle](https://sagecell.sagemath.org/)


### Multiplikation Matrix mit Vektor
```
latex.matrix_delimiters(left='[', right=']')    
A = matrix([[1,-5,-2],[2,-1,-1],[0,9,3]])        
v = vector([1,2,3])
pretty_print(A, Matrix(v).T, ' = ', Matrix(A * v).T)   
```


### Multiplikation zweier Matrizen
```
latex.matrix_delimiters(left='[', right=']')     
A = matrix([[1,-5,-2],[2,-1,-1],[0,9,3]])        
B = matrix([[1,2,1,0],[0,2,3,1],[1,1,2,-1]])
pretty_print(A, ' * ', B, ' = ', A * B)
```


### Lösung Ax = b 
```
A = Matrix([[1,1,-2],[1,-1,2],[3,1,0]])
b = vector([0,2,2])
A.solve_right(b)
```


### Elimination
Zunächst wird die augmentierte Matrix gebildet. Dann erfolgt die 
schrittweise Elimination. Die jeweilige Zeile wird durch eine Linearkombination von Zeilen ersetzt.
Der Zeilen-Index beginnt bei 0. D.h. in *set_row(1,...)*  wird Zeile 2 gesetzt.

```
latex.matrix_delimiters(left='[', right=']')
A = Matrix([[2,1,-2],[-1,-2,2],[3,0,-1]])
b = vector([-2,9,7])
A = A.augment(b,subdivide=True)
pretty_print(A)

A.set_row(1,A.linear_combination_of_rows((1,2,0)))    
pretty_print(A)
A.set_row(2,A.linear_combination_of_rows((-3,0,2)))  
pretty_print(A)
A.set_row(2,A.linear_combination_of_rows((0,-1,1)))  
pretty_print(A)
```

