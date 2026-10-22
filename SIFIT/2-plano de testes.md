## 🧪 **Plano de Testes - SIFIT (Sistema para Academias)**

### 📌 1. **Identificação**

* **Nome do Projeto**: SIFIT - Sistema de Gestão para Academias (CentrionWeb)
* **Versão Avaliada**: Versão web disponibilizada para a disciplina
* **Ambiente de Testes**: [https://sifit.centrion.com.br](https://sifit.centrion.com.br)
* **Tipo de Teste**: Teste Funcional Manual
* **Data do Documento**: 20/10/2026
* **Responsável**: Gabs

---

### 🎯 2. **Objetivo**

Realizar a verificação manual dos principais requisitos funcionais do SIFIT, com foco na validação dos fluxos críticos de uma academia (acesso, clientes, matrículas, planos, check-in, avaliações e financeiro), nas mensagens de erro, na consistência dos indicadores exibidos e na integridade das funcionalidades da interface web.

---

### 🧩 3. **Escopo**

**Incluído:**

* Autenticação de usuário
* Página Inicial (resumo da academia)
* Clientes
* Matrículas
* Planos
* Check-in e Presenças
* Avaliações físicas
* Financeiro (Contas a Receber e Contas a Pagar)
* Caixas
* Relatórios

**Excluído:**

* Aplicativo mobile do aluno
* Integrações externas (Pagar.me, WhatsApp, leitores de catraca/QR Code)
* Módulos de Inteligência & Automação, SifitBox/Crossfit, Anamnese e Enquetes
* Testes de performance, carga e segurança
* Testes diretos no banco de dados (MySQL)

---

### 🔧 4. **Ferramentas Utilizadas**

* Navegador Google Chrome
* Ferramentas de inspeção do navegador (DevTools)
* Extensão Jam (gravação dos vídeos de evidência)
* MySQL Workbench (consulta de apoio, somente leitura)
* Markdown + GitHub (documentação)

---

### 🧪 5. **Técnicas de Teste**

* Particionamento de equivalência
* Análise de valor limite
* Caminho feliz (Happy Path)
* Testes negativos
* Testes exploratórios
* Verificação de consistência entre telas (mesmo indicador em módulos diferentes)

---

### 📄 6. **Critérios de Aceitação**

* Todos os casos de teste devem passar conforme o resultado esperado.
* Nenhuma falha crítica nas funcionalidades principais (login, clientes, matrículas e financeiro).
* Indicadores e totais devem ser coerentes entre as telas.
* Mensagens de erro e validações devem ser claras e consistentes.

---

### 🚦 7. **Critérios de Saída (Exit Criteria)**

* Todos os testes do escopo foram executados.
* Falhas foram registradas, analisadas e reexecutadas se necessário.
* Evidências em vídeo (Jam) anexadas aos casos de teste e bugs.

---

### ⏱️ 8. **Cronograma Estimado**

| Atividade                   | Data Início | Data Fim   |
| --------------------------- | ----------- | ---------- |
| Planejamento de Testes      | 20/10/2026  | 20/10/2026 |
| Criação de Casos de Teste   | 20/10/2026  | 20/10/2026 |
| Execução dos Testes Manuais | 20/10/2026  | xx/xx/2026 |
| Registro e Report de Bugs   | 20/10/2026  | xx/xx/2026 |
| Encerramento e Evidências   | xx/xx/2026  | xx/xx/2026 |

---

### 📋 9. **Módulos a Serem Testados**

| Código RF | Módulo                          | Prioridade |
| --------- | ------------------------------- | ---------- |
| RF01      | Login                           | Alta       |
| RF02      | Página Inicial                  | Média      |
| RF03      | Clientes                        | Alta       |
| RF04      | Matrículas                      | Alta       |
| RF05      | Planos                          | Alta       |
| RF06      | Check-in e Presenças            | Média      |
| RF07      | Avaliações físicas              | Média      |
| RF08      | Financeiro (Receber / Pagar)    | Alta       |
| RF09      | Caixas                          | Média      |
| RF10      | Relatórios                      | Baixa      |

---

### 🐞 10. **Gestão de Defeitos**

* Bugs serão documentados com:

  * Título
  * Descrição
  * Passos para reproduzir
  * Evidência (vídeo no Jam)
  * Severidade (Crítica, Alta, Média, Baixa)
* Ferramenta sugerida: Trello ou GitHub Issues (para simulação)

---

### 📌 11. **Riscos Identificados**

| Risco                                                        | Impacto | Mitigação                                             |
| ------------------------------------------------------------ | ------- | ----------------------------------------------------- |
| Ambiente compartilhado com outros alunos (dados mudam)       | Alto    | Anotar IDs e datas no momento do teste e gravar vídeo |
| Sistema fora do ar                                           | Alto    | Tentar novamente após intervalo                       |
| Massa de dados de teste poluída (registros "Teste", "AAAA")  | Médio   | Usar prefixo próprio nos dados criados (ex.: "QA Gabs") |
| Usuário único com perfil Administrador                       | Médio   | Documentar o limite (sem testes de permissão)         |

---

### 📁 12. **Entregáveis**

* Análise de Requisitos (.md)
* Plano de Testes (.md)
* Cenários e Casos de Teste (.md – pasta "Cenarios de testes")
* Relatório de Bugs com evidências (.md)
* Relatório Final de Execução (.md)
