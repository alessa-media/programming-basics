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

### Variabeln zusammenfügen
```php
$varA = "hello";
$varB = "world";

$output = $varA." ".$varB; //hello world
echo $output;
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
  echo 'allowed to drink hard alcohol';
}
```

### Mit Comparison Operators
* siehe [Comparison Operator](https://www.php.net/manual/en/language.operators.comparison.php)
* es folgt ein Beispiel
```php
$ageAlessa = 18;
if($ageAlessa >= 18){
  echo 'allowed to drink hard alcohol';
}
```

| Operator   | Name                   | Description                                                  |
|------------|------------------------|--------------------------------------------------------------|
| $a == $b   | Equal                  | True if $a is equal to $b after type juggling.              |
| $a === $b  | Identical              | True if $a is equal to $b, and they are of the same type.   |
| $a !== $b  | Not identical          | True if $a is not equal to $b, or they are not of the same type. |
| $a < $b    | Less than              | True if $a is strictly less than $b.                        |
| $a > $b    | Greater than           | True if $a is strictly greater than $b.                     |
| $a >= $b   | Greater than or equal to | True if $a is greater than or equal to $b.                  |


### Mit Logical Operators
* siehe [Logical Operator](https://www.php.net/manual/en/language.operators.logical.php)
* verwendet, um Bedingungen zu kombinieren - BedingungA && BedingungB -> beide müssen erfüllt sein (AND)
* es folgt ein Beispiel
```php
$ageAlessa = 18;
$AlessaHasDrivingLiscence = true;
if($ageAlessa >= 18 && $AlessaHasDrivingLiscence){
  echo 'allowed to drive';
}
```

| Operator  | Name         | Description                                              |
|-----------|--------------|----------------------------------------------------------|
| $a xor $b | Xor          | True if either $a or $b is true, but not both.         |
| ! $a      | Not          | True if $a is not true.                                 |
| $a && $b  | And          | True if both $a and $b are true.                        |
| $a \|\| $b | Or          | True if either $a or $b is true.                        |


### IF-ELSE Statement
* wenn Kondition nicht übereinstimmt -> etwas anderes machen
```php
$alessaIs18 = false;
if($alessaIs18){
  echo 'allowed to drink hard alcohol';
} else {
  echo 'not allowed to drink hard alcohol';
}
```

### ELSE-IF Statement
* wenn Kondition nicht übereinstimmt -> auf andere Kondition prüfen
```php
$alessaIs18 = false;
$alessaIs16 = true;
if($alessaIs18){
  echo 'allowed to drink hard alcohol';
} else if ($alessaIs16) {
  echo 'allowed to drink soft alcohol';
}
```

