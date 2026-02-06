# Timeless LumeStack - Documentação Técnica do Projeto

## 1. Visão Geral

O **Timeless LumeStack** é uma aplicação web de e-commerce single-page (SPA) focada na venda de relógios de luxo. O sistema permite a navegação por catálogo, gestão de carrinho, checkout simulado, criação de contas de usuário e um painel administrativo para gestão de produtos e visualização de clientes.

**Objetivo deste documento:** Servir como fonte da verdade para o time de Quality Assurance (QA) elaborar planos de teste, casos de teste e relatórios de bugs.

## 2. Especificações Técnicas e Nuances

* **Stack:** React (Vite), TypeScript, Tailwind CSS.
* **Persistência de Dados:** O sistema utiliza **armazenamento em memória (RAM)**.
    * *Nuance Importante:* Ao recarregar a página (F5), todos os dados criados (novos usuários, itens no carrinho, pedidos realizados, edições de produtos) são **perdidos** e o estado volta ao inicial definido em `constants.ts`.
* **Backend:** Não há backend real. Todas as operações (Login, CRUD) são simuladas no frontend.

## 3. Perfis de Acesso e Credenciais de Teste

Para execução dos testes, utilize as seguintes credenciais fixas (Mock):

| Perfil | Email | Senha | Permissões |
| :--- | :--- | :--- | :--- |
| **Admin** | `admin@timelesslumestack.com` | `admin123` | Acesso total, Painel Administrativo (Produtos e Clientes). |
| **Cliente** | `joao@exemplo.com` | `user123` | Comprar, Ver Histórico de Pedidos, Editar Perfil. |
| **Guest** | N/A | N/A | Navegar, Buscar, Adicionar ao Carrinho. |

## 4. Requisitos Funcionais (Comportamento Esperado)

### 4.1. Navegação e UI Geral

* **Navbar:** Deve exibir o logo, links de navegação, ícone de favoritos, ícone de carrinho com contador (badge) e área do usuário.
    * *Badge do Carrinho:* Deve aparecer no canto superior direito do ícone e exibir a soma total de itens.
    * *Responsividade:* Em mobile, o menu deve ser colapsável (hambúrguer).
* **Performance:** A transição entre telas deve ser instantânea (< 200ms), sem bloqueios de interface.

### 4.2. Catálogo e Busca

* **Listagem:** Produtos devem ser exibidos em cards com Imagem, Nome, Material, Tamanho e Preço.
* **Busca:** O campo de busca deve filtrar produtos por **Nome** ou **Material**.
    * *Regra:* A busca deve ser *case-insensitive* (ignorar maiúsculas/minúsculas).

### 4.3. Detalhes do Produto

* **Visualização:** Ao clicar em um produto, deve abrir a tela de detalhes contendo imagem ampliada, descrição completa e especificações técnicas.
* **Legibilidade:** Todos os textos (descrição, preço, especificações) devem ter contraste adequado com o fundo para leitura.
* **Imagem:** A imagem deve manter a proporção correta (aspect ratio) sem distorções.
* **Ações:**
    * Botão "Adicionar ao Carrinho": Deve incrementar o contador na Navbar.
    * Botão "Favorito": Deve alternar o estado de favorito do item.

### 4.4. Carrinho de Compras

* **Acesso:** O clique no ícone do carrinho deve abrir a visualização do carrinho imediatamente.
* **Listagem:** Deve mostrar foto, nome, quantidade e subtotal de cada item.
* **Cálculos Financeiros:**
    * *Subtotal do Item:* `Preço Unitário * Quantidade`.
    * *Total do Carrinho:* Soma de todos os subtotais.
* **Edição:**
    * Botões `+` e `-`: Devem ajustar a quantidade. Mínimo de 1.
    * Botão "Remover" (Lixeira): Deve remover **apenas** o item selecionado da lista.

### 4.5. Checkout e Pagamento

* **Fluxo:** O botão "Finalizar Compra" no carrinho deve levar à tela de Checkout (se logado) ou Login.
* **Formulário:** Deve solicitar Nome, Endereço e Dados do Cartão.
* **Finalização:** Ao clicar em "Confirmar Pedido":
    1.  Gerar um número de pedido único.
    2.  Salvar o pedido no histórico do usuário.
    3.  Limpar o carrinho.
    4.  Redirecionar para a tela de "Confirmação de Pedido" exibindo o resumo.

### 4.6. Autenticação (Login e Registro)

* **Login:**
    * Admin e Cliente devem ser redirecionados para a Home após sucesso.
    * Senha incorreta deve exibir mensagem de erro.
    * Sistema deve ser estável e permitir login sempre que as credenciais estiverem corretas.
* **Registro:**
    * Deve validar se "Senha" e "Confirmar Senha" são iguais.
    * Ao registrar, o usuário já deve entrar logado.

### 4.7. Painel Administrativo (Admin Only)

* **Produtos:**
    * Listagem tabular de produtos.
    * Adicionar: Deve permitir criar novo produto que aparece imediatamente no catálogo.
    * Editar: Deve permitir alterar preço, estoque e descrições.
    * Excluir: Deve remover o produto do catálogo.
* **Clientes:**
    * Listagem de todos os usuários cadastrados.
    * Visualização de detalhes expandidos (Endereço, Telefone).
    * Visualização do histórico de pedidos de cada cliente.
    * **Segurança:** A senha do usuário, se exibida, é um dado sensível (verificar requisitos de segurança, embora no mock atual ela seja visível).

## 5. Requisitos Não-Funcionais

1.  **Usabilidade:** O sistema deve fornecer feedback visual para ações (ex: "Adicionado ao carrinho").
2.  **Desempenho:** Carregamento de imagens e transições de tela devem ser fluidos.
3.  **Compatibilidade:** Deve funcionar nas versões recentes do Chrome, Firefox e Safari.


Créditos:
LumeStack - Evento Profissão QA - realizado em janeiro 19/01/2026