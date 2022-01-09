# SNOW-Angular-Pipes-Filters

Pipes provide a way to transform values in an Angular template. 
Pipes are used with a Pipe (|) character, and take integers, strings, arrays, and date as input and returns a desired formatted output which can be displayed in the browser.
Syntax: {{title | uppercase}}
![image](https://user-images.githubusercontent.com/12488769/148705784-b0cb0d09-ce61-40dd-af1c-920bec0e048a.png)
Pipes can be easily used in HTML templates
![image](https://user-images.githubusercontent.com/12488769/148705796-98e52f57-8c0b-4b44-aa33-a27f0199378d.png)
![image](https://user-images.githubusercontent.com/12488769/148705797-faadf83b-258b-44f8-a120-47523cc871a9.png)

## Parameterizing a pipe

Pipes accept the any number of optional parameters to fine-tune their output. 
To add parameters to a pipe, follow the pipe name with a colon ( : ) and then the parameter value
![image](https://user-images.githubusercontent.com/12488769/148705820-92dac44a-467b-4bf9-a9b4-64e07857f76e.png)

## chaining pipes
We can chain pipe together in effective combinations.
![image](https://user-images.githubusercontent.com/12488769/148705842-87914291-ec99-496a-ba0a-1e0e96e26310.png)

## Built-in pipes
Date pipe - Used for formatting dates.
Decimal pipe - Used for formatting numbers. 
The syntax for Decimal Pipe: 
{{ value_expression | number : digitInfo }} where, digitInfo is optional. 
The represntaion of digitInfo: {minIntegerDigits}.{minFractionDigits}-{maxFractionDigits}. 
Where, 
minIntegerDigits - minimum integers before the decimal point (default is 1). 
minFractionDigits - minimum digits after the decimal point (default is 0). 
maxFractionDigits - maximum after the decimal point (default is 3). 
If minFractionDigits and maxFractionDigits value is 0, then the number is rounded off to nearest value.

![image](https://user-images.githubusercontent.com/12488769/148705853-da9032a3-356a-424e-aa7b-95dacf35d966.png)

Currency pipe - Used for formatting currencies


![image](https://user-images.githubusercontent.com/12488769/148705869-fd7b1fa9-6f4d-4e9e-b6e2-99fa010e834b.png)


Percent pipe - Used for formatting percentage values.
![image](https://user-images.githubusercontent.com/12488769/148705865-bb57b483-2b12-4082-8322-face2fd7aec3.png)
![image](https://user-images.githubusercontent.com/12488769/148705873-614517b5-57ce-443f-b4d6-955c96c603cd.png)


Slice pipe - Used for Slicing strings
Lowercase pipe - Used for converting strings into lowercase.
Uppercase pipe - Used for converting strings into uppercase
Titlecase pipe - Used for converting strings into title case

Json pipe - Used for Converting values into a JSON-format representation.
![image](https://user-images.githubusercontent.com/12488769/148705896-b9a759c0-60e5-4599-8e81-6c27595b2327.png)


## Async pipe
Used for unwrapping values from an asynchronous primitive. 
The async pipe subscribes to an Observable or Promise and returns the latest value it has emitted. 
Example: Here, we bind the Promise with the template. Clicking the Resolve button resolves the promise.
![image](https://user-images.githubusercontent.com/12488769/148705915-545f5ec0-b669-47d3-8778-46decfa885d1.png)

![image](https://user-images.githubusercontent.com/12488769/148705918-bc6b6193-754c-4eb7-bdca-b396bbf0e157.png)

## Custom pipe
We can create custom pipes using the 
ng g pipe <pipe-name> 
command in the terminal with the Angular CLI.
we create a custom pipe to count words by running the ng g pipe wordcount command in the terminal. 
The CLI creates 2 files – 
wordcount.pipe.spec.ts 
wordcount.pipe.ts

We import the @Pipe decorator from the core Angular library. If the Class is decorated with the @Pipe decorator, Angular knows that class is a pipe.
In the @Pipe decorator, we define the pipe name that used within template expressions.
The pipe class implements the PipeTransform interface to perform a transformation.
There is a transform method that accepts an input value followed by optional parameters and returns the transformed value.
![image](https://user-images.githubusercontent.com/12488769/148705943-2a046f06-5b89-49ad-8b2b-dd9b2a484be1.png)
  ![image](https://user-images.githubusercontent.com/12488769/148705947-2a57dfdc-5927-47e7-9e6a-f2da57941c74.png)


  
