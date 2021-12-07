# LoraWan 

## Do sensor até o usuário
O envio de informação desde um ou vários tipos de sensores, em operação remota,  pode seguir a configuração apresentada na seguinte imagem:



### End Node
Dispositivo eletrônico a batería com capacidade de monitoramento, procesamento e transmissão sem fio usando o protocolo LoRa na faixa de frequência desde 915 até 928 MHz.

### LoRa Gateway
Abstrai os dados do protocolo UDP do roteador de pacotes (packet forwarder) no formato JSON e envia-os para o servidor LoRa usando  MQTT.

### LoRa Server

É o servidor de rede LoRaWAN. Desduplica e trata as estruturas de carga recebidas do gateway, trata da camada MAC de LoRaWAN e agenda as transmissões para descarga dos dados.

### LoRa APP Server

É o servidor LoRaWAN da applicação  e lida com solicitações de conexão, criptografia de pacotes e oferece uma interface para serviços externos com APIs JSON, gRPC ou MQTT. Possui uma interface de usúario via web para administração de usuários, gestão de aplicações e dispositivos. Também, permite visualizar os dados dos sensores. Tanto LoRa Server quanto o App Server precisam de sua propria base de dados PostgreSQL.

