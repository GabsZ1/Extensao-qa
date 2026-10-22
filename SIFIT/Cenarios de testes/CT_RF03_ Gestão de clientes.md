## Cenário 03: Gestão de clientes.

### Caso de Teste 01: Listagem e busca de clientes por nome.

| ID       | Descrição |
| :------- | :-------- |
| C03-CT01 | O sistema deve listar os clientes e permitir a busca por nome. |

| **Pré-condições** |
| :---------------- |
| Existirem clientes cadastrados (ex.: "Rafael Santos"). |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela "Clientes" |
| **E** preenchemos "Rafael Santos" no campo "Nome" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** a lista deve exibir apenas os clientes que correspondem ao nome pesquisado |

| **Critérios de aceitação** |
| :------------------------- |
| O filtro deve retornar somente os registros correspondentes. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 02: Cadastro de cliente com campos obrigatórios vazios.

| ID       | Descrição |
| :------- | :-------- |
| C03-CT02 | O cadastro deve ser bloqueado quando os campos obrigatórios (*) estiverem vazios. |

| **Pré-condições** |
| :---------------- |
| Estar na tela "Novo Cliente" (/adicionar-cliente). |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela de cadastro de cliente |
| **E** deixamos em branco "Nome", "Status", "Sexo" e "Data de Nascimento" |
| **QUANDO** clicarmos em "Cadastrar Cliente" |
| **ENTÃO** o sistema deve exibir mensagens de validação nos campos obrigatórios e não salvar o registro |

| **Critérios de aceitação** |
| :------------------------- |
| Nenhum cliente deve ser criado sem os campos obrigatórios. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 03: Validação de CPF e data de nascimento inválidos.

| ID       | Descrição |
| :------- | :-------- |
| C03-CT03 | O cadastro deve rejeitar CPF inválido e data inexistente/futura. |

| **Pré-condições** |
| :---------------- |
| Estar na tela "Novo Cliente". |

| **Passos** |
| :--------- |
| **DADO** que estamos na tela de cadastro de cliente |
| **E** preenchemos os campos obrigatórios |
| **E** preenchemos "111.111.111-11" no campo "CPF" |
| **E** preenchemos "31/02/2099" no campo "Data de Nascimento" |
| **QUANDO** clicarmos em "Cadastrar Cliente" |
| **ENTÃO** o sistema deve informar que o CPF e a data são inválidos |

| **Critérios de aceitação** |
| :------------------------- |
| CPF com dígitos repetidos e datas inexistentes ou futuras não devem ser aceitos. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |
