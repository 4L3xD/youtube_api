# youtube_api

## 1. Criar credencial Youtube
Ref: https://developers.google.com/youtube/registering_an_application?hl=pt
1. [https://console.cloud.google.com/apis/library/youtube.googleapis.com](https://console.cloud.google.com/apis/library/youtube.googleapis.com?project=quickstart-1614639971971)
2. [https://console.cloud.google.com/apis/credentials](https://console.cloud.google.com/apis/credentials?hl=pt&project=quickstart-1614639971971&folder=&organizationId=)
    1. Criar credencial do tipo **Client Desktop**
    2. Fazer download do json na pasta do projeto
    3. Renomear o json para `client_secrets.json`

## 2. Instalar dependências do projeto
### A serem instaladas
- [https://pypi.org/project/httplib2/](https://pypi.org/project/httplib2/)
- [https://pypi.org/project/apiclient/](https://pypi.org/project/apiclient/)
- [https://pypi.org/project/oauth2client/](https://pypi.org/project/oauth2client/)

1. Criar requirements.txt com as seguintes libs

```python
apiclient==1.0.4
cachetools==4.2.2
certifi==2021.5.30
charset-normalizer==2.0.5
google-api-core==2.0.1
google-api-python-client==2.21.0
google-auth==2.1.0
google-auth-httplib2==0.1.0
googleapis-common-protos==1.53.0
httplib2==0.19.1
idna==3.2
oauth2client==4.1.3
protobuf==3.18.0
pyasn1==0.4.8
pyasn1-modules==0.2.8
pyparsing==2.4.7
requests==2.26.0
rsa==4.7.2
six==1.16.0
uritemplate==3.0.1
urllib3==1.26.6
```

1. Instalar requirements.txt

```python
python3 -m pip install -r requirements.txt
```

1. Substituir no script `apiclient` para `googleapiclient`

### Padrão do sistema
- [https://docs.python.org/2/library/httplib.html](https://docs.python.org/2/library/httplib.html)
1. deve ser chamada como `import http.client`
2. substituir o nome em todos os pontos do código

    `CTRL` + `F`
    Substituir: `httplib`

    Para: `http.client`

- [https://docs.python.org/3/library/os.html](https://docs.python.org/3/library/os.html)
- [https://docs.python.org/3/library/random.html](https://docs.python.org/3/library/random.html)
- [https://docs.python.org/3/library/sys.html](https://docs.python.org/3/library/sys.html)
- [https://docs.python.org/3/library/time.html](https://docs.python.org/3/library/time.html)

## 3. Adaptar script para python3
1. Adicionar parênteses nos `print`
2. Em todos os campos `except HttpError, e:` substituir a vírgula por `as`

## 4. Verificação de telefone para acesso de recursos
https://www.youtube.com/verify

## 5. Entendendo oauth2
https://python-oauth2.readthedocs.io/en/latest/

### Quando você instala manualmente suas libs:
*Adiciona as dependências do projeto em um arquivo txt chamado requirements*
pip freeze > requirements.txt
