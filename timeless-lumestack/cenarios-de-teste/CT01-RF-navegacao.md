## REQUISITO FUNCIONAL - Navegação e UI Geral

### CENÁRIO DE TESTE #01 - Validar Navbar

#### Caso de Teste
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT01-CT01` |
| **Título / Resumo** | Validar informações contidas no NavBar |
| **Pré-Condição** | Acesso https://timeless-lumestack.netlify.app/ |
| **Massa de Teste** | **Técnica: Teste de Usabilidade** <br> |
| **Passos (BDD)** | **DADO QUE** estou na página inicial. <br>**QUANDO** visualizo o Navbar.<br>**ENTÃO** consigo ver o logo, links de navegação, ícone de favoritos, ícone de carrinho com contador (badge) e área do usuário.  |
| **Prioridade** | Média |
| **Resultado Esperado** | Todos os componentes do Navbar devem estar presentes e visíveis |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |

---

#### Caso de Teste
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT01-CT02` |
| **Título / Resumo** | Validar Badge de Carrinho no canto superior direito e com exibição de soma total de itens, após adicionar itens.  |
| **Pré-Condição** | Acesso https://timeless-lumestack.netlify.app/ |
| **Massa de Teste** | **Técnica: Partição de Equivalência**<br> Selecione aleatoriamente e Adicione itens diferentes ao carrinho. <br>1. **0 item.** Quantidade total 0.<br>2. **1 item** Quantidade total 1.<br>3. **10 itens** Quantidade total 10. <br> |
| **Passos (BDD)** | **DADO QUE** estou na página de Produtos. <br> **QUANDO** Adicionei a (massa de teste) no carrinho <br> **E** visualizo ícone de carrinho no canto superior direito.<br>**ENTÃO** consigo ver o ícone do carrinho e um valor reference a soma total de itens.  |
| **Prioridade** | Média |
| **Resultado Esperado** | O ícone de carrinho está presente e mostrando a quantidade correta de itens nele. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |


---

