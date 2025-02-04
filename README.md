Cria uma pasta com o nome do projeto

```bash
$ mkdir projetodjango
```

Entre no diretorio e crie um ambiente virtual

```bash
$ cd projetodjango
$ python3 -m venv .venv
```

Ative o ambiente virtual

```bash
$ source .venv/bin/activate
```

Crie um arquivo requirements.txt, adicione as dependencias necessarias e execute o arquivo

```textile
django==3.1.12
djongo==1.3.7
setuptools
```

```bash
$ pip3 install -r requirements.txt
```

volte para o diretorio anterior

```bash
$ cd ..
```

Execute o comando para criar um aplicativo de configuração e orquestração dentro do diretorio projetodjango

```bash
$ django-admin startproject aplicativoconfig projetodjango
```

Entre no diretorio projetodjango e execute o servidor, para verificar se o projeto Django está funcionando

```bash
$ cd projetodjango
$ python manage.py runserver
```

Para criar aplicativo dentro do diretorio projetodjango

```bash
$ python manage.py startapp aplicativo
```
