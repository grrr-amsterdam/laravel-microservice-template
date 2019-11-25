# Laravel microservice template

This is a template repo for microservices running on AWS Lambda.

----------------------------------

## Installation

Install dependencies:

```
$ composer install
$ yarn install
```

Create a `.env` file, based on `.env.example`.

## API

Run a local server using

```
$ php artisan serve
```

## Deploy

You can use stages to deploy to `development`, `staging` and `production` (default: `development`).

### Prerequisites

1. You have the AWS cli tool installed.
2. You have configured a profile for this service.
3. You have created `.env.staging` and `.env.production` files, based on `.env.example`.
4. Make sure the value for `AWS_PROFILE` in the applicable `.env` file corresponds to the profile you created in step 2.

### Deploy staging

```
$ npx serverless deploy --stage staging --env staging 
```

### Deploy production

```
$ npx serverless deploy --stage production --env production 
```

Serverless will print the HTTP endpoints to the screen.

## Stack

Build on [Laravel](https://laravel.com) and [Bref](https://bref.sh), deployed using [Serverless framework](http://serverless.com/).

