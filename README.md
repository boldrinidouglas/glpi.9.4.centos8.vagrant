# glpi.9.4.centos8.vagrant 
 GLPI Versão 9.4 para CentOS 8 com Vagrant

## Introdução
A ideia aqui é oferecer uma experiência rápida e prática de DevOps com a entrega de uma instância no CentOS 8 com GLPI 4.2. Utilizei o Vagrante para simplificar a gerência de configuração de software das virtualizações para aumentar a produtividade do desenvolvimento e testes de novas versões.

## Pre-requisitos
* [Vagrant](https://www.vagrantup.com/downloads.html) Instalado
* VirtualBox (para este exemplo utilizei ele, porém poderá utilizar além do VirtualBox outros providers como: KVM, Hyper-V, Docker containers, VMware, e AWS.
* Máquina com pelo menos 4 GB e Processador com no mímimo 4 cores.

## Instalação
1. Crie um diretorio e copie os arquivos lá para dentro (glpifast.sh e Vagrantfile). 
2. Após isso entre com os comandos a seguir:
```#vagrant up```
3. Acesse a url: 192.168.1.10
4. Entre com as informações de banco: SQL server (MariaDB or MySQL): glpi | SQL user: glṕi | SQL password: glpipass
