# More Computations With Octave


<h1></h1>

<p></p>

<img src="images1/" alt="api">
<img src="images1/" alt="api">
<img src="images1/" alt="api">
<img src="images1/" alt="api">


```
>> A = [1 2; 3 4; 5 6]
A =

   1   2
   3   4
   5   6

>> B = [11 12; 13 14; 15 16]
B =

   11   12
   13   14
   15   16

>> C = [1 1; 2 2]
C =

   1   1
   2   2



```

<p></p>

```
>> A*C
ans =

    5    5
   11   11
   17   17



```

<p></p>

```
>> A .* B
ans =

   11   24
   39   56
   75   96



```

<p></p>

```
>> A .^ 2
ans =

    1    4
    9   16
   25   36

>> v = [1; 2; 3]
v =

   1
   2
   3
   


```

<p></p>

```
>> 1 ./ v
ans =

   1.00000
   0.50000
   0.33333

>> 1 ./ A
ans =

   1.00000   0.50000
   0.33333   0.25000
   0.20000   0.16667



```

<p></p>

```
>> log(v)
ans =

   0.00000
   0.69315
   1.09861

>> exp(v)
ans =

    2.7183
    7.3891
   20.0855



```

<p></p>

```

>> abs([-1; 2; -3])
ans =

   1
   2
   3



```

<p></p>

```
>> -v
ans =

  -1
  -2
  -3



```

<p></p>

```
>> v + ones(length(v),1)
ans =

   2
   3
   4
   


```

<p></p>

```

>> length(v)
ans =  3
>> ones(3,1)
ans =

   1
   1
   1

>> v+1
ans =

   2
   3
   4




```

<p></p>

```
>> A
A =

   1   2
   3   4
   5   6

>> A'
ans =

   1   3   5
   2   4   6

```

<p></p>

```
>> (A')'
ans =

   1   2
   3   4
   5   6

```

<p></p>

```


>> a = [1 15 2 0.5]
a =

    1.00000   15.00000    2.00000    0.50000

```

<p></p>

```
>> val = max(a)
val =  15
>> [val, ind] = max(a)
val =  15
ind =  2

```

<p></p>

```
>> max(A)
ans =

   5   6

>> a
a =

    1.00000   15.00000    2.00000    0.50000

>> a<3
ans =

   1   0   1   1

```

<p></p>

```
>> find(a < 3)
ans =

   1   3   4

```

<p></p>

```
>> A = magic(3)
A =

   8   1   6
   3   5   7
   4   9   2

>> help magic
'magic' is a function from the file /usr/local/octave/3.8.0/share/octave/3.8.0/m/special-matrix/magic.m

 -- Function File:  magic (N)
     Create an N-by-N magic square.  A magic square is an arrangement
     of the integers `1:n^2' such that the row sums, column sums, and
     diagonal sums are all equal to the same value.

     Note: N must be greater than 2 for the magic square to exist.

Help and information about Octave is also available on the WWW
at http://www.octave.org and via the help@octave.org
mailing list.
>> 

```

<p></p>

```
>> [r,c] = find(A >= 7)
r =

   1
   3
   2

c =

   1
   2
   3

```

<p></p>

```
>> A(2,3)
ans =  7

```

<p></p>

```
>> help find

>> a
a =

    1.00000   15.00000    2.00000    0.50000

>> sum(a)
ans =  18.500
>> prod(a)
ans =  15

```

<p></p>

```
>> floor(a)
ans =

    1   15    2    0

>> ceil(a)
ans =

    1   15    2    1

```

<p></p>

```
>> rand(3)
ans =

   0.81422   0.71600   0.66651
   0.61911   0.71305   0.60260
   0.94144   0.16352   0.25032

>> max(rand(3), rand(3))
ans =

   0.51457   0.71924   0.33277
   0.98311   0.47227   0.78557
   0.15051   0.18362   0.77568


```

<p></p>

```
>> A
A =

   8   1   6
   3   5   7
   4   9   2

>> max(A,[],1)
ans =

   8   9   7

>> max(A,[],2)
ans =

   8
   7
   9

```

<p></p>

```
>> max(max(a))
ans =  15
>> A(:)
ans =

   8
   3
   4
   1
   5
   9
   6
   7
   2

>> max(A(:))
ans =  9

```

<p></p>

```
>> A = magic(9)
A =

   47   58   69   80    1   12   23   34   45
   57   68   79    9   11   22   33   44   46
   67   78    8   10   21   32   43   54   56
   77    7   18   20   31   42   53   55   66
    6   17   19   30   41   52   63   65   76
   16   27   29   40   51   62   64   75    5
   26   28   39   50   61   72   74    4   15
   36   38   49   60   71   73    3   14   25
   37   48   59   70   81    2   13   24   35

>> sum(A,1)
ans =

   369   369   369   369   369   369   369   369   369

>> sum(A,2)
ans =

   369
   369
   369
   369
   369
   369
   369
   369
   369
```

<p></p>

```
>> eye(9)
ans =

Diagonal Matrix

   1   0   0   0   0   0   0   0   0
   0   1   0   0   0   0   0   0   0
   0   0   1   0   0   0   0   0   0
   0   0   0   1   0   0   0   0   0
   0   0   0   0   1   0   0   0   0
   0   0   0   0   0   1   0   0   0
   0   0   0   0   0   0   1   0   0
   0   0   0   0   0   0   0   1   0
   0   0   0   0   0   0   0   0   1

>> A
A =

   47   58   69   80    1   12   23   34   45
   57   68   79    9   11   22   33   44   46
   67   78    8   10   21   32   43   54   56
   77    7   18   20   31   42   53   55   66
    6   17   19   30   41   52   63   65   76
   16   27   29   40   51   62   64   75    5
   26   28   39   50   61   72   74    4   15
   36   38   49   60   71   73    3   14   25
   37   48   59   70   81    2   13   24   35

>> A .* eye(9)
ans =

   47    0    0    0    0    0    0    0    0
    0   68    0    0    0    0    0    0    0
    0    0    8    0    0    0    0    0    0
    0    0    0   20    0    0    0    0    0
    0    0    0    0   41    0    0    0    0
    0    0    0    0    0   62    0    0    0
    0    0    0    0    0    0   74    0    0
    0    0    0    0    0    0    0   14    0
    0    0    0    0    0    0    0    0   35
```

<p></p>

```
>> sum(sum(A .* eye(9)))
ans =  369

```

<p></p>

```
>> A = magic(3)
A =

   8   1   6
   3   5   7
   4   9   2


```

<p></p>

```
>> pinv(A)
ans =

   0.147222  -0.144444   0.063889
  -0.061111   0.022222   0.105556
  -0.019444   0.188889  -0.102778

>> temp = pinv(A)
temp =

   0.147222  -0.144444   0.063889
  -0.061111   0.022222   0.105556
  -0.019444   0.188889  -0.102778

>> 

```

<p></p>

```

```

<p></p>

```

```

<p></p>

```

```

<p></p>

```

```

<p></p>

```

```

<p></p>



```

```

<p></p>


```

```

<p></p>


```

```

<p></p>


```

```

<p></p>

```

```

<p></p>

```

```

<p></p>


```

```

<p></p>



```

```

<p></p>


```

```

<p></p>

```

```

<p></p>


```

```

<p></p>

```

```

<p></p>


```

```

<p></p>

```

```

<p></p>


```

```

<p></p>

<img src="images1/thumbsup.png" alt="api">
