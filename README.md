# Organizaçao-de-Dados---Adega

O **Adega Online** é um software de automação comercial e gestão de banco de dados desenvolvido para otimizar as operações diárias de um estabelecimento que atua nos segmentos de adega e tabacaria. O sistema visa solucionar uma crise operacional eliminando processos manuais, centralizando o fluxo de caixa, o controle rígoso de estoque e a gestão de créditos internos ("fiados").

---

##Cenário e Problema Identificado

A organização possui um alto volume transacional focado em vendas rápidas de balcão e contas de crédito abertas para clientes recorrentes. Sem um sistema centralizado, o estabelecimento enfrentava os seguintes gargalos:
* **Desorganização no Estoque:** Falta de precisão na reposição e no balanço financeiro.
* **Vendas Fragmentadas:** Inconsistências frequentes nos fechamentos de caixa diários.
* **Gestão de "Fiados":** Controle descentralizado sujeito a falhas humanas e esquecimentos de cobrança.
* **Desalinhamento Operacional:** Riscos de desvios e descumprimento de ordens operacionais.

---

##Funcionalidades Principais (Requisitos)

O sistema foi mapeado e construído sob os seguintes critérios essenciais:

##Requisitos Funcionais
* **Cadastro de Produtos (RF01):** CRUD completo (Criar, Ler, Atualizar e Deletar) contendo descrição, preço de custo, preço de venda e saldo de estoque.
* **Controle de Estoque Automatizado (RF02):** Baixa automática de itens integrada ao fluxo de vendas.
* **Controle de Fiado (RF03):** Registro de clientes elegíveis a prazo com histórico de débitos e limite de saldo.
* **Módulo de Vendas (RF04):** Checkout de balcão com cálculo automático e associação do operador logado.
* **Abertura e Fechamento de Caixa (RF05):** Controle do fluxo financeiro diário incluindo o aporte/troco inicial.

##Requisitos Não Funcionais
* **Usabilidade:** Interface intuitiva e limpa para operação rápida de novos funcionários.
* **Desempenho:** Arquitetura leve capaz de rodar fluidamente em computadores antigos ou simples.
* **Operação Offline:** Funcionamento autônomo sem dependência constante da internet para não travar as vendas de balcão.
* **Segurança:** Níveis de acesso protegidos por senha para separar as funções de operador e gerente.

---

##Regras de Negócio Implementadas

Para garantir a integridade financeira e legal do negócio, as seguintes diretrizes foram codificadas no sistema:
1. **Bloqueio de Estoque Negativo:** Uma venda só é processada se houver saldo físico disponível.
2. **Validação de Crédito:** O sistema impede vendas na modalidade "fiado" para clientes inadimplentes ou que ultrapassaram o limite estipulado pela gerência.
3. **Auditoria por Operador:** Toda transação ou alteração crítica é estritamente vinculada ao login do usuário ativo.
4. **Restrição Legal (Maioridade):** Travas de segurança e avisos para impedir a venda de produtos alcoólicos a menores de 18 anos.
5. **Acesso Restrito:** Funções críticas (alteração manual de preço, exclusão de dados e liberação de crédito especial) necessitam de credenciais de Gerente.

---

##Estrutura do Banco de Dados

O fluxo operacional e as entidades do sistema foram modelados com base no seguinte ecossistema de dados:
* **Cliente / Fiado:** Controle de limites e saldos devedores.
* **Usuário / Caixa:** Monitoramento de turnos e movimentação financeira diária.
* **Produto / Estoque / Item Venda:** Rastreabilidade total de saídas e reposições de mercadorias.

---

##Autores

. Denner RGM: 4733816
. Guilherme Schiavinato RGM: 47769068
. Gustavo Castro RGM: 47353716
. Juan Craveiro RGM: 45005273
. Victor Silva RGM: 47787945

