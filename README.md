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
django==
djongo==
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

Abra o arquivo settings.py na pasta projetodjango/aplicativoconfig para configurar banco de dados, lingua, formato da data, fuso horario e email

Comente a variavel DATABASES e adicione o seguinte codigo

```python
DATABASES = {
    'default':{
        'ENGINE':'djongo',
        'NAME':'name',
        'ENFORCE_SCHEMA': False,
        'CLIENT':{
            'host':'mongodb://0.0.0.0:27017/',
        }
    }
}
```

Defina o idioma

```python
LANGUAGE_CODE = 'pt-br'
```

Defina o formato da data

```python
DATE_INPUT_FORMATS = ('%d/%m/%Y')
```

Defina o fuso horario

```python
TIME_ZONE = 'America/Sao_Paulo'
```

Defina o teste com mensagens de e-mail que seriam enviadas no console

```python
EMAIL_BACKEND = 'django.core.mail.backends.console.EmailBackend'
```

Agora aplique as migrações do banco de dados

```bash
python3 manage.py makemigrations
python3 manage.py migrate
```
