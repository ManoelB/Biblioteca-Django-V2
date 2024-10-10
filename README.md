

# Sistema de Gerenciamento de Biblioteca

Este é um sistema de gerenciamento de biblioteca desenvolvido como parte da Trilha 7 - Desenvolvimento Back-End (Python) do programa Residência em TIC36. Ele permite a administração de livros, autores e categorias, com funcionalidades como listagem, criação, edição e exclusão de registros. Além disso, o sistema oferece recursos de paginação, ordenação e busca de registros utilizando Django, Django Rest Framework e Django Filter.

##Objetivo
. Reimplementar as views utilizando class-based views.
. Adicionar recursos de paginação de resultados, ordenação e busca de termos.
. Criar um repositório público no GitHub para a submissão do exercício.


## Desenvolvido por:
- Manoel Barbosa da Silva Filho

## Funcionalidades
- **Administração de Livros, Autores e Categorias**: Listar, criar, editar e excluir livros, autores e categorias.
- **Paginação**: Listagem de resultados com paginação (limite e offset).
- **Ordenação**: Ordenação dos registros por atributos específicos, como título e autor.
- **Busca**: Busca de registros por título, autor ou categoria.

## Tecnologias Abordadas:
- **Python**
- **Django**
- **Django Rest Framework**
- **Django Filter**
- **SQLite** (banco de dados padrão do Django para desenvolvimento)

## Instalação

### Passo 1: Clonar o repositório

```bash
git clone https://github.com/Gutis-007/OrmPratica.git
cd OrmPratica
```

### Passo 2: Criar um ambiente virtual

```bash
python -m venv venv
```

### Passo 3: Ativar o ambiente virtual

- **Windows**:

  ```bash
  .\venv\Scripts\activate
  ```

- **Linux/macOS**:

  ```bash
  source venv/bin/activate
  ```

### Passo 4: Instalar as dependências

```bash
pip install -r requirements.txt
```

### Passo 5: Migrar o banco de dados

Após a instalação das dependências, você precisa aplicar as migrações para configurar o banco de dados:

```bash
python manage.py migrate
```

### Passo 6: Popular o banco de dados com dados de exemplo

Para criar dados de exemplo (livros, autores e categorias), execute o seguinte comando:

```bash
python manage.py populate_db
```

> **Nota**: Esse comando deve ser executado apenas uma vez, pois ele insere registros no banco de dados.

### Passo 7: Executar o servidor de desenvolvimento

Agora, você pode iniciar o servidor localmente:

```bash
python manage.py runserver
```

A aplicação estará disponível no navegador no endereço [http://127.0.0.1:8000](http://127.0.0.1:8000).

## Endpoints da API

### Livros

- **Listar livros (com paginação e ordenação):**
  ```
  GET /livros/?limit=<limite>&offset=<deslocamento>&ordering=<campo>
  ```

- **Buscar livros por título, autor ou categoria:**
  ```
  GET /livros/?titulo=<termo>&autor=<termo>&categoria=<termo>
  ```

- **Criar um novo livro:**
  ```
  POST /livros/
  ```

- **Obter detalhes de um livro específico:**
  ```
  GET /livros/<id>/
  ```

- **Atualizar um livro:**
  ```
  PUT /livros/<id>/
  ```

- **Excluir um livro:**
  ```
  DELETE /livros/<id>/
  ```

### Autores

- **Listar autores:**
  ```
  GET /autores/
  ```

- **Criar um novo autor:**
  ```
  POST /autores/
  ```

### Categorias

- **Listar categorias:**
  ```
  GET /categorias/
  ```

- **Criar uma nova categoria:**
  ```
  POST /categorias/
  ```









https://github.com/ManoelB/Biblioteca-Django-V2/tree/master
