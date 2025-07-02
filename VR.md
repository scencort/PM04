Вам нужно выполнить установку VR-ready рабочей станции на чистой Ubuntu, на которой ещё ничего не настроено. Вот пошаговая инструкция, как это сделать:

---

## 1. Обновите систему

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y git curl wget build-essential
```

---

## 2. Установите графические драйверы

### Если у вас видеокарта NVIDIA:

```bash
sudo ubuntu-drivers autoinstall
sudo reboot
```

---

## 3. Установите SteamVR (для тестирования VR-оборудования)

```bash
sudo add-apt-repository multiverse
sudo apt update
sudo apt install -y steam
```
- Запустите Steam, войдите в аккаунт и установите SteamVR через магазин.

---

## 4. Установите Unity Hub (интегрированная среда разработки с поддержкой VR/AR)

```bash
wget https://public-cdn.cloud.unity3d.com/hub/prod/UnityHub.AppImage
chmod +x UnityHub.AppImage
./UnityHub.AppImage
```
- В Unity Hub установите версию Unity с поддержкой VR (например, 2022.x).
- В процессе установки выберите компоненты под Linux + поддержку Android/Windows (если нужны билды под них).

---

## 5. Установите SDK для VR/AR-шлема

- Для Oculus/Meta Quest: скачайте [Oculus Integration](https://developer.oculus.com/downloads/package/unity-integration/)
- Для HTC Vive: установите SteamVR Plugin из Unity Asset Store.
- Для HoloLens: скачайте [Mixed Reality Toolkit (MRTK)](https://github.com/microsoft/MixedRealityToolkit-Unity)
- Для других шлемов — SDK ищите на сайте производителя.

---

## 6. Установите инструменты для 3D-ассетов

- Blender (для моделей, анимаций и текстур):
    ```bash
    sudo apt install -y blender
    ```

---

## 7. Установите OBS Studio для записи экрана

```bash
sudo apt install -y obs-studio
```

---

## 8. Проверьте подключение VR-шлема

- Подключите шлем к ПК.
- Для Oculus: установите приложение Oculus Link (через SteamVR).
- Для Vive: убедитесь, что SteamVR видит устройство.

---

## 9. Создайте тестовый проект в Unity

- Создайте новый проект с 3D-шаблоном.
- Импортируйте нужный SDK для вашего шлема.
- Добавьте простую 3D-сцену.
- Запустите проект в режиме Play — убедитесь, что VR-шлем отображает сцену.

---

## 10. Составьте краткое руководство пользователя (по ГОСТ Р 59795–2021)

Выполните документирование: опишите, как запустить Unity, открыть проект, проверить подключение VR-шлема и начать разработку.

---

## Примерный список ПО для VR/AR-разработки на Ubuntu

- Unity Hub + Unity Editor
- Blender
- Steam + SteamVR
- OBS Studio
- SDK вашего VR/AR-шлема (Oculus, Vive, Hololens и др.)
- Графические драйверы (NVIDIA/AMD)
- Git

---

Если нужен подробный текст для отчёта или шаблон документа, скажите — подготовлю под ваш случай.