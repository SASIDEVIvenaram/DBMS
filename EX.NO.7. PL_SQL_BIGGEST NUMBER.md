# EXP NO 3:PL/SQL program -BIGGEST OF THREE NUMBERS  
### DATE: 
### AIM: 
To create PL/SQL program to find biggest of three numbers.

### ALGORITHM:
1. Declare the variable a, b, c and assign value in Declare section.
2. begin the section
3. Find biggest of three numbers 
4. 5. Display the result 
6. End the begin section.

### Program:
```
DECLARE
  
  num1 NUMBER := 10; 
  num2 NUMBER := 20; 
  num3 NUMBER := 15;
  biggest NUMBER;
BEGIN
  
  IF num1 >= num2 AND num1 >= num3 THEN
    biggest := num1;
  ELSIF num2 >= num1 AND num2 >= num3 THEN
    biggest := num2;
  ELSE
    biggest := num3;
  END IF;


  DBMS_OUTPUT.PUT_LINE('The biggest number is: ' || biggest);
END;
/
```

### Output:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/a45978e1-8639-46e5-884c-a35adf8becc3)

### Result:
Thust the program was performed sucessfully.
