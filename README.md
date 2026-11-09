# Projeto de Análise de Nomes com Streamlit e IBGE API

Este projeto consiste em uma aplicação web interativa desenvolvida com Streamlit, que permite aos usuários consultar a frequência de um determinado nome ao longo das décadas, utilizando dados fornecidos pela API do IBGE (Instituto Brasileiro de Geografia e Estatística).

## Funcionalidades:

- **Consulta de Nomes:** Os usuários podem inserir um nome em um campo de texto para buscar sua popularidade histórica.
- **Visualização de Dados:** A aplicação exibe a frequência do nome por década em formato de tabela e um gráfico de linha que mostra a evolução da popularidade do nome ao longo do tempo.
- **Integração com a API do IBGE:** Os dados são obtidos diretamente da API pública do IBGE, garantindo informações atualizadas e oficiais.

## Estrutura do Código (`web_app_ibge.py`):

- `pegar_nome_por_decadas(nome)`: Função responsável por construir a URL da API do IBGE, fazer a requisição e processar a resposta, retornando um dicionário com a frequência do nome por década.
- `get_url(url, params=None)`: Função auxiliar para realizar requisições HTTP GET e tratar possíveis erros.
- `main()`: Função principal que configura a interface do Streamlit, gerencia a entrada do usuário, chama as funções de busca de dados e exibe os resultados de forma tabular e gráfica.

## Como Rodar o Projeto:

Para executar este projeto, você precisará ter Python instalado, juntamente com as bibliotecas `streamlit`, `requests` e `pandas`.

1. Clone o repositório (se aplicável).
2. Instale as dependências:
   ```bash
   pip install streamlit requests pandas
   ```
3. Execute a aplicação Streamlit:
   ```bash
   streamlit run web_app_ibge.py
   ```

Após a execução, a aplicação será aberta em seu navegador padrão.

## Instalação com uv

```bash
git clone https://github.com/lucasmanoeldev/Web-app-IBGE.git
cd Web-app-IBGE
uv sync
uv run streamlit run web_app_ibge.py
```

Requer Python 3.13+ conforme `pyproject.toml`. O arquivo `web_app_ibge.py` contém a interface e a consulta HTTP. `uv.lock` registra as dependências resolvidas. O projeto consulta uma API externa e precisa de conexão com a internet.
