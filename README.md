<!--
*** Obrigado por estar vendo o nosso README. Se você tiver alguma sugestão
*** que possa melhorá-lo ainda mais dê um fork no repositório e crie uma Pull
*** Request ou abra uma Issue com a tag "sugestão".
*** Obrigado novamente! Agora vamos rodar esse projeto incrível : D
*** Video aula no youtube: https://www.youtube.com/watch?v=zz-vkI_L_iE
-->

# Primeiros Passos com Kubernetes para Ciência de Dados

<!-- PROJECT SHIELDS -->

[![npm](https://img.shields.io/badge/type-Open%20Project-green?&style=plastic)](https://img.shields.io/badge/type-Open%20Project-green)
[![GitHub last commit](https://img.shields.io/github/last-commit/GersonRS/challenge-delta-lake-deep-dive?logo=github&style=plastic)](https://github.com/GersonRS/challenge-delta-lake-deep-dive/commits/master)
[![GitHub Issues](https://img.shields.io/github/issues/gersonrs/challenge-delta-lake-deep-dive?logo=github&style=plastic)](https://github.com/GersonRS/challenge-delta-lake-deep-dive/issues)
[![GitHub Language](https://img.shields.io/github/languages/top/gersonrs/challenge-delta-lake-deep-dive?&logo=github&style=plastic)](https://github.com/GersonRS/challenge-delta-lake-deep-dive/search?l=python)
[![GitHub Repo-Size](https://img.shields.io/github/repo-size/GersonRS/challenge-delta-lake-deep-dive?logo=github&style=plastic)](https://img.shields.io/github/repo-size/GersonRS/challenge-delta-lake-deep-dive)
[![GitHub Contributors](https://img.shields.io/github/contributors/GersonRS/challenge-delta-lake-deep-dive?logo=github&style=plastic)](https://img.shields.io/github/contributors/GersonRS/challenge-delta-lake-deep-dive)
[![GitHub Stars](https://img.shields.io/github/stars/GersonRS/challenge-delta-lake-deep-dive?logo=github&style=plastic)](https://img.shields.io/github/stars/GersonRS/challenge-delta-lake-deep-dive)
[![NPM](https://img.shields.io/github/license/GersonRS/challenge-delta-lake-deep-dive?&style=plastic)](LICENSE)
[![Status](https://img.shields.io/badge/status-active-success.svg)](https://img.shields.io/badge/status-active-success.svg)

<!-- PROJECT LOGO -->

<p align="center">
  <img alt="logo" src="https://github.com/GersonRS/react-native-template-gersonrsantos-basic/raw/main/assets/logo.png"/>
</p>

# Overview

Este repositório contém os códigos e recursos utilizados na live "Primeiros Passos com Kubernetes para Ciência de Dados". Aqui, você encontrará exemplos práticos e instruções para começar a utilizar o Kubernetes em seus projetos de ciência de dados.

<!-- TABLE OF CONTENTS -->

# Tabela de Conteúdo
* [Sobre o Projeto](#sobre-o-projeto)
* [Feito Com](#feito-com)
* [Fluxo de versionamento](#fluxo-de-versionamento)
* [Começando](#come%C3%A7ando)
  + [Pré-requisitos](#pr%C3%A9-requisitos)
  + [Instalação do cluster](#instala%C3%A7%C3%A3o-do-cluster)
  + [Instalação das ferramentas](#instala%C3%A7%C3%A3o-das-ferramentas)
  + [Executando o projeto](#executando-o-projeto)
* [Estrutura de Arquivos](#estrutura-de-arquivos)
  + [Edição](#edi%C3%A7%C3%A3o)
* [Contribuição](#contribui%C3%A7%C3%A3o)
* [Licença](#licen%C3%A7a)
* [Contato](#contato)

<!-- ABOUT THE PROJECT -->

# Objetivo

O objetivo deste repositório é fornecer um guia básico e prático para cientistas de dados que desejam aprender como utilizar o Kubernetes para otimizar e escalar suas análises de dados.

# Fluxo de versionamento:

Projeto segue regras de versionamento [gitflow](https://www.atlassian.com/br/git/tutorials/comparing-workflows/gitflow-workflow).

# Feito Com

Abaixo segue o que foi utilizado na criação deste projeto:

* [Minikube](https://minikube.sigs.k8s.io/docs/start/) - Ferramenta de código aberto que permite criar um ambiente de teste do Kubernetes em sua máquina local. Com o Minikube, é possível criar e implantar aplicativos em um cluster Kubernetes em sua máquina local.
* [Helm](https://helm.sh/) - Ferramenta de gerenciamento de pacotes de código aberto para o Kubernetes. O Helm permite empacotar aplicativos Kubernetes em um formato padrão chamado de gráfico, que inclui todos os recursos necessários para implantar o aplicativo, incluindo configurações e dependências.
* [ArgoCD](https://argo-cd.readthedocs.io/en/stable/) - Ferramenta declarativa que usa a abordagem GitOps para implantar aplicações no Kubernetes. O Argo CD é gratuito, tem código aberto, é um projeto incubado pela CNCF, e possui uma interface web de visualização e gerenciamento dos recursos, mas também pode ser configurado via linha de comando.
* [Spark](https://spark.apache.org/) - O Spark é um framework de processamento de dados distribuído e de código aberto, que permite executar processamento de dados em larga escala, incluindo processamento em batch, streaming, SQL, machine learning e processamento de gráficos. Ele foi projetado para ser executado em clusters de computadores e fornece uma interface de programação fácil de usar para desenvolvedores; 
* [Airflow](https://airflow.apache.org/) - O Airflow é uma plataforma de orquestração de fluxo de trabalho de dados de código aberto que permite criar, agendar e monitorar fluxos de trabalho complexos de processamento de dados. Ele usa uma linguagem de definição de fluxo de trabalho baseada em Python e possui uma ampla gama de conectores pré-construídos para trabalhar com diferentes sistemas de armazenamento de dados, bancos de dados e ferramentas de processamento de dados; 
* [Reflector](https://github.com/emberstack/kubernetes-reflector) - O Reflector é uma ferramenta de sincronização de estado de código aberto que permite sincronizar recursos Kubernetes em diferentes clusters ou namespaces. Ele usa a abordagem de controlador de reconciliação para monitorar e atualizar automaticamente o estado dos recursos Kubernetes com base em um estado desejado especificado; 
* [Minio](https://min.io/) - O Minio é um sistema de armazenamento de objetos de código aberto e de alta performance, compatível com a API Amazon S3. Ele é projetado para ser executado em clusters distribuídos e escaláveis e fornece recursos avançados de segurança e gerenciamento de dados; 
* [Postgres](https://www.postgresql.org/) - O Postgres é um sistema de gerenciamento de banco de dados relacional de código aberto, conhecido por sua confiabilidade, escalabilidade e recursos avançados de segurança. Ele é compatível com SQL e é usado em uma ampla gama de aplicativos, desde pequenos sites até grandes empresas e organizações governamentais.

<!-- GETTING STARTED -->

# Começando

Siga estas instruções para configurar e utilizar os códigos deste repositório em seu ambiente local. 

Este guia apresentará uma série de comandos para instalar as ferramentas necessárias.

## Pré-requisitos

Para usar o kubernetes, você precisa ter os seguintes pré-requisitos instalados e configurados:

1. Minikube:
    - Instalação:  Visite o site do [Minikube](https://minikube.sigs.k8s.io/docs/start/). e siga as instruções do seu sistema operacional.
2. Docker:
    - Instalação: Instale o Docker seguindo as instruções do seu sistema operacional no [site do Docker](https://docs.docker.com/get-docker/).
3. Kubernetes CLI (kubectl):
    - Instalação: Instale `kubectl` seguindo as instruções do seu sistema operacional no [site do Kubernetes](https://kubernetes.io/docs/tasks/tools/install-kubectl/).
4. Helm:
    - Instalação: Instale o Helm seguindo as instruções para seu sistema operacional no [site do Helm](https://helm.sh/docs/intro/install/).

### instalação do cluster

O primeiro passo é montar um ambiente com um cluster Kubernetes local para executar a aplicação e o pipeline de dados. Para esta POC, usaremos o cluster de Kubernetes **[minikube](https://minikube.sigs.k8s.io/docs/)**. [Siga este guia de instalação para instalar o Minikube](https://minikube.sigs.k8s.io/docs/start/).

Também usaremos o **[helm](https://helm.sh/)** para nos ajudar a instalar algumas aplicações. [Siga este guia de instalação para instalar o Helm](https://helm.sh/docs/intro/install/).

Após instalar esses pré-requisitos, é hora de iniciar o nosso cluster Minikube. Para que tudo ocorra bem, é aconselhável usar um cluster de no mínimo 8GB de memória e 2 CPUs. Execute o seguinte comando no terminal:

```
minikube start --memory=8000 --cpus=2
```

Para acessar alguns serviços via loadbalancer no Minikube, é necessário utilizar o [tunelamento do minikube](https://minikube.sigs.k8s.io/docs/handbook/accessing/#example-of-loadbalancer). Para isso, abra uma nova aba no seu terminal e execute o seguinte comando:

```sh
minikube tunnel
```

Com isso, o seu ambiente estará pronto para receber acessos via loadbalancer.

### Instalação das ferramentas

Depois do ambiente inicializado será necessario instalar algumas aplicações que serão responsaveis por manter e gerenciar nosso pipeline de dados.

Estando conectado em um cluster Kubernetes, execute os seguintes comandos para criar todos os namespaces necessarios:

```sh
kubectl create namespace deepstorage
kubectl create namespace mlops
kubectl create namespace processing
```

helm repo add minio https://charts.min.io/
helm repo add jupyterhub https://hub.jupyter.org/helm-chart/
helm repo add community-charts https://community-charts.github.io/helm-charts

helm repo update
helm install minio minio/minio -f manifests/minio.yaml
helm install mlflow community-charts/mlflow
helm install postgresql oci://registry-1.docker.io/bitnamicharts/postgresql

helm upgrade --cleanup-on-fail \
  --install minio minio/minio \
  --values manifests/minio.yaml

echo http://$(kubectl get svc --namespace default minio --template "{{ range (index .status.loadBalancer.ingress 0) }}{{.}}{{ end }}"):9000

echo $(kubectl get secret minio --namespace default -o jsonpath="{.data.rootUser}" | base64 --decode):$(kubectl get secret minio -o jsonpath="{.data.rootPassword}" | base64 --decode)

helm upgrade --cleanup-on-fail \
  --install postgresql oci://registry-1.docker.io/bitnamicharts/postgresql \
  --values manifests/postgresql.yaml

echo $(kubectl get svc --namespace default postgresql --template "{{ range (index .status.loadBalancer.ingress 0) }}{{.}}{{ end }}")

helm upgrade --cleanup-on-fail \
  --install mlflow community-charts/mlflow \
  --values manifests/mlflow.yaml

echo http://$(kubectl get svc --namespace default mlflow --template "{{ range (index .status.loadBalancer.ingress 0) }}{{.}}{{ end }}"):5000
  
helm upgrade --cleanup-on-fail \
  --install kupyterhub jupyterhub/jupyterhub \
  --values manifests/jupyterhub.yaml

echo http://$(kubectl get service proxy-public --output jsonpath='{.status.loadBalancer.ingress[].ip}')

helm upgrade --cleanup-on-fail \
  --install kserve community-charts/kserve \
  --values manifests/kserve.yaml
  

Ótimo, agora que você configurou as ferramentas necessárias, temos o ambiente de desenvolvimento e de execução instalado e pronto para uso.

### Executando o projeto

Certifique-se de testar e validar seus pipelines de dados antes de implantá-los em produção. Isso ajudará a garantir que seus processos estejam funcionando corretamente e que os dados estejam sendo tratados de maneira apropriada.

## Estrutura de Arquivos

A estrutura de pastas está da seguinte maneira:

```bash
.
├── manifests
│   ├── database
│   ├── orchestrator
│   └── processing
└── secrets
# 35 directories, 327 files
```

Serão explicados os arquivos e diretórios na seção de [Edição](#edição).

---

### Edição

Nesta seção haverão instruções caso você queira editar o projeto, explicando para que os diretórios são utilizados e também os arquivos de configuração.

* **[access-control](/access-control/)** - Diretório contendo todos os arquivos de aplicação do projeto, é criado um diretório `manifests` para que o código da aplicação possa ser isolado em um diretório e facilmente portado para outros projetos, se necessário; 

* **[manifests](/manifests/)** - Diretório contendo todos os arquivos de aplicação do projeto, é criado um diretório `manifests` para que o código da aplicação possa ser isolado em um diretório e facilmente portado para outros projetos, se necessário; 

  + **[database](/manifests/database/)** - Diretório para guardar os arquivos de configuração das aplicações de database, por exemplo, a configuração de instalação da aplicação **[postgres](/manifests/database/postgres.yaml)**; 

to do o resto

<!-- CONTRIBUTING -->

## Contribuição

Contribuições são o que fazem a comunidade open source um lugar incrível para aprender, inspirar e criar. Qualquer contribuição que você fizer será **muito apreciada**.

1. Faça um Fork do projeto
2. Crie uma Branch para sua Feature (`git checkout -b feature/FeatureIncrivel`)
3. Adicione suas mudanças (`git add .`)
4. Comite suas mudanças (`git commit -m 'Adicionando uma Feature incrível!`)
5. Faça o Push da Branch (`git push origin feature/FeatureIncrivel`)
6. Abra um Pull Request

<!-- LICENSE -->

## 📌 Suporte

Entre em contato comigo em um dos seguintes lugares!

* Linkedin em [Gerson Santos](https://www.linkedin.com/in/gerson-santos-a1442a90/)
* Instagram [gersonrsantos](https://www.instagram.com/gersonrsantos/)

---

## 📝 Licença

<img alt="License" src="https://img.shields.io/badge/license-MIT-%2304D361?color=rgb(89, 101, 224)">

Distribuído sob a licença MIT. Veja [LICENSE](LICENSE) para mais informações.

### 📱 Social

Me acompanhe nas minhas redes sociais.

<p align="center">

 <a href="https://twitter.com/gersonrs3" target="_blank" >

     <img alt="Twitter" src="https://img.shields.io/badge/-Twitter-9cf?logo=Twitter&logoColor=white"></a>

  <a href="https://instagram.com/gersonrsantos" target="_blank" >

    <img alt="Instagram" src="https://img.shields.io/badge/-Instagram-ff2b8e?logo=Instagram&logoColor=white"></a>

  <a href="https://www.linkedin.com/in/gersonrsantos/" target="_blank" >

    <img alt="Linkedin" src="https://img.shields.io/badge/-Linkedin-blue?logo=Linkedin&logoColor=white"></a>

  <a href="https://t.me/gersonrsantos" target="_blank" >

    <img alt="Telegram" src="https://img.shields.io/badge/-Telegram-blue?logo=Telegram&logoColor=white"></a>

  <a href="mailto:gersonrodriguessantos8@gmail.com" target="_blank" >

    <img alt="Email" src="https://img.shields.io/badge/-Email-c14438?logo=Gmail&logoColor=white"></a>

</p>

---

Feito com ❤️ by **Gerson**
