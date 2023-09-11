# Fibonacci numbers

```pascal
program FibonacciNumber;

function fibonacci(n: Integer): Integer;
begin
    if (n = 0) or (n = 1)then
        fibonacci := 0
    else if n = 2 then
        fibonacci := 1
    else
        fibonacci := fibonacci(n - 1) + fibonacci(n - 2);
end;

var
    n, i: Integer;
    
begin
    write('Enter n : ');
    readln(n);
    writeln('The fibonacci number is : ', fibonacci(n));
    
    for i := 1 to n do
        write(fibonacci(i), ' ');
    
end.

```



