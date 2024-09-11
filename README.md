# App

sh
docker run -it --name api-solid-pg -e POSTGRESQL_USERNAME=docker -e POSTGRESQL_PASSWORD=docker -e POSTGRESQL_DATABASE=apisolid -p 5432:5432 bitnami/postgresql

	## RFs ( Requisitos Funcionais )

- [ ] Deve ser possivel se cadastrar;
- [ ] Deve ser possivel se autenticar;
- [ ] Deve ser possivel obter o perfil de um user logado;
- [ ] Deve ser possivel obter o numero de check-ins realizados pelo usuario logado;
- [ ] Deve ser possivel o user obter o seu historico de check-ins;
- [ ] Deve ser possivel o user buscar academias proximas;
- [ ] Deve ser possivel o user buscar academias pelo nome;
- [ ] Deve ser possivel o user realizar check-in em uma academia;
- [ ] Deve ser possivel validae o check-in de um user;
- [ ] Deve ser possivel cadastrar uma academia;


  ## RNs ( Regras de Negocios )

- [ ] O usuario nao deve poder se cadastrar com um e-mail duplicado;
- [ ] O usuario nao pode fazer dois check-ins no mesmo dia;
- [ ] O usuario nao pode fazer check-in se nao estiver perto (100m) da academia;
- [ ] O check-in so pode ser validado ate 20 minutos apos criado;
- [ ] O check-in so pode ser validado por administradores;
- [ ] A academia so pode ser cadastrada por administradores;



  ## RNFs ( Requisitos nao-funcionais )


- [ ] A senha do usuario precisa estar criptografada;
- [ ] Os dados da aplicacao precisam estar persistidos em um bando PostgreSQL;
- [ ] Todas Listas de dados precisam estar paginadoscom 20 itens por pagina;
- [ ] O usuario deve ser identificado por um JWT (JSON web token);