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
- ESP 32
- Sensor de temperatura DHT11
- Sensor ultrassônico HC-SR04
- Resistor 220 Ω
- Jumpers

### Inicialmente configure o seu projeto

* Navegue até a pasta do projeto, com seu console do SDK (ESP-IDF Command Prompt) e rode o comando abaixo.
```
idf.py menuconfig
```
#### Após rodar o comando a seguinte tela deve aparecer:

![menuconfig](https://drive.google.com/file/d/1WO8gpZSzAVsHSBAyMAmAAFNtqJMMEwb3/view?usp=sharing)

#### Acesse `Example Configuration` .

![port](https://user-images.githubusercontent.com/56330822/99081795-190acd00-25a2-11eb-8f07-d66c372a836d.PNG)

#### Configure a Porta `Port`, caso queira, ou  pode deixar a padrão que está executando na porta 3333.
#### Retorne a tela anterior.

#### Acesse `Example Connection Configuration` .

![Redeconfig](https://user-images.githubusercontent.com/56330822/99082473-f4fbbb80-25a2-11eb-8547-e671b19ec0ef.PNG)

#### Configure o Nome de sua rede `WiFi SSID`. 
#### Configure A Senha da sua rede `WiFi Password`.
#### Apos os procedimentos. Salve as alteraçoes e Saia do menuconfig..

### Build and Flash

Ainda na pasta do projeto, com seu console do SDK (ESP-IDF Command Prompt) 
Com tudo configurado conforme passado nos passos acima, execute a ferramenta de monitoramento para visualizar a saída serial utilizando o comando:

```
idf.py -p PORT flash monitor
```

#### Após rodar o comando a seguinte tela deve aparecer:

![rodando](https://user-images.githubusercontent.com/56330822/99083292-190bcc80-25a4-11eb-8d32-2093400483a2.PNG)

## Otimo! O servidor está no Ar.

#### Em vermelho na imagem, visualize o `IP` que o servidor obteve e em sequencia a `Porta` que definimos. Observe no seu console os dados atribuidos, e os guarde, que iremos utilizar em breve.

### Estabelecer uma conxão Cliente/Servidor.

#### Neste exemplo eu uso o Realterm, para estabelecer uma conexão cliente/server.
Lembrando inicie primeiro o servidor para receber os dados solicitados pelo cliente (aplicativo).

### Após baixar e instalar o realterm em seu dispositivo, execute-o.
### Vá até a Aba `Port`. Mostrada na iamgem.

![realterm1](https://user-images.githubusercontent.com/56330822/99087159-355e3800-25a9-11eb-9d7c-0d2e6e77b8c4.PNG)

### Na Aba Port. Prencha o campo `Port` com `IP:PORT` obtidos anteriormente. Apos isto Click! em Change para aplicar as configuraçoes.
### Ao lado, em Status os seguintes campos devem aparecer como vizualizados na imagem.

## Pronto! A conexão Cliente/Server foi estabelecia.

### Agora voce pode enviar seus codigos ASCII ao servidor. E receber as informaçoes requisitadas.
### Exemplo de codigo `TEMP` e `DIST` enviados. Mostrados na imagem.

![req](https://user-images.githubusercontent.com/56330822/99088037-3cd21100-25aa-11eb-85b8-7390de8bc8fe.PNG)

### Agora voce mesmo pode enviar os codigos: `TEMP`, `DIST`, `UMID`, `LEDB` e `HELP` para obter respostas do servidor.

## Hardware montado

![1605657509003](https://user-images.githubusercontent.com/56330822/99466001-52349b80-291a-11eb-998a-e4559d3dead5.jpg)
![1605657508995](https://user-images.githubusercontent.com/56330822/99466040-68daf280-291a-11eb-879b-badacaad7450.jpg)

### Funcionamento(links abaixo).

https://drive.google.com/file/d/1FW2UvrYbyrKgUVBmfQuviJEhruBpIOhX/view?usp=sharing
https://drive.google.com/file/d/1FV6pgn5strIO8e3OTrx3VouHx9_sFR5Q/view?usp=sharing


