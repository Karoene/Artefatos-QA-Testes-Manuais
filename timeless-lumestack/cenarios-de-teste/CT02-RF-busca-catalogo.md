## REQUISITO FUNCIONAL - Catálogo e Busca

## Cenário de Teste #01 - Realizar Busca e Explorar Catálogo


##### CASO DE TESTE
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT02-CT01` |
| **Título / Resumo** | Validar exibição dos cards de produtos. |
| **Pré-Condição** | Acesso à URL: [Timeless LumeStack](https://timeless-lumestack.netlify.app/) |
| **Passos (BDD)** | **DADO QUE** estou na página de listagem de produtos<br>**QUANDO** visualizo os produtos nessa tela<br>**ENTÃO** os produtos estão exibidos em cards individuais com Imagem, Nome, Material, Tamanho e Preço.  |
| **Estratégia Adicional** | **Teste Exploratório:** Executar sessão focada em UI/UX para verificar:<br>1. Se as imagens não estão quebradas.<br>2. Se o preço está formatado (R$).<br>3. Se textos longos quebram o layout do card.<br> |
| **Prioridade** | Alta  |
| **Resultado Esperado** | Produtos devem ser listados com imagem, nome, material, tamanho e preço visíveis e formatados. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |

---

##### CASO DE TESTE
----

| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT02-CT02` |
| **Título / Resumo** | Filtrar produtos por Nome ou Material (Regra Case-insensitive). |
| **Pré-Condição** | Acesso à URL: [Timeless LumeStack](https://timeless-lumestack.netlify.app/) > Aba Coleção. |
| **Massa de Teste** | **Técnica: Partição de Equivalência**<br>1. **Nome Exato:** "Relógio" (Válida)<br>2. **Material:** "Ouro" (Válida)<br>3. **Case-Insensitive:** "ouro" ou "reLÓGIO" (Válida - Regra de Negócio)<br>4. **Inexistente:** "#$#%#%" (Inválida) |
| **Passos (BDD)** | **DADO QUE** estou na aba Coleção<br>**QUANDO** insiro um valor da massa de teste no campo busca<br>**E** clico em buscar<br>**ENTÃO** a página retorna a lista de todos os produtos que contenham as informações passadas no campo.  |
| **Prioridade** | Alta  |
| **Resultado Esperado** | O site deve retornar os produtos correspondentes ou mensagem de vazio, ignorando maiúsculas/minúsculas. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |