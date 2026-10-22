# ✅ **Relatório Final de Execução de Testes - SIFIT**

**Sistema testado:** SIFIT - Sistema para Academias (CentrionWeb)
**Responsável:** Gabs
**Data de execução:** 20/10/2026 (execução parcial — atualizar ao concluir)
**Ambiente:**

* Sistema operacional: Windows
* Navegador: Google Chrome (preencher versão)
* URL: [https://sifit.centrion.com.br](https://sifit.centrion.com.br)
* Perfil do usuário: Administrador

---

## 📊 **Resumo da Execução**

| Total de Casos de Teste | Executados | Passaram | Falharam | Pendentes | Bugs Registrados |
| ----------------------- | ---------- | -------- | -------- | --------- | ---------------- |
| 30                      | 11         | 3        | 8        | 19        | 14               |

> Os casos "Pendentes" envolvem envio de formulários (cadastros, login inválido, geração de PDF) e devem ser executados e gravados no Jam para completar o relatório.

---

## 🔍 **Cobertura por Módulo**

| Código RF | Módulo                       | Casos | Executados | Passaram | Falharam | Bug(s) Associado(s)        |
| --------- | ---------------------------- | ----- | ---------- | -------- | -------- | -------------------------- |
| RF01      | Login                        | 3     | 1          | 1        | 0        | -                          |
| RF02      | Página Inicial               | 3     | 3          | 1        | 2        | BUG-001, BUG-008, BUG-009, BUG-010, BUG-013 |
| RF03      | Clientes                     | 3     | 0          | 0        | 0        | -                          |
| RF04      | Matrículas                   | 3     | 1          | 1        | 0        | -                          |
| RF05      | Planos                       | 3     | 1          | 0        | 1        | BUG-003, BUG-014           |
| RF06      | Check-in e Presenças         | 3     | 2          | 0        | 2        | BUG-004, BUG-010           |
| RF07      | Avaliações físicas           | 3     | 1          | 0        | 1        | BUG-006, BUG-011           |
| RF08      | Financeiro (Receber / Pagar) | 3     | 2          | 0        | 2        | BUG-002, BUG-012, BUG-013  |
| RF09      | Caixas                       | 3     | 0          | 0        | 0        | BUG-005                    |
| RF10      | Relatórios                   | 3     | 0          | 0        | 0        | BUG-013                    |
| RF12      | Produtos (exploratório)      | -     | -          | -        | -        | BUG-007                    |

---

## 🧾 **Resultado por Caso de Teste**

| Caso     | Título                                              | Resultado |
| -------- | --------------------------------------------------- | --------- |
| C01-CT01 | Login com credenciais válidas                       | ✅ Passou |
| C01-CT02 | Login com senha incorreta                           | ⏳ Pendente |
| C01-CT03 | Login com campos em branco                          | ⏳ Pendente |
| C02-CT01 | Exibição dos indicadores da Página Inicial          | ❌ Falhou (BUG-008, BUG-009, BUG-010) |
| C02-CT02 | Consistência do valor em aberto                     | ❌ Falhou (BUG-001) |
| C02-CT03 | Navegação pelo menu lateral                         | ✅ Passou |
| C03-CT01 | Busca de clientes por nome                          | ⏳ Pendente |
| C03-CT02 | Cadastro de cliente com obrigatórios vazios         | ⏳ Pendente |
| C03-CT03 | Validação de CPF e data inválidos                   | ⏳ Pendente (sem aviso imediato ao digitar; confirmar ao salvar) |
| C04-CT01 | Listagem das matrículas e indicadores               | ✅ Passou |
| C04-CT02 | Busca de matrícula por código                       | ⏳ Pendente |
| C04-CT03 | Cadastro de matrícula sem cliente/plano             | ⏳ Pendente |
| C05-CT01 | Filtro de planos por status                         | ⏳ Pendente |
| C05-CT02 | Consistência dos indicadores de planos              | ❌ Falhou (BUG-003) |
| C05-CT03 | Cadastro de plano com valor inválido                | ⏳ Pendente (indício: BUG-014) |
| C06-CT01 | Visualização do painel de check-in                  | ❌ Falhou (BUG-004) |
| C06-CT02 | Check-in rápido com código inexistente              | ⏳ Pendente |
| C06-CT03 | Consulta de presenças por período                   | ❌ Falhou (BUG-004) |
| C07-CT01 | Filtro de avaliações por status                     | ⏳ Pendente |
| C07-CT02 | Validação da data da avaliação                      | ⏳ Pendente (indício: BUG-006) |
| C07-CT03 | Indicadores mensais de avaliações                   | ❌ Falhou (BUG-011) |
| C08-CT01 | Filtro de contas a receber por período              | ❌ Falhou (BUG-012) |
| C08-CT02 | Totais de contas a pagar pendentes                  | ❌ Falhou (BUG-002) |
| C08-CT03 | Cadastro de conta sem valor                         | ⏳ Pendente |
| C09-CT01 | Filtro de caixas por status                         | ⏳ Pendente |
| C09-CT02 | Fechamento de caixa com data futura                 | ⏳ Pendente (indício: BUG-005) |
| C09-CT03 | Paginação da lista de caixas                        | ⏳ Pendente |
| C10-CT01 | Relatório de clientes em PDF                        | ⏳ Pendente |
| C10-CT02 | Relatório com período invertido                     | ⏳ Pendente |
| C10-CT03 | Relatório de caixas sem registros                   | ⏳ Pendente |

---

## 🐞 **Resumo dos Bugs Reportados**

| ID      | Título                                                                   | Severidade | Status |
| ------- | ------------------------------------------------------------------------ | ---------- | ------ |
| BUG-001 | Valor "em aberto" exibe R$ 0,00 mesmo com mensalidade vencida            | Alta       | Aberto |
| BUG-002 | "Total a Pagar" e "Valor Restante" zerados com contas pendentes          | Alta       | Aberto |
| BUG-003 | Receita estimada e quantidade de alunos inconsistentes na tela de Planos | Alta       | Aberto |
| BUG-004 | Check-ins do dia contabilizados mas não listados                         | Média      | Aberto |
| BUG-005 | Caixas fechados com data final no futuro                                 | Média      | Aberto |
| BUG-006 | Avaliação registrada com data 01/01/1970 00:00                           | Média      | Aberto |
| BUG-007 | Produto cadastrado sem nome                                              | Média      | Aberto |
| BUG-008 | Quantidade de clientes ausentes diferente entre telas                    | Média      | Aberto |
| BUG-009 | Alunos em risco de evasão zerado com aluno em médio risco                | Média      | Aberto |
| BUG-010 | Pico de movimento divergente entre Página Inicial e Check-in             | Baixa      | Aberto |
| BUG-011 | Média mensal de avaliações igual a 0 com avaliações no mês               | Baixa      | Aberto |
| BUG-012 | Formatação monetária inconsistente em Contas a Receber                   | Baixa      | Aberto |
| BUG-013 | Textos da interface sem acentuação e com erro de concordância            | Baixa      | Aberto |
| BUG-014 | Plano cadastrado com valor R$ 999.999,99 por dia                         | Baixa      | Aberto |

---

## 📈 **Gráfico de Resultado (Texto Alternativo)**

**Casos por status:**

* ✅ Passaram: 3
* ❌ Falharam: 8
* ⏳ Pendentes: 19

**Severidade dos bugs:**

* 🟥 Alta: 3
* 🟨 Média: 6
* 🟩 Baixa: 5

---

## 📁 **Evidências e Documentos**

* ✔️ [Análise de Requisitos](1-Analise%20de%20requisitos.md)
* ✔️ [Plano de Testes](2-plano%20de%20testes.md)
* ✔️ [Cenários e Casos de Teste](Cenarios%20de%20testes)
* 🐛 [Relatório de Bugs](3-Relatorio-de-Bugs.md)
* 📹 Evidências em vídeo hospedadas no Jam.dev

---

## ✅ **Conclusão**

A execução dos testes no SIFIT mostrou que a navegação e as telas de listagem funcionam de forma estável, mas foram encontradas **falhas de consistência nos indicadores**, principalmente nos módulos **financeiros** (Página Inicial, Contas a Pagar e Planos), onde valores e totais aparecem zerados ou diferentes entre telas. Esse tipo de falha afeta diretamente a tomada de decisão do gestor da academia (cobrança, receita e despesas).

Também há indícios de **falta de validação nos cadastros** (datas inválidas, nomes vazios, valores extremos e fechamento de caixa com data futura), que precisam ser confirmados com os testes pendentes.

🔍 **Identificação da Causa Raiz (Root Cause Analysis)**

A maior parte dos bugs encontrados tem um padrão em comum: **o mesmo indicador é calculado de formas diferentes em telas diferentes** (ex.: ausentes, pico de movimento, valor em aberto). A causa provável é a falta de uma regra de cálculo centralizada, com cada tela fazendo sua própria consulta ou filtrando dados por critérios diferentes (período, unidade, status). Já os registros com data 01/01/1970, produto sem nome e caixa com data futura apontam para **validações ausentes no front-end e no back-end**.

Usar os **5 Porquês** em cada bug e consultar o banco (MySQL Workbench, somente leitura) ajuda a confirmar se o problema está no dado gravado ou no cálculo da tela, e assim evitar que se repita.
