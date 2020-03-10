---
layout: default
title: Ilha de Mapeamento
nav_order: 3
description: "Documentação da ilha de Mapeamento"
permalink: /mapeamento
---

# Ilha de Mapeamento

A área de mapeamento será responsável por capturar informações dos cliente externos(usuários comuns e possíveis compradores) e clientes internos(funcionários do estabelecimento), todos deverão se conectar a rede wireless do local, os dados capturados serão apenas informações sobre distancia(RSSI e subtração de ruídos) dos dispositivo moveis(ou qualquer outro dispositivo conectado a rede) para que sejá possível realizar a triangulação de distancia em relação as outras antenas e se tornar possível saber a localização exata do dispositivo.
Existem diversas tecnologias que poderiam ser utilizadas para esse rastreamento como bluetooth e rfid, optamos pelo Wirelles devido a essas outras tecnologias gerarem um desconforto nas pessoa ao precisar utilizar e fazer algo diferente em seus dispositivos as quais estão habituadas(apenas questão de habito do ser humano) e o wirelless podemos criar uma motivação a mais nas pessoas, essa motivação seria o acesso a internet sem consumir dados moveis do aparelho, tornando assim mais fácil a aceitação ao uso da ferramenta, outra questão é sobre gerar um relatório com o numero de adesões e aceitação do cliente ao uso, nessa tecnologia é possível detectar os dispositivos mesmo que esses não se conetem a rede e também se torna possível saber em quais locais a pessoa andou, com menos precisão mas ainda sim passível de ser monitorado.
Faremos também o controlo das gôndulas e estoque, optamos por utilizar algo mais simples e de fácil acesso aos estabelecimentos, usaremos apenas um leitor de código de barras para entrada no estoque e saída, as saídas do estoque lançam automaticamente os produtos a sua respectiva gondula/prateleira e localização no supermercado que ficam armazenados em uma outra tabela, a qual os produtos receberão baixa ao ser bipados no caixa na hora do pagamento.
O controle dos carrinhos será controlada apenas com um melhor processo documentando a responsabilidade de um funcionário que de hora em hora irá passar por todas a fileiras do mercado e irá levar os carrinhos até a area definida na entrada do local, o aplicativo apenas indicara sempre ao usuário esse local.

* **Capitação e monitoramento dos clientes.**
	Uma rede Wireless com Access Points estarão espalhadas pelo local, a partir da distancia(RSSI) em que a pessoa se encontra da antena em que está conectada, será feito uma triangulação com o sinal das outras antenas dessa forma passando a localização exata do cliente, esse calculo leva em consideração a subtração do ruido. 
* **Controle e mapeamento do estoque.**
	Estoque será controlado via código de barras do produto, ao sair do estoque o produto devera ser lido seu código de barras e entrara para a nova tabela de gôndula do produto que somente recebera baixa ao ser passo pelo caixa. 
* **Controle e mapeamento de carrinhos.**
	O carrinho será controlado apenas através de um processo, onde terá uma pessoa que devera passar a cada hora pelo corredores do local e levar os carrinhos até o ponto definido na entrada do estabelecimento, o aplicativo sempre indicara esse ponto para a pessoa que precisar.