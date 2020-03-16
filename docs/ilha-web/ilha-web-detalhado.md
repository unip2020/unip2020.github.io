---
layout: default
title: Ilha WEB Detalhado
parent: Ilha de WEB
permalink: /web/detalhe
nav_order: 1
---

# Detalhe Geral

O setor administrativo com todas as suas burocracias têm demonstrado ultimamente
o quão necessário é um sistema administrativo que possa auxiliar e facilitar a vida
do administrador, podendo gerir o estoque, colaboradores e outras funções
administrativas.
A quantidade de startups que atuam no setor administrativo é grande, mas é ainda
um mercado com um grande potencial de crescimento.
Nos últimos anos estamos vivenciando o nascimento de grandes startups e uma das
ferramentas mais queridas para desenvolvimento de sistemas dessa nova geração
é a utilização de frameworks que auxiliam neste processo.
O Angular foi a primeira iniciativa do google na construção de um framework,
portanto o Angular é um framework javascript para a construção de páginas únicas
em que o usuário recebe todos os arquivos da aplicação, ou seja, ele não precisa
mais consultar ao servidor para buscar outra página.
Um exemplo seria caso o usuário está na página inicial e ele acessa a página de
contato não é necessário ele ir lá no servidor buscando a página de contato, pois, a
página já armazenada na máquina dele, ou seja, quem faz essa rota é a aplicação
frontend executada diretamente no navegador dele.
Esse trabalho tem como objetivo a criação de um sistema administrativo integrado,
dessa forma será possívelá gerir estoques, ajudar na administração dos colaboradores e em outras funções administrativas.

* **Requisitos Funcionais**

    * **Funcionário**
        * **Cadastro de produto:**
            * Incluir produto – O funcionário irá cadastrar o produto no sistema.
        * **Cadastrar categoria:**
            * Nome da categoria – O funcionário vai cadastrar qual a categoria do produto.
            * Editar atributos – Em caso de cadastrar errado a categoria, o funcionário tem como editar e modificar a descrição.
            * Remover categoria – Caso não precise mais de uma certa categoria, tem como exclui-la
        * **Cadastrar lote recebido:**
            * Incluir lote de produto – Assim que chegar o lote de mercadoria, o funcionário vai cadastrar neste modulo.
        * **Ver estoque:**
            * Visualizar produto – O funcionário responsável do estoque, tem como ver as seguintes funcionalidades: descrição, quantidade, posição, pedido de compra, lote.
        * **Cadastrar outros funcionários:**
            * Cadastro de colaboradores – A pessoa responsável, irá cadastrar os novos colaboradores da empresa.
            * Cadastro de Terceiros – A pessoa responsável, irá cadastrar os novos prestadores de serviço da empresa.
    * **Administrativo**
        * **Ver estoque:**
            * Visualizar produto – O funcionário responsável do estoque, tem como ver as seguintes funcionalidades: descrição, quantidade, posição, pedido de compra, lote.
        * **Ver relatórios:**
            * Produtos a vencer – Controle de produtos a vencer.
            * Pedidos de compra – Controlar os pedidos de compra.
            * Consumo diário, semanal e anual de produtos – Controlar o consumo dos produtos da empresa.
            * Movimentação – Controlar a movimentação dos produtos na empresa.
        * **Ver funcionários:**
            * Fixa cadastral – Modulo de visualização da função e setor do funcionário.
        * **Ver produtos:**
            * Visualizar produto – Modulo de visualização dos produtos em estoque.
            * Alterar descrição do produto – Pra caso precise alterar a descrição do produto.
        * **Balanço de vendas:**
            * Vendas a prazo – Balanço contábil das vendas a prazos.
            * Vendas à vista – Balanço contábil das vendas a vista.
            * Lucro – Balanço contábil do lucro da empresa.
        * **Gerenciar cargos:**
            * Fixa cadastral – Módulo onde somente o gerente tem a permissão de visualizar e gerenciar os funcionários com as informações da função, setor e salário.
            * Horas trabalhadas – Controle das horas trabalhadas.
            * Horas extras – Controle das horas extras
            * Excluir funcionário – Em caso de demissão do funcionário.

# Caso de uso

## Módulo do administrador.

Para o administrador do sistema, é de grande importância conhecer seus números,
pois é somente através deles, é possível conhecer completamente a sua empresa.
Pensando nisso, foi atribuído funcionalidades, para que o administrador possa ter
total controle e acesso aos seus dados.

**Visualização de estoque:**

Permite conhecer todos os produtos disponíveis em estoque e suas respectivas
quantidades.

**Gerenciamento de colaboradores:**

Possibilidade um controle de todos os colaboradores e seus respectivos cargos e
responsabilidades, tendo um controle total de cada área da empresa e seus
responsáveis.

**Análise de preços:**

Com base em um balanço do valor comprado e na demanda do produto, permitir
analisar a melhor margem de revenda, tendo em vista o melhor lucro e a demanda
sobre o produto.

**Balanço de vendas:**

Se consiste em um relatório geral, que analisa todas os dados anteriores.
É possível obter um balanço dos itens vendidos e do percentual de lucro em cima, visando melhorar a margem de lucro e o fluxo de mercadoria no mercado.
Com base em gráficos, permite ao administrador identificar itens com venda insatisfatórios e analisar meios de otimizar as suas vendas.

**Relatórios:**

Através dos relatórios, se obtém as informações de tudo que foi vendido, itens em
estoque e margens de lucro.
Permite que o administrador identifique valores de vendas diárias, itens que estão
prestes a vencer, e itens que não estão tendo um bom desempenho de venda,
assim conseguindo analisar meios de otimizar controlar suas vendas.

## Módulo do funcionário.

**Cadastro de produto:**

Facilite o cadastro de produto ao inventário, com o cadastro de informações úteis
aos administradores, onde o funcionário deve inserir o produto, a data da chegada,
categoria, validade e lote.

**Consulta de estoque:**

Caso um determinado produto não seja encontrado nas prateleiras, é possível
através de uma simples consulta, saber quantos desse item ainda estão disponíveis
para o cliente.
Em casos de esgotamento, é possível acionar um alerta, caso não haja previsão de
reabastecimento do produto.

**Fazer pedido ao fornecedor:**

Possibilita ao gerente solicitar o reabastecimento de um produto e realizar cotações
com o fornecedor

**Cadastro de funcionários:**

Aba destinada a inclusão de novos funcionários ao sistema, habilitando acessos e
responsabilidades.

**Requisitos Não Funcionais**

* **Desempenho**
    * Em nosso sistema administrativo integrado, focaremos em desenvolver um projeto no qual tenha um tempo de resposta curto e seja feita diversas funções com agilidade.
* **Usabilidade**
    * Em questão de usabilidade do sistema, sua interface gráfica será desenvolvida de forma que fique fácil interagir com o sistema independente do nível do conhecimento do usuário, facilitando o uso e padronizando todo o sistema.
* **Confiabilidade**
    * Neste ponto teremos uma questão de garantia para atender a todos pré-requisitos definidos pelo usuário.
* **Segurança**
    * Quando falamos sobre o ponto de segurança, todo o sistema será com base da criptografia web SHA2 trazendo uma maior segurança para o usuário e confidencialidade da informação que estará circulando pelo sistema.
* **Disponibilidade**
    * O sistema será hospedado em um servidor no qual sua disponibilidade deverá ser 24x7, pois, vários setores e funções dependem dele para o funcionamento do estabelecimento e seus respectivos setores.
* **Manutenção**
    * Será executado manutenção preventiva a cada período pré-determinado pelo responsável, onde nela será possível prever os erros que poderão ocorrer e corrigindo-os com antecedência.
* **Tecnologias envolvidas**
    * Quando falamos sobre as tecnologias aplicadas a este sistema, podemos citar por exemplo HTML5 para o desenvolvimento do layout, CSS3 para a criação visual da interface, JavaScript para gerenciar funções de scripts, Rest API para comunicação, Materialize para auxiliar no desenvolvimento.

## Tecnologia aplicada

O ​ **Visual Studio Code​** , desenvolvido em 2015 pela Microsoft, é uma IDE, ou editor de código-fonte, ou editor de texto multiplataforma disponibilizado pela Microsoft destinado à desenvolver aplicações web, ele oferece suporte para muitas linguagens, neste projeto iremos utilizar o JavaScript, HTML e CSS.

**JavaScript** é uma linguagem de programação que foi criada em 1996 pelo famoso programador Brendan Eich (foi um dos fundadores da Mozilla Corporation), a intenção era tornar as programações dentro das páginas web com alertas e animações mais simples. Atualmente o JavaScript, além de animações e alertas, implementa gráficos, mapas ou informações que se atualizam em períodos padronizados, por exemplo

**HTML (Hypertext Markup Language)**, é o componente de base pra web, e também é uma linguagem de marcação usada para estruturar páginas web; ela é fundamentada em tags, que representam diversos elementos de uma página, como imagens, links, botões, etc.

**CSS​ (Cascading Style Sheets)** é um mecanismo para adicionar estilo a um documento web, e também é uma linguagem de folhas de estilo; ele representa a parte visual do site (cor do texto e do fundo, fonte, espaçamento, tabelas, layouts, ajustar imagens para suas telas).

**Materialize** é um framework front-end tem o intuito de entregar uma design mais limpo, consciente e objetivo, para aplicativos e páginas mobile em diferentes plataformas; é uma combinação bem elaborada dos fundamentos do bom design clássico com a adição de tecnologia e ciência.

**Rest Api** é uma interface que fornece dados em um formato padronizado baseado em requisições HTTP; ela fica parada até que acontece uma requisição, É como uma moto estacionada que só é ativada após a ignição com a chave.