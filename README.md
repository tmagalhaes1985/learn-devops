Se você chegou até aqui, é porque está se garantindo! Vejamos o que se espera tecnicamente de você:

## Bash

- Compreender como o Terminal funciona
- Navegar pela estrutura de sistema de arquivos do Linux
- Manipular arquivos pelo Terminal
- Redirecionamento de I/O, standard input, standard output, pipes, filtros
- Permissões
- Controle de jobs
- Shell scripts

## Design e gerenciamento de infraestrutura

- Análise avançada de logs
- SSH avançado
- Configurar um nome de domínio
- Compreender o funcionamento do DNS
- Configurar um certificado SSL
- Gerenciar servidores web como Apache e Nginx
- Gerenciar balanceadores de carga
- Configurar bancos de dados em setups Primary/Replica
- Gerenciar configurações de Firewall
- Desenhar infraestruturas de aplicações web
- Monitorar infraestruturas de aplicações web
- Resolver problemas de stacks de aplicações web

## Projeto de exemplo

Ok, não precisa ficar com medo, mas enfim chegamos ao desafio técnico. Se você se perder por qualquer motivo, se acalme e façamos como todo mundo faz no dia a dia: busque ajuda no Google e StackOverflow, ninguém vai te recriminar por isso!

Neste projeto, vamos passar pelos seguintes desafios:

- Criar uma infraestrutura web como as que sustentam o Facebook, LinkedIn, Twitter, etc.
- Aprender como trabalhar com escalabilidade
- Desenvolver ferramentas para ambientes em nuvem (neste projeto utilizaremos a AWS)

**Nota**: Tente implementar o máximo de funcionalidades possíveis e forneça uma descrição detalhada sempre que aplicável.

1. Crie um script de Infraestrutura como Código (Terraform ou CloudFormation) para criar os componentes abaixo na AWS:

    - VPC com duas sub-redes (uma pública e uma privada)
    - Tabelas de roteamento para cada sub-rede
    - Grupos de segurança para permitir acesso somente nas porta 80 e 443
    - ELB e ALB
    - Zona privada no Route 53 com entradas CNAME para o ALB e ELB
    - Política IAM para item 3.

2. Crie um Ansible Playbook do Ansible para realizar as seguintes tarefas:

    - Selecionar uma AMI Linux (Amazon Linux 2)
    - Instalar um servidor web (Apache ou Nginx)
    - Baixar um código do de um repositório git
    - Configurar o servidor web com as melhores práticas de segurança (liste-as na sua documentação)
    - Crie um certificado auto-assinado para o servidor web
    - Publique um site de demonstração usando o certificado auto-assinado

3. Execute o Ansible Playbook

    - Execute o Playbook em um job do Packer e crie uma nova AMI
    - Crie um ASG automaticamente usando a AMI criada na etapa acima e anexe-a ao ELB
    - Demonstre as capacidades do ALB criando duas políticas de roteamento de domínio diferentes
    - A instância em execução atrás do ALB deve ter uma role anexada, permitindo acesso a um bucket específico do S3 e extrair imagens do S3

4. Crie um script usando qualquer linguagem de programação preferida (Python, Node.js, Java etc.) para realizar as seguintes atividades:

    - Listar os serviços da AWS que estão sendo usados ​​em termos de região
    - Listar detalhes de cada serviço, como EC2, RDS etc.
