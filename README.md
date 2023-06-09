# Informe
Codigo de ejercicios de Fisica
import math 


def fisica(Vo, Vf, t1, t2, a, h_i):
  #Ingresar el tema a realizar 
  # "Calcular desplazamiento":
  # "Tiempo de caida":
  # "Calcular a dos tiempos"
  # "Altura máxima"
    cadena = "Altura máxima"

    if cadena == "Calcular desplazamiento":
       #Para calcular el desplzamiento se debe ingresar : Vo , a , t1
        velocidad_inicial = Vo  #  m/seg
        aceleracion = a  #  m/seg^2
        tiempo = t1  #  seg

        velocidad_final = velocidad_inicial + (aceleracion * tiempo)
        desplazamiento = (velocidad_inicial * tiempo) + (0.5 * aceleracion * tiempo**2)

        print("Velocidad final es:", velocidad_final, " m/seg")
        print("El Desplazamiento es:", desplazamiento, " metros")

    elif cadena == "Tiempo de caida":

      #Para calcular el tiempo de caida se debe ingresar : a , h inicial 
      altura_inicial = h_i  # Altura inicial en metros
      gravedad = a  #  m/seg^2

      velocidad_final = math.sqrt(2 * gravedad * altura_inicial)
      tiempo_caída = math.sqrt((2 * altura_inicial) / gravedad)

      print("La velocidad final es:", velocidad_final, "m/seg")
      print("El tiempo de caída es:", tiempo_caída, "seg")

    elif cadena == "Calcular a dos tiempos":

       #Para calcular a dos tiempos se debe ingresar : Vo , t1,t2,a

      velocidad_inicial = Vo  #  m/seg
      tiempo_1 = t1  # Tiempo en segundos para la velocidad constante
      aceleracion = a  #  m/seg^2
      tiempo_2 = t2  # Tiempo en segundos para la aceleración

      velocidad_final = velocidad_inicial + (aceleracion * tiempo_2)

      desplazamiento_1 = velocidad_inicial * tiempo_1
      desplazamiento_2 = (velocidad_inicial * tiempo_2) + (0.5 * aceleracion * tiempo_2**2)
      desplazamiento_total = desplazamiento_1 + desplazamiento_2

      print("La velocidad final es:", velocidad_final, "m/seg")
      print("El Desplazamiento total es:", desplazamiento_total, "metros")

    elif cadena == "Altura máxima":
      
      #Para calcular la altura máxima se debe ingresar : Vo ,a
     
      velocidad_inicial = Vo  #  m/s
      aceleracion_gravedad = a  #  m/s^2
     
      tiempo_alcanzar_altura_maxima = - Vo / a
      altura_maxima = (Vo ** 2) / (2 * abs(a))


      print("La altura máxima alcanzada es de :", altura_maxima, "metros")
      print("El tiempo para alcanzar la altura máxima es de :", tiempo_alcanzar_altura_maxima, "seg")


#     Ingreso de datos para la realización de ejercicios
#     Orden de ingreso de datos
#     Vo,Vf,t1,t2,a, h inicial
fisica(20,0,10,0,9.8,0)
