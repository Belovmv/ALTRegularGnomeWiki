---
title: Figma
appstreamFlatpak: io.github.Figma_Linux.figma_linux
---

# Figma

Figma — неофициальная версия Figma для Linux построенная на Electron.

## Установка c помощью Flatpak <Badge type="danger" text="Неофициальная сборка" />

При наличии пакета [Flatpak](/flatpak), можно установить **Figma** одной командой:

```shell
flatpak install flathub io.github.Figma_Linux.figma_linux
```

<!--@include: ./parts/install/software-flatpak.md-->

<!--@include: ./parts/warns/unpriveleged-spases.md -->

## Установка c помощью epm play <Badge type="danger" text="Неофициальная сборка" />

При наличии пакета [eepm](/epm), можно установить **Figma** одной командой:

```shell
epm play figma
```

## Установка из репозитория GitHub

Загрузите пакет `.rpm` со страницы релизов приложения `figma-linux` сервиса Github, затем установите через терминал: 

::: code-group

```shell[apt-get]
su -
cd ../home/`USER`/Загрузки
apt-get update
apt-get install figma-linux-*.x86_64.rpm
```
```shell[epm]
сd Загрузки
epm -i figma-linux-*.x86_64.rpm
```
:::

`USER` — имя вашего пользователя.