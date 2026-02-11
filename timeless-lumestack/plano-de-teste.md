## PLANO DE TESTES


**1) Informações gerais**

- ## Visão geral

    Este documento descreve o planejamento estratégico dos testes a serem realizados no produto Timeless-LumeStack, que é uma aplicação web de e-commerce single-page (SPA). Com objetivo de mapear as estratégias de testes a serem utilizadas, bem como detalhamento de risco, e cronograma do projeto de testes.

- ## Identificador único

    #PT-PROJETO-V1.0

- ## Responsáveis

    Karoene Mendonça

- ## Escopo geral

    - Serão realizados testes manuais com base nos requisitos funcionais da documentação da aplicação web fornecida    
    -  Não serão realizados testes nos requisitos não-funcionais, devido à falta da documentação destes.

    **Detalhes do Produto**:
    - Ambiente: Web SPA [Timeless LumeStack](https://timeless-lumestack.netlify.app/)
    - Versão do site: pública, 2026

   **Referências**:
    - Documentação de Requisitos do Sistema: documentacao-requisitos.md


**2) Contexto do teste**


- ## Escopo do teste

    - Funcionalidades a serem testadas (**In-Scope**)
        - Navegação e UI Geral
            - Navbar
        - Funcionalidade Busca e Catálogo
            - Listagem, Busca
        - Funcionalidade Detalhes do Produto
            - Visualização, Legibilidade, Imagem, Ações
        - Funcionalidade Carrinho de Compras
            - Acesso, Listagem, Cálculos Financeiros, Edição
        - Funcionalidade Checkout e Pagamento
            - Fluxo, Formulário, Finalização
        - Módulo Autenticação
            - Login e Registro
        - Módulo Painel Administrativo
            - Produtos, Clientes, Segurança

    - Funcionalidades que não serão testadas (**Out-of-Scope**)
        - Não serão testados os requisitos não-funcionais dispostos na documentação.
        - Requisito funcional 4.1, Performance. Se encaixa em requisito não-funcional.
        - Requisito funcional 4.1, Responsividade. Se encaixa em requisito não-funcional.
        - Não está no escopo de testes: Testes de integração com sistemas externos.
    
- ## Ferramentas
    - Jira: para gestão das tarefas e reporte de incidentes.
    - Chrome Versão 144.0.7559.133: para execução dos testes.
   
      
**3) Riscos e Mitigação**

- Riscos do Projeto
    - Indisponibilidade do ambiente de testes.

- Estratégia de Mitigação
    - Pausa no Projeto e entre em contato com o dono do produto (Lumestack).


**4) Estratégia de teste**

- Entregáveis de teste
    - Cenário e Caso de Teste
    - Log de Teste
    - Plano de Teste
    - Relatório de Incidentes
    - Relatório de Conclusão de Teste

- Técnicas de teste
    - Teste Exploratório: focadas em investigar o comportamento do site além dos roteiros predefinidos.
    - Teste Funcional com técnica Particionamento de equivalência: para cobrir caminhos felizes e infelizes no módulo de login. 

- Critérios de conclusão de teste
    - 100% dos testes mapeados no documento Caso de Teste sejam realizados.

- Métricas a serem coletadas
    - Quantidade de testes planejados e executados.
    - Quantidade de Incidentes mapeados e reportados.

- Requisitos de dados de teste
    - 1 usuário e senha cadastrados previamente.
    - Produtos fictícios no carrinho .
    - Dados de cartão de crédito para teste (fictícios).

- Novo teste e teste de regressão
    - Não serão realizados Teste de Confirmação e Teste de Regressão pois o plano cobre um ambiente simulado sem a presença de desenvolvedores ou acesso ao código fonte.

- Desvios da Estratégia de Teste
    - Requer análise dos requisitos funcionais para possível aplicação de outras técnicas de teste.

**5) Atividades e estimativas**

- Documentação: 3 dias.
- Elaboração de casos de teste: 2 dias.
- Execução dos testes: 1 dia.

**6) Equipe**

- Karoene Mendonça, Analista de Teste.

**7) Cronograma**

- 9 de Fevereiro: Entrega do Plano de Teste.
- 10 de Fevereiro: Escrita dos casos de teste.
- 12 de Fevereiro: Execução dos Testes.
- 13 de Fevereiro: Escrita do Relatório de Incidentes.
- 14 de Fevereiro: Entrega do Relatório Final de Teste.