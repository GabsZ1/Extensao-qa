## Cenário 10: Geração de relatórios.

### Caso de Teste 01: Geração de relatório de clientes em PDF.

| ID       | Descrição |
| :------- | :-------- |
| C10-CT01 | O sistema deve gerar o relatório de clientes. |

| **Pré-condições** |
| :---------------- |
| Usuário autenticado. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Relatórios" |
| **E** selecionamos "Clientes" em "Tipo de Relatório" |
| **E** definimos "Data Início" e "Data Fim" |
| **QUANDO** clicarmos em "Gerar Relatório" |
| **ENTÃO** um PDF com o cadastro e a situação dos alunos deve ser gerado |

| **Critérios de aceitação** |
| :------------------------- |
| O PDF deve abrir/baixar com os dados do período. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 02: Relatório com data final anterior à inicial.

| ID       | Descrição |
| :------- | :-------- |
| C10-CT02 | O sistema deve validar o período. |

| **Pré-condições** |
| :---------------- |
| Usuário autenticado. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Relatórios" |
| **E** preenchemos "Data Início" = 31/10/2026 e "Data Fim" = 01/10/2026 |
| **QUANDO** clicarmos em "Gerar Relatório" |
| **ENTÃO** o sistema deve informar que o período é inválido |

| **Critérios de aceitação** |
| :------------------------- |
| Nenhum relatório deve ser gerado com período invertido. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 03: Relatório de caixas sem registros no período.

| ID       | Descrição |
| :------- | :-------- |
| C10-CT03 | O sistema deve tratar períodos sem dados. |

| **Pré-condições** |
| :---------------- |
| Usuário autenticado. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Relatórios" |
| **E** selecionamos "Caixas" e um período sem movimento (ex.: 01/01/2010 a 31/01/2010) |
| **QUANDO** clicarmos em "Gerar Relatório" |
| **ENTÃO** deve ser exibida a mensagem de que não há registros no período |

| **Critérios de aceitação** |
| :------------------------- |
| O sistema não deve gerar erro nem PDF em branco sem aviso. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |
