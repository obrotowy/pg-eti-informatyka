---
#title: Drugie kolo PAA
#author: Emilian Zawrotny
geometry: margin=2cm
---

## Zadanie
Dany jest graf kubiczny G. Ustal w jakim czasie można stwierdzić podaną własność. Każdy wiersz jest oceniany z osobna, pod warunkiem, a punkty przyznane jeśli nie ma w nim błędnych odpowiedzi.

| Twierdzenie      | Złożoność | Twierdzenie      | Złożoność | Punkty (max 4) |
|------------------|-----------|------------------|-----------|----------------|
| $\chi(G) \leq 1$ |           | $\chi(G) \geq 1$ |           |                |
| $\chi(G) \leq 2$ |           | $\chi(G) \geq 2$ |           |                |
| $\chi(G) \leq 3$ |           | $\chi(G) \geq 3$ |           |                |
| $\chi(G) \leq 4$ |           | $\chi(G) \geq 4$ |           |                |

## Rozwiązanie

Twierdzenie Brooks'a mówi nam, że $\chi(G) \leq \Delta$, chyba że G jest grafem pełnym (kliką) bądź nieparzystym cyklem, wówczas $\chi(G) = \Delta+1$. A dla naszego grafu G: $\Delta = 3$.

Rozważmy specjalne przypadki grafów kubicznych:
- Graf kuratowskiego ($K_{3,3}$) - $\chi(K_{3,3}) = 2$
- Graf $K_4$ - $\chi(K_4) = 4$

### Rozwiązanie każdego z twierdzeń
- $\chi(G) \leq 1$ - Trywialne, dla żadnego grafu kubicznego nie zachodzi taka własność - stąd $O(1)$
- $\chi(G) \geq 1$ - Trywialne, zachodzi dla każdego grafu kubicznego - $O(1)$
- $\chi(G) \geq 2$ - Wystarczy sprawdzić, G jest grafem dwudzielnym, możemy to zrobić w czasie $O(n)$
- $\chi(G) \geq 2$ - Trywialne, zachodzi dla każdego grafu kubicznego
- $\chi(G) \leq 3$ - Wystarczy sprawdzić, czy G nie jest kliką $K_4$ (sprawdzając czy n < 4) - $O(1)$
- $\chi(G) \geq 3$ - Wystarczy sprawdzić, czy graf nie jest dwudzielny - $O(n)$
- $\chi(G) \leq 4$ - Trywialne, zawsze prawda (na mocy twierdzenia Brooksa)
- $\chi(G) \geq 4$ - Prawda tylko i wyłącznie, gdy G jest kliką $K_4$ - $O(1)$

| Twierdzenie      | Złożoność | Twierdzenie      | Złożoność |
|------------------|-----------|------------------|-----------|
| $\chi(G) \leq 1$ | O(1)      | $\chi(G) \geq 1$ | O(1)      |
| $\chi(G) \leq 2$ | O(n)      | $\chi(G) \geq 2$ | O(1)      |
| $\chi(G) \leq 3$ | O(1)      | $\chi(G) \geq 3$ | O(n)      |
| $\chi(G) \leq 4$ | O(1)      | $\chi(G) \geq 4$ | O(1)      |