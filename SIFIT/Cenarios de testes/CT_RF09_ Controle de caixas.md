## Cenário 09: Controle de caixas.

### Caso de Teste 01: Filtro de caixas por status.

| ID       | Descrição |
| :------- | :-------- |
| C09-CT01 | O sistema deve filtrar caixas abertos e fechados. |

| **Pré-condições** |
| :---------------- |
| Existirem caixas abertos e fechados. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Caixas" |
| **E** selecionamos "Aberto" no filtro "Status" |
| **QUANDO** clicarmos em "Buscar" |
| **ENTÃO** devem ser exibidos apenas os caixas com status "ABERTO" (quantidade igual ao card "Caixas Abertos") |

| **Critérios de aceitação** |
| :------------------------- |
| A lista deve corresponder ao status e ao card. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 02: Fechamento de caixa com data futura.

| ID       | Descrição |
| :------- | :-------- |
| C09-CT02 | A data final de um caixa fechado não pode ser posterior à data atual. |

| **Pré-condições** |
| :---------------- |
| Existir caixa aberto. |

| **Passos** |
| :--------- |
| **DADO** que estamos fechando um caixa aberto |
| **E** informamos uma data final posterior a hoje |
| **QUANDO** confirmarmos o fechamento |
| **ENTÃO** o sistema deve impedir o fechamento com data futura |

| **Critérios de aceitação** |
| :------------------------- |
| Nenhum caixa deve ficar FECHADO com data final no futuro. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 03: Paginação da lista de caixas.

| ID       | Descrição |
| :------- | :-------- |
| C09-CT03 | A paginação deve navegar entre os registros. |

| **Pré-condições** |
| :---------------- |
| Existirem mais de 10 caixas. |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Caixas" com "10 por pagina" |
| **QUANDO** clicarmos na página "2" |
| **ENTÃO** devem ser exibidos os registros 11 a 20 e o texto "Mostrando 11 a 20 de 20 caixas" |

| **Critérios de aceitação** |
| :------------------------- |
| A paginação deve exibir os registros corretos. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |
