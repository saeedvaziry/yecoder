---
title: 'Create simple broadcast for Laravel and Livewire without using websockets'
date: '2023-08-12T10:31:00+00:00'
author: Saeed Vaziry
layout: post
url: /posts/create-simple-broadcast-for-laravel-and-livewire-without-using-websockets
draft: true
categories:
    - PHP
    - Livewire
    - Laravel
    - Websockets
    - Broadcasting
tags:
    - php
    - laravel
    - livewire
    - websockets
    - broadcasting
---

Sometimes you have small applications and you don't want to spend more on the servers or make it complex by setting up a socket server for realtime updates on the application. In these cases it makes sense to pull the data every couple of seconds and give the realtime feeling to the users.

In this post I will show you how you can make it happen with Laravel and Livewire in the easiest way! So bear with me until the end of this post :)

