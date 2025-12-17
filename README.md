# contact-form

## 環境構築

- リポジトリをクローン  
  git clone git@github.com:e-misora/fortify-test.git  
  cd fortify-test
- docker のビルド 起動  
  docker-compose up -d --build
- 環境変数を設定  
  cd src  
  cp .env.example .env  
  .env ファイルを編集して必要な値を設定

  ```bash:.env
  DB_HOST=mysql
  DB_DATABASE=laravel_db
  DB_USERNAME=laravel_user
  DB_PASSWORD=laravel_pass
  ```

- Laravel パッケージのインストール  
  docker-compose exec php bash  
  composer install
- アプリケーションを実行するためのキーを作成  
  docker-compose exec php bash  
  php artisan key:generate
- マイグレーション実行  
  docker-compose exec php bash  
  php artisan migrate
- シーディング実行  
  docker-compose exec php bash  
  php artisan db:seed

## 使用技術（実行環境）

- php:
- Laravel:
- MySQL:8.0.26
- nginx:1.21.1

## URL

- お問い合わせフォーム  
  http://localhost
- ユーザー登録画面  
  http://localhost/register
