# Diagramas Vs Código en Java

## Diagramas de Algoritmos
Los diagramas permiten diseñar y mostrar el flujo de datos en un proceso o algoritmo.

Ejemplo de un diagrama completo:

![diagrama1](https://nancyparada.com/app/uploads/2019/04/diagrama-de-algoritmo.jpg "Diagrama completo")


## Código Base de Un Programa en Java
Nuestro código base incluye un Scanner para permitir lectura por teclado. Todo programa en java tiene un nombre que se escribe con la primera letra de cada palabra en mayuscula y el archivo donde se guarda se nombre exactamente igual y se le añade la extension _.java_


```java
import java.util.Scanner;

public class NombreDePrograma {
  public static void main( String []args) {
    Scanner entrada = new Scanner(System.in);
    // aqui va el codigo de nuestro programa
  
  }
}
```

## Leer

Cuando necesitamos leer algo para guardarlo en una variable. Lo que se lee o "el valor" siempre se guarda en una variable que tiene un "nombre_variable". Los nombres de variables van de acuerdo a la naturaleza del valor que guardan.

### En un diagrama leemos asi

![diagrama1](https://nancyparada.com/app/uploads/2019/04/leer.png "simbolo de lectura")

### En Java esto se convierte en un proceso de al menos 3 pasos:
1. debemos "declarar" la variable que vamos a utilizar especificando el tipo de dato que vamos a almacenar en esa variable (numero entero, numero real, cadena de caracteres, datos booleanos, etc). 
2. Luego imprimimos un mensaje solicitandole al usuario que ingrese un valor
3. leemos ese valor usando un Scanner y lo guardamos en la variable que declaramos.

```java
int numero;
System.out.print("Ingrese numero: ");
numero = input.nextInt();
```

Los tipos de variables mas usados son:

```java
int numero_decimal_sin_comas; // 1,2, 10000, -10, -15,0,... 
float numero_con_decimales; // 1.23, 3.141516...
String cadena_de_caracteres; //nombre, juan, pedro, CABA, La Plata, ...
boolean verdadero_o_falso; // true si es verdadero, false si es falso
char caracter; // M o F por ejemplo, 1 solo caracter.
```

El Scanner para leer por teclado es algo externo a nuestro programa (es un codigo que esta fuera de nuestro codigo) debemos importarlo para ello en la primera linea escribimos


```java
import java.util.Scanner;
```

Luego de importado podemos usarlo en nuestro programa para leer por teclado declarando una variable de tipo Scanner y luego inicializandola. Podemos colocarle el nombre que queramos como con cualquier otra variable pero es preferible usar nombres que denoten el uso que se le va a dar como input, lector, entrada, etc.

```java
Scanner entrada = new Scanner(System.in);
```

### Es una buena practica declarar todas las variables al principio de nuestro codigo junto a la declaracion del Scanner y asi es mas ordenado, tambien podemos agregar comentarios al lado para acordarnos luego que significa esa variable dentro de nuestro código, por ejemplo:

```java
Scanner entrada = new Scanner(System.in);

int numero1; //primer numero
int numero2; // segundo numero
float porcentaje; // porcentaje de ventas del mes
String NombrePersona; // Nombre de una Persona

System.out.print("Ingrese numero 1: ");
numero1 = input.nextInt();

System.out.print("Ingrese numero 2: ");
numero2 = input.nextInt();
```

## Salida

Todo programa asi como tiene una entrada, tiene una salida. Por lo general la salida de nuestros programas van orientadas a imprimir resultados del proceso que se ejecuta en el programa

### En diagrama de algoritmos seria

![diagrama1](https://nancyparada.com/app/uploads/2019/04/salida.png "simbolo de salida")

### En java tenemos varias opciones, todas forman parte del package _System.out_

```java
// imprime el texto entre comillas y no cambia a la siguiente linea. 
System.out.print("Mensaje sin salto de linea"); 

// imprime el texto entre comillas y cambia a la siguiente linea. 
System.out.println("Mensaje con salto de linea"); 

// para imprimir valores que hemos guardado en variables usamos printf
System.out.printf("El resultado de la operacion es:%d",resultado); 
System.out.printf("El resultado de la operacion es:%d y el segundo resultado es %f",r1, r2); 

/* printf imprime el texto entre comillas sustituyendo en la cadena de caracteres %FORMATO 
por el valor de la variable y puede recibir todas las variables que deseemos agregar separandolas
de la cadena de caracteres del mensaje, con comillas
los mas usados son:
%d numeros enteros (int) (-1 4 0 1000 etc)
%f numeros reales (float) (-1.5 4.34 0.53 1000.45 etc)
%s Strings ("Juan" "Programador" "(+54) 11 1234 3456" etc)
```


## Condicionales o Decisiones

Una estructura condicional es donde evaluamos una condicion y decidimos si se cumple o no (verdadero o falso). Dependiendo de si es _verdadero_ o _falso_ se ejecuta un flujo o el otro.

### En diagrama de algoritmos seria asi

![diagrama1](https://nancyparada.com/app/uploads/2019/04/condicion.png "simbolo de condicional")

### En java utilizamos las estructuras _if_ y _if/else_

```java
//si nos interesa solo la parte verdadera, cuando se cumple la condicion
//note que n1==n2 es nuestra condicion de ejemplo y es algo que varia de acuerdo al programa
//note que == se usa para comparar igualdad, = en java se usa para asignar un valor a una variable
if (n1 == n2) {
  //instrucciones a ejecutar si se cumple la condicion
}

// si nos interesa tanto la parte verdadera como falsa usamos if/else
if (n1 == n2) {
  //instrucciones a ejecutar SI se cumple la condicion
} else {
  //instrucciones a ejecutar SI NO se cumple la condicion
}

// note que podemos tener if anidados, es decir, un if dentro de otro if o dentro de un else
if (n1 == n2) {
  //instrucciones a ejecutar SI se cumple la condicion
} else {
  if (n1 > n2) {
    //instrucciones a ejecutar SI se cumple la condicion
  } else {
    //instrucciones a ejecutar SI NO se cumple la condicion
  }
}
```

## calculos y asignaciones

### En Diagrama de algoritmos
![diagrama1](https://nancyparada.com/app/uploads/2019/04/calculo.png "simbolo de calculo")

### En java se usa = y operaciones matematicas (+,-,*,/)

```java
resultado = a+b

// podemos hacer varias operaciones matematicas dentro de la misma instruccion
sueldo = 500 + 50*numeroAutosVendidos;
promedio = (nota1 + nota2+ nota3)/3
```

*nota:* recuerde que toda variable  en java debe tener un tipo y ser declarada antes de usarse.
