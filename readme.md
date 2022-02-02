- [1.1. Visual Studio Code](#11-visual-studio-code)
  - [1.1.1. Instalação](#111-instalação)
  - [1.1.2. Visão Geral](#112-visão-geral)
  - [1.1.2.1. Explorador de arquivos](#1121-explorador-de-arquivos)
  - [1.1.2.2. Ferramenta de pesquisa](#1122-ferramenta-de-pesquisa)
  - [1.1.2.3. Git](#1123-git)
  - [1.1.2.4. Extensões](#1124-extensões)
  - [1.1.2.5. Contas](#1125-contas)
  - [1.1.2.6. Configurações](#1126-configurações)
  - [1.1.3. Configuração do Python](#113-configuração-do-python)
  - [1.1.3.1. env](#1131-env)
  - [1.1.3.2. poetry](#1132-poetry)
  - [1.1.4. Configuração do R](#114-configuração-do-r)
  - [1.1.4.1. Renv](#1141-renv)
  - [1.1.5. Git](#115-git)
  - [1.1.5.1. Problemas comuns](#1151-problemas-comuns)
  - [1.1.6. DotEnv](#116-dotenv)
  - [1.1.7. SSH](#117-ssh)
- [2. Máquinas Virtuais GCP](#2-máquinas-virtuais-gcp)
- [2.1. Criação](#21-criação)
- [2.2. Conexão](#22-conexão)



# 1.1. Visual Studio Code

## 1.1.1. Instalação

Para instalar basta entrar no [site](https://code.visualstudio.com/) baixar e instalar.

## 1.1.2. Visão Geral

<img src="./img/vs_start.JPG" alt="Barra de Ferramentas do VSCode">

o VS Code trabalha sempre com projetos, ou seja, cada projeto precisa estar em uma pasta separada, nessa página inicial podemos abrir um projeto, um arquivo, clonar um repositório do git ou abrir os projetos mais recentes.



<img src="./img/vs_barra.JPG" alt="Barra de Ferramentas do VSCode">

Na sequência temos as seguintes ferrametas:

- Explorador de arquivos;
- Ferramenta de pesquisa;
- Git;
- Extensões;
- Contas;
- Configurações.


## 1.1.2.1. Explorador de arquivos

Nessa primeira aba temos o explorador de arquivos.

<img src="./img/vs_explorer1.JPG" alt="Explorer do VSCode">

Nessa aba podemos:

1. Ver a lista de arquivos abertos;
2. Ver a lista de todos arquivos;
3. Criar pastas;
4. Atualizar lista de arquivos;
5. Minimizar todas as pastas abertas;
6. Ver os pontos do código aberto;
7. Ver histórico de alterações do arquivo aberto.

Clicando com o botão direito nos espaços sem arquivos temos mais diversas opções:

<img src="./img/vs_explorer2.JPG" alt="Click do botão direito no Explorer do VSCode">

## 1.1.2.2. Ferramenta de pesquisa

Aqui temos uma ferramenta de pesquisa onde também podemos fazer substituições.

<img src="./img/vs_search.JPG" alt="Search do VSCode">

Temos as opções:

1. Ignorar diferença de letra maiúscula e minuscula;
2. Procurar palavra completa;
3. Utilizar expressão regular.


## 1.1.2.3. Git

Primeiramente essa aba não tem utilizada para projetos sem git, por isso ao abrir temos a seguinte tela:

<img src="./img/vs_git_start.JPG" alt="Git do VSCode">

Ao inicializar o repositório local temos a seguinte visão:

<img src="./img/vs_git.JPG" alt="Git do VSCode">

Com o git configurado podemos:

1. Ver a lista de arquivos modificados;
2. Ver as alterações realizas em cada arquivo;
3. Abrir o arquivo;
4. Remover mudanças realizadas;
5. Adicionar arquivos para área de stage;
6. Escrever a mensagem do commit;
7. Realizar todas as ações necessárias do git.

## 1.1.2.4. Extensões

O VScode é altamente configurável aqui existe uma imensidão de extensões, a lista de extensões que eu mais utilizo:

1. Code Spell Checker e Brazilian Portuguese - Code Spell Checker: Para correção de erros de ortografia;
2. Draw.io Integration - Para fazer diagramas;
3. GitLens - Melhorias para o git;
4. Jupyter - Para trabalhar com notebooks diretamente do vscode;
5. Markdown All in One - Melhorias para markdown;
6. Material Icon Theme - Pacote de ícones bonitinho;
7. Monokai Charcoal high contrast - Tema que utilizo;
8. Path Intellisense - Para ajudar a completar os caminhos de arquivos;
9. Python e Pylance - Melhorias para programar com python;
10. R e R Markdown All in One - Melhorias para programar com R;
11. Rainbow Brackets - Para colorir as chaves, colchetes e parenteses.


## 1.1.2.5. Contas

Essa parte é para armazenar suas configurações e extensões utilizadas na nuvem.

## 1.1.2.6. Configurações

<img src="./img/vs_config.JPG" alt="Configurações do VSCode">

Como o VSCode é altamente editável, aqui podemos:

1. Rodar comandos (F1);
2. Alterar as configurações do VSCode;
3. Alterar os atalhos do teclado;
4. [Criar snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets);
5. Alterar o tema;
6. Alterar os ícones;




## 1.1.3. Configuração do Python

## 1.1.3.1. env

## 1.1.3.2. poetry


## 1.1.4. Configuração do R

## 1.1.4.1. Renv

## 1.1.5. Git

## 1.1.5.1. Problemas comuns



## 1.1.6. DotEnv


## 1.1.7. SSH


# 2. Máquinas Virtuais GCP

# 2.1. Criação

1. Mudar para a região us-east1 
2. Alterar o disco de inicialização:
   1. Imagens personalizadas
   2. Selecionar um projeto
   3. gglobo-infraessentials-hub
   4. Selecionar a imagem oracle para ambiente linux ou windows
   5. Selecionar o tipo de disco que será utilizado
3. Expandir "Rede, discos, segurança, gerenciamento, locatário único"
   1. Em interfaces de rede, selecionar redes compartilhadas comigo e selecionar a rede "sb-int-programacao-us-e1-hdg-prd"

# 2.2. Conexão

1. É preciso estar conectado à VPN vpncorp.globo.com
2. Seguir o [tutorial](https://infra.globoi.com/infra/omnicloud/gcp/acesso_ssh/)
3. Exemplo: `ssh douglas_braga_g_globo@10.88.10.6 -i C:\\Users\\douglasm\\.ssh\\google_compute_engine`
