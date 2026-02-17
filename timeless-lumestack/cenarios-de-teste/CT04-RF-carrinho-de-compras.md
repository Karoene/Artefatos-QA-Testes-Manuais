CT remover itens iguais do carrinho e itens diferentes

#### Caso de Teste
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT01-CT03` |
| **Título / Resumo** | Validar Badge de Carrinho no canto superior direito e com exibição de soma total de itens, após remover itens.  |
| **Pré-Condição** | Acesso https://timeless-lumestack.netlify.app/ > Aba Carrinho. O carrinho deve estar com produtos adicionados. |
| **Massa de Teste** | **Técnica: Partição de Equivalência**<br> Remova os itens do carrinho: <br>1. **0 item.** Quantidade total 0.<br>2. **1 item** Quantidade total 1.<br>3. **10 itens** Quantidade total 10. <br> |
| **Passos (BDD)** | **DADO QUE** estou na página de Carrinho.  <br> **QUANDO** removo a (massa de teste) do carrinho <br> **E** visualizo ícone de carrinho no canto superior direito.<br>**ENTÃO** consigo ver o ícone do carrinho e um valor reference a diminuição total de itens.  |
| **Prioridade** | Média |
| **Resultado Esperado** | O ícone de carrinho está presente e mostrando a quantidade correta de itens nele. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |


---