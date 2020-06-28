<p align="center" class="text-center" style="text-align:center;"><a href="https://github.com/i9w3b" target="_blank"><img src="https://cdn.jsdelivr.net/gh/i9w3b/cdn/img/logo-200px.png" width="200"></a></p>
<p align="center" class="text-center" style="text-align:center;">
<a href="https://github.com/i9w3b/dev-master/blob/master/LICENSE.md"><img src="https://img.shields.io/github/license/i9w3b/dev-master" alt="License"></a>
<a href="https://github.com/i9w3b/dev-master"><img src="https://img.shields.io/github/languages/count/i9w3b/dev-master" alt="GitHub Language Count"></a>
<a href="https://github.com/i9w3b/dev-master"><img src="https://img.shields.io/github/repo-size/i9w3b/dev-master" alt="GitHub Repo Size"></a>
<a href="https://github.com/i9w3b/dev-master/releases"><img src="https://img.shields.io/github/v/release/i9w3b/dev-master" alt="GitHub Release"></a>
<a href="https://packagist.org/packages/i9w3b/dev-master"><img alt="Packagist Downloads" src="https://img.shields.io/packagist/dt/i9w3b/dev-master"></a>
</p>

# DevMaster

Dependências para automatizar e gerenciar ambiente de desenvolvimento Laravel

## Estrutura

```bash
├── composer.json
├── LICENSE.md
└── README.md
```

## Instalação

Execute o seguinte comando:

```bash
composer require i9w3b/dev-master --dev
```

Para criar as configurações padrão de autenticação caso ainda não tenha execute:

```bash
php artisan ui bootstrap --auth
```

Variações do comando acima (bootstrap, vue, react)

Em seguida, você deve publicar os ativos do pacote web-tinker executando os comandos:

```bash
php artisan web-tinker:install
php artisan vendor:publish --provider="Spatie\WebTinker\WebTinkerServiceProvider" --tag="config"
```

Agora irá conseguir acessar a rota http://seu_projeto/tinker

Para configurar o Telescope deve primeiro configurar o arquivo `.env` com as configurações do banco de dados.

Publicando os ativos do pacote Telescope executando os comandos:

```bash
php artisan telescope:install
php artisan migrate
```

Agora irá conseguir acessar a rota http://seu_projeto/telescope

Alterar  os comandos:

```bash
php artisan telescope:install
php artisan migrate
```

Subistituir as visualizações (welcome, home) e o layout app.blade.php
Execute o seguinte comando:
```bash
php artisan vendor:publish --tag=devmaster-view
```

Ou se deseja somente subistituir o layout app.blade.php
Execute o seguinte comando:

```bash
php artisan vendor:publish --tag=devmaster-view-layouts
```

## Segurança

Caso descubra algum problema relacionado à segurança, envie um e-mail para `marcelosenaonline@gmail.com` em vez de usar o rastreador de problemas.

## Licença

[MIT](https://github.com/i9w3b/dev-master/blob/master/LICENSE.md) © [i9W3b](https://github.com/i9w3b) | Consulte [LICENSE.md](https://github.com/i9w3b/dev-master/blob/master/LICENSE.md) para obter mais informações.