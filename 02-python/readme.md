- [1. Ambiente Virtual](#1-ambiente-virtual)
  - [1.1. venv](#11-venv)
- [2. poetry](#2-poetry)
- [3. DotEnv](#3-dotenv)
  - [3.1. Utilização no python](#31-utilização-no-python)

# 1. Ambiente Virtual

É de extrema importância termos todo nosso ambiente de desenvolvimento separado em ambientes virtuais para:

1. Gestão de dependências do projeto;
2. Evitar conflitos de pacotes.

## 1.1. venv

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

Abrindo um arquivo python nesse projeto podemos ver na aba inferior que o vscode identifica o ambiente virtual utilizado:

<img src="./img/vs_barra_inferior1.JPG" alt="Configurações do VSCode">

Agora ao abrirmos o terminal o vscode ativa o ambiente automágicamente e podemos instalar pacotes neste ambiente:

```sh
pip install pandas
```

E podemos fazer o "freeze" das dependências
```sh
pip freeze > requirements.txt
```


# 2. poetry

O venv já resolve muito dos problemas relacionados à ambientes virtuais, o poetry trás algumas melhorias e facilidades.

Para instalar basta seguir o passo a passo pelo [site](https://python-poetry.org/docs/#installation)

Principais comandos:

1. `poetry new {NOME DO PROJETO}`: Cria uma estrutura básica de projetos;
2. `poetry shell`: Ativa o ambiente virtual;
3. `poetry add|remove {PACOTE}`: Adiciona|Remove pacotes equivalente ao pip install;
4. `poetry add|remove {PACOTE} -D`: Adiciona|Remove pacotes de desenvolvimento;
5. `poetry export -o requirements.txt`: Exporta dependências;


Ver o [vídeo](https://www.youtube.com/watch?v=naGF7EIUFp0&ab_channel=EduardoMendes) caso queira se aprofundar no tema.

# 3. DotEnv

Para armazenamento de senhas e chaves é recomendável utilizar o arquivo `.env`, esse formato segue o padrão

```
USUARIO1=user1
SENHA1=iksdngige945892745
```

## 3.1. Utilização no python

1. Instalação
```
pip install python-dotenv | poetry add python-dotenv
```

2. Utilização
``` python
from os import getenv
from dotenv import load_dotenv

load_dotenv()

print(getenv("USUARIO1"), getenv("SENHA1"))
```

Caso queira se aprofundar pode utilizar o [dynaconf](https://www.dynaconf.com/).
