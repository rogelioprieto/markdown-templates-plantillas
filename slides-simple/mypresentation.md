---
title: Título
subtitle: Subtítulo
author: Rogelio Prieto Alvarado
institute: FIUAS | PITUAS
date: Junio, 2019
toc-title: Agenda
output: beamer_presentation
classoption: t
lang: es-MX 
---


# Lenguaje awk

## Awk

Es un lenguaje de programación descriptivo.

Awk es a la vez, un lenguaje de programación y un procesador de
textos que puede ser usado para manipular datos de muchas maneras
útiles. Particularmente cuando los datos de entrada pueden ser vistos como registros (renglones) y campos (columnas).

Awk está incluido por _default_ en todas las versiones modernas de
sistemas Linux. En Ubuntu se tiene la versión de GNU: ```gawk```.

Fue diseñado para realizar tareas como recuperación, transformación, reducción y validación de datos.

## Awk
1. Su función básica es buscar archivos por líneas (o por otras
unidades de texto) que contengan ciertos patrones.

1. Cuando una línea encuentra una de los patrones, ```awk``` ejecuta las
acciones especificadas en esa línea.

1. AWK continúa el procesamiento de las líneas de entrada de esta
manera hasta que alcanza el final del archivo de entrada.


## Awk – Ejecución (1/2). Sintaxis
```bash
awk ’program’ input-file1 input-file2 ...  
```


## Awk – Ejecución (1/2). Ejemplo
```bash
awk '/hola/' datos.txt
```
# Ejercicios

## Ejercicio 01

Imprimir el primer campo de un archivo que contiene los datos separados por :
```awk
awk -F: '{print $1}' /etc/passwd
```

## Ejercicio 02

Crear el archivo ejemplo02.awk
```awk
{
text = $1 " home at " $6
print text  
}
```

. . .

Ejecutar
```bash
awk -F: -f ejemplo02.awk /etc/passwd
```

## Ejemplo - inserción de imagen


![Imagen de demostración.](images/puzzle.png)



## Ejemplo - tabla

| Tablas          | son                   | fáciles  |
| --------------- |:---------------------:| --------:|
| col 3 está      | alineado a la derecha |    $1950 |
| col 2 está      | centrado              |      $12 |
| última          | línea                 |       $1 |


