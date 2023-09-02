grupo: Juan Jose Marroquin Aquino - 7690-23-16390
      Jose Miguel Marroquin Aquino - 7690-23- 16393
      



c++ ahorcado
#include <iostream>
#include <string>

int main() {
    int x, n, a, error;
    char letra;
    std::string secreta, vector1, vector2;

    std::cout << "Ingresa la palabra secreta: ";
    std::cin >> secreta;

    n = secreta.length();
    vector1 = secreta;
    vector2.resize(n, '_');

    a = 0;
    while (a < 5) {
        for (x = 0; x < n; x++) {
            std::cout << vector2[x];
        }
        std::cout << std::endl;

        std::cout << "Ingresa una letra: ";
        std::cin >> letra;

        error = 1;
        for (x = 0; x < n; x++) {
            if (letra == vector1[x]) {
                if (vector2[x] == '_') {
                    vector2[x] = letra;
                    error = 0;
                }
            }
        }

        if (vector1 == vector2) {
            std::cout << "Felicidades, has ganado el juego" << std::endl;
            a = 6;
        } else {
            if (error == 1) {
                a++;
            }

            if (a == 1) {
                std::cout << ".\n.\n.\n.\nTe quedan 4 intentos" << std::endl;
            } else if (a == 2) {
                std::cout << ".....\n.\n.\n.\nTe quedan 3 intentos" << std::endl;
            } else if (a == 3) {
                std::cout << ".....\n.   o\n.\n.\nTe quedan 2 intentos" << std::endl;
            } else if (a == 4) {
                std::cout << ".....\n.   o\n.   ^\n.\nTe quedan 1 intento" << std::endl;
            } else if (a == 5) {
                std::cout << ".....\n.   o\n.   ^\n.   ^\nPERDISTE, QUEDASTE AHORCADO" << std::endl;
            }
        }
    }

    return 0;
}

psudocodigo ahorcado
Algoritmo detarea
	Definir x,n,a,error Como entero
	Definir letra,secreta,vector1,vector2 Como Caracter
	Escribir "Ingresa la palabra secreta"
	leer secreta
	n = Longitud(secreta)
	Dimension vector1[n], vector2[n]
	para x = 1 hasta n  
		vector1(x) = Subcadena(secreta,x,x)	
		vector2(x) = "_"
	FinPara
	a = 0
	Mientras a < 5 Hacer
		para x = 1 Hasta n //Con Paso 1 Hacer
			Escribir vector2(x) Sin Saltar
		FinPara
		Escribir ""
		Escribir "Ingresa una letra"
		leer letra
		error = 1
		para x = 1 Hasta n Con Paso 1 Hacer
			si letra == vector1(x) Entonces
				si vector2(x) == "_" Entonces
					vector2(x) = letra
					error = 0
					c = c + 1
				FinSi
			FinSi			
		FinPara
		
		si c == n Entonces
			Escribir "Felicidades has ganado el juego"
			a = 6
		SiNo
			si error == 1 Entonces
				a = a + 1
			FinSi		
			
			si a == 1 Entonces
				Escribir "."
				Escribir "."
				Escribir "."
				Escribir "."
				Escribir "Te quedan 4 intentos"
			FinSi
			si a == 2 Entonces
				Escribir "....."
				Escribir "."
				Escribir "."
				Escribir "."
				Escribir "Te quedan 3 intentos"
			FinSi
			si a == 3 Entonces
				Escribir "....."
				Escribir ".   o"
				Escribir "."
				Escribir "."
				Escribir "Te quedan 2 intentos"
			FinSi
			si a == 4 Entonces
				Escribir "....."
				Escribir ".   o"
				Escribir ".   ^"
				Escribir "."
				Escribir "Te queda 1 intento"
			FinSi
			si a == 5 Entonces
				Escribir "....."
				Escribir ".   o"
				Escribir ".   ^"
				Escribir ".   ^"
				Escribir "AHORCADO"
			FinSi
		FinSi		
	FinMientras
FinAlgoritmo














c++ pitagoras 
#include <iostream>
iusing namespace std;
int main() {
    int a, b, c;
    int n = 4;

    for (a = 1; a <= n - 1; a++) {
        for (b = 1; b <= n - 1; b++) {
            for (c = 1; c <= n - 1; c++) {
                if (a * a + b * b == c * c) {
                    std::cout << "terna pitagorica (" << a << "," << b << "," << c << ")" << std::endl;
                }
            }
        }
    }

    return 0;
}

pitagoras pseudocodigo

Algoritmo TernaPitagorica
		definir a, b, c Como Entero
		n=500
		para a=1 hasta n-1
			para b=1 hasta n-1
				para c= 1 hasta n-1
					si a^2 + b^2 = c^2 Entonces
						mostrar "terna pitagorica (",a,",",b,",",c,")"
					FinSi
					
				FinPara
			FinPara
		FinPara
		
FinAlgoritmo
