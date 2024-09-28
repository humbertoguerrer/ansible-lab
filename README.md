## Lab Vagrant com Ansible para Provisionamento Multi-OS

Lab utilizando Vagrant para criar um ambiente com quatro máquinas virtuais e Ansible para provisionamento automatizado. <br>
<br>
O foco é configurar um ambiente heterogêneo com servidores Linux e Windows.

- **Servidor 1**: CentOS 7 (IP: 192.168.56.5) com sincronização de pastas locais.
- **Servidor 2**: Ubuntu 20.04 (IP: 192.168.15.5) com sincronização de pastas locais.
- **Servidor 3**: Ubuntu 18.04 (IP: 192.168.15.6).
- **Servidor 4**: Windows Server (IP: 192.168.56.6).

O provisionamento é feito utilizando **Ansible**, com funções pré-configuradas para instalar e gerenciar serviços como o proxy Squid.

### Destaques:
- Configuração de rede pública e portas mapeadas para acesso via host.
- Sincronização de pastas locais para deploy rápido de arquivos.
- Script Ansible para automatizar a configuração de múltiplos servidores, organizados em grupos de inventário para diferentes ambientes.
- Provisionamento para servidores Linux (CentOS, Ubuntu) e Windows.
