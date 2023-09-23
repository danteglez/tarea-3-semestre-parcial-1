# tarea-3-semestre-parcial-1
---
### En este trabajo estaran todos los trabajos hechos en las clases con una pequeña explicacion de cada programa con mis propias palabras

``` 
N=input("Ingresa un numero: ")
N=int(N)
#lista del 1 a N
lista=list(range(1,N+1))
#multiplicar los numeros de la lista por 2
lista2=[i*2 for i in lista]
#suma de los numeros de la lista
suma=sum(lista2)
#imprimir la suma
print(suma)
``` 
En este algoritmo suma los N numeros pares 
funciona con:
- Range: este sirve para poder crear la lista de numero que hay entre el 1 al N
- Lista2: este funciona para multiplicar los numeros por 2 para luego sumarlos
- suma: este sirve para sumar la lista y poder ver el resultado

---
```
while True:
 print("\nMi Calculadora")
 print("1. Suma")
 print("2. Resta")
 print("3. Multiplicación")
 print("4. División")
 print("5. Salir")
 opcion = input("Selecciona una opción: ")
 if opcion == '5':
    print("¡Hasta luego!")
    break
 elif opcion<'1' or opcion > '5':
    print("opcion no valida")
 else:
   num1 = float(input("Ingresa el primer número: "))
   num2 = float(input("Ingresa el segundo número: "))
   
   if opcion == '1':
      print("Resultado:", num1 + num2)
   elif opcion == '2':
      print("Resultado:", num1 - num2)
   elif opcion == '3':
      print("Resultado:", num1 * num2)
   elif opcion == '4':
      if num2 != 0:
         print("Resultado: ", num1 / num2)
      else:
         print("No se puede dividir entre cero")
   else:
      print("¡Gracias por usar Mi Calculadora!")

 
#Ejercicio 2

class MiCalculadora:
 def __init__(self):
    pass
 def suma(self, a, b):
    return a + b
 def resta(self, a, b):
    return a - b
 def multiplicacion(self, a, b):
    return a * b
 def division(self, a, b):
    if b != 0:
        return a / b
    else:
        return "No se puede dividir entre cero" 
calculadora = MiCalculadora()
while True:
 print("\nMi Calculadora")
 print("1. Suma")
 print("2. Resta")
 print("3. Multiplicación")
 print("4. División")
 print("5. Salir")
 opcion = input("Selecciona una opción: ")
 if opcion == '5':
    print("¡Gracias por usar Mi Calculadora!")
    break
 elif opcion < '1' or opcion > '5':
        print("Opción no válida")
 else:
    num1 = float(input("Ingresa el primer número: "))
    num2 = float(input("Ingresa el segundo número: "))
 if opcion == '1':
    print("Resultado:", calculadora.suma(num1, num2))
 elif opcion == '2':
    print("Resultado:", calculadora.resta(num1, num2))
 elif opcion == '3':
    print("Resultado:", calculadora.multiplicacion(num1, num2))
 elif opcion == '4':
    if num2 != 0:
        print("Resultado:", calculadora.division(num1, num2))
    else:
        print("No se puede dividir entre cero")
 

 #Ejercicio 3

def suma(a, b):
 return a + b
def resta(a, b):
 return a - b
def multiplicacion(a, b):
 return a * b
def division(a, b):
 return a / b

def mi_calculadora(opcion, num1, num2):
 if opcion == '1':
    return suma(num1, num2)
 elif opcion == '2':
    return resta(num1, num2)
 elif opcion == '3':
    return multiplicacion(num1, num2)
 elif opcion == '4' and num2 != 0:
    return division(num1, num2)
 else:
    return "Opción no válida"
while True:
 print("\nMi Calculadora")
 print("1. Suma")
 print("2. Resta")
 print("3. Multiplicación")
 print("4. División")
 print("5. Salir")
 opcion = input("Selecciona una opción: ")
 if opcion == '5':
    print("¡Gracias por usar Mi Calculadora!")
    break
 elif opcion < '1' or opcion > '5':
    print("Opción no válida")
 else:
    num1 = float(input("Ingresa el primer número: "))
    num2 = float(input("Ingresa el segundo número: "))
    resultado = mi_calculadora(opcion, num1, num2)
 print("Resultado:", resultado) 
 ```
Aqui podemos ver como es que se hace de fomas diferentes una calculadora y eso es lo que me gusta de progamar y es como es que todos hacen lo mismo pero se hacen de forma diferente, cada uno es un razonamiento diferente.
sinceramente no tengo mucho que explicar solo son calculadoras usando:
- ciclos while: se repite el codigo mientras que una condicion sea verdadera
- def: se utiliza para definir funciones 
- if: si algo es verdadero ejecuta el codigo 
- elif: funciona parecido a if solo este se ejecuta si if es falso 
- else: y else es si if o elif son falsos

---

```
def suma(a:int|float, b:int|float)->int|float:
    return a+b

res=suma(3,5.3)
print(res)
```
en este algoritmo puedo ver una suma normal donde se puede usar enteros o decimales 

---

```
import streamlit as st

st.sidebar.title("calculadora ICI")

def operacion_suma():

    name = st.text_input("Nombre: ")
    n1= st.number_input("Numero 1")
    n2= st.number_input("Numero 2")

    if st.button("Sumar"):
        st.success(f"Hola {name}")
        st.write(f"{n1} + {n2} = {n1+n2}")
def operacion_resta():

    name = st.text_input("Nombre: ")
    n1= st.number_input("Numero 1")
    n2= st.number_input("Numero 2")

    if st.button("Restar"):
        st.success(f"Hola {name}")
        st.write(f"{n1} - {n2} = {n1-n2}")
def operacion_multiplicacion():
    name= st.text_input("Nombre: ")
    n1= st.number_input("Numero 1")
    n2= st.number_input("Numero 2")
    if st.button("Multiplicar"):
        st.success(f"Hola {name}")
        st.write(f"{n1} * {n2} = {n1*n2}")
def operacion_division():
    name= st.text_input("Nombre: ")
    n1= st.number_input("Numero 1")
    n2= st.number_input("Numero 2")
    if st.button("Dividir"):
        st.success(f"Hola {name}")
        st.write(f"{n1} / {n2} = {n1/n2}")
def opcion_acercade():
    st.write("Derechos Reservados  ")
    st.write("UCOL-FIME_ICI")

opcion = st.sidebar.selectbox("Opciones", [
    "Suma", "Resta", "Multiplicacion", "Division", "Acerca de"
    ])


match opcion:
    case "Suma":
        st.write("Esta es la opcion de suma... ")
        operacion_suma()
    case "Resta":
        st.write("Esta es la opcion de resta... ")
        operacion_resta()
    case "Multiplicacion":
        st.write("Esta es la opcion de multiplicacion... ")
        operacion_multiplicacion()
    case "Division":
        st.write("Esta es la opcion de division... ")
        operacion_division()
    case "Acerca de":
        opcion_acercade()
```

en este algoritmo es una calculadora pero se puede usar para un diccionario llamado streamlit,
con este se puede hacer paginas web y diseñarlas a tu gusto