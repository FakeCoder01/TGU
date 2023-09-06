# Упражнение по программированию на языке Паскаль

| <a href="#">1</a> | <a href="#">2</a> | <a href="#">3</a> | <a href="#">4</a> | <a href="#">5</a> |
|:---|:---|:---|:---|:---|

## I. Основы

1. ### Даны 2 целых числа. Вычислите их произведение.

### Отвечать :

#### Код
```

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
[Result of First Program](/1st%20Semester/Task%201/images/1.png)


## II. Ветвления

2. ### Даны 3 числа. Выведите числа в порядке возрастания.

### Отвечать :

#### Код
```

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
[Result of Second Program](/1st%20Semester/Task%201/images/2.png)


3. ### Даны координаты центра и радиус круга. Определите, лежит ли точка с заданными координатами внутри круга (все значения вещественные).

### Отвечать :

#### Код
```

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
[Result of Third Program (1)](/1st%20Semester/Task%201/images/3-1.png)
[Result of Third Program (1)](/1st%20Semester/Task%201/images/3-2.png)


## III. Циклы

4. ### Без деления найдите целую часть частного и остаток от деления двух заданных целых чисел.

### Отвечать :

#### Код
```

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
[Result of Fourth](/1st%20Semester/Task%201/images/4.png)


## IV. Массивы

5. ### Поменяйте местами последний максимальный и первый минимальный элемент массива и выведите весь массив.

### Отвечать :

#### Код


```

```

#### Результат