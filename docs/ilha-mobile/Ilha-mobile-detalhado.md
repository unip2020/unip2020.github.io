---
layout: default
title: Ilha Mobile Detalhado
parent: Ilha de Mobile
permalink: /mobile/detalhe
nav_order: 1
---

# Detalhe Geral

## Introdução

O propósito deste documento é informar aos participantes do projeto sobre seu desenvolvimento geral, suas funções, benefícios além de possíveis restrições e limitações, tudo de forma detalhada e o mais clara possível para um entendimento geral.
O documento possui os requisitos funcionais e não funcionais especificados de acordo com o planejamento desenvolvido pelos participantes do projeto.

## Finalidade

O projeto consiste da criação de um aplicativo para celulares Android que visa trazer serviços e ferramentas digitais para auxiliar o usuário.

## Escopo

O projeto foi dividido em múltiplas ilhas com finalidades e escopos diferentes, cada uma responsável por um setor, sendo estes: Backend, Web, Mobile, Holograma e Mapeamento. Este documento refere a ilha de desenvolvimento mobile, o qual o objetivo é desenvolver um aplicativo de celular cujo desempenha tarefas que ajudem o usuário a: localizar produtos, navegar o supermercado, ajustar seu carrinho de compras e conferir produtos e promoções realizadas pelo supermercado.

## Visão Geral
Além desta seção introdutória, as seções seguintes estão organizadas como descrito abaixo.
* **Seção 2** - Descrição geral: apresenta uma descrição geral do projeto, caracterizando qual é o seu escopo e descrevendo seus usuários.
* **Seção 3** - Requisitos não funcionais: cita e descreve brevemente os requisitos não funcionais do projeto.
* **Seção 4** - Requisitos funcionais: cita e descreve brevemente os requisitos
funcionais do projeto.
* **Seção 5** - Casos de uso: descreve o funcionamento de certas interações de atores com o projeto
* **Seção 6** - Tecnologías usadas: cita e descreve as tecnologias usadas para o desenvolvimento do projeto.

## Descrição Geral
O objetivo do aplicativo mobile é facilitar a experiência de compra dos usuários utilizando ferramentas de localização e listagem. Ele visa principalmente atingir usuários que têm dificuldade de navegar em supermercados ou que desejam ir direto ao produto desejado sem ter que procurá-los diretamente.

**Requisitos não funcionais**

1. **Dispositivo portátil:**
O aplicativo necessita de um dispositivo móvel com um sistema android versão 7 ou superior.
2. **Banco de dados:**
O aplicativo necessita de acesso à um banco de dados com informações sobre os produtos disponíveis e clientes cadastrados.
3. **Sistema de localização:**
O aplicativo necessita de acesso à um sistema de localização em interiores para traçar rotas.

**Requisitos funcionais:**

1. **Cadastrar conta:**
 * O aplicativo deve permitir que o usuário se cadastre como cliente. A tela de cadastro de conta consiste de campos de texto obrigatórios e opcionais e um botão “Finalizar cadastro”.

    * **Campos obrigatórios:**
        * E-mail.
        * Senha.
        * Nome.
    * **Campos opcionais:**
        * Endereço.
        * CEP.

2. **Fazer login com conta cliente:**
O aplicativo deve permitir que o usuário faça login com sua conta. A tela de login consiste de campos de identificação, um botão “Fazer login” e um botão “Criar conta”.
3. **Consultar produto:**
O aplicativo deve permitir que o usuário consulte informações sobre um ou mais produtos.
4. **Gerar rota até um produto:**
O aplicativo deve gerar uma rota do presente local do usuário até um produto especificado caso esta seja solicitada pelo usuário.
5. **Gerar carrinho de compras:**
O aplicativo deve permitir que o usuário adicione produtos consultados a um carrinho.
6. **Contatar SAC:**
O aplicativo deve permitir que o usuário consiga entrar em contato com o SAC.

**Casos de uso:**

**Cadastro de conta**

<table>
    <thead>
        <tr>
            <td colspan="2"><b>[CASE01] Cadastro de conta</b></td>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><b>Referência</b></td>
            <td>[ReqF01] Cadastrar cliente</td>
        </tr>
        <tr>
            <td><b>Sumário</b></td>
            <td>O usuário faz o cadastro de uma conta cliente.</td>
        </tr>
        <tr>
            <td><b>Pré-condições</b></td>
            <td>O dispositivo usado deve ter conexão com a internet.</td>
        </tr>
        <tr>
            <td><b>Atores</b></td>
            <td>Cliente, Servidor.</td>
        </tr>
        <tr>
            <td><b>Descrição</b></td>
            <td>
                1. O Cliente pressiona o botão “criar nova conta”.<br>
                2. O aplicativo exibe uma tela que contém um formulário com campos para os dados necessários para o cadastro e um botão para “criar sua conta”.<br>
                3. O Cliente pressiona o botão “criar sua conta”.<br>
                4. O aplicativo envia os dados preenchidos ao Servidor para validação.<br>
                5. O aplicativo recebe um retorno do Servidor confirmando o cadastro.<br>
                6. O aplicativo retorna à tela inicial.
            </td>
        </tr>
        <tr>
            <td><b>Alternativas</b></td>
            <td>
                1. No passo 3, caso haja algum campo obrigatório vazio ou com dados inválidos, o aplicativo exibe um aviso na tela informando o campo a ser preenchido corretamente e o formato de dados válido para o campo.<br>
                2.No passo 5, caso o Servidor retorne um erro com o processo de validação o aplicativo exibe um aviso na tela informando o motivo. E.g: “E-mail já cadastrado”.
            </td>
        </tr>
        <tr>
            <td><b>Exceção</b></td>
            <td>
                O cadastro da conta cliente não pode ser concluído caso o Cliente deixe de preencher um campo obrigatório, caso dados inválidos tenham sido preenchidos ou caso existam dados salvos anteriormente no servidor que sejam idênticos aos dados preenchidos.
            </td>
        </tr>
    </tbody>
</table>


**Consultar produto**

<table>
    <thead>
        <tr>
            <td colspan="2"><b>[CASE02] Consultar produto</b></td>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><b>Referência</b></td>
            <td>[ReqF03] Consultar produto</td>
        </tr>
        <tr>
            <td><b>Sumário</b></td>
            <td>O cliente pesquisa produtos disponíveis.</td>
        </tr>
        <tr>
            <td><b>Pré-condições</b></td>
            <td>O dispositivo usado deve ter conexão com a internet.</td>
        </tr>
        <tr>
            <td><b>Atores</b></td>
            <td>Cliente, Servidor.</td>
        </tr>
        <tr>
            <td><b>Descrição</b></td>
            <td>
                1. O Cliente preenche o campo de pesquisa com o nome ou parte do nome do produto desejado.<br>
                2. O Cliente pressiona o botão “Pesquisar”.<br>
                3. O dados usados para pesquisa são enviados ao backend.<br>
                4. O backend retorna informações sobre os produtos relacionados à pesquisa.<br>
                5. O aplicativo exibe uma tela com o resultado da pesquisa.
            </td>
        </tr>
        <tr>
            <td><b>Alternativas</b></td>
            <td> - </td>
        </tr>
        <tr>
            <td><b>Exceção</b></td>
            <td>
                A pesquisa não deve ser efetuada caso o cliente não preenche o campo de pesquisa.
            </td>
        </tr>
    </tbody>
</table>

**Adicionar produtos ao carrinho**

<table>
    <thead>
        <tr>
            <td colspan="2"><b>[CASE03] Adicionar produtos ao carrinho</b></td>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><b>Referência</b></td>
            <td>[ReqF03] Consultar produto, [ReqF05] Gerar carrinho de compras</td>
        </tr>
        <tr>
            <td><b>Sumário</b></td>
            <td>Cliente adiciona produtos consultados à um carrinho de compras digital.</td>
        </tr>
        <tr>
            <td><b>Pré-condições</b></td>
            <td>O dispositivo usado deve ter conexão com a internet, [CASE02].</td>
        </tr>
        <tr>
            <td><b>Atores</b></td>
            <td>Cliente.</td>
        </tr>
        <tr>
            <td><b>Descrição</b></td>
            <td>
                1. O Cliente determina a quantidade de produto a ser adicionado.<br>
                2. O cliente pressiona o botão “Adicionar ao carrinho”.<br>
                3. O aplicativo adiciona o produto na lista do carrinho.
            </td>
        </tr>
        <tr>
            <td><b>Alternativas</b></td>
            <td> - </td>
        </tr>
        <tr>
            <td><b>Exceção</b></td>
            <td>
                O produto não é adicionado ao carrinho caso a quantidade determinada seja menor ou igual a 0.
            </td>
        </tr>
    </tbody>
</table>

**Geração de rota até um produto**

<table>
    <thead>
        <tr>
            <td colspan="2"><b>[CASE04] Geração de rota até um produto</b></td>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><b>Referência</b></td>
            <td>[ReqF03] Consultar produto, [ReqF05] Gerar rota até um produto</td>
        </tr>
        <tr>
            <td><b>Sumário</b></td>
            <td>O cliente determina um produto, uma rota partindo da posição atual do cliente indo até o produto determinado é gerada e exibida no aplicativo.</td>
        </tr>
        <tr>
            <td><b>Pré-condições</b></td>
            <td>O dispositivo usado deve ter conexão com a internet, [CASE02].</td>
        </tr>
        <tr>
            <td><b>Atores</b></td>
            <td>Cliente, Backend.</td>
        </tr>
        <tr>
            <td><b>Descrição</b></td>
            <td>
                1. O cliente pressiona o botão “rota”.<br>
                2. O aplicativo envia dados sobre o local para o backend.<br>
                3. Após serem processados o backend retorna informações de rota.<br>
                4. O aplicativo exibe a rota em um tela no aplicativo.
            </td>
        </tr>
        <tr>
            <td><b>Alternativas</b></td>
            <td> - </td>
        </tr>
        <tr>
            <td><b>Exceção</b></td>
            <td>
                A rota não é gerada caso ocorra um erro com o processamento de dados de rota.
            </td>
        </tr>
    </tbody>
</table>

## Tecnologias usadas

No desenvolvimento do projeto foram utilizadas as tecnologias descritas abaixo, escolhidas durante o planejamento, para realizar funções específicas.

1. **Android Studio**  
Android Studio é uma ferramenta de desenvolvimento mobile, desenvolvida pela Google utilizando como base o IntelliJ IDEA da JetBrains. É uma IDE de código aberto que trabalha especificamente para o desenvolvimento na plataforma Android, possuindo diversas utilidades que ajudam bastante na simplificação e agilização do desenvolvimento do código, dentre eles:
* Suporte para compilações baseadas em Gradle;
* Refatoração de código específica para Android;
* Editor de layout que permite que usuários arrastem componentes de interface de usuário, com opção de pré-visualizar layouts em várias configurações de tela;
* Integração com GitHub.  
Levando em consideração essas utilidades, Android Studio foi considerada a melhor ferramenta para o desenvolvimento respectivo do projeto.

2. **Kotlin:**  
Kotlin é uma linguagem de programação multiplataforma de propósito geral que trabalha utilizando a JVM, assim como Java. Ela foi escolhida para se trabalhar no projeto por possuir uma versatilidade maior que a linguagem Java, que seria a outra opção para se utilizar no desenvolvimento.
Ela é uma linguagem muito mais eficiente e com código mais simples, graças aos seus lambdas e co-rotinas, além de ser ​ null-safe, o que ajuda bastante no apuramento de bugs e erros. Além disso ela possui uma integração bem robusta com Java, permitindo que você utilize de basicamente quase todas as funções e bibliotecas que são utilizáveis em Java.

3. **Unity**  
Unity é uma game engine, ou seja, é uma IDE projetada com foco em desenvolvimento de jogos. Embora sua principal funcionalidade seja desenvolvimento de jogos, diversas outras funcionalidades foram adicionadas à Unity ao longo dos anos, tornando possível o desenvolvimento de vários tipos diferentes de softwares.
Unity possui suporte para diversas plataformas, como Linux, Windows e principalmente Android, facilitando o processo de integração com das funcionalidades AR com a parte mobile do projeto.

4. **Linguagem C#**  
C# é uma linguagem de programação multi-paradigma de propósito geral. Projetada para ser simples, moderna e para ser usada no desenvolvimento de componentes de software adequados para ambientes distribuídos. C# é também a linguagem principal da Unity, a game engine que está sendo usada para desenvolvimento do módulo de geração de rotas usando Realidade Aumentada.

5. **Firebase**  
Firebase é um conjunto de serviços prestados a área mobile e web, no caso deste projeto sua utilização principal é o Firebase Auth, que é o serviço de autenticação de login utilizado pelo usuário.

6. **Android Jetpack**  
Android Jetpack é um conjunto de componentes, ferramentas e orientações que ajudam no desenvolvimento de aplicações android. É basicamente um conjunto essencial de bibliotecas para desenvolvimento android de maneira geral, e nosso projeto não é exceção;

7. **Android Room**  
Room é uma biblioteca de persistência que fornece uma interação com banco de dados SQLite, é uma ferramenta que serve como uma camada de interação com o banco de dados.