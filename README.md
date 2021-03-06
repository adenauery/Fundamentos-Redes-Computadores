## Fundamentos de Redes de Computadores


### Primeiro Encontro - 01/09/2020

#### Sockets TCP & UDP
[Introdução ao Conceito de Sockets](http://olaria.ucpel.edu.br/materiais/lib/exe/fetch.php?media=introducao-sockets.pdf)

#### Conceitos Relacionados à IoT:
* [Slides](http://olaria.ucpel.edu.br/materiais/lib/exe/fetch.php?media=iot_slides_introdutorios.pdf)
* [IoT Comic Book](https://iotcomicbook.org/)

#### Trocando Informações Sensoriadas do Meio entre equipamentos
  * Conceitos
    * [Protocolo MQTT - Material IBM](https://www.ibm.com/developerworks/br/library/iot-mqtt-why-good-for-iot/index.html)
    * [Protocolo MQTT - Material Curto Circuito](https://www.curtocircuito.com.br/blog/introducao-ao-mqtt/)
    * [Slides sobre MQTT - Material UFC](https://pt.slideshare.net/MaurcioMoreiraNeto/protocolo-mqtt-redes-de-computadores)
    * [Comparação MQTT & Outros Protocolos](https://medium.com/internet-das-coisas/iot-05-dando-uma-breve-an%C3%A1lise-no-protocolo-mqtt-e404e977fbb6)
  * Plataformas de Software
    * [Mosquitto da Eclipse Foundation](https://mosquitto.org)
    * [Brokers MQTT gratuitos e pagos para utilizar em projetos da IoT](https://diyprojects.io/8-online-mqtt-brokers-iot-connected-objects-cloud/#.XzfHmEl7nUI)
    * [Explorando o uso de MQTT em Programas Python](https://fazbe.github.io/Usando-o-paho-mqtt-para-Python/)


#### Instalando os Clientes da Plataforma Mosquitto

* sudo apt install mosquitto-clients

* Testes feitos com o Broker: broker.emqx.io

* mosquitto_sub -h broker.emqx.io -t pi4

* mosquitto_pub -h broker.emqx.io -t pi4 -m "Primeira Conexao"


#### Publicando com Scritp Bash em Broker MQTT
~~~
#!/bin/bash
contador=1
while [ $contador -le 10 ]
do
        mosquitto_pub -h broker.emqx.io -t pi4 -m $contador
        sleep 3
        let contador=contador+1
done
~~~

### Segundo Encontro - 29/09/2020

#### Novos Cenários de Aplicação: discussões sobre Sensores, Atuadores, Cloud and Fog Computing.
 * [Apresentação](http://olaria.ucpel.edu.br/materiais/lib/exe/fetch.php?media=apresentacao-fund-redes-computadores.pdf)
 
#### Rede SIGFOX para Sensores e Atuadores:
 * https://www.sigfox.com

#### Exemplos de Pesquisas Envolvendo os Cursos:

~~~
Douglas Scheunemann
http://olaria.ucpel.edu.br/douglas/

Anderson Cardozo
http://olaria.ucpel.edu.br/acardozo/

Rogerio Albandes: 
http://olaria.ucpel.edu.br/ralbandes/

Veronica Tabim:
http://olaria.ucpel.edu.br/vtabim/

Patrick Fernandes
http://olaria.ucpel.edu.br/patrickjbf/

Felipe Haertel
http://olaria.ucpel.edu.br/fhaertel/

˜˜˜
