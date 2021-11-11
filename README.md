# Me Conta? #


Wrapper do projeto **Me conta?**.

> Começe por aqui para iniciar o desenvolvimento!

---
| Quality                                                                                                                                                                      | Frontend                                                                                                        | Backend                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MeConta_me-conta&metric=alert_status)](https://sonarcloud.io/dashboard?id=MeConta_me-conta) | [![Heroku](https://heroku-badge.herokuapp.com/?app=me-conta-frontend)](https://me-conta-frontend.herokuapp.com) | [![Heroku](https://heroku-badge.herokuapp.com/?app=me-conta-backend)](https://me-conta-backend.herokuapp.com) |
---

## :warning: Requerimentos ##

* [Node](https://nodejs.org/)
* [Docker](https://www.docker.com/products/docker-desktop)
* ~~[Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)~~
(Não é **necessário**, mas interessante)

## :package: Instalação ##

Clone este repositório com a opção **--recursive**

```bash
git clone --recursive https://github.com/MeConta/me-conta.git
```

## :whale: Rodar com o Docker compose ##

- Crie o arquivo `.env.local` para os projetos **frontend** e **backend** preenchendo as variáveis faltantes no `.env`
> Para o **backend** `.env` não possuí os dados de **ADMIN** nem **SMTP**

> Para o **frontend**, adicionar o link do backend (http://localhost:3000) ou do Heroku

- Na pasta do projeto:
    - Faça a migração do banco de dados (se necessário):
      ```bash
      docker compose run --rm migration
      ```
    - Inicie o backend:
      ```bash
      docker compose up -d api
      ```
    - Inicie o frontend: Na pasta do projeto:
    ```bash
      docker compose up -d front
    ```

---
    
| Backend                                  | Frontend                                  |
|------------------------------------------|-------------------------------------------|
| O backend deverá abrir na porta **3000** | O frontend deverá abrir na porta **3005** |

---

## :robot: Deploy ##


Por meio do [Github Actions](https://github.com/features/actions) todos os **commits** e **Pull requests** feitos na *main* iniciam o processo automático de deploy.

Os projetos de [Frontend](https://github.com/MeConta/me-conta-frontend) e [Backend](https://github.com/MeConta/me-conta-backend) serão disponibilizados no [Heroku](https://heroku.com)

---
### Links do **Heroku** ###
| BACKEND                                          | FRONTEND                                            | HEROKU                                                |
|--------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------|
| [Backend](https://me-conta-backend.herokuapp.com)| [Frontend](https://me-conta-frontend.herokuapp.com) | [Storybook](https://me-conta-storybook.herokuapp.com) | 

---

## Atualizando a codebase ##

Para atualizar os submodules ao dar pull utilizar:

```bash
git pull --recurse-submodules
```
