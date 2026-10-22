# Relatório de Bugs

**Software:** SIFIT - Sistema para Academias

**QA responsável:** Gabs

**Data:** 20.10.26

> Bugs marcados com "(Confirmação)" nos passos foram encontrados nos dados existentes; reproduza o cadastro para confirmar e gravar a evidência.

---

### 🐞 **Bug 01: Valor "em aberto" exibe R$ 0,00 mesmo com mensalidade vencida**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-001 | Na Página Inicial, o card "em aberto" e o "Total em aberto" mostram R$ 0,00, porém o bloco "Mensalidades pendentes" lista Rafael Santos (vencido em 12/05/2026) e "Ações recomendadas" indica "Cobrar 1 alunos com pagamento em aberto". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Fazer login no sistema |
| 2. Na Página Inicial, observar o card "R$ ... em aberto" |
| 3. Rolar até o bloco "Mensalidades pendentes" |
| 4. Comparar o "Total em aberto" com a mensalidade vencida listada |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O total em aberto deve somar o valor das mensalidades vencidas listadas. | O total exibe R$ 0,00 mesmo com mensalidade vencida na lista. |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Página Inicial / Financeiro | C02-CT02: Consistência do valor em aberto |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 02: "Total a Pagar" e "Valor Restante" zerados com contas pendentes**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-002 | Em Contas a Pagar, existem 2 contas com status PENDENTE (uma de R$ 200,00), mas os cards "Total a Pagar" e "Valor Restante" exibem 0. O valor da conta aparece incompleto ("R$ 200,00 / R$"). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar o menu "Contas a Pagar" |
| 2. Observar os cards "Total a Pagar" e "Valor Restante" |
| 3. Comparar com as contas #24 e #25 com status PENDENTE |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Os cards devem somar as contas pendentes (ex.: R$ 200,00) e o valor deve ser exibido completo. | Os cards exibem 0 e o valor aparece como "R$ 200,00 / R$". |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Contas a Pagar | C08-CT02: Totais de contas a pagar pendentes |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 03: Receita estimada e quantidade de alunos inconsistentes na tela de Planos**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-003 | A "Receita Estimada" é R$ 0,00 com 3 alunos em planos pagos. O ranking "Planos com mais alunos" mostra "Mensalidade R$ 0,00" e "1 aluno" para o plano "QA Keltton Plano Limite", enquanto a lista exibe o mesmo plano com R$ 99,90 e "0 aluno(s)". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar o menu "Planos" |
| 2. Observar o card "Receita Estimada" |
| 3. Observar o ranking "Planos com mais alunos" |
| 4. Localizar o plano #61 "QA Keltton Plano Limite" na lista e comparar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Receita, mensalidade e número de alunos devem ser iguais em todos os pontos da tela. | Receita R$ 0,00; ranking mostra R$ 0,00 / 1 aluno e a lista mostra R$ 99,90 / 0 aluno(s). |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Planos | C05-CT02: Consistência dos indicadores de planos |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 04: Check-ins do dia contabilizados mas não listados**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-004 | A tela Check-in mostra "3 Check-ins hoje", porém a tabela exibe "Nenhum registro encontrado", "Presentes agora" é 0 e a tela Presenças (atalho Hoje) mostra "Total no período 0". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar o menu "Check-in" (Unidade Centro) |
| 2. Observar o card "Check-ins hoje" e a tabela |
| 3. Acessar "Presenças" e clicar em "Hoje" |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A tabela e a tela Presenças devem listar os check-ins contabilizados no card. | Card indica 3 check-ins, mas nenhuma lista mostra registros. |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Check-in / Presenças | C06-CT01 e C06-CT03 |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 05: Caixas fechados com data final no futuro**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-005 | Na lista de Caixas existem caixas com status FECHADO e data final posterior à data atual (#27: Final 19/11/2026; #26: Final 24/10/2026, consultados em 20/10/2026). Indica ausência de validação da data de fechamento. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar o menu "Caixas" |
| 2. Filtrar status "Fechado" |
| 3. Observar a data "Final" dos caixas #26 e #27 |
| 4. (Confirmação) Fechar um caixa informando data futura |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O sistema não deve permitir fechar caixa com data final futura. | Caixas aparecem fechados com data final no futuro. |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Caixas | C09-CT02: Fechamento de caixa com data futura |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 06: Avaliação registrada com data 01/01/1970 00:00**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-006 | Na lista de Avaliações, a avaliação #42 (Fulano 1) aparece com data 01/01/1970 00:00, valor padrão de data vazia, indicando que o sistema aceita salvar sem data válida. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar o menu "Avaliações" |
| 2. Localizar a avaliação #42 |
| 3. (Confirmação) Cadastrar avaliação sem data |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A data da avaliação deve ser obrigatória e válida. | Avaliação salva/exibida com 01/01/1970 00:00. |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Avaliações | C07-CT02: Validação da data da avaliação |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 07: Produto cadastrado sem nome**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-007 | Na tela Produtos, o registro #7 aparece apenas com o tipo "Venda" e status "Ativo", sem nome. O campo nome não está sendo exigido no cadastro. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar o menu "Produtos" |
| 2. Observar o registro #7 |
| 3. (Confirmação) Clicar em "Novo" e salvar sem nome |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O nome do produto deve ser obrigatório. | Produto #7 existe sem nome. |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Produtos (RF12) | Teste exploratório |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 08: Quantidade de clientes ausentes diferente entre telas**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-008 | A Página Inicial exibe "8 Clientes Ausentes", enquanto a tela Clientes exibe "Ausentes 0" no mesmo momento. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Na Página Inicial, anotar o valor de "Clientes Ausentes" |
| 2. Acessar "Clientes" e observar o card "Ausentes" |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O mesmo indicador deve ter o mesmo valor nas duas telas. | Página Inicial: 8 / Clientes: 0. |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Página Inicial / Clientes | C02-CT01: Exibição dos indicadores |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 09: Alunos em risco de evasão zerado com aluno em médio risco**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-009 | O card "0 alunos em risco de evasão" contradiz o bloco "Inteligência de Retenção", que mostra 1 aluno em médio risco por "Ausência prolongada". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Na Página Inicial, observar o card "alunos em risco de evasão" |
| 2. Observar o bloco "Inteligência de Retenção" |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O card deve considerar os alunos classificados em risco. | Card mostra 0 e o bloco mostra 1 aluno em médio risco. |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Página Inicial | C02-CT01: Exibição dos indicadores |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 10: Pico de movimento divergente entre Página Inicial e Check-in**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-010 | A Página Inicial informa "Pico de movimento 00h - 01h", enquanto a tela Check-in informa "Horário de maior movimento: 18h às 20h". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Na Página Inicial, observar "Pico de movimento" |
| 2. Acessar "Check-in" e observar "Pico de movimento" |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O horário de pico deve ser o mesmo nas duas telas. | 00h - 01h x 18h às 20h. |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Página Inicial / Check-in | C02-CT01 e C06-CT01 |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 11: Média mensal de avaliações igual a 0 com avaliações no mês**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-011 | Na tela Avaliações, o card "Avaliação no Mês" mostra 2, mas "Média Mensal" mostra 0. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar o menu "Avaliações" |
| 2. Observar os cards "Avaliação no Mês" e "Média Mensal" |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A média deve refletir as avaliações registradas. | Média mensal 0 com 2 avaliações no mês. |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Avaliações | C07-CT03: Indicadores mensais de avaliações |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 12: Formatação monetária inconsistente em Contas a Receber**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-012 | A conta #1589 exibe "R$ 50000 / R$ 50.000,00": o primeiro valor está sem separador de milhar e sem centavos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar "Contas a Receber" |
| 2. Observar o valor da conta #1589 |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Valores devem seguir o padrão R$ 50.000,00. | Valor exibido como "R$ 50000". |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Contas a Receber | C08-CT01: Filtro de contas a receber por período |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 13: Textos da interface sem acentuação e com erro de concordância**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-013 | Vários textos estão sem acento ou com concordância errada: "Relatorios", "Historico de avaliacoes fisicas", "Ultimos 7 dias", "Este mes", "Codigo" (Contas a Pagar), "10 por pagina" e "Cobrar 1 alunos". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar "Relatórios", "Contas a Receber", "Contas a Pagar" e "Caixas" |
| 2. Observar títulos, filtros e paginação |
| 3. Na Página Inicial, observar "Ações recomendadas para hoje" |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Textos com ortografia correta e padronizada. | Textos sem acentuação e "Cobrar 1 alunos". |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Diversos (UI) | Teste exploratório |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---

### 🐞 **Bug 14: Plano cadastrado com valor R$ 999.999,99 por dia**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-014 | Existe o plano #59 "sdASD" com valor R$ 999.999,99 / 1 dia, indicando ausência de validação de valor máximo/razoável no cadastro de planos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar "Planos" |
| 2. Localizar o plano #59 |
| 3. (Confirmação) Cadastrar plano com valor extremo |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O sistema deve alertar ou limitar valores fora do padrão. | Plano salvo com R$ 999.999,99 / dia. |

| **Ambiente** |
| ------------ |
| Ambiente web de testes (sifit.centrion.com.br) |
| Desktop com Windows |
| Google Chrome (preencher versão) |
| Usuário com perfil Administrador |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Planos | C05-CT03: Cadastro de plano com valor inválido |

| **Evidência(s)** |
| :---: |
| [Vídeo](link-do-jam) |

---
