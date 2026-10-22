## Cenário 08: Financeiro - Contas a Receber e a Pagar.

### Caso de Teste 01: Filtro de contas a receber por período.

| ID       | Descrição |
| :------- | :-------- |
| C08-CT01 | O sistema deve filtrar contas a receber pelos atalhos de período. |

| **Pré-condições** |
| :---------------- |
| Usuário autenticado. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Contas a Receber" |
| **QUANDO** clicarmos no atalho "Este mes" |
| **ENTÃO** os cards "Entradas", "Saídas", "Líquido", "Previsto para o Mês" e "Recebido no Mês" devem refletir a lista exibida |

| **Critérios de aceitação** |
| :------------------------- |
| Os totais devem corresponder às contas listadas e os valores devem ter formatação monetária padrão. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 02: Totais de contas a pagar pendentes.

| ID       | Descrição |
| :------- | :-------- |
| C08-CT02 | O total a pagar deve somar as contas pendentes. |

| **Pré-condições** |
| :---------------- |
| Existirem contas a pagar pendentes (ex.: #24 – Centrion Web – R$ 200,00). |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Contas a Pagar" |
| **QUANDO** a lista for carregada com contas "PENDENTE" |
| **ENTÃO** "Total a Pagar" e "Valor Restante" devem exibir a soma das contas pendentes |

| **Critérios de aceitação** |
| :------------------------- |
| Os totais não podem ser 0 quando há contas pendentes com valor. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 03: Cadastro de conta sem valor.

| ID       | Descrição |
| :------- | :-------- |
| C08-CT03 | Não deve ser possível salvar uma conta sem valor ou com valor zero. |

| **Pré-condições** |
| :---------------- |
| Estar no formulário "Nova Conta" de Contas a Pagar. |

| **Passos** |
| :--------- |
| **DADO** que estamos no formulário "Nova Conta" |
| **E** preenchemos o fornecedor e a descrição |
| **E** deixamos o valor em branco ou "0,00" |
| **QUANDO** tentarmos salvar |
| **ENTÃO** o sistema deve exibir mensagem de validação do valor |

| **Critérios de aceitação** |
| :------------------------- |
| Contas sem valor não devem ser cadastradas. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |
