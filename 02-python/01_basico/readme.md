## 1. Porque python?

[Anualmente o github realiza uma pesquisa](https://octoverse.github.com/#top-languages-over-the-years) e um dos motivos para aprender python é por ser uma das linguagens mais utilizadas.

![](img/pesquisa_github.png)

Tá, mas por que ela é uma das mais utilizadas?

Aqui vão alguns motivos:

1. Um dos principais pontos para essa ampla utilização é a escrita parecida com o inglês;

Conseguem entender esse código?
```python
entrada = int(input("Digite quantos anos você tem:"))

if entrada >= 18:
    print("Cuidado, você ja pode ser preso!")
else:
    print("Fica a vontade")
```
2. É versátil, pode ser utilizada em diversas áreas diferentes:
   - Desenvolvimento de software;
   - Ciência de dados, análise de dados, machine learning;
   - Ethical hacker;
   - Cloud architect;
   - QA;
   - Desenvolvimento de Games;
   - Desenvolvimento de aplicações web;
   - Desenvolvimento de aplicativos.
  
3. Amigável para iniciantes;
4. É open-source, livre para usar e comercializar;
5. [Extensa biblioteca de pacotes para expandir as funcionalidades do python](https://pypi.org/);
6. Comunidade gigantesca.
7. [Documentação top <3](https://docs.python.org/pt-br/3/)


## 2. Utilização

1. [Podemos instalar](https://www.python.org/downloads/);
2. [Usar online](https://www.online-python.com/).

## 3. Sintaxe

Como comentado anteriormente, o python possui uma escrita fácil, a sintaxe básica consiste de:

- Comentário

    ```python
    # Isso é um comentário que será ignorado pelo python
    ```

    ```python
    """
    Isso é uma string com várias linhas
    Mas como não estamos fazendo nada com ela, também é como se fosse um comentário
    """
    ```

- Atribuição

    ```python
    var = 10
    ```

    ```python
    var1, var2 = 10, 20
    ```

- Valor Nulo

    ```python
    var = None
    ```

- Saída

    ```python
    print("Olá mundo")
    ```

- Entrada

    ```python
    var = input("Essa mensagem aparecerá no terminal para o usuário")
    ```

    OBS: O input do python sempre retorna uma string.

    Podemos transformar em inteiro, fazendo:

    ```python
    idade = int(input("Quantos anos você tem?"))
    ```

- Indentação

    O python utiliza a indentação e `:` para identificação do bloco de código, como por exemplo, condições, loops e entre outros

    ```python
    entrada = int(input("Digite quantos anos você tem:"))

    if entrada >= 18:
        print("Cuidado, você ja pode ser preso!")
    else:
        print("Fica a vontade")
    ```

- Blocos

  - if/elif/else
  - for/else
  - while/else
  - def
  - try/except /finally/else
  - class
  - with



## 4. Tipo de variáveis

Principais tipos de variáveis

<table>
    <tbody><tr>
        <th class="text-right">Números: </th>
        <td>int, float</td>
    </tr>
    <tr>
        <th class="text-right">Strings: </th>
        <td>str e unicode</td>
    </tr>
    <tr>
        <th class="text-right">Listas e tuplas: </th>
        <td>list, tuple</td>
    </tr>
    <tr>
        <th class="text-right">Dicionários: </th>
        <td>dict</td>
    </tr>
    <tr>
        <th class="text-right">Booleanos: </th>
        <td>bool (True, False)</td>
    </tr>
    <tr>
        <th class="text-right">Conjuntos: </th>
        <td>set, frozenset</td>
    </tr>
    <tr>
        <th class="text-right">None: </th>
        <td></td>
    </tr>
    </tbody>
</table>


```python
type("text")        # <class 'str'>
type(1)             # <class 'int'>
type(0.99)          # <class 'float'>
```

```python
type(1) == int      # True
type(0.99) == float # True
```


## 5. Operações matemáticas

Temos as operações básicas `+ - * /`


```python
10 + 10 # 20
20 - 10 # 10
2 * 10  # 20
20 / 2  # 10.0 divisão sempre retorna um float
```

Temos também:

- Potência

```python
10 ** 2 # 100
```

- Resto da divisão

```python
10 % 2 # 0
3 % 2  # 1
```

- Divisão inteira

```python
10 // 3 # 3
```

- Máximo, mínimo e valor absoluto

```python
max(5, 6, 7) # 7
min(5, 6, 7) # 5
abs(-1)      # 1
``` 

## 6. Strings

- Podemos usar aspas duplas ou simples, ex:

    ```python
    print("Olá mundo!")
    ```

    ```python
    print('Olá mundo!')
    ```

- Podemos "somar" strings, ex:

    ```python
    print("Olá" + "mundo" + "!")
    ```

    Para "somar" variáveis de outro tipo na string, precisamos fazer a conversão, ex:

    ```python
    print("Olá mundo!" + str(3.14))
    ```


Alguns métodos que podemos utilizar:

<table>
<tbody>
    <tr>
        <th>método</th>
        <th>descrição</th>
    </tr>
    <tr>
        <td>len()</td>
        <td>mostra o tamanho da string</td>
    </tr>
    <tr>
        <td>lower()</td>
        <td>caixa baixa</td>
    </tr>
    <tr>
        <td>upper()</td>
        <td>caixa alta</td>
    </tr>
    <tr>
        <td>str()</td>
        <td>converte em string</td>
    </tr>
    <tr>
        <td>isalpha()</td>
        <td>retorna False se a string contiver algum caracter que não seja letras</td>
    </tr>
    <tr>
        <td>split()</td>
        <td>separa em uma lista de strings</td>
    </tr>
</tbody>
</table>

Exemplo de utilização:

```python
print("Olá mundo!".upper()) # "OLÁ MUNDO!"
```

```python
print("Olá mundo!".split(" ")) # ['Olá', 'mundo!']
```

- Podemos acessar letras por index, ex:

    ```python
    "python"[0]   # p
    "python"[0:3] # pyt
    ```

## 7. Condicionais

A sintaxe básica de condicionais:

```python
if expressão:
    print("True")
else:
    print("False")
```

Onde a expressão precisa retornar um valor `True` ou `False`

```python
idade = int(input("Quantos anos você tem?"))

if idade < 18:
    print("ainda é uma criança")
elif idade < 60:
    print("você é jovem")
else:
    print("ainda está em forma")
```


## 8. Listas, tuplas, sets e dicionários

- Listas

    ```python
    frutas = ["laranja", "maçã", "pera", "banana"]
    ```

    - Alguns métodos que podemos utilizar:

      - copy(): Retorna uma cópia da lista
      ```python
      frutas2 = frutas # Essa lista é exatamente a mesma lista, ou seja, toda alterações que fizermos em uma, a outra também será alterada
      frutas3 = frutas.copy() # Essa é efetivamente uma cópia
      ```

      - append: Adiciona um elemento no final da lista
      ```python
      frutas.append("melão")
      print(frutas) # ['laranja', 'maçã', 'pera', 'banana', 'melão']
      ```

      - extend: Adiciona todos os elementos de uma outra lista
      ```python
      frutas.extend(["kiwi", "maçã"])
      print(frutas) # ['laranja', 'maçã', 'pera', 'banana', 'melão', 'kiwi', 'maçã']
      ```

      - insert(i, x): Adiciona um elemento em uma posição

      ```python
      frutas.insert(1, "melão")
      print(frutas) # ['laranja', 'melão', 'maçã', 'pera', 'banana', 'melão', 'kiwi', 'maçã']
      ```

      - remove(x): Remove o primeiro elemento da lista com valor igual a x
      ``` python
      frutas.remove("melão")
      print(frutas) # ['laranja', 'maçã', 'pera', 'banana', 'melão', 'kiwi', 'maçã']
      ```

      - pop(x): Remove o elemento na posição x e retorna o valor
    
      ``` python
      print(frutas.pop(0)) # laranja
      print(frutas) # ['maçã', 'pera', 'banana', 'melão', 'kiwi', 'maçã']
      ```

      - index(x): Retorna a posição do primeiro elemento igual a x
      ```python
      print(frutas.index("maçã")) # 0
      ```

      - count(x): Conta quantos elementos são iguais a x
      ```python
      print(frutas.count("maçã")) # 2
      ```
      - sort(): Ordena lista
      ```python
      frutas.sort()
      print(frutas) # ['banana', 'kiwi', 'maçã', 'maçã', 'melão', 'pera']
      ```

      - reverse(): Inverte a lista
      ```python
      frutas.reverse()
      print(frutas) # ['pera', 'melão', 'maçã', 'maçã', 'kiwi', 'banana']
      ```

      - clear(): Remove todos os elementos da lista
      ```python
      frutas.clear()
      print(frutas) # []
      ```

    - Assim como na string, podemos acessar pelo index:
    ```python
    print(frutas3[2]) # pera
    ```

    - Podemos contar quantos elementos a lista possui:
    ```python
    print(len(frutas3)) # 4
    ```

- Tuplas

    Vimos que listas são mutáveis, as tuplas são imutáveis, ou seja, depois de criadas não podem ser alteradas.

    Outra recomendação é que a lista seja utiliza para objetos homogêneos, ou seja, todos elementos do mesmo tipo e sobre o mesmo assunto, como vimos anteriormente, uma lista de frutas.

    Exemplo de tupla, onde temos Nome e Idade:

    ```python
    [("Ana", 20), ("Jorge", 35), ("Jubileu", 15)]
    ```

- Sets

    Sets são sempre ordenadas e deduplicadas:

    ```python
    frutas = {"laranja", "maçã", "pera", "banana", "banana", "maçã"}
    print(frutas) # {'banana', 'pera', 'maçã', 'laranja'}
    print(len(frutas)) # 4
    ```


- Dicionários

    O dicionario é uma estrutura chave valor, onde cada chave precisa ser única.

    Algumas formas de criar um dicionário:

    ```python
    d = {
        "Ana": 10,
        "José": 20,
        "Laura": 35
    }

    d = dict(
        Ana = 10,
        José = 20,
        Laura = 35
    )

    d = dict(
        [
            ("Ana", 10),
            ("José", 20),
            ("Laura", 30)
        ]
    )

    ```

    - Tamanho
    ```python
    print(len(d)) # 3
    ```

    - Seleção
    ```python
    print(d["Ana"]) # 10
    ```

    - Modificação
    ```python
    d["Ana"] = 30
    print(d["Ana"]) # 30
    ```

    - Remoção
    ```python
    del d["Ana"]
    ```

    ```python
    print(d["Ana"])

    # Traceback (most recent call last):
    # File "<pyshell#8>", line 1, in <module>
    #     d['Ana']
    # KeyError: 'Ana'
    ```

    OBS: Podemos usar o get para não dar erro

    ```python
    d.get("Ana") # None
    d.get("Ana", -1) # -1
    ```

    - Criação
    ```python
    d["Ana"] = 50
    print(d["Ana"]) # 50
    ```

    - Chave e valor:
    ```python
    print(d.keys()) # dict_keys(['Ana', 'José', 'Laura'])
    print(d.values()) # dict_values([50, 20, 30])
    ```


## 9. Loops

## 10. Funções
