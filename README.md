# Biblia NVI & Harpa Crista para M5Stack Cardputer ADV

[![Platform](https://img.shields.io/badge/Platform-ESP32--S3-orange.svg)](https://docs.espressif.com/)
[![Framework](https://img.shields.io/badge/Framework-Arduino-blue.svg)](https://www.arduino.cc/)
[![Device](https://img.shields.io/badge/Hardware-M5Stack%20Cardputer%20ADV-green.svg)](https://docs.m5stack.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Firmware standalone em arquivo `.bin` e codigo-fonte aberto para o **M5Stack Cardputer** e **Cardputer ADV** (ESP32-S3 com display 240x135 e teclado TCA8418).

Permite a leitura completa da Biblia Sagrada (versao NVI) e de todos os 640 hinos da Harpa Crista diretamente no dispositivo, de forma 100% offline, silenciosa e com texto nitido.

---

## Caracteristicas Principais

- **Biblia Sagrada Completa (NVI - Nova Versao Internacional):**
  - Todos os 66 livros (39 do Antigo Testamento e 27 do Novo Testamento).
  - 1.189 capitulos e mais de 31.000 versiculos.
  - Numeracao de versiculos destacada em dourado.
- **Harpa Crista Completa:**
  - Todos os 640 hinos tradicionais com estrofes e refrao (`[Coro]`).
- **Texto Limpo e Legivel:**
  - Caracteres normalizados para visualizacao perfeita no display 240x135 sem glifos ou simbolos quebrados.
- **100% Offline e Independente:**
  - Todo o banco de dados e compactado e embutido diretamente na memoria Flash do ESP32-S3.
  - Nao requer Wi-Fi, internet ou arquivos adicionais para funcionar.
- **Silencioso:**
  - Modo somente leitura com saida de som desativada para leitura em reunioes, cultos ou estudos.
- **Recursos Extras:**
  - **Busca Rapida:** Digite `JO 3`, `SL 23`, `15` ou `H 545` para ir direto ao capitulo ou hino.
  - **Palavra do Dia:** Sorteia um versiculo biblico aleatorio a cada clique.
  - **Hino Aleatorio:** Sorteia um hino da Harpa Crista.
  - **Indicador de Bateria:** Mostra a porcentagem exata da bateria no canto superior direito.

---

## Controles no Teclado do Cardputer

| Tecla / Acao | Funcao |
| :--- | :--- |
| **`;` / `W` / `K`** | Mover cursor para cima / Pagina anterior |
| **`/` / `S` / `J`** | Mover cursor para baixo / Proxima pagina |
| **`,` / `A` / `H`** | Capitulo anterior / Pagina anterior |
| **`.` / `D` / `L`** | Proximo capitulo / Proxima pagina |
| **`Space` (Espaco)** | Avancar pagina no leitor / Novo versiculo aleatorio |
| **`N`** | Avancar diretamente para o proximo capitulo ou hino |
| **`P`** | Voltar diretamente para o capitulo ou hino anterior |
| **`Enter`** | Confirmar selecao / Abrir capitulo ou hino |
| **`Del` / `Backspace` / `BtnA` (G0)** | Voltar ao menu anterior / Apagar caractere |
| **`0` a `9`** | Digitar diretamente o numero do hino ou capitulo desejado |

---

## Como Instalar no seu Cardputer

### Metodo 1: Pelo Cartao MicroSD (M5Launcher) - Mais Rapido
1. Baixe o arquivo binario compilado: `bin/Cardputer_Biblia_Harpa_ADV.bin`.
2. Copie para a raiz ou para a pasta do seu cartao MicroSD.
3. Insira o MicroSD no Cardputer, ligue o dispositivo com a tecla `G0` pressionada (ou abra o **M5Launcher**).
4. Selecione `Cardputer_Biblia_Harpa_ADV.bin` e grave no slot de execucao.

### Metodo 2: Gravacao Direta via Cabo USB-C
Conecte o Cardputer ao computador via USB-C e execute com o Python:
```bash
python -m esptool --chip esp32s3 write_flash 0x10000 bin/Cardputer_Biblia_Harpa_ADV.bin
```
Ou use qualquer gravador via navegador (como [ESP Web Flasher](https://espressif.github.io/esptool-js/)).

---

## Licenca

Este projeto e distribuido sob a licenca MIT.
