Uma boa prática é não deixar exposto informações sensíveis dentro de seu código, como por exemplo, senhas de acesso, informações do banco de dados entre outros.

Para resolver este problema, podemos utilizar o arquivo `.env` para armazenar essas informações.

**Por conter informações sensíveis, não devemos subir este arquivo para o git, por isso sempre deixamos ele no `gitignore`**.

Exemplo de arquivo:
```
USUARIO1=user1
SENHA1=iksdngige945892745
```

A utilização no python é simples, basta:

1. Instalação

Utilizando poetry, execute:
```
poetry add python-dotenv
```

Caso, contrário, execute:
```
pip install python-dotenv
```

2. Utilização
``` python
from os import getenv
from dotenv import load_dotenv

load_dotenv()

print(getenv("USUARIO1"), getenv("SENHA1"))
```

Caso queira se aprofundar pode utilizar o [dynaconf](https://www.dynaconf.com/).
