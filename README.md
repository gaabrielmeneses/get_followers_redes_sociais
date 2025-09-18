# get\_followers\_redes\_sociais

Este repositório contém scripts em Python para obter a contagem de seguidores e curtidas de perfis em diferentes redes sociais, incluindo **Facebook**, **Twitter** e **Instagram**.

## Funcionalidades

* Obter o número de **seguidores no Facebook**.
* Obter o número de **curtidas no Facebook**.
* Obter o número de **seguidores no Twitter**.
* Obter o número de **seguidores no Instagram**.

## Pré-requisitos

Antes de rodar o código, você precisa ter instalado:

* Python 3.x
* Bibliotecas Python:

  ```bash
  pip install requests beautifulsoup4 tweepy lxml
  ```

## Configuração

1. **Twitter API**:
   Para usar a função `get_twitter_followers`, é necessário ter credenciais da API do Twitter (`API Key`, `API Secret Key`, `Access Token`, `Access Token Secret`) e substituí-las no script:

   ```python
   auth = tweepy.OAuthHandler('API_KEY', 'API_SECRET_KEY')
   auth.set_access_token('ACCESS_TOKEN', 'ACCESS_TOKEN_SECRET')
   ```

2. **Usuário alvo**:
   Defina o usuário das redes sociais que você deseja consultar:

   ```python
   user = 'nome_do_usuario'
   url_face = 'https://www.facebook.com/' + user
   url_insta = 'https://www.instagram.com/' + user
   ```

## Como usar

Basta executar o script Python para obter a contagem de seguidores:

```python
num_seguidores_face = get_facebook_followers(url_face)
num_seguidores_twitter = get_twitter_followers(user)
num_seguidores_instagram = get_instagram_followers(url_insta)

print("Facebook:", num_seguidores_face)
print("Twitter:", num_seguidores_twitter)
print("Instagram:", num_seguidores_instagram)
```

## Observações

* O scraping do **Facebook** e **Instagram** pode parar de funcionar caso o site altere o HTML ou as APIs públicas.
* Para **Twitter**, é necessário manter as credenciais de API atualizadas.
* Esse código é apenas para fins educativos e pessoais; respeite as políticas de uso das redes sociais.

## Licença

Este projeto está aberto para uso livre, sem restrições específicas.
