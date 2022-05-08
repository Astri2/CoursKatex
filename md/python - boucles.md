# Les boucles

## La boucle While

C’est une boucle qui s’exécute tant que le booléen est Vrai

formule générale : while <"booléen">

```python
while i < 10 :
  print(i)
  i+=1
```

## La boucle For

c’est une boucle qui énumère les objets d’une liste 

formule générale : for <"variable à définir"> in <"list">

```python
liste = ["a","b","c","d"]
for lettre in liste :
  print(lettre)
```

## La fonction récursive

c'est une fonction qui va se réappeler tant qu'une condition d'arrêt n'est pas réalisée

```python
def test( numero ):
    if numero < 1:
        return i
    else:
        test( numero - 1 )
```
