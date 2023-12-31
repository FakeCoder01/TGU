<!-- Headers -->

# Упражнение по программированию на языке Паскаль

| <a href="#даны-2-целых-числа-вычислите-их-произведение">1</a> | <a href="#даны-3-числа-выведите-числа-в-порядке-возрастания">2</a> | <a href="#даны-координаты-центра-и-радиус-круга-определите-лежит-ли-точка-с-заданными-координатами-внутри-круга-все-значения-вещественные">3</a> | <a href="#без-деления-найдите-целую-часть-частного-и-остаток-от-деления-двух-заданных-целых-чисел">4</a> | <a href="#поменяйте-местами-последний-максимальный-и-первый-минимальный-элемент-массива-и-выведите-весь-массив">5</a> |
|:---|:---|:---|:---|:---|



<!-- Answer Starts From Here -->

## I. Основы

1. ### Даны 2 целых числа. Вычислите их произведение.

### Отвечать :

#### Код
```pascal

program ProductOfTwoNumbers;
var
    num1, num2, answer : integer;
begin
  write('Enter the First Number : ');
  readln(num1);
  write('Enter the Second Number : ');
  readln(num2);
  
  answer := num1 * num2;
  writeln ('The Answer is : ', answer);
  
end.

```

#### Результат
![Result of First Program](images/1.png)


## II. Ветвления

2. ### Даны 3 числа. Выведите числа в порядке возрастания.

### Отвечать :

#### Код
```pascal

program ThreeIntegersInAscendingOrder;
var
    num1, num2, num3, temp : integer;
begin
  write('Enter the First Number : ');
  readln(num1);
  write('Enter the Second Number : ');
  readln(num2);
  write('Enter the Third Number : ');
  readln(num3);
  
  if num1 > num2 then
    begin
        temp := num1;
        num1 := num2;
        num2 := temp;
     end;
  
  if num1 > num3 then
    begin
        temp := num1;
        num1 := num3;
        num3 := temp;
    end;
  
  if num2 > num3 then
    begin
        temp := num2;
        num2 := num3;
        num3 := temp;
    end;
  
  writeLn('Integers in ascending order : ', num1, ' ', num2, ' ', num3);
  
end.

```

#### Результат
![Result of Second Program](images/2.png)


3. ### Даны координаты центра и радиус круга. Определите, лежит ли точка с заданными координатами внутри круга (все значения вещественные).

### Отвечать :

#### Код
```pascal

program IfPointExixtsInACircle;
var
    cx, cy, x, y, radius, distance : Real;
begin
  write('Enter the Coordinates of the Centre of the Circle as (CX CY) : ');
  readln(cx, cy);
  write('Enter the Radius of the Circle : ');
  readln(radius);
  write('Enter the Coordinates of the Point as (X Y) : ');
  readln(x, y);
  
  distance := Sqrt(Sqr(x - cx) + Sqr(y - cy));
  
  if distance < radius then
    writeln('The point exists inside the circle.')
  else if distance = radius then
    writeln('The point lies on the circumference of the circle.')
  else
    writeln('The point is outside the circle.');
  
end.

```

#### Результат
![Result of Third Program (1)](images/3-1.png)
![Result of Third Program (2)](images/3-2.png)


## III. Циклы

4. ### Без деления найдите целую часть частного и остаток от деления двух заданных целых чисел.

### Отвечать :

#### Код
```pascal

program IntegerQuotientAndRemainder;

var
  dividend, divisor, quotient, remainder: Integer;

begin
  write('Enter the dividend : ');
  readLn(dividend);
  
  write('Enter the divisor : ');
  readln(divisor);
  
  quotient := 0;
  remainder := dividend;
  
  while remainder >= divisor do
  begin
    remainder := remainder - divisor;
    quotient := quotient + 1;
  end;
  
  writeln('Integer quotient : ', quotient);
  writeln('Remainder : ', remainder);
end.

```

#### Результат
![Result of Fourth](images/4.png)


## IV. Массивы

5. ### Поменяйте местами последний максимальный и первый минимальный элемент массива и выведите весь массив.

### Отвечать :

#### Код
```pascal

program MaxMinSwap;

function find_max_element(arr: array of Integer; n: Integer): Integer;
var
  i, pos: Integer;
  maxVal: Integer;
begin
  pos := 0;
  maxVal := arr[0];
  for i := 0 to n-1 do
  begin
    if arr[i] >= maxVal then
    begin
      maxVal := arr[i];
      pos := i;
    end;
  end;
  find_max_element := pos;
end;

function find_min_element(arr: array of Integer; n: Integer): Integer;
var
  i, pos: Integer;
  minVal: Integer;
begin
  pos := 0;
  minVal := arr[0];
  for i := 0 to n-1 do
  begin
    if arr[i] < minVal then
    begin
      minVal := arr[i];
      pos := i;
    end;
  end;
  find_min_element := pos;
end;

procedure swap_max_min_element(var arr: array of Integer; maxElementPos, minElementPos: Integer);
var
  temp: Integer;
begin
  temp := arr[maxElementPos];
  arr[maxElementPos] := arr[minElementPos];
  arr[minElementPos] := temp;
end;

var
  i, n: Integer;
  arr: array of Integer;
  maxElementPos, minElementPos: Integer;

begin
  write('Enter the size of the array : ');
  readln(n);
  SetLength(arr, n);
  
  
  for i := 0 to n-1 do
  begin
    write('Enter the ', i + 1 ,'th element : ');
    readln(arr[i]);
  end;


  maxElementPos := find_max_element(arr, n);
  writeln('The maximum element: ', arr[maxElementPos]);

  minElementPos := find_min_element(arr, n);
  writeln('The minimum element: ', arr[minElementPos]);

  swap_max_min_element(arr, maxElementPos, minElementPos);


  write('The array after swap is: ');
  for i := 0 to n-1 do
  begin
    write(arr[i], ' ');
  end;
  writeln;
end.

```

#### Результат
![Result of fifth](images/5.png)