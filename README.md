# Projeto de Controle de LEDs WS2818B com Joystick no Raspberry Pi Pico

Este projeto utiliza um Raspberry Pi Pico para controlar uma matriz de LEDs WS2818B com base na posição de um joystick analógico. O código lê as entradas do joystick e acende o LED correspondente na matriz, permitindo uma interação visual simples.

## Funcionalidades

- Controle de uma matriz de 5x5 LEDs WS2818B.
- Leitura da posição do joystick em dois eixos (X e Y).
- Mapeamento da posição do joystick para a matriz de LEDs.
- Atualização dinâmica dos LEDs com base na posição do joystick.

## Componentes Necessários

- Raspberry Pi Pico
- LEDs WS2818B (25 unidades)
- Joystick analógico
- Resistores e fios para conexão
- Fonte de alimentação adequada (se necessário)

## Estrutura do Código

O código é dividido em várias funções principais:

- `npInit()`: Inicializa a comunicação com os LEDs e configura todos os LEDs para apagados.
- `npSetLED()`: Define a cor de um LED específico na matriz.
- `npClear()`: Apaga todos os LEDs na matriz.
- `npWrite()`: Atualiza o estado dos LEDs no hardware.
- `joystickInit()`: Inicializa o ADC para ler os valores do joystick.
- `getJoystickLEDIndex()`: Mapeia a posição do joystick para um índice de LED na matriz.

## Como Configurar e Executar

1. **Configuração do Ambiente**: Certifique-se de ter o ambiente de desenvolvimento do Raspberry Pi Pico configurado. Você pode usar o [Pico SDK](https://github.com/raspberrypi/pico-sdk) para compilar o código.

2. **Conexões**:
   - Conecte os LEDs WS2818B ao pino GPIO especificado no código (pino 7).
   - Conecte os eixos X e Y do joystick aos pinos GPIO correspondentes (pinos 27 e 26).

3. **Compilar o Código**:
   - Clone este repositório e navegue até o diretório do projeto.
   - Compile o projeto usando o CMake com o Pico SDK.

4. **Carregar o Código**:
   - Carregue o firmware compilado no Raspberry Pi Pico.

5. **Executar o Projeto**:
   - Conecte a fonte de alimentação ao Raspberry Pi Pico.
   - Abra um terminal serial para visualizar a saída de depuração.
   - Mova o joystick para acender o LED correspondente na matriz.

## Contribuições

Sinta-se à vontade para fazer melhorias ou reportar problemas. Pull requests são bem-vindos!

## Licença

Este projeto é licenciado sob a [Licença MIT](LICENSE).