## Cenário 02: Acesso e visualização da Página Inicial.

### Caso de Teste 01: Exibição dos indicadores da Página Inicial.

| ID       | Descrição |
| :------- | :-------- |
| C02-CT01 | Após o login, a Página Inicial deve exibir o resumo da academia. |

| **Pré-condições** |
| :---------------- |
| Usuário autenticado no sistema. |

| **Passos** |
| :--------- |
| **DADO** que realizamos o login com sucesso |
| **QUANDO** a Página Inicial for carregada |
| **ENTÃO** devem ser exibidos os cards: alunos em risco de evasão, valor em aberto, pico de movimento, avaliações pendentes, Clientes Ativos, Clientes Ausentes, Sem Matrículas, Personais, Matrículas no Período, Desistências e Renovações |

| **Critérios de aceitação** |
| :------------------------- |
| Todos os indicadores devem ser exibidos e carregados sem erro. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 02: Consistência do valor em aberto com as mensalidades pendentes.

| ID       | Descrição |
| :------- | :-------- |
| C02-CT02 | O total em aberto deve corresponder às mensalidades pendentes listadas. |

| **Pré-condições** |
| :---------------- |
| Existir ao menos uma mensalidade vencida (ex.: Rafael Santos, vencida em 12/05/2026). |

| **Passos** |
| :--------- |
| **DADO** que estamos na Página Inicial |
| **QUANDO** observarmos o card "em aberto" e o bloco "Mensalidades pendentes" |
| **ENTÃO** o valor "Total em aberto" deve ser igual à soma das mensalidades vencidas listadas |

| **Critérios de aceitação** |
| :------------------------- |
| O valor em aberto não pode ser R$ 0,00 quando houver mensalidade vencida listada. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |

---

### Caso de Teste 03: Navegação pelo menu lateral.

| ID       | Descrição |
| :------- | :-------- |
| C02-CT03 | Os itens do menu lateral devem abrir os módulos correspondentes. |

| **Pré-condições** |
| :---------------- |
| Usuário autenticado no sistema. |

| **Passos** |
| :--------- |
| **DADO** que estamos na Página Inicial |
| **QUANDO** clicarmos em "Clientes", "Matrículas", "Planos", "Check-in" e "Relatórios" no menu lateral |
| **ENTÃO** cada tela deve abrir com o título correspondente ao item clicado |

| **Critérios de aceitação** |
| :------------------------- |
| A navegação deve ser funcional e sem erros de carregamento. |

| **Resultado** | **Evidência** |
| :-----------: | :-----------: |
| _preencher_ | [Vídeo](link-do-jam) |
