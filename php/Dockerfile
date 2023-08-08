FROM php:8.1-fpm

# Устанавливаем необходимые пакеты и утилиты
RUN apt-get update && apt-get install -y \
    git \
    zip \
    unzip \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Устанавливаем Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Устанавливаем расширение PDO для работы с MySQL
RUN docker-php-ext-install pdo pdo_mysql

# Устанавливаем расширение PDO для работы с PostgreSQL
RUN docker-php-ext-install pdo pdo_pgsql

# Указываем рабочую директорию внутри контейнера
WORKDIR /var/www/html
