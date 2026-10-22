## Cenário 04: Gerenciamento de matrículas.

### Caso de Teste 01: Listagem das matrículas e indicadores.

| ID       | Descrição |
| :------- | :-------- |
| C04-CT01 | A tela deve exibir as matrículas com plano e status. |

| **Pré-condições** |
| :---------------- |
| Usuário autenticado. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Matrículas" |
| **QUANDO** a tela for carregada |
| **ENTÃO** devem ser exibidos os cards "Matrículas Ativas", "Recorrentes", "Não Renovadas", "Cadastradas este Mês" |
| **E** a lista com código, aluno, plano e status (ATIVO, INATIVO, CANCELADO) |

| **Critérios de aceitação** |
| :------------------------- |
| Os indicadores devem ser coerentes com a lista exibida. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 02: Busca de matrícula por código.

| ID       | Descrição |
| :------- | :-------- |
| C04-CT02 | O sistema deve localizar uma matrícula pelo código. |

| **Pré-condições** |
| :---------------- |
| Existir a matrícula #236. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Matrículas" |
| **E** preenchemos "236" no campo "Código" |
| **QUANDO** clicarmos em "Buscar" |
| **ENTÃO** deve ser exibida a matrícula #236 – Rafael Santos – Teste Diaria QA Verify |

| **Critérios de aceitação** |
| :------------------------- |
| Apenas a matrícula pesquisada deve ser exibida. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 03: Cadastro de matrícula sem cliente ou plano.

| ID       | Descrição |
| :------- | :-------- |
| C04-CT03 | Não deve ser possível cadastrar matrícula sem cliente e plano. |

| **Pré-condições** |
| :---------------- |
| Estar na tela "Cadastrar Matrícula". |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela de cadastro de matrícula |
| **E** não selecionamos cliente nem plano |
| **QUANDO** tentarmos salvar |
| **ENTÃO** o sistema deve exibir mensagens de validação e não salvar |

| **Critérios de aceitação** |
| :------------------------- |
| Nenhuma matrícula deve ser criada sem cliente e plano. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |
