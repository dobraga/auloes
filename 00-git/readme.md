- [1. Git](#1-git)
  - [1.1. SSH](#11-ssh)

## 1. Git


[O Git é um sistema de controle de revisão distribuído, rápido, escalável e com um conjunto de comandos incomumente rico que oferece operações de alto nível e acesso completo aos seus recursos.](https://git-scm.com/docs/git/pt_BR)

Para configurar o git:

1. [Instalar](https://git-scm.com/downloads)
2. Executar:  
  git config --global user.name "Fulano de Tal"  
  git config --global user.email "fulanodetal@exemplo.br"

<img src="./img/git.png" alt="Configurações do VSCode">

Principais comandos:

1. `git add`: Adiciona modificações realizadas à área de stage;
2. `git reset`: Remove modificações da área de stage;
3. `git commit -m {MENSAGEM}`: Faz o commit das alterações na área de stage com a MENSAGEM;
4. `git commit -a -m {MENSAGEM}`: Faz o commit de TODAS alterações com a MENSAGEM, **não recomendado** ;
5. `git push`: Sobe alterações para o repositório remoto;
6. `git pull`: Puxa alterações do repositório remoto para o repositório local.


Principais arquivos:

1. `.gitignore`: Ignora arquivos no git;  
      Esse arquivo precisa estar na raiz do projeto onde o projeto se encontra, todos arquivos presentes nesse arquivo são ignorados pelo git, ex:
      ```
      *.xlsx
      *.csv
      env
      ```
2. `.gitkeep`: Mantém pasta no git mesmo sem arquivos.  
      Agora imagina que temos uma pasta chamada `dados` onde todos arquivos não estarão no git pois foram ignorados, como essa pasta não tem nenhum arquivo ela não existirá no git, para que ela exista basta adicionar o arquivo `.gitkeep` dentro da pasta.


### 1.1. SSH

[Usando o protocolo SSH, você pode se conectar a servidores e serviços remotos e se autenticar neles. Com chaves SSH, você pode conectar-se a GitHub sem inserir seu nome de usuário e token de acesso pessoal em cada visita.](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/about-ssh)


1. Gerar uma chave SSH:
```sh
ssh-keygen -t rsa
```

2. Copiar chave publica:

Windows:
```sh
type %HOMEPATH%\.ssh\id_rsa.pub
```

Linux:
```sh
cat ~/.ssh/id_rsa.pub
```

3. Ao copiar a chave publica [seguir o passo-a-passo a partir do passo **2**](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/.adding-a-new-ssh-key-to-your-github-account)


Após feito isso, nossa máquina está conectada ao github.
