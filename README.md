# 🥥 O Problema com a Barraca de Coco

## 📘 Contexto
Téo, vendedor independente em Balneário Camboriú, recebeu uma proposta para alugar uma barraca de venda de cocos nos finais de semana.  
O aluguel custa **R$ 18,00 por fim de semana**.  
O fornecedor vende uma dúzia de cocos por **R$ 6,00** (ou seja, R$ 0,50 por unidade).  
Na praia, o preço de venda é **R$ 2,00 por coco**.  
Téo pode pegar um empréstimo com o **gerente Epaminondas** e contará com **Miro**, um garoto que receberá **15% de comissão** sobre as vendas quando cobrir o atendimento.

---

## 🧩 1. Itens Iniciais do Product Backlog (Requisitos Funcionais)

1. **Gerenciar Estoque de Cocos** – registrar compras, quantidade por lote, custo unitário e saldo em estoque.  
2. **Registrar Vendas por Unidade** – lançar vendas por data, quantidade vendida, preço unitário, total e vendedor (Téo ou Miro).  
3. **Calcular Custos e Lucros** – calcular custo de mercadoria vendida, receita, despesas (aluguel, comissão, empréstimo) e lucro líquido.  
4. **Gerenciar Funcionários / Comissões** – cadastrar atendentes e calcular automaticamente o valor de comissão.  
5. **Registrar Financiamentos e Despesas Fixas** – registrar empréstimos e despesas fixas (como o aluguel).

---

## 🔢 2. Ordem de Prioridade

| Prioridade | Funcionalidade |
|-------------|----------------|
| 1️⃣ | Gerenciar Estoque de Cocos |
| 2️⃣ | Registrar Vendas por Unidade |
| 3️⃣ | Calcular Custos e Lucros |
| 4️⃣ | Gerenciar Funcionários / Comissões |
| 5️⃣ | Registrar Financiamentos e Despesas Fixas |

**Justificativa:** começa-se pelos cadastros e controle de estoque e vendas, que são a base do sistema. Depois vêm os módulos financeiros e de comissões.

---

## 🧠 3. Histórias de Usuário

### 📦 Gerenciar Estoque
**Como** Téo (proprietário), **quero** registrar uma compra de cocos (lote, quantidade, custo) **para** saber o estoque disponível e o custo unitário.  
*Critério de aceitação:* registrar compra atualiza o estoque e calcula o custo médio.

### 💰 Registrar Vendas
**Como** atendente (Téo ou Miro), **quero** registrar uma venda por unidade **para** controlar a saída do estoque e a receita.  
*Critério:* venda reduz o estoque e registra o valor total e o vendedor.

### 📈 Calcular Lucros
**Como** Téo, **quero** visualizar o lucro líquido semanal **para** saber se a barraca é lucrativa.  
*Critério:* relatório mostra receita, custo de compra, despesas e lucro final.

### 🧾 Gerenciar Comissões
**Como** Téo, **quero** registrar o percentual de comissão do atendente **para** calcular automaticamente o valor devido ao Miro.  
*Critério:* comissão de 15% é calculada sobre o total de vendas do vendedor.

### 🏦 Registrar Financiamento / Despesa
**Como** Téo, **quero** registrar empréstimos e despesas fixas **para** acompanhar os custos no fluxo de caixa.  
*Critério:* o sistema guarda valor, parcelas e juros do empréstimo.

---

## 🚀 4. Sprint Backlog

**Objetivo do Sprint 1:**  
Entregar a base operacional: cadastro de estoque + registro de vendas + relatório financeiro simples.

**Itens do Sprint Backlog:**
- Criar estrutura e banco de dados do sistema.  
- Implementar módulo de **estoque** (compra e saldo).  
- Implementar módulo de **vendas** (registro e atualização de estoque).  
- Criar **relatório básico de lucro**.  
- Testes e validação com o cliente (Téo).

**Critério de aceitação do Sprint:**  
- Compras e vendas funcionando.  
- Estoque atualizado automaticamente.  
- Relatório mostra receita e lucro bruto.

---

## 🎭 5. Modelo de Casos de Uso

### 👥 Atores
- **Téo:** proprietário e administrador do sistema.  
- **Miro:** atendente/vendedor.  
- **Fornecedor:** fornece cocos.  
- **Banco:** fornece empréstimos.  
- **Sistema:** plataforma de controle da barraca.

### 🧾 Casos de Uso Principais
1. Registrar Compra de Cocos  
2. Registrar Venda  
3. Gerenciar Estoque  
4. Calcular Comissões  
5. Gerar Relatório Financeiro  
6. Registrar Empréstimo / Despesa  

---

### 🧩 Exemplo de Caso de Uso — *UC01 Registrar Compra de Cocos*
**Ator Primário:** Téo  
**Pré-condição:** fornecedor cadastrado.  
**Fluxo Principal:**
1. Téo acessa “Registrar Compra”.  
2. Informa data, quantidade, custo total.  
3. Sistema calcula custo unitário e atualiza estoque.  
4. Mostra saldo atualizado.  

**Fluxo Alternativo:** se a quantidade for inválida, o sistema exibe erro.  
**Pós-condição:** estoque atualizado e compra registrada.

---

### 🧾 Exemplo de Caso de Uso — *UC02 Registrar Venda*
**Ator Primário:** Miro ou Téo  
**Pré-condição:** deve existir estoque suficiente.  
**Fluxo Principal:**
1. Atendente abre tela de “Registrar Venda”.  
2. Informa quantidade e vendedor.  
3. Sistema verifica estoque e registra a venda.  
4. Calcula comissão se o vendedor for Miro (15%).  
5. Mostra total da venda e saldo atualizado.

---

## ⏳ 6. Duração do Primeiro Sprint

**Duração proposta:** `2 semanas (10 dias úteis)`

**Justificativa:**  
- Tempo suficiente para desenvolver e testar a base do sistema.  
- Curto o bastante para receber feedback rápido.  
- Adequado para times pequenos (1–3 pessoas) e entregas frequentes.

---

## ⚙️ 7. Aplicação dos Princípios Ágeis Durante o Sprint

- **Entregas frequentes:** MVP funcional ao final das 2 semanas (compra, venda e relatório).  
- **Colaboração com o cliente:** reuniões semanais com Téo para validação das telas e funcionalidades.  
- **Feedback contínuo:** após cada entrega parcial, ajustes feitos conforme sugestões do cliente.  
- **Adaptação a mudanças:** backlog pode ser atualizado a qualquer momento conforme novas ideias do cliente.  
- **Transparência:** uso de quadro Kanban ou Scrum (To Do / Doing / Done) e dailies curtas.  
- **Foco em valor:** primeiro entregar o essencial — registrar vendas e calcular lucros.

---

## 💡 Cálculo de Lucro (exemplo prático)

| Descrição | Valor Unitário (R$) |
|------------|---------------------|
| Preço de venda | 2,00 |
| Custo de compra | 0,50 |
| Comissão Miro (15%) | 0,30 |
| **Lucro líquido por coco** | **1,20** |

**Despesas fixas:**  
- Aluguel: R$ 18,00 por fim de semana  
- Empréstimo: conforme parcelas definidas  

**Lucro total por fim de semana:** depende da quantidade de cocos vendidos.  

---

## 🧾 Resumo Geral
Este projeto aplica princípios ágeis (Scrum) ao cenário da **barraca de coco** do Téo.  
O sistema proposto visa automatizar **estoque, vendas, comissões, despesas e lucros**, ajudando Téo a visualizar o desempenho da barraca e tomar decisões financeiras.

---
