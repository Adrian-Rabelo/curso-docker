# Curso de Docker da Cod3r

## Conceitos

## O que é Docker?

O Docker é uma tecnologia de virtualização. Porém não é uma tecnologia de virtualização tradicional. Diferente do acostumado, criar uma máquina virtual a partir do Virtual BOX, o Docker não trabalha com esse conceito de máquinas virtuais. Ele é uma engine de administração de container.

O Docker é open source e escrito em GO.

## Porque não usar uma VM?

Praticamente todas as vantagens de uma VM estão presentes em um container, com a diferença de que um container, por compartilhar o Kernel do sistema operacional host, consegue ser muito mais leve e rápido que uma VM, consumindo menos recursos.

## O que são Containers?

- **Segregração de processo** no mesmo Kernel (isolamento)
- **Sistema de arquibos** criados a partir de uma imagem
- Ambientes leves e portáteis no qual aplicações são executadas
- Encapsula todos os binários e bibliotecas necessárias para execução de um App
- Algo entre um **chroot** e uma **VM**

## O que são imagens Docker

- Modelo de sistema de arquivos somente-leitura usado para criar containers
- Imagens são criadas através de um processo chamado **build**
- São armazenadas em repositórios no Registry
- São compostas por uma ou mais camadas (layers)
- Uma camada representa uma ou mais mudanças no sistema de arquivos
- Uma camada também é chamada de imagem intermediária
- A junção dessas camadas formam a imagem
- Apenas a última camada pode ser alterada quando o container for iniciado
- AUFS (**A**dvanced multi-layered **U**nification **F**ile**S**ystem) é muito usado
- O grande objetivo dessa estratégia de dividir imagem em camadas é o reuso
- É possível compor imagens a partir de camadas de outras imagens

## Imagem vs Container

A imagem é um modelo usado para realizar um container. A partir de uma imagem é possível iniciar vários containers.
