## Cenário 07: Avaliações físicas.

### Caso de Teste 01: Filtro de avaliações por status.

| ID       | Descrição |
| :------- | :-------- |
| C07-CT01 | O sistema deve filtrar avaliações pendentes e realizadas. |

| **Pré-condições** |
| :---------------- |
| Existirem avaliações pendentes e realizadas. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Avaliações" |
| **E** selecionamos "Pendente" no filtro "Status" |
| **QUANDO** clicarmos em "Buscar" |
| **ENTÃO** devem ser exibidas somente avaliações com status "pendente" |

| **Critérios de aceitação** |
| :------------------------- |
| O filtro deve retornar apenas o status selecionado. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 02: Validação da data da avaliação.

| ID       | Descrição |
| :------- | :-------- |
| C07-CT02 | Avaliações não devem ter datas inválidas ou padrão (01/01/1970). |

| **Pré-condições** |
| :---------------- |
| Estar na tela "Cadastrar Avaliação". |

| **Passos** |
| :--------- |
| **DADO** que estamos cadastrando uma avaliação |
| **E** deixamos o campo de data vazio ou preenchemos uma data inválida |
| **QUANDO** tentarmos salvar |
| **ENTÃO** o sistema deve exigir uma data válida |

| **Critérios de aceitação** |
| :------------------------- |
| Nenhuma avaliação deve ser salva com data vazia/inválida (ex.: 01/01/1970 00:00). |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 03: Indicadores mensais de avaliações.

| ID       | Descrição |
| :------- | :-------- |
| C07-CT03 | Os cards devem refletir as avaliações do período. |

| **Pré-condições** |
| :---------------- |
| Existirem avaliações no mês atual. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Avaliações" |
| **QUANDO** observarmos "Avaliação no Mês", "Mês Passado" e "Média Mensal" |
| **ENTÃO** a "Média Mensal" deve ser coerente com as quantidades exibidas |

| **Critérios de aceitação** |
| :------------------------- |
| A média não pode ser 0 quando há avaliações no mês. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |
