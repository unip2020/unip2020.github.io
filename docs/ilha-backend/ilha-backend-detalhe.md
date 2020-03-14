---
layout: default
title: Ilha Backend Detalhado
parent: Ilha de Backend
nav_order: 1
---

# Detalhe Geral
O Projeto recebeu o nome de Super Mercado Inteligente e está sendo desenvolvido para melhorar a experiência de navegação do cliente durante suas compras, além de seus outros módulos que visam controle de estoque, mapeamento, controle de fluxo, análise de produtos e funcionários.
Ilha de Backend:
Esta ilha é o centro de todo o projeto, onde serão desenvolvidos serviços em uma arquitetura REST para que possamos gerenciar os recursos do supermercado de diversas plataformas diferentes.

![](./../../../assets/images/bed.png)

**Requisitos Não Funcionais:**

* **Servidor Cloud:**
O que é cloud computing?
Cloud computing ou computação em nuvem é uma tecnologia que oferece recursos computacionais remotos, como memória, processamento e armazenamento de dados. Nela, você pode hospedar sites, e-commerces, softwares e outros sistemas.
Por que cloud computing?
Escolher uma das soluções em cloud, seja IaaS (Infraestrutura como Serviço) ou PaaS (Plataforma como Serviço), garante aos seus projetos o uso da capacidade sob demanda, otimização de performance, segurança e previsibilidade de custos, sem compartilhar espaço ou recursos computacionais.

<img src="./../../../assets/images/cloud.png" height="250" width="250">

* **Linguagem de Programação JAVA**
O que é Spring Boot
Spring Boot é um projeto da Spring que veio para facilitar o processo de configuração e publicação de nossas aplicações. Você escolhe os módulos que deseja através dos starters que inclui no pom.xml do seu projeto. Eles, basicamente, são dependências que agrupam outras dependências.
Apesar do Spring Boot, através da convenção, já deixar tudo configurado, nada impede que você crie as suas customizações caso sejam necessárias.

![](./../../../assets/images/sbfa.png)

* **Banco de Dados** 
O que é o PostgreSQL?
O PostgreSQL é um sistema de gerenciamento de banco de dados objeto-relacional (SGBDOR) baseado no POSTGRES Versão 4.2 desenvolvido pelo Departamento de Ciência da Computação da Universidade da Califórnia em Berkeley. O POSTGRES foi pioneiro em vários conceitos que somente se tornaram disponíveis muito mais tarde em alguns sistemas de banco de dados comerciais.
O PostgreSQL é um descendente de código fonte aberto deste código original de Berkeley, que suporta grande parte do padrão SQL e oferece muitas funcionalidades modernas, como:
* comandos complexos
* chaves estrangeiras
* gatilhos
* visões
* integridade transacional
* controle de simultaneidade multiversão
Além disso, o PostgreSQL pode ser ampliado pelo usuário de muitas maneiras como, por exemplo, adicionando novos
* tipos de dado
* funções
* operadores
* funções de agregação
* métodos de índice
* linguagens procedurais
Devido à sua licença liberal, o PostgreSQL pode ser utilizado, modificado e distribuído por qualquer pessoa para qualquer finalidade, seja particular, comercial ou acadêmica, livre de encargos.

![](./../../../assets/images/heroku.png)

**Requisitos Funcionais:**

* **WEB Gerenciamento** 

    * Cadastrar, Alterar e Excluir Produtos.
    * Cadastrar, Alterar e Excluir Categoria de Produtos.
    * Cadastrar, Alterar e Excluir Funcionários.
    * Cadastrar, Alterar e Excluir Setores.
    * Cadastrar, Alterar e Excluir Fornecedores.
    * Inserir entrada de Lotes.
    * Dar entrada em pedidos de produtos aos Fornecedores.

* **Mobile** 

    * Mostrar localização de produtos.
    * Inserir, Alterar e Excluir Pedidos de Clientes.
    * Adicionar, Alterar e Remover itens da lista de compras do Cliente.
