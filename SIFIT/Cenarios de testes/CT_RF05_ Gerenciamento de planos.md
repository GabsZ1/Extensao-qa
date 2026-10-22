## Cenário 05: Gerenciamento de planos.

### Caso de Teste 01: Filtro de planos por status.

| ID       | Descrição |
| :------- | :-------- |
| C05-CT01 | O sistema deve filtrar planos por status Ativo/Inativo. |

| **Pré-condições** |
| :---------------- |
| Existirem planos ativos e inativos. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Planos" |
| **E** selecionamos "Inativo" no filtro "Status" |
| **QUANDO** clicarmos em "Buscar" |
| **ENTÃO** a lista deve exibir somente planos com status "inativo" |

| **Critérios de aceitação** |
| :------------------------- |
| Somente planos do status selecionado devem ser exibidos. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 02: Consistência dos indicadores de planos.

| ID       | Descrição |
| :------- | :-------- |
| C05-CT02 | Receita estimada, mensalidade e quantidade de alunos devem ser coerentes. |

| **Pré-condições** |
| :---------------- |
| Existirem alunos matriculados em planos pagos (ex.: "QA Keltton Plano Limite" – R$ 99,90). |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Planos" |
| **QUANDO** observarmos "Receita Estimada", o ranking "Planos com mais alunos" e a lista de planos |
| **ENTÃO** a receita estimada deve somar as mensalidades dos alunos ativos |
| **E** o ranking e a lista devem mostrar o mesmo número de alunos e o mesmo valor de mensalidade |

| **Critérios de aceitação** |
| :------------------------- |
| Os valores e contagens devem ser iguais em todos os pontos da tela. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 03: Cadastro de plano com valor inválido.

| ID       | Descrição |
| :------- | :-------- |
| C05-CT03 | O sistema deve validar o campo "Valor Mensal". |

| **Pré-condições** |
| :---------------- |
| Estar no formulário "Novo Plano". |

| **Passos** |
| :--------- |
| **DADO** que estamos no formulário "Novo Plano" |
| **E** preenchemos o nome "Plano QA" |
| **E** preenchemos "-10" (negativo) e depois "999999,99" no campo "Valor Mensal" |
| **QUANDO** clicarmos em salvar |
| **ENTÃO** o sistema deve recusar valores negativos e alertar sobre valores fora do padrão |

| **Critérios de aceitação** |
| :------------------------- |
| Valores negativos não devem ser aceitos e valores extremos devem ser validados. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |
