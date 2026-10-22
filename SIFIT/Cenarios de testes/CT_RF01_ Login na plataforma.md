## Cenário 01: Login na plataforma.

### Caso de Teste 01: Login com credenciais válidas.

| ID       | Descrição |
| :------- | :-------- |
| C01-CT01 | O login será realizado com usuário e senha válidos. |

| **Pré-condições** |
| :---------------- |
| As credenciais fornecidas pelo professor (usuário e senha) devem ser válidas. |

| **Passos** |
| :--------- |
| **DADO** que estamos na página de login do SIFIT (sifit.centrion.com.br/login) |
| **E** preenchemos o usuário fornecido no campo "Login" |
| **E** preenchemos a senha fornecida no campo "Senha" |
| **QUANDO** clicarmos no botão "Entrar" |
| **ENTÃO** seremos redirecionados para a Página Inicial (/dashboard) com a saudação "Boa tarde, <nome>!" |

| **Critérios de aceitação** |
| :------------------------- |
| O redirecionamento para a Página Inicial deve ocorrer corretamente. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 02: Tentativa de login com senha incorreta.

| ID       | Descrição |
| :------- | :-------- |
| C01-CT02 | O login falhará quando a senha for inválida. |

| **Pré-condições** |
| :---------------- |
| O usuário informado deve existir no sistema. |

| **Passos** |
| :--------- |
| **DADO** que estamos na página de login do SIFIT |
| **E** preenchemos o usuário válido no campo "Login" |
| **E** preenchemos "senhaerrada" no campo "Senha" |
| **QUANDO** clicarmos no botão "Entrar" |
| **ENTÃO** uma mensagem de erro de credenciais inválidas será exibida e o usuário permanecerá na tela de login |

| **Critérios de aceitação** |
| :------------------------- |
| Deve ser exibida uma mensagem clara de erro e o acesso não pode ser liberado. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 03: Tentativa de login com campos em branco.

| ID       | Descrição |
| :------- | :-------- |
| C01-CT03 | O login falhará quando os campos obrigatórios estiverem em branco. |

| **Pré-condições** |
| :---------------- |
| Nenhuma. |

| **Passos** |
| :--------- |
| **DADO** que estamos na página de login do SIFIT |
| **E** deixamos os campos "Login" e "Senha" em branco |
| **QUANDO** clicarmos no botão "Entrar" |
| **ENTÃO** o sistema deve indicar que os campos são obrigatórios |

| **Critérios de aceitação** |
| :------------------------- |
| Os campos obrigatórios devem exibir mensagens de validação. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |
