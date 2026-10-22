## Cenário 06: Check-in e presenças.

### Caso de Teste 01: Visualização do painel de check-in.

| ID       | Descrição |
| :------- | :-------- |
| C06-CT01 | O painel deve exibir indicadores e a lista de check-ins do dia. |

| **Pré-condições** |
| :---------------- |
| Usuário autenticado. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Check-in" |
| **E** a unidade "Unidade Centro" está selecionada |
| **QUANDO** a tela for carregada |
| **ENTÃO** devem ser exibidos "Check-ins hoje", "Presentes agora", "Meta do dia", "Média diária" e "Taxa de frequência" |
| **E** a tabela deve listar os check-ins contabilizados em "Check-ins hoje" |

| **Critérios de aceitação** |
| :------------------------- |
| A quantidade do card deve bater com os registros da tabela. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 02: Check-in rápido com código inexistente.

| ID       | Descrição |
| :------- | :-------- |
| C06-CT02 | O sistema deve recusar check-in com código de cliente inexistente. |

| **Pré-condições** |
| :---------------- |
| Usuário autenticado. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Check-in" |
| **E** preenchemos "999999" no campo de "Entrada rápida" |
| **QUANDO** clicarmos em "Realizar check-in" |
| **ENTÃO** deve ser exibida mensagem informando que o cliente não foi encontrado |

| **Critérios de aceitação** |
| :------------------------- |
| Nenhum check-in deve ser registrado para código inexistente. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 03: Consulta de presenças por período.

| ID       | Descrição |
| :------- | :-------- |
| C06-CT03 | A tela Presenças deve listar as entradas do período escolhido. |

| **Pré-condições** |
| :---------------- |
| Usuário autenticado. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Presenças" |
| **QUANDO** clicarmos no atalho "Hoje" |
| **ENTÃO** o "Total no período" deve ser igual ao número de check-ins de hoje exibido na tela Check-in |

| **Critérios de aceitação** |
| :------------------------- |
| Os números de Presenças e Check-in devem ser coerentes. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |
