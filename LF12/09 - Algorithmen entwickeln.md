---
sticker: emoji//1f532
---
# Übungsaufgabe 1:
Schreibe ein Python-Programm, das die Fibonacci-Folge bis zur angegebenen Anzahl von Elementen generiert und ausgibt. Verwende dabei eine iterative Methode zur Berechnung der Fibonacci-Zahlen.

# Übungsaufgabe 2:
Schreibe eine Funktion in Python, die überprüft, ob eine gegebene Zahl eine Primzahl ist. Verwende dabei den Algorithmus des "Sieb des Eratosthenes".
*Tobias' Lösung:*
``` javascript
function checkPrime(n) {
    for(let i=2; i <= Math.sqrt(n); i++){
        if(n%i==0) {
            return false
        }
    }
    return true
}

if(checkPrime(8)){
    console.log("Das ist eine Primzahl!")
} else {
    console.log("Das ist keine Primzahl!")
}
```

*Tims & Matthes' Lösung:*

``` javascript
function f(n) {
	let arr = [...Array(n-1)].map((e,i)=>i+2)
		for(let k=0; arr[k];k++){
			arr=arr.filter(e=>e%arr[k]||e==arr[k])
		}   
	return arr.includes(n) 
}
```
# Übungsaufgabe 3:
Schreibe eine Funktion in Python (oder einer anderen Sprache), die prüft, ob ein gegebenes Wort ein Palindrom ist (also vorwärts und rückwärts gelesen dasselbe ergibt).

# Übungsaufgabe 4:
Gegeben ist ein iterativ implementierter Algorithmus, der die Summe der ersten `n` natürlichen Zahlen berechnet. Schreibe eine rekursive Funktion, die das Gleiche tut.

#### Iterative Version:

``` Python
function sumOfFirstNIterative(n) {
  let sum = 0;
  for (let i = 1; i <= n; i++) {
    sum += i;
  }
  return sum;
}
```
Deine Aufgabe ist es, eine rekursive Funktion `sumOfFirstNRecursive` zu schreiben, die das gleiche Ergebnis wie `sumOfFirstNIterative` liefert.
#### Rekursive Version:
*Tobias' Verson*
``` javascript
function sumUp(n) {
	  sum = 0;
	  for (let i = 1; i <= n; i++) {
	    sum += i
	  }
	  return sum;
	}
	// Rekursiv:
	
	// Hochlaufend:
	function sumToN(n, i = 0, sum = 0) {
	  if (i == n) return sum + i;
	  return sumToN(n, i + 1, sum + i);
	}
	  
	// Ablaufend:
	function sumFromN(n, sum = 0) {
	  if (n == 0) return sum;
	  return sumFromN(n - 1, sum + n);
	}
	
	// Shorter:
	function sumRek(n) {
	  if (n == 0) return 0;
	  return n + sumRek(n - 1);
	}
	
	console.time("Iterativ");
	for (let j = 0; j < 1000000; j++) sumUp(100);
	console.timeEnd("Iterativ");
	
	console.time("Rekursiv up");
	for (let j = 0; j < 1000000; j++) sumToN(100);
	console.timeEnd("Rekursiv up");
	
	console.time("Rekursiv down");
	for (let j = 0; j < 1000000; j++) sumFromN(100);
	console.timeEnd("Rekursiv down");
	
	console.time("Rekursiv down2");
	for (let j = 0; j < 1000000; j++) sumRek(100);
	console.timeEnd("Rekursiv down2");
}
```

**Anforderungen:**

1. Die rekursive Funktion `sumOfFirstNRecursive` sollte die Summe der ersten `n` natürlichen Zahlen berechnen.
2. Die Funktion sollte rekursiv sein und keine Schleifen verwenden.
3. Verwende die iterative Version `sumOfFirstNIterative` als Referenz, um sicherzustellen, dass deine rekursive Funktion das gleiche Ergebnis liefert.

#### Hinweise:

- Denke daran, dass die Summe der ersten `n` natürlichen Zahlen gleich `n + (n-1) + (n-2) + ... + 1` ist.
- Überlege, wie du den rekursiven Aufruf definieren kannst, um die Summe der ersten `n` natürlichen Zahlen zu berechnen.
- Achte darauf, die Abbruchbedingung zu definieren, um die Rekursion zu beenden.

# Schwerpunkt Programmierung IHK (2021-Herbst, AO 1997)

## Anwendungsentwicklung Teil 1

### Aufgabe 2
- Klassendiagramme lesen (LF 11)
- Code schreiben & Algorithmen implementieren (LF 5 / LF 8)

### Aufgabe 3
- Klassendiagramm erstellen (LF 11)
- Theorie Objektorientierung (LF 8)
- Sequenzdiagramm ergänzen (LF 11)