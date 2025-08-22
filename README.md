# TESTE-DESAFIO-FIFA21
# Relatório de Teste de API de Jogadores de Futebol

Este repositório contém o relatório de teste de uma API de jogadores de futebol, com foco na verificação de suas funcionalidades de busca e filtragem.

---

### Resumo Executivo

O teste de regressão da API foi concluído. A análise técnica revelou que a aplicação **não atende aos requisitos com sucesso**, com **8 dos 14** casos de teste falhando. Falhas críticas foram identificadas, especialmente nas funcionalidades de busca e filtragem de dados.

---

### Análise Técnica

A análise dos resultados aponta para falhas significativas que comprometem a estabilidade e usabilidade da API.

* **Pontos Fortes:** A API é responsiva e retorna dados rapidamente para requisições básicas.
* **Pontos Fracos:**
    * **Lógica de Filtragem Quebrada:** Múltiplos endpoints retornam dados incorretos ou listas vazias.
    * **Inconsistência de Endpoints:** A API carece de endpoints para filtros combinados, como "melhores jogadores K por posição".
    * **Erros de Formato de Resposta:** Alguns endpoints retornam um tipo de dado incorreto (objeto em vez de array).
    * **UI Não Resiliente:** A interface do usuário não lida corretamente com as respostas vazias da API, exibindo uma tela em branco em vez de uma mensagem de erro amigável.

---

### Bugs Encontrados

Para uma visualização mais rápida, os 8 bugs encontrados estão resumidos na tabela abaixo.

| ID do Teste | Funcionalidade | Status Final | Bug Encontrado? |
| :--- | :--- | :--- | :--- |
| **TESTE-003** | Listar jogadores por equipe | **Falhou** | Sim |
| **TESTE-004** | Listar jogadores por liga | **Falhou** | Sim |
| **TESTE-005** | Listar jogadores por nacionalidade | **Falhou** | Sim |
| **TESTE-007** | Detalhes do jogador (com ID) | **Falhou** | Sim |
| **TESTE-009** | Melhores jogadores K por posição | **Falhou** | Sim |
| **TESTE-010** | Melhores jogadores K por nacionalidade | **Falhou** | Sim |
| **TESTE-011** | Melhores jogadores K por liga | **Falhou** | Sim |
| **TESTE-013** | Melhor time por liga | **Falhou** | Sim |

---

### Como Executar os Testes

Para verificar os resultados, você pode importar a collection do Postman para rodar todos os testes automaticamente.

1.  **Baixe o arquivo de collection** (`api-collection.json`) deste repositório.
2.  No Postman, clique em **File > Import** e selecione o arquivo baixado.
3.  Na sua collection, selecione a pasta **Testes** e clique em **Run**.
4.  O Postman Runner irá executar todas as requisições e mostrar os resultados dos testes.

---

### Conclusão e Recomendação

A API **não atende com sucesso aos requisitos**. Recomenda-se que a equipe de desenvolvimento priorize a correção dos bugs listados para garantir a estabilidade e a integridade da aplicação.
