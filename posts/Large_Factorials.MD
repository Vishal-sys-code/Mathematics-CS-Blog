---
title: 'Large Factorials'
date: 'August 19, 2022'
excerpt: ''
cover_image: '/images/posts/factorial.jpg'
---
# <b>Higher Factorials</b>

<b>```Factorial :```</b> Factorial of a non-negative integer, is the multiplication of all integers smaller than or equal to n. <br>

```
n! = n * (n-1) * (n-2) * ....... * 1
```

For normal n values upto 15 we can get the factorials by the above formula however, for higher values the product will be get rising upto big integers so the above formula will be failed in the computers to solve. <br>

To solve higher factorials we have two approaches: 
<li> Stirling's Aprroximation Approach</li>
<li> Ramanujan's Approach</li>

<br>

<b>```Stirling approximation:```</b> is an approximation for calculating factorials. It is also useful for approximating the log of a factorial. <br>

<a href=""><img src="https://drive.google.com/uc?export=view&id=1rLtV-ofEm1kwNJYL8YH1OiG4bL0dV7pr" 
style="width: 450px; max-width: 100%; height: auto" title="Click to enlarge picture"></a>

```
n! =~ sqrt(2*pi*n) * pow((n/e), n) 
```

</b>```Note:```</b> <i>This formula will not give the exact value of the factorial because it is just the approximation of the factorial.</i>

<b>```Code :```</b>

```
long long int stirlingApproximation(int n){
    if (n == 1)
        return 1;
    long long int z;
    float e = 2.71;
    z = sqrt(2*3.14*n) * pow((n/e), n);
    return z;
}
```

<hr>

Similary we have, <br>

<b>```Ramanujan's Factorial approximation:```</b> is an approximation for calculating factorials. It is also useful for approximating the log of a factorial. <br>

<a href=""><img src="https://drive.google.com/uc?export=view&id=18PkPY3WnndbR3x4fUJbBTi0XF25QlEBp" 
style="width: 300px; max-width: 100%; height: auto" title="Click to enlarge picture"></a>

<b>```The approximation of Ramanujan is :```</b>

<a href=""><img src="https://drive.google.com/uc?export=view&id=1VIUA3AwT0TcJ2rOULcz4EQ2QmCK6sL2y" 
style="width: 450px; max-width: 100%; height: auto" title="Click to enlarge picture"></a>


<b>```Implementation 1 :```</b>

```
def ramanujan(x):
        fact = sqrt(pi)*(x/e)**x
        fact *= (((8*x + 4)*x + 1)*x + 1/30.)**(1./6.)
        return fact
```

<b>```Implementation 2 (trickier implementation):```</b>

```
def ramanujan2(x):
        fact = sqrt(pi)*(x/e)**x
        fact *= (((8*x + 4)*x + 1)*x + 1/30.)**(1./6.)
        if isinstance(x, int):
             fact = int(fact)
        return fact
```

<hr>