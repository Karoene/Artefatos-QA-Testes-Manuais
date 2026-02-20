## REQUISITO FUNCIONAL - Detalhes do Produto

## Cenário de Teste #03 - Analisar detalhamento de um Produto

##### CASO DE TESTE
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT03-CT01` |
| **Título / Resumo** | Validar tela de detalhes de um produdo. |
| **Pré-Condição** | Acesso à URL: [Timeless LumeStack](https://timeless-lumestack.netlify.app/) > Aba Coleção. |
| **Massa de Teste** | **Técnica: Teste de Usabilidade**<br> |
| **Passos (BDD)** | **DADO QUE** estou na tela de listagem de produtos. <br>**QUANDO** clico em um produto aleatório <br>**E** o site carrega a página de detalhes <br>**ENTÃO** visualizo todas as informações do produto, sendo: contendo imagem ampliada, descrição completa e especificações técnicas.  |
| **Prioridade** | Alta |
| **Resultado Esperado** | Todo produto deve conter na tela de detalhes: Imagem, Nome, Material, Tamanho, Preço, descrição e especificações.|
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |

---

##### CASO DE TESTE
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT03-CT02` |
| **Título / Resumo** | Validar propriedade aspect ratio da imagem do produto na tela de detalhes. |
| **Pré-Condição** | Tela de detalhes > Acessar menu dev-tools. Opção "inspecionar elemento" em cima da imagem. |
| **Massa de Teste** | **Técnica: Teste exploratório**<br> |
| **Passos (BDD)** | **DADO QUE** estou na página de detalhes do produto. <br>**QUANDO** acesso o menu dev-tools <br>**E** encontro a propriedade da imagem, através da escolha da opção "inspecionar elemento". <br>**ENTÃO** a propriedade deve estar configurada "aspect ratio". |
| **Prioridade** | Baixa |
| **Resultado Esperado** | A propriedade da proporção da imagem deve ser "aspect ratio", e não haver distorções na imagem do produto. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |

---

##### CASO DE TESTE
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT03-CT03` |
| **Título / Resumo** | Validar botão "Favorito" em produto que não está favoritado. |
| **Pré-Condição** | Página de detalhes de produto. |
| **Massa de Teste** | **Técnica: Teste mudança de estado**<br> |
| **Passos (BDD)** | **DADO QUE** estou na página de detalhes de um produto que não está com status de Favorito. <br>**QUANDO** visualizo o botão "Favorito" <br>**E** clico para favoritar este produto. <br>**ENTÃO** o estado de favorito do produto deve alterar para "favoritado".<br>**E** o botão "Favorito" muda de cor. |
| **Prioridade** | Baixa |
| **Resultado Esperado** | O estado do produto é alterado para favoritado e a cor do botão muda. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |

---
##### CASO DE TESTE
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT03-CT04` |
| **Título / Resumo** | Validar botão "Favorito" em produto que está favoritado. |
| **Pré-Condição** | Página de detalhes de produto. Produto já deve ter sido favoritado. |
| **Massa de Teste** | **Técnica: Teste mudança de estado**<br> |
| **Passos (BDD)** | **DADO QUE** estou na página de detalhes de um produto que está com status de Favorito. <br>**E** visualizo que a cor do botão "Favorito" está mudada. <br>**QUANDO** clico no botão "Favorito".<br>**ENTÃO** o estado do produto deve alterar de "Favorito" para "Removido de Favorito".  <br>**E** a cor do botão volta para a anterior. |
| **Prioridade** | Baixa |
| **Resultado Esperado** | O estado do produto é alterado para "removido de favorito" e a cor do botão altera. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |

---

##### CASO DE TESTE
| Campo | Descrição |
| :--- | :--- |
| **ID** | `CT03-CT05` |
| **Título / Resumo** | Validar Botão "Adicionar ao Carrinho" ao adicionar um e mais produtos iguais produto no carrinho. |
| **Pré-Condição** | Aba Detalhes do Produto. Carrinho Vazio. |
| **Massa de Teste** | **Técnica: Partição de Equivalência**<br> Adicione o item da página no carrinho conforme quantidades: <br>1. **0 item.** Quantidade total 0.<br>2. **1 item** Quantidade total 1.<br>3. **10 itens** Quantidade total 10. <br>  |
| **Passos (BDD)** |**DADO QUE** estou na página de um produto específico. <br> **QUANDO** clico no botão "Adicionar ao Carrinho" (conforme dados da massa de teste) <br> **E** visualizo ícone de carrinho no canto superior direito.<br>**ENTÃO** consigo ver o ícone do carrinho e um valor reference a soma total de itens.  |
| **Prioridade** | Alta |
| **Resultado Esperado** |  Consigo adicionar itens ao carrinho quando clico no botão e a quantidade está correta. |
| **Status da Execução** | <ul><li>[ ] Passou (Sucesso)</li><li>[ ] Falhou (Erro encontrado)</li><li>[ ] Bloqueado</li><li>[ ] Skipped</li></ul> |

---

