---
sticker: emoji//1f532
---
# Musterlösung 1:

``` Python
def fibonacci(n):
    fib = [0, 1]
    for i in range(2, n):
        fib.append(fib[i-1] + fib[i-2])
    return fib

anzahl = int(input("Geben Sie die Anzahl der Fibonacci-Zahlen ein: "))
fibonacci_folge = fibonacci(anzahl)
print(fibonacci_folge)
```


# Musterlösung 2:

``` Python
def ist_primzahl(n):
    if n <= 1:
        return False
    primes = [True] * (n+1)
    primes[0] = primes[1] = False
    p = 2
    while p * p <= n:
        if primes[p]:
            for i in range(p * p, n+1, p):
                primes[i] = False
        p += 1
    return primes[n]

zahl = int(input("Geben Sie eine Zahl ein: "))
ergebnis = ist_primzahl(zahl)
print(ergebnis)
```

# Musterlösung 3:

``` Python
def ist_palindrom(wort):
    wort = wort.lower()
    rückwärts = wort[::-1]
    if wort == rückwärts:
        return True
    else:
        return False

eingabe = input("Geben Sie ein Wort ein: ")
ergebnis = ist_palindrom(eingabe)
print(ergebnis)
```

# Musterlösung 4: 

``` Python
// Rekursive Version
function sumOfFirstNRecursive(n) {
  // Basisfall: Wenn n gleich 1 ist, ist die Summe einfach 1
  if (n === 1) {
    return 1;
  }

  // Die Summe der ersten n natürlichen Zahlen ist gleich n plus die Summe der ersten (n-1) natürlichen Zahlen
  return n + sumOfFirstNRecursive(n - 1);
}

// Testen der rekursiven Funktion
console.log(sumOfFirstNRecursive(5)); // Sollte 15 ergeben (1 + 2 + 3 + 4 + 5 = 15)

// Überprüfen mit der iterativen Version
console.log(sumOfFirstNIterative(5)); // Sollte ebenfalls 15 ergeben
```
