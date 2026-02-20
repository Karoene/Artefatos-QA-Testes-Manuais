## REQUISITO FUNCIONAL - Carrinho de Compras

## Cenário de Teste #04 - Analisar e validar funcionamento do carrinho de compras

#### Caso de Teste
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT04-CT01` |
| **Título / Resumo** | Validar Badge de Carrinho no canto superior direito e com exibição de soma total de itens, após remover itens.  |
| **Pré-Condição** | Acesso https://timeless-lumestack.netlify.app/ > Aba Carrinho. O carrinho deve estar com produtos adicionados. |
| **Massa de Teste** | **Técnica: Partição de Equivalência**<br> Remova os itens do carrinho: <br>1. **0 item.** Quantidade total 0.<br>2. **1 item** Quantidade total 1.<br>3. **10 itens** Quantidade total 10. <br> |
| **Passos (BDD)** | **DADO QUE** estou na página de Carrinho.  <br> **QUANDO** removo a (massa de teste) do carrinho <br> **E** vou para outra tela e visualizo ícone de carrinho no canto superior direito.<br>**ENTÃO** consigo ver o ícone do carrinho e um valor reference a diminuição total de itens.  |
| **Prioridade** | Média |
| **Resultado Esperado** | O ícone de carrinho está presente e mostrando a quantidade correta de itens nele. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |


---
#### Caso de Teste
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT04-CT02` |
| **Título / Resumo** | Validar abertura e visualização do carrinho a partir de qualquer tela. |
| **Pré-Condição** | Acesso https://timeless-lumestack.netlify.app/ |
| **Massa de Teste** | **Técnica: Teste Exploratório com Hipótese**<br> Acesse o carrinho a partir da telas do site, teste todas que encontrar.   |
| **Passos (BDD)** | **DADO QUE** estou na tela (massa de teste) <br>**QUANDO** clico no ícone de carrinho (canto supeior direito) <br>**ENTÃO** o site redireciona para a tela Carrinho de compra. |
| **Prioridade** | Alta |
| **Resultado Esperado** | O site deve redirecionar o usuário para a tela de carrinho de compra imediatamente. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |

---
#### Caso de Teste
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT04-CT03` |
| **Título / Resumo** | Validar informações do carrinho de compras |
| **Pré-Condição** | Aba Carrinho. > Ao menos 1 Produto adicionado ao carrinho previamente.|
| **Massa de Teste** | **Técnica: Visualização**<br> |
| **Passos (BDD)** | **DADO QUE** estou no carrinho de compras <br>**QUANDO** visualizo o/os produtos no meu carrinho <br>**ENTÃO** consigo ver as informações foto, nome, quantidade e subtotal de cada item. |
| **Prioridade** | Alta |
| **Resultado Esperado** | O usuário consegue ver facilmente todas as informações sobre a foto, nome, quantidade e subtotal de cada item. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |

---

#### Caso de Teste
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT04-CT04` |
| **Título / Resumo** | Validar mensagem de carrinho vazio |
| **Pré-Condição** | Aba Carrinho. > Carrinho deve estar vazio.|
| **Massa de Teste** | **Técnica: Visualização**<br> |
| **Passos (BDD)** | **DADO QUE** estou no carrinho de compras <br>**QUANDO** visualizo a tela de detalhes <br>**ENTÃO** consigo ver a mensagem "Carrinho Vazio". |
| **Prioridade** | Media |
| **Resultado Esperado** | O usuário consegue ver facilmente a mensagem de carrinho vazio. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |


---
#### Caso de Teste
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT04-CT05` |
| **Título / Resumo** | Validar edição de quantidade de itens no carrinho e calculo de valor. |
| **Pré-Condição** | Aba Carrinho. |
| **Massa de Teste** | **Técnica:Teste Exploratório com Hipótese**<br> A hipótese é: consigo fazer edição de quantidade de quantidade de itens no carrinho e o calculo dos valores está correto. <br> CT1 - No carrinho há itens diferentes e eu removo todos eles, e a soma total está sempre correta a cada remoção. <br> CT2 - No carrinho há itens diferentes e eles possuem quantidades diferentes, consigo diminuir todas as unidade, e a soma total está correta para cada item e valor total. <br> CT3 - No carrinho há apenas 1 item e o valor unitário e total estão corretos. <br> **Obs: teste para livre exploração do cenário da hipótese.**|
| **Passos (BDD)** | **DADO QUE** estou na tela de carrinho de compras <br>**QUANDO** eu executo os teste (massa de teste)<br>**ENTÃO** todas as informaçòes sobre as quantidade e valores estão corretas. |
| **Prioridade** | Alta |
| **Resultado Esperado** | Todas as informações estão corretas, sendo: os valores a cada atualização de quantidade e o botão edição de quantidade + e - funcionam conforme esperado e botão de remoção de item tambem.  |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |

---
