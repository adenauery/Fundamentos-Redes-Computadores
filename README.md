## Fundamentos de Redes de Computadores

### Segundo Encontro - 13/09/2021 (Segunda-Feira) - 19h

#### Conceitos Relacionados a Sistemas que Operam em Redes de Computadores:

* [Slides](http://olaria.ucpel.edu.br/materiais/lib/exe/fetch.php?media=iot_slides_introdutorios.pdf)
* [O Protocolo HTTP](http://olaria.ucpel.edu.br/materiais/lib/exe/fetch.php?media=protocolo-http.pdf)
* [Enlace de Dados](http://olaria.ucpel.edu.br/materiais/lib/exe/fetch.php?media=enlace-de-dados.pdf)
* [IoT Comic Book](https://iotcomicbook.org/)
* [Portas Usuais em TCP/IP](https://pt.wikipedia.org/wiki/Lista_de_portas_dos_protocolos_TCP_e_UDP)

### Primeiro Encontro - 23/08/2021 (Segunda-Feira) - 19h

#### Sockets TCP & UDP
[Introdução ao Conceito de Sockets](http://olaria.ucpel.edu.br/materiais/lib/exe/fetch.php?media=introducao-sockets.pdf)

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

* mosquitto_sub -h broker.emqx.io -t pi2a

* mosquitto_pub -h broker.emqx.io -t pi2a -m "Primeira Conexao"


#### Publicando com Scritp Bash em Broker MQTT
~~~
#!/bin/bash
contador=1
while [ $contador -le 10 ]
do
        mosquitto_pub -h broker.emqx.io -t pi2a -m $contador
        sleep 3
        let contador=contador+1
done
~~~

