# MPV

MPV — Свободный легковесный кроссплатформенный медиаплеер. Поддерживает множество форматов медиафайлов и субтитров.

![Draw attention to the window](/mpv/mpv.png)


## Установка из репозитория 

**MPV** можно установить через терминал:

::: code-group

```shell[apt-get]
su -
apt-get update
apt-get install mpv
```

```shell[epm]
epm -i mpv
```
::: 

## Установка c помощью Flatpak

При наличии пакета [Flatpak](/flatpak), можно установить **Mpv** одной командой:

```shell
flatpak install flathub io.mpv.Mpv
```

## Проблемы с замедлением видео

При просмотре некоторых видео, особенно 4к, возможно замедление видеопотока, при этом звуковая дорожка идет без опозданий. Для выхода из этой ситуации существует два варианта.

1. Использование профиля fast, для этого в терминале видео необходимо запустить с использование профиля fast

```shell
mpv --profile=fast video.mp4
```

2. Использование аппаратного декодирования. Для этого в файле настроек **mpv.conf** необходимо прописать **hwdec** и **vo**

Для сессии X.org рекомендуется

```
hwdec=vaapi
vo=gpu-next
```

Для сессии Wayland рекомендуется

```
hwdec=vaapi
vo=dmabuf-wayland
```

## Проблемы с "потуханием" экрана при просмотре видео 

Для решения это проблемы существует два решения:

1. В сессии X.org должно быть достаточно добавления одной опции в **mpv.conf**

```
stop-screensaver
```

В сессии Wayland сложнее, учитывая что MPV не совсем поддерживает wayland, то вышеописанная опция работать не будет.
Видео нужно запускать с учетом **gnome-session-inhibit**

```shell
gnome-session-inhibit mpv video.mp4
```

Для этого можно прямо указать, как написано выше, либо заходим в **/usr/share/applications/mpv.desktop** и после **Exec=** перед **mpv**  пишем **gnome-session-inhibit** 

2. Более простое решение

:::info
Ниже вариант предпочтительный
:::

Устанавливаем расширение для Gnome - Caffeine

::: code-group

```shell[apt-get]
su -
apt-get update
apt-get install gnome-shell-extension-caffeine
```

```shell[epm]
epm -i gnome-shell-extension-caffeine
```

Затем нужно перезапустить сессию и не забыть включить Caffeine