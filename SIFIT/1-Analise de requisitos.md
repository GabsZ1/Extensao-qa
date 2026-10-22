## 📦 **Requisitos Funcionais Detalhados para Testes Manuais - SIFIT**

> Sistema de gestão para academias (SIFIT – CentrionWeb), acessado em [sifit.centrion.com.br](https://sifit.centrion.com.br).
> Requisitos levantados por exploração da interface web do sistema.

---

### 🔐 **RF01 - Autenticação de Usuário**

**Descrição**: O sistema deve permitir o acesso somente a usuários cadastrados.

* **Funcionalidades esperadas**:

  * Login com usuário e senha válidos.
  * Mensagem de erro em caso de login inválido ou campos vazios.
  * Opção "Manter conectado".
  * Link "Esqueci minha senha".
  * Opção "Sair" no menu do usuário.

---

### 🏠 **RF02 - Página Inicial (Resumo da Academia)**

**Descrição**: Após o login, o sistema deve exibir um painel com o resumo da academia no período selecionado.

* **Funcionalidades esperadas**:

  * Filtro de período (data inicial e final).
  * Cards: alunos em risco de evasão, valor em aberto, pico de movimento, avaliações pendentes.
  * Indicadores: Clientes Ativos, Clientes Ausentes, Sem Matrículas, Personais, Matrículas no Período, Desistências e Renovações.
  * Inteligência de Retenção (alto/médio/baixo risco e "Saúde da Academia").
  * Mensalidades pendentes com opção de cobrança via WhatsApp.
  * Agenda do dia, últimas entradas e aniversariantes.
  * Navegação pelo menu lateral para os demais módulos.

---

### 👤 **RF03 - Gestão de Clientes**

**Descrição**: O sistema deve permitir o gerenciamento dos alunos (clientes).

* **Funcionalidades esperadas**:

  * Listagem com código, nome, plano e status.
  * Filtros por código, nome, status (Ativo/Inativo), situação (Adimplente/Inadimplente), plano e personal.
  * Indicadores: Clientes Cadastrados, Clientes Ativos, Sem Matrículas, Ausentes.
  * Cadastro de cliente com campos obrigatórios (Nome, Status, Sexo, Data de Nascimento) e opcionais (CPF, RG, contatos, endereço, foto, acesso ao app, responsável).
  * Paginação (20, 50 ou 100 por página).

---

### 📝 **RF04 - Matrículas**

**Descrição**: Vincular clientes a planos e acompanhar a situação dos contratos.

* **Funcionalidades esperadas**:

  * Listagem com código, aluno, plano e status (Ativo, Inativo, Cancelado).
  * Busca por código e nome.
  * Indicadores: Matrículas Ativas, Recorrentes, Não Renovadas, Cadastradas este Mês.
  * Cadastro de nova matrícula.

---

### 💳 **RF05 - Planos**

**Descrição**: Cadastro e controle dos planos oferecidos pela academia.

* **Funcionalidades esperadas**:

  * Listagem com nome, valor, periodicidade, status e quantidade de alunos.
  * Filtro por código, nome e status.
  * Indicadores: total de planos, ativos, alunos em planos e receita estimada.
  * Ranking "Planos com mais alunos".
  * Cadastro de plano (grupo, cobrança, parcelas, valor mensal, valor de matrícula, personal, dependentes).

---

### ✅ **RF06 - Check-in e Presenças**

**Descrição**: Controle de entrada dos alunos na academia.

* **Funcionalidades esperadas**:

  * Seleção de unidade (Centro, Sul, Norte).
  * Indicadores em tempo real: check-ins hoje, presentes agora, meta do dia, média diária e taxa de frequência.
  * Check-in manual e entrada rápida por código/QR Code.
  * Tela de Presenças com filtro por período (Hoje, Esta semana, Este mês).

---

### 📏 **RF07 - Avaliações Físicas**

**Descrição**: Registro e acompanhamento das avaliações físicas dos alunos.

* **Funcionalidades esperadas**:

  * Listagem com aluno, data/hora, avaliador e status (Pendente/Realizado).
  * Filtros por código, nome e status.
  * Indicadores: avaliações no mês, mês passado e média mensal.
  * Cadastro de avaliação.

---

### 💰 **RF08 - Financeiro (Contas a Receber e Contas a Pagar)**

**Descrição**: Controle das entradas e saídas financeiras.

* **Funcionalidades esperadas**:

  * Filtros por código, nome, tipo de data (vencimento/recebimento/pagamento), período e status.
  * Atalhos de período (Hoje, Ontem, Últimos 7 dias, Este mês).
  * Totais: entradas, saídas, líquido, previsto, recebido, pendentes, atrasadas, total a pagar e valor restante.
  * Cadastro de nova conta.

---

### 🧾 **RF09 - Caixas**

**Descrição**: Abertura, fechamento e consulta dos caixas.

* **Funcionalidades esperadas**:

  * Filtro por período e status (Aberto/Fechado).
  * Indicadores: caixas abertos, fechados, locais de caixa e registros no período.
  * Abrir caixa e fechar caixa.
  * Paginação (10, 20 ou 50 por página).

---

### 📈 **RF10 - Relatórios**

**Descrição**: Geração de relatórios em PDF.

* **Funcionalidades esperadas**:

  * Tipos: Avaliações, Clientes, Colaboradores, Matrículas, Contas a Receber, Contas a Pagar e Caixas.
  * Filtro por data de início e fim.
  * Geração do relatório em PDF.

---

### 👥 **RF11 - Colaboradores**

**Descrição**: Cadastro da equipe (professores, personais, administrativos).

* **Funcionalidades esperadas**:

  * Listagem com código, nome e status.
  * Indicadores: colaboradores cadastrados, ativos e personais.
  * Cadastro de novo colaborador.

---

### 🛒 **RF12 - Produtos**

**Descrição**: Cadastro de produtos para venda ou troca por pontuação.

* **Funcionalidades esperadas**:

  * Filtros por código, nome, status e tipo (Venda/Pontuação).
  * Indicadores: total, ativos, inativos e para venda.
  * Cadastro de produto com nome obrigatório.
