# Proyecto-Estacion-de-Subte-Arduino

![portada](https://github.com/IbarrolaCamila/Proyecto-Estacion-de-Subte-Arduino/blob/main/img/TINKERCAD.png "portada")
## Integrantes:
* Ibarrola Camila.
* Franco Beltran.
* Mateo Ciotti.
* Matias Diaz.

## Proyecto: ESTACIONES DE SUBTE.

![subte](https://github.com/IbarrolaCamila/Proyecto-Estacion-de-Subte-Arduino/blob/main/img/DOJO2.png "subte")

## Descripción

Un sistema que permite al usuario saber a qué estación de subte está, además indica las estaciones 
que faltan hasta llegar a destino. 

## Función principal

Su función es prender los leds ,y el buzzer cuando el subte esté posicionado en cada estación.
Mientras el display 7 segmentos, indica cuantas estaciones faltan para llegar a destino.  

Muestra de como se conforma el codigo:
```c++
//FUNCIÓN PRINCIPAL:
void Secuencia(){
  Serial.println("Ejecutando la secuencia");
  Buzzer_estacion(2000,100);//diferentes sonidos en cada estación. 
  prende_apagar_led(LED_DOS, LED_UNO);//prende y apaga el led, de la estación donde esté posicionado en el momento.
  prender_numeros(0); //muestra el número de estaciones que falta para llegar a destino. por el Display 7 segmentos.
  
  delay(1000);
  
  Buzzer_estacion(2500, 100);
  prende_apagar_led(LED_UNO, LED_DOS);
  prender_numeros(1);
  
  delay(1000);
  
  Buzzer_estacion(3000, 100);
  prende_apagar_led(LED_DOS, LED_TRES);
  prender_numeros(2);
  
  delay(1000);
  
  Buzzer_estacion(4000, 100);
  prende_apagar_led(LED_TRES, LED_CUATRO);
  prender_numeros(3);
  
  delay(1000);
  
  Buzzer_estacion(3000, 100);
  prende_apagar_led(LED_CUATRO, LED_TRES);
  prender_numeros(2);
  
  delay(1000);
  
  Buzzer_estacion(2000, 100);
  prende_apagar_led(LED_TRES, LED_DOS);
  prender_numeros(1);
  
  delay(1000);
}
```

## Link del proyecto :bullettrain_side:
* [proyecto](https://www.tinkercad.com/things/k3UB8dzCkfp-dojo-2/editel?sharecode=12arpQE7rdqUSzyPkCzbLUD4u1XqaNa1t1efZn32NeM)


### Fuentes
* [tutorial markdown](https://www.youtube.com/watch?v=oxaH9CFpeEE)
* [emojis](https://gist.github.com/rxaviers/7360908)