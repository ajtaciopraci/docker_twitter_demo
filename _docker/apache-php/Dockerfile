FROM php:8.0-apache

RUN apt update && \
    apt install -y git pkg-config

RUN apt-get -y --no-install-recommends install cmake make git gcc g++ libbz2-dev libstxxl-dev libstxxl1v5 libxml2-dev wget \
    libzip-dev libboost-all-dev lua5.2 liblua5.2-dev freetds-dev libtbb-dev -o APT::Install-Suggests=0 -o APT::Install-Recommends=0

RUN apt-get install -y libmcrypt-dev \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev \
    libxml2-dev \
    libedit-dev \
    libicu-dev \
    libssl-dev \
    freetds-dev \
    libc-client-dev \
    libkrb5-dev \
    curl \
    libcurl3-dev \
    openssl \
    libonig-dev

RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libmcrypt-dev libxml2-dev

RUN docker-php-ext-install mbstring
RUN docker-php-ext-install curl




RUN a2enmod rewrite


RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin/ --filename=composer

