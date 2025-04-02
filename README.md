# Projeto Super Portfólio

<details>
<summary><strong>🧑‍💻 O que deverá ser desenvolvido</strong></summary><br />

Neste projeto, você vai praticar os seus conhecimentos em Django e Django Rest Framework. Você irá desenvolver uma API para gerenciamento de dados de perfil e projetos em um super portfólio. Vamos lá? 🤩

</details>

<details>
  <summary><strong>📝 Habilidades a serem trabalhadas</strong></summary><br />

- Utilizar o _Django REST Framework_ para criar endpoints com entidades aninhadas.
- Utilizar o módulo _Simple JWT_ para implementar autenticação no Django REST Framework.

</details>

<details>

   <summary><strong>‼ Antes de começar a desenvolver </strong></summary><br />

1. Este projeto usa dependências que não são funcionais em todas as versões do Python. Por isso, recomendamos que seu Python esteja na versão `3.10.0` ou superior. Você pode usar o `Pyenv`, basta seguir nosso tutorial sobre [instalação e uso do Pyenv](https://app.betrybe.com/learn/course/5e938f69-6e32-43b3-9685-c936530fd326/module/f04cdb21-382e-4588-8950-3b1a29afd2dd/section/aa76abc8-b842-40d9-b5cc-baa960952129/lesson/0fe67ea0-1046-4b55-a37c-44afcfa9ed0a).
  
> ⚠️ **ATENÇÃO: NUNCA REMOVA VERSÕES ANTIGAS INSTALADAS DO PYTHON. SEU SISTEMA OPERACIONAL PODE DEPENDER DELAS!** ⚠️

2. Para conseguir instalar a dependência `mysqlclient` você precisa garantir a existência de algumas bibliotecas no seu sistema operacional:

- **Debian/Ubuntu**
```bash
sudo apt-get install python3-dev default-libmysqlclient-dev build-essential pkg-config
```

- **Mac**
```bash
brew install mysql pkg-config
```

3. Clone o repositório

- Use o comando: `git clone git@github.com:tryber/python-035-python-projeto-super-portfolio.git`
- Entre na pasta do repositório que você acabou de clonar:
  - `cd python-035-python-projeto-super-portfolio`

4. Crie uma branch a partir da branch `main`

- Verifique que você está na branch `main`
  - Exemplo: `git branch`
- Se você não estiver, mude para a branch `main`
  - Exemplo: `git checkout main`
- Agora, crie uma branch à qual você vai submeter os `commits` do seu projeto:
  - Você deve criar uma branch no seguinte formato: `nome-sobrenome-nome-do-projeto`;
  - Exemplo: `git checkout -b maria-soares-super-portfolio`

5. Crie / altere os arquivos que precisar para desenvolver os requisitos

6. Adicione as mudanças ao _stage_ do Git e faça um `commit`

- Verifique que as mudanças ainda não estão no _stage_:
  - Exemplo: `git status` (devem aparecer listados os novos arquivos em vermelho)
- Adicione o novo arquivo ao _stage_ do Git:
  - Exemplo:
    - `git add .` (adicionando todas as mudanças - _que estavam em vermelho_ - ao stage do Git)
    - `git status` (devem aparecer listados os arquivos em verde)
- Faça o `commit` inicial:
  - Exemplo:
    - `git commit -m 'iniciando o projeto. VAMOS COM TUDO :rocket:'` (fazendo o primeiro commit)
    - `git status` (deve aparecer uma mensagem tipo _nothing to commit_ )

7. Adicione a sua branch com o novo `commit` ao repositório remoto

- Usando o exemplo anterior: `git push -u origin maria-soares-super-portfolio`

8. Crie um novo `Pull Request` _(PR)_

- Vá até a página de _Pull Requests_ do [repositório no GitHub](https://github.com/tryber/python-0x-project-super-portfolio/pulls)
  - Clique no botão verde _"New pull request"_
  - Clique na caixa de seleção _"Compare"_ e escolha a sua branch **com atenção**
- Coloque um título para o seu _Pull Request_
  - Exemplo: _"Cria tela de busca"_
- Clique no botão verde _"Create pull request"_

- Adicione uma descrição para o _Pull Request_, um título nítido que o identifique, e clique no botão verde _"Create pull request"_

 <img width="1335" alt="Exemplo de pull request" src="https://user-images.githubusercontent.com/42356399/166255109-b95e6eb4-2503-45e5-8fb3-cf7caa0436e5.png">

- Volte até a [página de _Pull Requests_ do repositório](https://github.com/tryber/python-0x-project-super-portfolio/pulls) e confira que o seu _Pull Request_ está criado

</details>

<details>

<summary><strong>⌨️ Durante o desenvolvimento</strong></summary><br />

Faça `commits` das alterações que você fizer no código regularmente, pois assim você garante visibilidade para o time da Trybe e treina essa prática para o mercado de trabalho :) ;

- Lembre-se de sempre após um (ou alguns) `commits` atualizar o repositório remoto;
- Os comandos que você utilizará com mais frequência são:

  - `git status` _(para verificar o que está em vermelho - fora do stage - e o que está em verde - no stage)_;
  - `git add` _(para adicionar arquivos ao stage do Git)_;
  - `git commit` _(para criar um commit com os arquivos que estão no stage do Git)_;
  - `git push -u origin nome-da-branch` _(para enviar o commit para o repositório remoto na primeira vez que fizer o `push` de uma nova branch)_;
  - `git push` _(para enviar o commit para o repositório remoto após o passo anterior)_.

</details>

<details>
  <summary><strong>🎛 Linter</strong></summary><br />

Para garantir a qualidade do código, vamos utilizar nesses exercícios o linter `Flake8`. Assim o código estará alinhado com as boas práticas de desenvolvimento, sendo mais legível e de fácil manutenção! Para rodá-lo localmente no projeto, execute o comandos abaixo:

```bash
python3 -m flake8
```

⚠️ **PULL REQUESTS COM ISSUES DE LINTER NÃO SERÃO AVALIADAS.
ATENTE-SE PARA RESOLVÊ-LAS ANTES DE FINALIZAR O DESENVOLVIMENTO!** ⚠️

</details>

<details>
  <summary><strong>🏕️ Ambiente Virtual</strong></summary><br />

O Python oferece um recurso chamado de ambiente virtual, que permite sua máquina rodar sem conflitos diferentes tipos de projetos com diferentes versões de bibliotecas.

1. Criar o ambiente virtual

```bash
python3 -m venv .venv
```

2. Ativar o ambiente virtual

```bash
source .venv/bin/activate
```

3. Instalar as dependências no ambiente virtual

```bash
python3 -m pip install -r dev-requirements.txt
```

Com o seu ambiente virtual ativo, as dependências serão instaladas neste ambiente.
Quando precisar desativar o ambiente virtual, execute o comando "deactivate". Lembre-se de ativar novamente quando voltar a trabalhar no projeto.

O arquivo `dev-requirements.txt` contém todas as dependências que serão utilizadas no projeto, ele está agindo como se fosse um `package.json` de um projeto `Node.js`.

</details>

<details>
  <summary><strong>🛠 Testes</strong></summary><br />

Para executar os testes certifique-se de que você está com o ambiente virtual ativado.

<strong>Executar os testes</strong>

```bash
python3 -m pytest
```

O arquivo `pyproject.toml` já configura corretamente o pytest. Entretanto, caso você tenha problemas com isso e queira explicitamente uma saída completa, o comando é:

```bash
python3 -m pytest -s -vv
```

Caso precise executar apenas um arquivo de testes basta executar o comando:

```bash
python3 -m pytest tests/nomedoarquivo.py
```

Caso precise executar apenas uma função de testes basta executar o comando:

```bash
python3 -m pytest -k nome_da_func_de_tests
```

Se desejar que os testes parem de ser executados quando acontecer o primeiro erro, use o parâmetro `-x`

```bash
python3 -m pytest -x tests/test_jobs.py
```

Para executar um teste específico de um arquivo, basta executar o comando:

```bash
python3 -m pytest tests/nomedoarquivo.py::test_nome_do_teste
```

Se quiser saber mais sobre a instalação de dependências com `pip`, veja esse [artigo](https://medium.com/python-pandemonium/better-python-dependency-and-package-management-b5d8ea29dff1).

</details>

<details>
  <summary><strong>🏃🏾 Executando o Projeto</strong></summary>
    <br />
  Para a realização deste projeto, utilizaremos um banco de dados chamado `super_portfolio_database`. Já existe um script de criação do banco pronto no arquivo `database/01_create_database.sql` que será copiado para dentro do container. Não altere este script.

  Para rodar o MySQL via Docker execute os seguintes comandos na raiz do projeto:

  ```bash
  docker build -t super-portfolio-db .
  docker run -d -p 3306:3306 --name=super-portfolio-mysql-container -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=super_portfolio_database super-portfolio-db
  ```

  Esses comandos irão fazer o build da imagem e subir o container Docker.

  Lembre-se de que o MySQL utiliza por padrão a porta 3306. Se já houver outro serviço utilizando esta porta, considere desativá-lo ou mudar a porta no comando acima.

</details>

## Quando finalizar o projeto não esquecer

<details>
<summary><strong>🗂 Compartilhe seu portfólio!</strong></summary>
  <br />

Você sabia que o LinkedIn é a principal rede social profissional e compartilhar o seu aprendizado lá é muito importante para quem deseja construir uma carreira de sucesso? Compartilhe esse projeto no seu LinkedIn, marque o perfil da Trybe (@trybe) e mostre para a sua rede toda a sua evolução.

</details>

<details>
<summary><strong>🗣 Nos dê feedbacks sobre o projeto!</strong></summary>
  <br />

Ao finalizar e submeter o projeto, não se esqueça de avaliar sua experiência preenchendo o formulário.
**Leva menos de 3 minutos!**

[Formulário de avaliação do projeto](https://be-trybe.typeform.com/to/ZTeR4IbH#cohort_hidden=CH35-PYTHON&template=betrybe/python-0x-projeto-super-portfolio)

</details>

</details>

<details>
<summary><strong>🎨 Estilize seu projeto</strong></summary>
  <br />

Você sabia que esse projeto já possui um arquivo de estilização? Após iniciar o app `projects`, basta mover para dentro da pasta `projects` a pasta `mova_static` e renomeá-la como `static`. A partir daí, você pode acessar o arquivo `style.css` na pasta `static/css` e personalizar o projeto de acordo com seu gosto. Ou, se preferir, pode usar a estilização que já está lá, e dessa forma seu projeto se parecerá com o projeto da imagem abaixo. Para isso, basta usar as `classes`e os `ids` indicados neste [documento do Figma](https://www.figma.com/file/QmSXGRYh4ygdOqCt9iYpA0/Super-Portf%C3%B3lio?type=design&node-id=0%3A1&mode=design&t=ItePvBriNEV4aBdX-1).

![Home page image](/assets/home-page.png)

</details>

---

# Requisitos obrigatórios

Você é uma pessoa desenvolvedora fullstack que já desenvolveu vários projetos enquanto estudava um conjunto de tecnologias específicas. Agora, sua atenção será direcionada para entrar para o mercado de trabalho e para isso, apresentar um portfólio com todos os seus projetos é algo importantíssimo. Seu objetivo aqui será desenvolver este portfólio com seu perfil, projetos, links importantes do seu LinkedIn e disponibilizá-lo para visualização por meio do deploy via Railway.

A seguir está o escopo de cada tarefa que te levará a conclusão do seu Super Portfólio! 🤩

## 1 - Implemente a autenticação com simple JWT

> <b>🍀 Dica:</b> Antes de iniciar a implementação da autenticação, certifique-se de que tanto o container Docker com o banco de dados quanto o servidor estão rodando.

<br />

<details>
  <summary>
    <b>✍️ Detalhes do requisito</b>
  </summary>

- Implemente a autenticação com **Simple JWT** no projeto para que somente pessoas logadas possam ter acesso a aplicação.
- Use a rota `token/` para a obtenção do Token JWT.
- Use a rota `token/refresh/` para a atualização do Token JWT.
- Use a rota `token/verify/` para a verificação do Token JWT.

</details>

<details>
  <summary>
    <b>🤖 O que será verificado pelo avaliador</b>
  </summary>

- Se ao usar credenciadas incorretas a autenticação falha.
- Se ao usar credenciadas corretas autenticação é bem sucedida.
- Se a rota de verificação de token está funcionando corretamente.
- Se a rota de atualização de token está funcionando corretamente.

</details>

## 2 - Inicie o app `projects` e crie um C.R.U.D para `Profile`

Inicie um app com o nome `projects` e crie um **C.R.U.D.** para o model `Profile`. Para isso, você deve criar as rotas, views e serializers necessários para que seja possível realizar as operações de C.R.U.D. para a model `Profile`.

> <b>🍀 Dica:</b> Os requisitos seguintes exigirão a criação de modelos. Lembre-se que sempre que criar/modificar um modelo, é necessário criar as migrações para espelhar as modificações para os bancos de dados, inclusive o banco de testes contam com estas modificações. O comando para gerar a migration a partir dos modelos criados é:

</b>

```bash
python3 manage.py makemigrations
```

<details>
  <summary>
    <b>✍️ Detalhes do requisito</b>
  </summary>
  <br />
  <details>
    <summary>
      <b>✍️ Model Profile</b>
    </summary>

- Crie a classe `Profile`.
- A classe `Profile` deve herdar os `models` do Django.
- A classe `Profile` deve ter as propriedades: `name`, `github`, `linkedin`, e `bio`.
- A propriedade `name` deve ser um campo de caracteres com um tamanho máximo de **100 caracteres**.
- As propriedades `github`, `linkedin` devem ser campos de **URL**.
- A propriedade `bio` deve ser um campo de texto sem tamanho máximo definido.
- As propriedades devem ser:
  - `name`: Campo de caracteres, com tamanho máximo de **100 caracteres**.
  - `github`: Campo de **URL**.
  - `linkedin`: Campo de **URL**.
  - `bio`: Campo de texto, sem tamanho máximo definido.
- As propriedades `name`, `github`, `linkedin`, e `bio` não devem aceitar informações vazias ou maiores que 500 caracteres.
- O método `__str__` da classe `Profile` deve retornar a propriedade `name` do perfil criado.

  </details>

<details>
  <summary>
    <b>✍️ Rotas </b>
  </summary>

As operações do C.R.U.D. devem ser acessadas apor meio da rota: `profiles/`, a partir da URL base `http://localhost:8000/`. Em que:

- A rota `profiles` deve aceitar requisições do tipo `GET` e retornar uma lista com todos os perfis cadastrados.
- A rota `profiles/` deve aceitar requisições do tipo `POST` e criar um novo perfil com as informações passadas.
- A rota `profiles/<id_do_perfil>` deve aceitar requisições do tipo `GET` e retornar o perfil com o `id` especificado.
- A rota `profiles/<id_do_perfil>/` deve aceitar requisições do tipo `PATCH` e atualizar o perfil com o `id` especificado.
- A rota `profiles/<id_do_perfil>/` deve aceitar requisições do tipo `DELETE` e deletar o perfil com o `id` especificado.

</details>

</details>

<details>
  <summary>
    <b>🤖 O que será verificado pelo avaliador</b>
  </summary>

- Se o app iniciado se chama `projects`.
- Se o app criado está devidamente instalado no `settings.py`.
- Se o endpoint `http://localhost:8000/profiles` existe.
- Se ao acessar a rota `profiles` devidamente autenticado será retornada uma lista completa com todos os perfis cadastrados.
- Se a rota `profiles` aceitar requisições do tipo `POST` e cria um novo perfil se a pessoa usuária estiver devidamente autenticada.
- Se a rota `profiles/<id_do_perfil>` aceita requisições do tipo `GET` e retorna o perfil com o `id` especificado,  se a pessoa usuária estiver devidamente autenticada.
- Se a rota `profiles/<id_do_perfil>/` aceita requisições do tipo `PATCH` e atualiza o perfil com o `id` especificado,  se a pessoa usuária estiver devidamente autenticada.
- Se a rota `profiles/<id_do_perfil>/` aceita requisições do tipo `DELETE` e deleta o perfil com o `id` especificado, se a pessoa usuária estiver devidamente autenticada.

</details>

## 3 - Crie um C.R.U.D para `Project`

Crie um **C.R.U.D.** para o model `Project`. Para isso, você deve criar as rotas, views e serializers necessários para que seja possível realizar as operações de C.R.U.D. para a model `Project`.

<details>
  <summary>
    <b>✍️ Detalhes do requisito</b>
  </summary>
  <br />
  <details>
    <summary>
      <b>✍️ Model Project</b>
    </summary>

- Crie a classe `Project`.
- A classe `Project` deve herdar os `models` do Django.
- A classe `Project` deve ter as propriedades: `name`, `description`, `github_url`, `keyword`, `key_skill` e `profile`.
- As propriedades `name`, `keywords` e `key_skill` devem ser campos de caracteres com um tamanho máximo de **50 caracteres**.
- A propriedade `description` deve ser um campo de texto com um tamanho máximo de **500 caracteres**.
- A propriedade `github_url` deve ser um campo de **URL**.
- A propriedade `profile` deve ser um campo de relacionamento com a classe `Profile`.
- As propriedades devem ser:
  - `name`: Campo de caracteres, com tamanho máximo de **50 caracteres**.
  - `description`: Campo de texto, , com tamanho máximo de **500 caracteres**.
  - `github_url`: Campo de **URL**.
  - `keyword`:  Campo de caracteres, com tamanho máximo de **50 caracteres**.
  - `key_skill`:  Campo de caracteres, com tamanho máximo de **50 caracteres**.
  - `profile`: Campo de chave estrangeira(_foreign key_) com a classe `Profile`.
- As propriedades `name`, `description`, `github_url`, `keywords` e `key_skills` não devem aceitar informações vazias ou maiores que 500 caracteres.
- O relacionamento presente em `profile` deve ser do tipo `1:N`, em que um perfil pode ter vários projetos.
- O método `__str__` da classe `Project` deve retornar a propriedade `name` do projeto criado.

> <b>🍀 Dicas:</b> Existe um tipo de campo específico pra URLs no Django. Para saber mais, acesse a [documentação](https://docs.djangoproject.com/en/3.2/ref/models/fields/#urlfield). 😉
  </details>

<details>
  <summary>
    <b>✍️ Rotas </b>
  </summary>

As operações do C.R.U.D. devem ser acessadas apor meio da rota: `projects/`, a partir da URL base `http://localhost:8000/`. Em que:

- As rotas `projects/` e `projects/<id_do_projeto>/` devem ser acessíveis apenas por pessoas usuárias autenticadas.
- A rota `projects/` deve aceitar requisições do tipo `GET` e retornar uma lista com todos os projetos cadastrados.
- A rota `projects/` deve aceitar requisições do tipo `POST` e criar um novo projeto com as informações passadas.
- A rota `projects/<id_do_projeto>/` deve aceitar requisições do tipo `GET` e retornar o projeto com o `id` especificado.
- A rota `projects/<id_do_projeto>/` deve aceitar requisições do tipo `PATCH` e atualizar o projeto com o `id` especificado.
- A rota `projects/<id_do_projeto>/` deve aceitar requisições do tipo `DELETE` e deletar o projeto com o `id` especificado.

</details>

</details>

<details>
  <summary>
    <b>🤖 O que será verificado pelo avaliador</b>
  </summary>

- Se o endpoint `http://localhost:8000/projects` existe.
- Se ao acessar a rota `projects` devidamente autenticado será retornada uma lista completa com todos os projetos cadastrados.
- Se a rota `projects` aceita requisições do tipo `POST` e cria um novo projeto se a pessoa usuária estiver devidamente autenticada.
- Se a rota `projects/<id_do_projeto>/` aceita requisições do tipo `GET` e retorna o projeto com o `id` especificado,  se a pessoa usuária estiver devidamente autenticada.
- Se a rota `projects/<id_do_projeto>/` aceita requisições do tipo `PATCH` e atualiza o projeto com o `id` especificado,  se a pessoa usuária estiver devidamente autenticada.
- Se a rota `projects/<id_do_projeto>/` aceita requisições do tipo `DELETE` e deleta o projeto com o `id` especificado, se a pessoa usuária estiver devidamente autenticada.

</details>

## 4 - Customize as ViewSets para `Profile`

Customize a ViewSet de `Profile` para que as rotas do tipo `GET` possam ser acessadas sem a necessidade de autenticação, renderizando diretamente um template com todas as informações pertinentes ao invés de haver retorno da API.

> <b>🍀 Dica:</b> Há como definir uma função dentro de uma ViewSet que dá diferentes permissões de acesso para diferentes métodos HTTP conforme o tipo de requisição. No caso deste requisito, por exemplo, o método GET é permitido para qualquer pessoa, enquanto os outros métodos (POST, PATCH e DELETE) requerem autenticação. Desta forma, a função que faz a diferenciação de permissões de acesso deve ser definida dentro da ViewSet pode ser definida da seguinte forma:

</b>

```python
    def get_permissions(self):
        if self.request.method == 'GET':
            return [AllowAny()]
        return [IsAuthenticated()]
```

<details>
  <summary>
    <b>✍️ Detalhes do requisito</b>
  </summary>

- Crie uma classe chamada `ProfileViewSet` em `projects/views.py`.
- Essa classe deve herdar de `ModelViewSet`.
- A classe `ProfileViewSet` deve ter uma função que exige autenticação a depender do método utilizado na requisição.
- As rotas do tipo `GET` podem ser acessadas sem a necessidade de autenticação, renderizando diretamente um template com todas as informações pertinentes.
- As rotas do tipo `POST`, `PATCH` e `DELETE` só podem ser acessadas por pessoas usuárias autenticadas.
- Utilize o método `retrieve` para exibir os detalhes de um perfil (_profile_), renderizando um template HTML com esses detalhes e informações relacionadas. Esse método deve verificar se a requisição é um `GET` e, se não for, chamar a implementação padrão de recuperação de detalhes usando `super().retrieve()`.
- Após recuperar o perfil, renderize um template HTML com o perfil. O template deve ser criado no caminho `projects/templates/profile_detail.html`.

> <b>🍀 Dica:</b> A função `retrieve` é chamada quando o Viewset recebe, entre outras possibilidades, a requisição `GET`. Customizando ela, conseguimos direcionar cada verbo HTTP para uma renderiza'ncção de dados diferente . Desta forma, você pode utilizar a função abaixo como base para desenvolver o que é solicitado:

</b>

```python
class ProfileViewSet(viewsets.ModelViewSet):
    # defina a queryset
    # defina a classe do serializer

    def get_permissions(self):
        if self.request.method == 'GET':
            return [AllowAny()]
        return [IsAuthenticated()]

    def retrieve(self, request, *args, **kwargs):
        if request.method == 'GET':
          # busque o id do perfil
          # crie uma variável para guardar esse perfil

            return render(
              # passe os parâmetros necessários para o template:
              # a requisição, o caminho do template e um dict com dados para o template
            )
        return super().retrieve(request, *args, **kwargs)
```

</details>

<details>
  <summary>
    <b>🤖 O que será verificado pelo avaliador</b>
  </summary>

- Se o endpoint `http://localhost:8000/profiles` existe.
- Se ao acessar a rota `profiles` mesmo sem autenticação será retornada uma lista completa com todos os perfis cadastrados.
- Se a rota `profiles/<id_do_perfil>/` aceita requisições do tipo `GET` e retorna o perfil com o `id` especificado.
- Se a rota `profiles` aceita requisições do tipo `POST` e cria um novo perfil se a pessoa usuária estiver devidamente autenticada.
- Se a rota `profiles/<id_do_perfil>/` aceita requisições do tipo `PATCH` e atualiza o perfil com o `id` especificado,  se a pessoa usuária estiver devidamente autenticada.
- Se a rota `profiles/<id_do_perfil>/` aceita requisições do tipo `DELETE` e deleta o perfil com o `id` especificado, se a pessoa usuária estiver devidamente autenticada.

</details>

## 5 - Crie um C.R.U.D inline para `Certificate` e `CertifyingInstitution`

Crie um **C.R.U.D.** inline para o model `Certificate` e `CertifyingInstitution`, para que em uma única requisição seja possível ver/criar as instituições certificadoras e seus respectivos certificados em uma única requisição. Para isso, você deve criar as rotas, views e serializers necessários para que seja possível realizar as operações de C.R.U.D. para as models `Certificate` e `CertifyingInstitution`.

> <b>🍀 Dica:</b> Para criar um C.R.U.D. inline, você deve herdar do `serializers.ModelSerializer` no serializer que conterá a outra entidade, para definir um atributo que contenha uma instância do serializer a ser contido. Neste momento você pode usar o argumento `(many=True)` para indicar que o campo de relacionamento representa vários objetos relacionados, ou seja, serializando várias certificações para uma instituição certificadora. Além disso, você deve sobrescrever a função `create` do serializer.

<details>
  <summary>
    <b>✍️ Detalhes do requisito</b>
  </summary>
  <br />
  <details>
    <summary>
      <b>✍️ Model CertifyingInstitution</b>
    </summary>

- Crie a classe `CertifyingInstitution`.
- A classe `CertifyingInstitution` deve herdar os `models` do Django.
- A classe `CertifyingInstitution` deve ter as propriedades: `name` e `url`.
- A propriedade `name` deve ser um campo de caracteres com um tamanho máximo de **100 caracteres**.
- A propriedade `url` deve ser um campo de **URL**.
- As propriedades `name` e `url` não devem aceitar informações vazias ou maiores que 500 caracteres.
- O método `__str__` da classe `CertifyingInstitution` deve retornar a propriedade `name` da instituição certificadora criada.

</details>

  <details>
    <summary>
      <b>✍️ Model Certificate</b>
    </summary>

- Crie a classe `Certificate`.
- A classe `Certificate` deve herdar os `models` do Django.
- A classe `Certificate` deve ter as propriedades: `name`, `certifying_institution`, `timestamp` e `profiles`.
- A propriedade `name` deve ser um campo de caracteres com um tamanho máximo de **100 caracteres**.
- A propriedade `certifying_institution` deve ser um campo de relacionamento de chave estrangeira com a classe `CertifyingInstitution`.
- A propriedade `timestamp` deve ser um campo de data e hora preenchido automaticamente no momento de sua criação.
- A propriedade `profiles` deve ser um campo de relacionamento do tipo `ManyToMany` com a classe `Profile` com o atributo `related_name` definido como `certificates`.
- As propriedades `name`, `certifying_institution`, `timestamp`, e `profiles` não devem aceitar informações vazias ou maiores que 500 caracteres.
- O método `__str__` da classe `Certificate` deve retornar a propriedade `name` do certificado criado.
  </details>

<details>
  <summary>
    <b>✍️ Rotas </b>
  </summary>

As operações do C.R.U.D. devem ser acessadas apor meio das rotas: `certificates/`, e `certifying-institutions/` a partir da URL base `http://localhost:8000/`. Em que:

- As rotas `certificates/` e `certificates/<id_do_certificado>/` devem ser acessíveis apenas por pessoas usuárias autenticadas.
- A rota `certificates/` deve aceitar requisições do tipo `GET` e retornar uma lista com todos os certificados cadastrados.
- A rota `certificates/` deve aceitar requisições do tipo `POST` e criar um novo certificado com as informações passadas.
- A rota `certificates/<id_do_certificado>/` deve aceitar requisições do tipo `GET` e retornar o certificado com o `id` especificado.
- A rota `certificates/<id_do_certificado>/` deve aceitar requisições do tipo `PATCH` e atualizar o certificado com o `id` especificado.
- A rota `certificates/<id_do_certificado>/` deve aceitar requisições do tipo `DELETE` e deletar o certificado com o `id` especificado.

- As rotas `certifying-institutions/` e `certifying-institutions/<id_da_instituição-certificadora>/` devem ser acessíveis apenas por pessoas usuárias autenticadas.
- A rota `certifying-institutions/` deve aceitar requisições do tipo `GET` e retornar uma lista com todas as instituições certificadoras cadastradas.
- A rota `certifying-institutions/` deve aceitar requisições do tipo `POST` e criar uma nova instituição certificadora com as informações passadas. Essa instituição deve conter pelo menos um certificado para ser criada.
- A rota `certifying-institutions/<id_da_instituição-certificadora>/` deve aceitar requisições do tipo `GET` e retornar a instituição certificadora com o `id` especificado.
- A rota `certifying-institutions/<id_da_instituição-certificadora>/` deve aceitar requisições do tipo `PATCH` e atualizar a instituição certificadora com o `id` especificado. **Não é necessário** que as atualizações possam ser inline também.
- A rota `certifying-institutions/<id_da_instituição-certificadora>/` deve aceitar requisições do tipo `DELETE` e deletar a instituição certificadora com o `id` especificado.

</details>

</details>

<details>
  <summary>
    <b>🤖 O que será verificado pelo avaliador</b>
  </summary>

- Se o endpoint `http://localhost:8000/certificates/` existe.
- Se ao acessar a rota `certificates` devidamente autenticado será retornada uma lista completa com todos os certificados cadastrados.
- Se a rota `certificates` aceita requisições do tipo `POST` e cria um novo certificado se a pessoa usuária estiver devidamente autenticada.
- Se a rota `certificates/<id_do_certificado>/` aceita requisições do tipo `GET` e retorna o certificado com o `id` especificado,  se a pessoa usuária estiver devidamente autenticada.
- Se a rota `certificates/<id_do_certificado>/` aceita requisições do tipo `PATCH` e atualiza o certificado com o `id` especificado,  se a pessoa usuária estiver devidamente autenticada.
- Se a rota `certificates/<id_do_certificado>/` aceita requisições do tipo `DELETE` e deleta o certificado com o `id` especificado, se a pessoa usuária estiver devidamente autenticada.

- Se o endpoint `http://localhost:8000/certifying-institutions/` existe.
- Se ao acessar a rota `certifying-institutions` devidamente autenticado será retornada uma lista completa com todos os certificados cadastrados.
- Se a rota `certifying-institutions` aceita requisições do tipo `POST` e cria uma nova instituição certificadora se a pessoa usuária estiver devidamente autenticada.
- Se a rota `certifying-institutions/<id_da_instituição-certificadora>/` aceita requisições do tipo `GET` e retorna a instituição certificadora com o `id` especificado,  se a pessoa usuária estiver devidamente autenticada.
- Se a rota `certifying-institutions/<id_da_instituição-certificadora>/` aceita requisições do tipo `PATCH` e atualiza a instituição certificadora com o `id` especificado,  se a pessoa usuária estiver devidamente autenticada.
- Se a rota `certifying-institutions/<id_da_instituição-certificadora>/` aceita requisições do tipo `DELETE` e deleta a instituição certificadora com o `id` especificado, se a pessoa usuária estiver devidamente autenticada.

</details>

## 6 - Exibir uma página de perfil completa

O template de `Profile` deve ser atualizado para que seja possível visualizar todas as informações de um perfil, incluindo seus certificados e instituições certificadoras.

> <b>🍀 Dica:</b> Para que seja possível exibir também os certificados, você precisará alterar a função `retrieve`, nas views.

<details>
  <summary>
    <b>✍️ Detalhes do requisito</b>
  </summary>

- Ao acessar um perfil, deve ser possível visualizar os certificados e instituições certificadoras de um perfil.

</details>

<details>
  <summary>
    <b>🤖 O que será verificado pelo avaliador</b>
  </summary>

- Se ao acessar um perfil é ser possível visualizar os certificados e instituições certificadoras dele.
  - O **projeto** deve ter seu nome, habilidade-chave e palavra-chave exibidas.
  - O **certificado** deve exibir seu nome e o nome de sua instituição certificadora.

</details>

---

# Requisito não avaliativo

## 7. Faça o deploy de seu projeto Django

Para que seu projeto esteja acessível e pronto para ser visualizado por pessoas de recrutamento, fazer deploy dele pode ser um grande diferencial. Lembre-se que sempre que precisar, você pode consultar o material sobre **deploy com Django** do curso. 😉
