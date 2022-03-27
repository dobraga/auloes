
# 1. PyPI e pip

[O Python Package Index (PyPI) é um repositório de software para a linguagem de programação Python. O PyPI ajuda você a encontrar e instalar software desenvolvido e compartilhado pela comunidade Python.](https://pypi.org/)


[pip é a ferramenta mais popular para instalar pacotes Python e que já é instalado em conjunto do Python. Ele fornece os principais recursos essenciais para localizar, baixar e instalar pacotes do PyPI e outros índices de pacotes Python.](https://packaging.python.org/en/latest/key_projects/#pip)


- Instalação
    - Via PyPI
        ```sh
        pip install nome-do-pacote
        ```

    - Via arquivos de distribuição

        ```sh
        pip install caminho/nome-do-pacote.tar.gz
        ```

        ```sh
        pip install caminho/nome-do-pacote.whl
        ```

    - Via `requirements.txt`

        `requirements.txt` são arquivos contendo uma lista de itens a serem instalados usando pip install assim:

        ```sh
        pip install -r requirements.txt
        ```

        [Exemplo de arquivo `requirements.txt`](https://pip.pypa.io/en/stable/reference/requirements-file-format/#example):
        
            ```requirements.txt
            ###### Requirements without Version Specifiers ######
            pytest
            pytest-cov
            beautifulsoup4

            ###### Requirements with Version Specifiers ######
            #   See https://www.python.org/dev/peps/pep-0440/#version-specifiers
            docopt == 0.6.1             # Version Matching. Must be version 0.6.1
            keyring >= 4.1.1            # Minimum version 4.1.1
            coverage != 3.5             # Version Exclusion. Anything except version 3.5
            Mopidy-Dirble ~= 1.1        # Compatible release. Same as >= 1.1, == 1.*
            ```

- Atualização
    ```sh
    pip install --upgrade nome-do-pacote
    ```

- Remoção
    ```sh
    pip uninstall nome-do-pacote
    ```

# 2. Ambiente Virtual 

É de extrema importância termos todo nosso ambiente de desenvolvimento separado em ambientes virtuais.

Imagina que ao longo do tempo teremos diversos projetos, cada um com suas peculiaridades e necessidades e se utilizasse a mesma instalação do python para todos os projetos poderíamos ter diversos problemas. Principais motivos para utilização de ambientes virtuais:

1. Gestão de dependências do projeto;
2. Evitar conflitos de pacotes.


## 2.1. venv

O próprio python trás um pacote para criação de ambientes virtuais chamado venv.


Passos para utilização:

1. Para criar o ambiente basta executar no terminal:

```sh
python -m venv env
```

2. Para ativar o ambiente virtual:

No cmd
```sh
env/Scripts/activate.bat
```

No powershell
```sh
env/Scripts/Activate.ps1
```

No bash do linux
```sh
source env/bin/activate
```

Abrindo um arquivo python nesse projeto podemos ver na aba inferior que o vscode identifica o ambiente virtual utilizado.

Agora ao abrirmos o terminal o vscode ativa o ambiente automágicamente e podemos instalar pacotes neste ambiente:

```sh
pip install pandas
```

E podemos fazer o "freeze" das dependências utilizadas no projeto
```sh
pip freeze > requirements.txt
```


## 2.2. poetry

O venv já resolve muito dos problemas relacionados à ambientes virtuais, o poetry trás algumas melhorias e facilidades.

Para instalar basta seguir o passo a passo pelo [site](https://python-poetry.org/docs/#installation)

Principais comandos:

1. `poetry new {NOME DO PROJETO}`: Cria uma estrutura básica de projetos;
2. `poetry shell`: Ativa o ambiente virtual;
3. `poetry add|remove {PACOTE}`: Adiciona|Remove pacotes equivalente ao pip install;
4. `poetry add|remove {PACOTE} -D`: Adiciona|Remove pacotes de desenvolvimento;
5. `poetry export -o requirements.txt`: Exporta dependências;


Ver o [vídeo](https://www.youtube.com/watch?v=naGF7EIUFp0&ab_channel=EduardoMendes) caso queira se aprofundar no tema.
