FROM php:8.1-fpm

# Устанавливаем необходимые пакеты и утилиты
RUN apt-get update && apt-get install -y \
    git \
    zip \
    unzip \
    && rm -rf /var/lib/apt/lists/*

# Устанавливаем Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Указываем рабочую директорию внутри контейнера
WORKDIR /var/www/html
