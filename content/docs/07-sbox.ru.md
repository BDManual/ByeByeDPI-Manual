---
title: SberBOX/SlimBox
weight: 7
---

## Определение устройства

### Устройства на Android 9

- SberBox:
  - SBDV-00001, SBDV-00002 (все модификации)
  - SBDV-00004, SBDV-00004C
- OKKO SmartBox (с прошивкой SberBox)
- SberBoxTime
- SberBoxTop
- SberPortal
- Sber TV (кроме моделей на Android 13)

### Устройства на Android 13

- SBDV-00004V (обновленный)
- SBDV-00004Р (обновленный)
- SBDV-00005
- SBDV-00006 (SberBox 2)

## Инструкции по настройке

### Инструкция для Android 13

> ⚠️ На этих устройствах работает только подключение через компьютер

#### Включение режима разработчика

- Откройте настройки Android
- Перейдите: Настройки устройства → Об устройстве
- Найдите **Сборка ОС** и нажмите на этот пункт несколько раз до появления сообщения об активации режима разработчика
- Вернитесь назад и перейдите в **Для разработчиков**
- Включите **Отладка по Wi-Fi**
- Запомните показанные *IP-адрес* и *порт*

#### Подключение через ADB AppControl

- Установите [ADB AppControl](https://adbappcontrol.com/ru/#download) на компьютер
- Введите *IP-адрес* и *порт* из настроек устройства
- Нажмите на значок **Wi-Fi** для подключения
- На вкладке **Консоль** выполните команды:

```
  shell pm grant io.github.romanvht.byedpi android.permission.WRITE_SECURE_SETTINGS
  shell appops set io.github.romanvht.byedpi WRITE_SETTINGS allow
  shell appops set io.github.romanvht.byedpi ACTIVATE_VPN allow
```

### Инструкция для Android 9

#### Подготовка через Sber Studio

- Войдите на [developers.sber.ru/studio](https://developers.sber.ru/studio/settings/devices) с вашим Сбер ID
- Нажмите "**+ добавить**" и укажите:
- Серийный номер (16 символов из настроек), Учтите: все буквы заглавные, O - это цифра 0
- Тип устройства (для OKKO выберите "OKKO Smart Box")
- Включите **функция ADB**

#### 2А. Через ADB TV (простой способ)

- Установите [ADB TV](https://adbappcontrol.com/tv/download/?r=latest&lang=ru)
- На вкладке **Консоль** выполните:

```
  pm grant io.github.romanvht.byedpi android.permission.WRITE_SECURE_SETTINGS
  appops set io.github.romanvht.byedpi WRITE_SETTINGS allow
  appops set io.github.romanvht.byedpi ACTIVATE_VPN allow
```

#### 2Б. Через компьютер

- Установите [ADB AppControl](https://adbappcontrol.com/ru/#download)
- Введите *IP-адрес* устройства и *порт* 5555
- На вкладке **Консоль** выполните:

```
  shell pm grant io.github.romanvht.byedpi android.permission.WRITE_SECURE_SETTINGS
  shell appops set io.github.romanvht.byedpi WRITE_SETTINGS allow
  shell appops set io.github.romanvht.byedpi ACTIVATE_VPN allow
```

## Решение проблем

### ADB не включается:

- Проверьте *тип устройства* и *серийный номер*
- Убедитесь, что устройство в сети
- Проверьте *Сбер ID*

### Проблемы подключения:

- Проверьте *IP-адрес* (может меняться)
- Устройства должны быть в одной сети
- Проверьте настройки роутера

## Альтернативный метод для YouTube

### Настройка ByeByeDPI

- В ByeByeDPI:
  - Настройки (шестеренка справа вверху)
    - Режим : *Proxy*
    - Порт: *1080*
  - На главном экране нажмите большую кнопку **Старт**

### Настройка SmartTube

- Установите вариант **arm64_v8a** [SmartTube](https://github.com/yuliskov/SmartTube/releases/latest)
- В настройках SmartTube:
  - Общие → Интернет-цензура
  - Включите "Использовать веб-прокси"
    - Имя: *127.0.0.1*
    - Порт: *1080*
    - Тип: *SOCKS*
  - Нажмите **Тест** и **ОК**