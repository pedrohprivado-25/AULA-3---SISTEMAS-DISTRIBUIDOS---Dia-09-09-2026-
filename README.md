# Aula 3 - Sistemas Distribuídos

Nesta aula de Sistemas Distribuídos, continuamos os estudos sobre comunicação entre processos, dando foco aos protocolos **TCP e UDP** e à comunicação entre cliente e servidor utilizando Python.

Durante a aula, colocamos o UDP em prática criando um servidor e um cliente, executando os dois em terminais diferentes e realizando o envio e recebimento de mensagens. Também fizemos alterações no servidor para que ele pudesse continuar funcionando e receber várias mensagens. 

## Conteúdos estudados

- Comunicação entre processos
- Protocolos de comunicação
- Diferenças entre TCP e UDP
- Endereço IP e portas
- Sockets em Python
- Comunicação cliente-servidor
- Recebimento de vários datagramas
- Comunicação entre computadores pela rede
- Localização de serviços em sistemas distribuídos

Na parte teórica, vimos que o **TCP** é orientado à conexão e possui mecanismos de confiabilidade, ordenação e retransmissão de dados. Já o **UDP** trabalha com datagramas e não oferece as mesmas garantias, sendo interessante em situações onde velocidade e baixa latência são mais importantes. 

## Atividade prática

Na atividade prática, criamos os arquivos `servidor_udp.py` e `cliente_udp.py` e executamos cada um em um terminal. O servidor ficou aguardando as mensagens enviadas pelo cliente e, após o envio, conseguimos verificar a comunicação funcionando corretamente. 

Também modificamos o servidor para utilizar um `while True`, permitindo que ele continuasse funcionando depois de receber uma mensagem e pudesse receber novos envios sem precisar ser reiniciado. 

## Comunicação pela rede

Outra parte da aula foi testar a comunicação entre computadores diferentes. Para isso, o servidor foi configurado com `0.0.0.0` e utilizamos o comando `ipconfig` para descobrir o endereço IPv4 do computador que estava executando o servidor. Esse endereço foi então utilizado pelo cliente para realizar a comunicação pela rede. 

Nos testes realizados, conseguimos enviar uma mensagem pelo cliente e receber a resposta do servidor, mostrando na prática a comunicação entre os dispositivos utilizando UDP. 

## Desafio conceitual

Também foi realizado um desafio para analisar qual protocolo seria mais adequado em diferentes situações.

| Situação | Protocolo escolhido |
|---|---|
| Transferência de arquivo | TCP |
| Videoconferência | UDP |
| Operação financeira crítica | TCP |
| Jogo on-line | UDP |

A atividade mostrou que não existe um protocolo que seja simplesmente "melhor" que o outro. A escolha depende das necessidades de cada aplicação, principalmente em relação à confiabilidade, velocidade e latência. 

## O que aprendi

Nesta aula consegui entender melhor na prática como funciona a comunicação entre um cliente e um servidor utilizando UDP. Além da parte de programação, também ficou mais claro para mim quando faz mais sentido utilizar TCP ou UDP dependendo do tipo de aplicação.

Outro ponto que achei interessante foi perceber que, em sistemas distribuídos maiores, não basta apenas saber o IP e a porta de um servidor. Também é necessário pensar em como os serviços são encontrados e como os diferentes componentes conseguem continuar se comunicando quando existem vários servidores ou quando algum deles apresenta uma falha. 

## Arquivos desta aula

- `aula3.pptx` — Slides utilizados na aula
- `ATIVIDADE PRATICA - Aula - 3 Sistemas Distribuidos.docx` — Atividade prática de comunicação UDP
- `SISTEMAS DISTRIBUÍDOS — AULA 3 DESAFIO.docx` — Desafios práticos da aula
- `Desafio_Conceitual_TCP_UDP_Aula_3.docx` — Desafio conceitual sobre TCP e UDP

## Conclusão

A Aula 3 foi importante para continuar a parte prática de Sistemas Distribuídos. Através dos testes com Python, consegui visualizar melhor como funciona a comunicação entre processos e como dois computadores podem trocar informações pela rede.

Além disso, a comparação entre TCP e UDP ajudou a entender que a escolha do protocolo deve levar em consideração o que a aplicação realmente precisa.
