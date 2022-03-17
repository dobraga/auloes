- [1. Instalação e Configuração](#1-instalação-e-configuração)
- [2. Estágios de um arquivo](#2-estágios-de-um-arquivo)
- [3. Principais comandos](#3-principais-comandos)
- [4. Arquivos auxiliares](#4-arquivos-auxiliares)
- [5. SSH](#5-ssh)



[O Git é um sistema de controle de revisão distribuído, rápido, escalável e com um conjunto de comandos incomumente rico que oferece operações de alto nível e acesso completo aos seus recursos.](https://git-scm.com/docs/git/pt_BR)


# 1. Instalação e Configuração

1. [Instalar](https://git-scm.com/downloads)
2. Para configurar o nome e email que serão utilizados:  
  git config --global user.name "Fulano de Tal"  
  git config --global user.email "fulanodetal@exemplo.br"

# 2. Estágios de um arquivo

<img src="./img/git.png">

1. Workspace: Arquivos do seu projeto;
2. Staging: Área de arquivos a serem "commitados";
3. Local repository: Repositório local do git (pasta .git);
4. Remote repository: Repositório remoto como github, gitlab, bitbucket e etc.


# 3. Principais comandos

1. `git init`: Inicializa um repositório local;
2. `git clone {REPOSITÓRIO}`: Clona um repositório remoto para sua máquina;
3. `git status`: Status atual de modificações;
4. `git diff {ARQUIVO}`: Mostra visualmente as modificações realizadas no ARQUIVO;
5. `git add`: Adiciona modificações realizadas à área de stage;
6. `git restore {ARQUIVO}`: Remove modificação da área de stage; 
7. `git reset`: Remove modificações da área de stage;
8. `git commit -m "{MENSAGEM}"`: Faz o commit das alterações na área de stage com a {MENSAGEM};
9. `git commit -a -m "{MENSAGEM}"`: Faz o commit de TODAS as alterações com a {MENSAGEM}, **não recomendado** ;
10. `git push`: Sobe alterações para o repositório remoto;
11. `git pull`: Puxa alterações do repositório remoto para o repositório local.


# 4. Arquivos auxiliares

1. `.gitignore`: Ignora arquivos no git;  
      Esse arquivo precisa estar na raiz do projeto, todos os arquivos presentes nesse arquivo são ignorados pelo git, ex:
      ```
      *.xlsx
      *.csv
      env
      ```
2. `.gitkeep`: Permite subir pasta para o git mesmo sem arquivos.  
      Agora imagina que temos uma pasta chamada `dados` onde todos arquivos não estarão no git pois foram ignorados, como essa pasta não tem nenhum arquivo ela não existirá no git, para que ela exista basta adicionar o arquivo `.gitkeep` dentro da pasta.


# 5. SSH

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
