



![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143019386/573b708a-189b-4f4f-b55b-4b443c69c8d5)



# ¡Bienvenidos al repositorio del Grupo 5 del curso de Fundamentos de biodiseño!
## Proyecto: Modelo de lente de Realidad Virtual para Detección de Glaucoma a Través del Fondo de Ojo 


## ¿Quiénes somos?

Somos estudiantes de la carrera de Ingeniería Biomedíca de Pontificia Universidad Católica del Perú (PUCP) en conjunto con la Universidad Peruana Cayetano Heredia (UPCH). Buscamos diseñar soluciones tecnológicas, las cuales sean capaces de antender una necesidad en el ámbito de la salud.

## Objetivo
Encontrar la propuesta de solución más factible trabajando todos de manera colaborativa, y así, ser capaces de afrontar la enfermedad del *Glaucoma*, de la cual hablaremos más adelante y veremos cómo esta afecta tanto a nivel nacional como internacional.
Si deseas conocer un poco más acerca de nuestro proyecto, puedes darle click al siguiente enlace: https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/tree/main/Listado%20de%20entregables

##  El equipo 5

- Alexander Martinez (Colaborador - Encargado del software) - alexander.martinez@upch.pe
- Jairo Villalobos (Colaborador - Encargado de la página web) - jairo.villalobos@upch.pe
- Hudson Oliva (Colaborador - Encargado de investigación) - hudson.oliva@upch.pe
- Nicolas Herrera (Colaborador - Líder y encargado del hardware) - nicolas.herrera@upch.pe
- Ariana Dextre (Colaborador) - Encargado del modelado) - ariana.dextre@upch.pe


### Profesores del curso

- Paulo Camilo Alberto Vela Anton
- Umbert Lewis de la Cruz Rodriguez
- Eder Juárez
- Jose Alonso Cáceres del Aguila


/*
  Active Learning Labs
  Harvard University 
  tinyMLx - OV7675 Camera Test

*/

#include <TinyMLShield.h>

bool commandRecv = false; // flag used for indicating receipt of commands from serial port
bool liveFlag = false; // flag as true to live stream raw camera bytes, set as false to take single images on command
bool captureFlag = false;

// Image buffer;
byte image[176 * 144 * 2]; // QCIF: 176x144 x 2 bytes per pixel (RGB565)
int bytesPerFrame;

void setup() {
  Serial.begin(9600);
  while (!Serial);

  initializeShield();

  // Initialize the OV7675 camera
  if (!Camera.begin(QCIF, RGB565, 1, OV7675)) {
    Serial.println("Failed to initialize camera");
    while (1);
  }
  bytesPerFrame = Camera.width() * Camera.height() * Camera.bytesPerPixel();

  Serial.println("Welcome to the OV7675 test\n");
  Serial.println("Available commands:\n");
  Serial.println("single - take a single image and print out the hexadecimal for each pixel (default)");
  Serial.println("live - the raw bytes of images will be streamed live over the serial port");
  Serial.println("capture - when in single mode, initiates an image capture");
}

void loop() {
  int i = 0;
  String command;

  bool clicked = readShieldButton();
  if (clicked) {
    if (!liveFlag) {
      if (!captureFlag) {
        captureFlag = true;
      }
    }
  }

  // Read incoming commands from serial monitor
  while (Serial.available()) {
    char c = Serial.read();
    if ((c != '\n') && (c != '\r')) {
      command.concat(c);
    } 
    else if (c == '\r') {
      commandRecv = true;
      command.toLowerCase();
    }
  }

  // Command interpretation
  if (commandRecv) {
    commandRecv = false;
    if (command == "live") {
      Serial.println("\nRaw image data will begin streaming in 5 seconds...");
      liveFlag = true;
      delay(5000);
    }
    else if (command == "single") {
      Serial.println("\nCamera in single mode, type \"capture\" to initiate an image capture");
      liveFlag = false;
      delay(200);
    }
    else if (command == "capture") {
      if (!liveFlag) {
        if (!captureFlag) {
          captureFlag = true;
        }
        delay(200);
      }
      else {
        Serial.println("\nCamera is not in single mode, type \"single\" first");
        delay(1000);
      }
    }
  }
  
  if (liveFlag) {
    Camera.readFrame(image);
    Serial.write(image, bytesPerFrame);
  }
  else {
    if (captureFlag) {
      captureFlag = false;
      Camera.readFrame(image);
      Serial.println("\nImage data will be printed out in 3 seconds...");
      delay(3000);
      for (int i = 0; i < bytesPerFrame - 1; i += 2) {
        Serial.print("0x");
        Serial.print(image[i+1], HEX);
        Serial.print(image[i], HEX);
        if (i != bytesPerFrame - 2) {
          Serial.print(", ");
        }
      }
      Serial.println();
    }
  }
}





