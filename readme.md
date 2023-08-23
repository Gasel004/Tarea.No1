*PSEUDOCODIGO*
//Programa que simula una calculadora de conversión de medidas de longitud (pies, pulgadas, varas, yardas, metros)
//Pidiendo al usuario ingresar el dato que desea convertir, teniendo presente que el dato se tomara en la medida de centimetros.
Algoritmo medidas_de_longitud
	Definir d1,r Como Real
	Definir conversión Como Caracter
	Definir opc como entero
	Escribir "Bienvenido:"
	Escribir " Ingrese la cantidad la cual desea convertir; "
	Escribir "(Recuerde que la cantidad sera tomada en centimetros)"
	leer d1
	Limpiar Pantalla
//Se le desplegara un menú de opciones al usuario y tendra que escojer a que medida desea realizar su conversión
	Escribir "** Selecione la medida a la cual desea desea realizar su conversión **"
	Escribir"1: Conversión a Metros:" 
	Escribir"2: conversión a Yardas:" 
	Escribir"3: Conversión a Varas:" 
    Escribir"4: Conversión a Pulgadas:" 
    Escribir"5: Conversión a Pies:"
	leer opc
	Limpiar Pantalla
//Se realizaran los procesos necesarios para realizar la conversion que el usuario selecciono anteriormente 
	si (opc==1)Entonces
//Para convertir centimetros a metros devemos de dividir la cantidad que ingreso el usuario por 100 es decir; m/100
		r<-d1/100
		conversión<-" Conversion de Centimetros a Metros "
	SiNo
		si(opc==2)Entonces
//Para convertir centimetros a yardas debemos de dividir el numero ingresado por 91.44 es decir: n/91.44
			r<-d1/91.44
			conversión<-"Conversión de Centimetros a Yardas "
		SiNo
			si(opc==3)Entonces
				r<-d1/83.90
				Escribir "Conversión de Centimetros a Varas"
			SiNo
				si (opc==4)Entonces
//Para convertir centimetros a pulgadas debemos de dividir el numero ingresado por 2.54 es decir; n/2.54
					r<-d1/2.54
					conversión<-"Conversión de Centimetros a Pulgadas "
				SiNo
					si (opc==5)Entonces
//Para realizar la conversión a pies se debe dividir el numero ingresado por 30.48 es decir; n/30.48
						r<-d1/30.48
						conversión<-"Conversión de Centimetros a Pies "
					SiNo
//Si el usuario ingresa una Opcion no valida se le mostrara el siguiente mensaje
						Limpiar Pantalla
						Escribir "La opcción seleccionado no se reconoce, se le invita a mejorar su comprensión lectora :v"
						
					FinSi
				FinSi
			FinSi
		FinSi
	FinSi
	Escribir "El resultado de la ", conversión, "es: ",r
FinAlgoritmo



*C++*
//Programa que sirva como conversor de longitudes entre ellas a; (metros, yardas, varas, pulgadas y pies)
//Pidiendo la usuario ingresar el dato que desea convertir este debe ser ingresado en longitud de centimetros.
//Luego se le mostrara al usuario los tipos de conversion puede realiar el programa.
//Luego se realizara la conversión selecciona por el usuario y se le mostrara el resultado en la medida que anteriormente selecciono. :3
#include <iostream>

int main() {
    double centimetros;
    
    //Pedimos ingresar la cantidad en centimetro y la guardamos en la variable centimetros
    std::cout <<"\n***Bienvenido***\n";
	std::cout << "Ingrese la cantidad en centimetros: ";
    std::cin >> centimetros;
    
    //se le muestra al usuario un menu con las medidas disponibles para convertir la cantidad anteriormente ingresada en centimetros;
    int opcion;
    
    //utilizamos la funcion do para mostrar el menu de opciones junto con while para repetir este mismo menu luego de una conversion. 
    do {
        std::cout << "\n--- Tipos de Conversion disponibles ---\n";
        std::cout << "1. Convertir a Metros\n";
        std::cout << "2. Convertir a Yardas\n";
        std::cout << "3. Convertir a Varas\n";
        std::cout << "4. Convertir a pulgadas\n";
        std::cout << "5. Convertir a pies\n";
        std::cout << "6. Salir\n";
        std::cout << "Ingrese el numero de opcion: ";
        std::cin >> opcion;
        
    //Utilizamos un switch para hacer los respectivos procedimientos necesarios para realizar la conversión deseado por usuario, teniendo 6 procesos entre ellos el salir del programa
	//Tambien agregaremos una opcion llamada default que se mostrara cuando el usuario seleccione una opción que no se encuentre en el anterior menú de opciones.    
        switch (opcion) {
            case 1:
                // Convertir a Metros(n/100)
                std::cout << "Resultado en metros: " << centimetros / 100 << std::endl;
                break;
            case 2:
                // Convertir a Yardas(n/91.44)
                std::cout << "Resultado en Yardas: " << centimetros / 91.44 << std::endl;
                break;
            case 3:
                // Convertir a Varas(n/83.90)
                std::cout << "Resultado en Varas: " << centimetros / 83.90 << std::endl;
                break;
            case 4:
            	//Convertir a Pulgadas(n/2.54)
                std::cout << "Resultado en Pulgdas: "<< centimetros / 2.54 << std::endl;
                break;
            case 5:
                // Convertir a Pies(n/30.48)
                std::cout << "Resultado en Pies: " << centimetros / 30.48 << std::endl;
                break;    
            case 6:
                // Saliendo del programa(El usuario desea salir del programa :(  )
                std::cout << "Saliendo del programa." << std::endl;
                break;
            default:
                std::cout << "!Opcion seleccionada no valida, revisa la opciones y intentalo de nuevo :3" << std::endl;
                break;
        }
//El siclo while servira para repetir el menu de conversion al finalizar alguna de las mismas.  
	} while (opcion != 6);
    
    return 0;
}


//+__+



*PYTHON*
#Programa que simule un conversor con 5 tipos de conversión de longitudes las cuales son;metros, yardas, varas, pulgadas, pies.
#El programa tiene como primera función pedir N cantidad en centimetros la cual ingresara el usuario.
#Posteriormente se le mostrar un menú con los 5 tipos de conversión disponibles anteriormente mencionados
#El usuario escojera el que quiera, posteriormente se le mostrara la conversión a la longitud escojida


#Definimos las operaciones para realizar conversiónes;

#A Metros(n/100)
def convertir_a_metros(centimetros):
    return centimetros / 100

#A Yardas(n/91.44)
def convertir_a_yardas(centimetros):
    return centimetros / 91.44

#A Varas(n/83.90)
def convertir_a_varas_(centimetros):
    return centimetros / 83.90

#A Pulgadas(n/2.54)
def convertir_a_pulgadas(centimetros):
    return centimetros / 2.54

#A Pies(n/30.48)
def convertir_a_pies(centimetros):
    return centimetros / 30.48

#Se le pedira al usuario una cantidad la cual sera tomada y guardada en la variable centimetros
def main():
    centimetros = float(input("***BIENVINIDO***\n Ingrese la cantidad en centímetros que desea convertir: "))

   
    while True:
#Se le mostará al usuario el menú de conversiones disponibles en el cual el seleccionara el que quiera.
        print("\n--- Menu de Conversiones ---")
        print("1. Convertir a Metros. ")
        print("2. Convertir a Yardas. ")
        print("3. Convertir a Varas")
        print("4. Convertir a Pulgadas")
        print("5. Convertir a Pies")
        print("6 Salir")

#La opción que escoja se guardara en la variable opcion        
        opcion = input("Ingrese el número de Conversión deseada : ")

#Usaremos el siclo if para realizar los procesos correspondiente y mostrar el resultado de conversión final.       
        if opcion == "1":
            metros = convertir_a_metros(centimetros)
            print(f"{centimetros} centímetros equivalen a {metros:.2f} metros")

        elif opcion == "2":
            pies = convertir_a_yardas(centimetros)
            print(f"{centimetros} centímetros equivalen a {yardas:.2f} yardas")

        elif opcion == "3":
            pies = convertir_a_varas(centimetros)
            print(f"{centimetros} centímetros equivalen a {varas:.2f} varas")
            
        elif opcion == "4":
            pulgadas = convertir_a_pulgadas(centimetros)
            print(f"{centimetros} centímetros equivalen a {pulgadas:.2f} pulgadas")

        elif opcion == "5":
            pies = convertir_a_pies(centimetros)
            print(f"{centimetros} centímetros equivalen a {pies:.2f} pies")

        elif opcion == "4":
            print("Salir del programa.")
            break
#Si el usuario ingresa una opción que no este dentro del anterior menú se le mostrará un mensaje el cúal es el siguiente;
        else:
            print("Opción inválida. Por favor, ingrese una opción válida.")

#El siguiente bloque tendra como función asegurarase de que el escrib main se ejecute unicamente cuando el codigo sea abierto directamente.
if __name__ == "__main__":
    main()

