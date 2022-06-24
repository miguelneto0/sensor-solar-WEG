# sensor-solar-WEG

Este é um projeto desenvolvido para fins e refere-se aos trabalhos práticos da disciplina de Sistemas de Tempo Real da Universidade Federal de Santa Catarina - UFSC.

Trata-se de controlador de boiler acoplado de sensores de umidade e temperatura, que são alimentados por energia solar pelo acionamento de uma bomba (B1) dos coletores de água, uma bomba (B2) para os canos de abastecimento e um aquecedor (A1) que transporta água quente para o boiler. Este trabalho é implementado em linguagem C e o código base é fornecido pelo Professor Romulo Oliveira, na página da da disciplina (https://link). 

O trabalho conta ainda com uma aplicação na nuvem (acessada através da plataforma WEGnology https://wegnlogy.io) que pode monitorar e enviar comandos para a instrumentação. A WEGnology é um produto da empresa WEG que permite criar aplicações de IoT disponibilizando diversos recursos através de uma simples conta de usuário por meio da aba Sandbox.

Neste trabalho, foi utilizado o protocolo MQTT para comunicação entre a instrumentação e o app da WEG. A plataforma fornece um MQTT Broker embutido e um formato para criação dos tópicos MQTT providos pela Losant (um conjunto de softwares para soluções IoT da WEGnology), que facilita a troca de mensagens através de mensagens PUBLISH e SUBSCRIBE, nesse caso, acessando os tópicos da aplicação configurados no momento da criação do Device. A troca de mensagens, nesse caso, é realizada através de mensagens com o formato losant/DEVICEId/state e losant/DEVICEId/command.
