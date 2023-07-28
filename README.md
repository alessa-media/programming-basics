# programming-basics

## Variablen
### Strings - Zeichenketten
```php
  $string = "test"; 
  $name = "alessa";
```

### Integers - Ganzzahlen
```php
  $integer = 123;
  $alter = 21;
```

### Booleans - True/False
* es gibt nur die zwei möglichen Werte true oder false
```php
  $boolean = false;
  $AlessaCanCode = true;
```


### Arrays - mehrere Variabeln in einer Variabel

```php
  $int_array = array(1,2,3);
  $zahlen = array(1,2,3); 

  $string_array = array("test1","test2","test3");
  $testfaelle = array("test1","test2","test3"); 
```

```php
  $alter_personen = array(
    "Tom" => 21,
    "Manuel" => 20
  );
```

## Funktionen
* return ist optional
* Übergabeparameter sind optional
```php
function functionName(parameterA,parameterB){
    $sum = $parameterA + $parameterB;
    return $sum;
}
```

## Schleifen
### foreach
```php
$array = array(1, 2, 3, 4);
foreach ($array as $element) {
    echo $element;
}
```
### for
* mit $i++; wird die Variabel $i inkrementiert (um 1 erhöht)
* so wird $i = 20 z.b. zu $i = 21
```php
for ($i = 1; $i < 20; $i++){ // i = Variabel
  echo $i;
}
```
### while
* Im while wird nur geprüft, ob die Bedingung stimmt.
* wie foreach, nur ist $i nicht vordefiniert, kann (z.B. durch Nutzer) eingegeben werden
* Auch $i++ muss nicht dabei sein, weil per se nicht gerechnet wird

```php
$i = 1;
while ($i<20){
  $i++;
}
```

### do while
* erster Durchgang immer ohne Prüfung
* Zuerst Aktion, dann Prüfung (Beispiel: Zuerst Schlüssel drehen, dann prüfen, ob Auto läuft.)
```php
$i = 1;

do{
  $i++;
} while ($i<20)
```

## IF-Statements

### mit Boolean
* direkte Prüfung ohne [Comparison Operator](https://www.php.net/manual/en/language.operators.comparison.php) möglich
```php
$alessaIs18 = true;
if($alessaIs18){
  echo 'allowed to drive';
}

### 
* direkte Prüfung ohne Operator möglich
```php
$alessaIs18 = true;
if($alessaIs18){
  echo 'allowed to drive';
}
```

