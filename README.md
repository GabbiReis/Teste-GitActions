# Frontend e Backend com Docker e GitHub Actions

<div align="center">
    
![logo-DOCKER](https://cdn.iconscout.com/icon/free/png-256/docker-10-1175197.png)

</div>

Esta é uma aplicação de teste. Foram desenvolvidos Dockerfiles tanto para o backend quanto para o frontend, e ela está utilizando o GitHub Actions para realizar o processo de CI/CD.

## Índice

- [Instalação](#instalação)
    - [Uso](#uso)
- [Observações](#observações)
    - [GitHub Actions](#github-actions)
- [Licença](#licença)


## Instalação

Para rodar a aplicação diretamente na sua máquina, siga os passos abaixo:

1. **Clone o repositório:**
    ```bash
    git clone https://github.com/GabbiReis/Teste-GitActions.git
    cd Teste-GitActions
    ```

2. **Instale o Docker na sua máquina, caso ainda não tenha:**
    - Siga as instruções oficiais de instalação do Docker para sua plataforma em [Docker Get Started](https://docs.docker.com/get-docker/).

3. **Abra seu terminal e execute os seguintes comandos:**

    - Para subir os containers:
      ```bash
      docker-compose up -d
      ```

    - Para parar os containers:
      ```bash
      docker-compose stop
      ```

## Observações

- Certifique-se de que o Docker e o Docker Compose estão instalados e configurados corretamente na sua máquina.
- Verifique se os containers estão funcionando conforme esperado após executar os comandos.

Para mais informações, consulte a [documentação do Docker](https://docs.docker.com/) e [Docker Compose](https://docs.docker.com/compose/).

## Git Actions

O arquivo de configuração do GitHub Actions está localizado em `.github/workflows/git-pipeline.yml`. O pipeline funciona da seguinte maneira:

- Ele possui um estágio de build, onde realiza o processo de construção da imagem Docker, sobe os containers usando o Docker Compose, instala as dependências do npm, e, em seguida, constrói o frontend e gera um artefato.

- Depois, no estágio de deploy, que ocorre após o estágio de build, o pipeline pega o artefato gerado, faz o download e realiza o deploy no GitHub Pages.

  
<div align="center">
    
  ![icon-GIT-ACTIONS](https://creazilla-store.fra1.digitaloceanspaces.com/icons/3255852/github-icon-sm.png)
  
</div>

## Licença

Este projeto está licenciado sob a licença MIT.
