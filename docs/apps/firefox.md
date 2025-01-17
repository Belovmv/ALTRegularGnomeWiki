---
title: Firefox
appstreamRepo: org.mozilla.firefox
appstreamFlatpak: org.mozilla.firefox
---


# Firefox

Firefox — популярный графический веб-браузер с открытым исходным кодом, разрабатываемый Mozilla.

## Установка из репозитория 

**Firefox** можно установить любым привычным и удобным способом:

<!--@include: ./parts/install/software-repo.md-->

**Установка через терминал**

::: code-group

```shell[apt-get]
su -
apt-get update
apt-get install firefox
```
```shell[epm]
epm -i firefox
```
:::


## Установка c помощью Flatpak

При наличии пакета [Flatpak](/flatpak), можно установить **Firefox** одной командой:

```shell
flatpak install flathub org.mozilla.firefox
```

<!--@include: ./parts/install/software-flatpak.md-->
<!--@include: ./parts/warns/unpriveleged-spases.md -->

## Установка с помощью Snaps

При наличии пакета [snapd](/snap), можно установить **Firefox** одной командой:

```shell
snap install firefox
```

## Firefox Gnome theme

Склонируйте скрипт и установите **Firefox GNOME theme**:

```shell
git clone https://github.com/rafaelmardojai/firefox-gnome-theme 
cd firefox-gnome-theme
./scripts/auto-install.sh
```

## Издания Firefox

**Firefox Extended Support Release** — версия с длительным сроком поддержки для комплексной безопасности и защиты данных.

**Firefox Beta** — нестабильная платформа для тестирования и разработки. По умолчанию Бета отправляет данные в Mozilla, а иногда и нашим партнерам, чтобы помочь нам справиться с проблемами и попробовать идеи

**Firefox Developer Edition** — нестабильная платформа для тестирования и разработки. По умолчанию Developer Edition отправляет данные в Mozilla, а иногда и нашим партнерам, чтобы помочь нам справиться с проблемами и попробовать идеи.

**Firefox Nightly** — нестабильная платформа для тестирования и разработки. По умолчанию Nightly отправляет данные в Mozilla, а иногда и нашим партнерам, чтобы помочь нам справиться с проблемами и попробовать идеи.