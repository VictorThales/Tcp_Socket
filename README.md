<img alt="GoStack" src="https://lh6.googleusercontent.com/proxy/K5fmOf83OCmcXLL6A8C661JiY_kCgEehnEzR8zyhludeemsL9n4R3vq1Q2aQBN_Vvd1PucGHzvY21aQNl_mvkhHDVNTAeFlgTLxVWaAQ4_eX" />

# TCP Server UTDE(Umidade, Temperatura, Distancia, Estado)

O aplicativo desenvolvido cria um socket TCP com uma porta especificada e aguarda uma solicitação de conexão do cliente. Depois de aceitar a solicitação do cliente, a conexão entre o servidor e o cliente é estabelecida e o aplicativo aguarda os dados que serão enviados pelo cliente. Os dados enviados são processados como texto ASCII e retorna a resposta ao cliente cuja oque foi solicitado. Neste exemplo o cliente irá enviar TEMP, UMID ou DIST, e o aplicativo retornará os valores respectivos de cada sensor.

## Antes de começar

### Verifique a versão do seu SDK.
- [X] Algoritmo Desenvolvido com SDK Version ESP-IDF v4.1-dirty
### Descompacte-o na pasta do seu SDK.
- [X] Libs já incluidas e importadas neste diretorio.
- Defina os pinos dos sensores no cabeçalho do projeto 

## Componentes
Componentes utilizados: 
1. ESP 32
1. Sensor de temperatura DHT11
1. Sensor ultrassônico HC-SR04
1. Resistor 220 Ω
1. Jumper ~~à gosto~~


