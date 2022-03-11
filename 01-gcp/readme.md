- [1. Máquinas Virtuais GCP](#1-máquinas-virtuais-gcp)
- [2. Criação](#2-criação)
- [3. Conexão](#3-conexão)


# 1. Máquinas Virtuais GCP

# 2. Criação

1. Mudar para a região us-east1 
2. Alterar o disco de inicialização:
   1. Imagens personalizadas
   2. Selecionar um projeto
   3. gglobo-infraessentials-hub
   4. Selecionar a imagem oracle para ambiente linux ou windows
   5. Selecionar o tipo de disco que será utilizado
3. Expandir "Rede, discos, segurança, gerenciamento, locatário único"
   1. Em interfaces de rede, selecionar redes compartilhadas comigo e selecionar a rede "sb-int-programacao-us-e1-hdg-prd"

# 3. Conexão

1. É preciso estar conectado à VPN vpncorp.globo.com
2. Seguir o [tutorial](https://infra.globoi.com/infra/omnicloud/gcp/acesso_ssh/)
3. Exemplo: `ssh douglas_braga_g_globo@10.88.10.6 -i C:\\Users\\douglasm\\.ssh\\google_compute_engine`
