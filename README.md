# Explorando evolução de código

Neste exercício, iremos explorar a evolução de código em sistemas reais.

Iremos utilizar a ferramenta [GitEvo](https://github.com/andrehora/gitevo).
Essa ferramenta analisa a evolução de código em repositórios Git nas linguagens Python, JavaScript, TypeScript e Java, e gera relatórios `HTML` como [este](https://andrehora.github.io/gitevo-examples/python/pandas.html).

Mais exemplos de relatórios podem ser podem ser encontrados em https://github.com/andrehora/gitevo-examples.

# Passo 1: Selecionar repositório a ser analisado

Selecione um repositório relevante na linguagem de sua preferência (Python, JavaScript, TypeScript ou Java).
Você pode encontrar projetos interessantes nos links abaixo:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

# Passo 2: Instalar e rodar a ferramenta GitEvo

> [!NOTE]
> Antes de instalar a ferramenta, é recomendado criar e ativar um [ambiente virtual Python](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#create-and-use-virtual-environments).

Instale a ferramenta [GitEvo](https://github.com/andrehora/gitevo) com o comando:

```
$ pip install gitevo
```

Execute a ferramenta no repositório selecionado utilizando o comando abaixo (ajuste conforme a linguagem do repositório).
Substitua `<git_url>` pela URL do repositório que será analisado:

```shell
# Python
$ gitevo -r python <git_url>

# JavaScript
$ gitevo -r javascript <git_url>

# TypeScript
$ gitevo -r typescript <git_url>

# Java
$ gitevo -r java <git_url>
```

Por exemplo, para analisar o projeto Flask escrito em Python:

```
$ gitevo -r python https://github.com/pallets/flask
```

> [!NOTE]
> Essa etapa pode demorar alguns minutos pois o projeto será clonado e analisado localmente.

# Passo 3: Explorar o relatório de evolução de código

Após executar a ferramenta [GitEvo](https://github.com/andrehora/gitevo), é gerado um relatório `HTML` contendo diversos gráficos sobre a evolução do código.

Abra o relatório `HTML` e observe com atenção os gráficos.

# Passo 4: Explicar um gráfico de evolução de código

Selecione um dos gráficos de evolução e explique-o com suas palavras.
Por exemplo, você pode:

- Detalhar a evolução ao longo do tempo
- Detalhar se as curvas estão de acordo com boas práticas
- Explicar grandes alterações nas curvas
- Explorar a documentação do repositório em busca de explicações para grandes alterações
- etc.

Seja criativo!

# Instruções para o exercício

1. Crie um `fork` deste repositório (mais informações sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Adicione o relatório `HTML` no seu fork.
3. No Moodle, submeta apenas a URL do seu `fork`.

Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork:

1. Repositório selecionado: https://github.com/sherlock-project/sherlock
   
2.
  <img width="1043" height="521" alt="image" src="https://github.com/user-attachments/assets/d358d01f-6c6c-42d6-bdcf-4a7911978bfe" />

   Em relação as boas práticas, classes muito grandes podem ser um problema, já que, dificultam a manutenção do sistema, dessa forma, a redução de ~127 LOC para ~74 LOC vista no gráfico, pode indicar uma refatoração positiva, separando responsabilidades em classes menores, assim como funções menores costumam ser mais legíveis e fáceis de testar. Portanto, o projeto parece estar refatorando classes grandes em unidades menores, mantendo funções relativamente estáveis, para tornar mais fácil as futuras manutenções e correções que o sistema possa eventualmente passar.

3.
  <img width="1046" height="506" alt="image" src="https://github.com/user-attachments/assets/aa970a0d-a529-4114-af5b-223217c5cc26" />

  O aumento de try e raise geralmente indica que há mais tratamento de exceções no código, ou seja, o código está capturando e gerando mais exceções explicitamente. Isso pode sugerir que o código está mais robusto, pois há mais previsibilidade na forma como erros são tratados. Dessa forma, um aumento no número de exceções tratadas ou levantadas não necessariamente significa que o software ficou “mais propenso a erros”, mas sim que os desenvolvedores adicionaram mais verificações e tratamentos. Pode também refletir mudanças na implementação ou na estratégia de tratamento, e não necessariamente aumento da robustez por si só.
