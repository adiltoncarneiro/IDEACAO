Instalando o Esp32 wemos Oled built in na Ide arduino.

compiar o aquivo .jason em arquivo>preferencias.
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_dev_index.json
Instalar as bibliotecas Adafruit_SSD1306.h; Adafruit_GFX.h

Sketch>Incluir biblioteca>Gerenciar Biblioteca

Incluir essas bibliotecas as bibliotecas abaixo no programa

include <Wire.h>
include <Adafruit_GFX.h>
include <Adafruit_SSD1306.h>
include <SPI.h>
include <Fonts/FreeSerif12pt7b.h>
Caso algumas dessas bibliotecas não esteja em sua IDE, basta instalar na aba Gerencia Biblioteca.

Veja o exemplo "Test_ESP32_na_IDE_arduino.ino"

Outro exemplo é usando a biblioteca #include "SSD1306.h" e reconfigurar os pinos SAD e SCL usando o comando SSD1306 screen(0x3c, 5, 4). Neste caso, a biblioteca SSD1306.h também precisa estar instalada.
Veja o exemplo ESP32-oled-wemos.ino. em que é feito uma medida de um sinal do ldr e mostrado no display.

Atenção, quando for gravar no Esp 32 com Oled Built in, vá em Ferramentas e escolha a placa "Wemos Lolin32" e a porta onde o esp está conectado.

Maiores informações sobre comandos para uso do display Oled no esp32, veja este link Guia Completo do Display OLED (parte 2) - Como programar - Blog Eletrogate