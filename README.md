# Web UI со Stable Diffusion с использованием Gradio
Проект для курса по организации процессов с DS и ML на Stepik.org. Интерфейс браузера на основе библиотеки интерфейсов [Gradio](https://gradio.app/docs/) для Stable Diffusion. Опирается на решение от [пользователя](https://github.com/AUTOMATIC1111/). 

## Сценарий txt2img:

![txt2img](https://github.com/ayranamo/project-1-stable-diff-gradioui/blob/main/txt2img.png)

## Сценарий img2img:
![img2img](https://github.com/ayranamo/project-1-stable-diff-gradioui/blob/main/img2img.png)

## Установка и запуск
Убедитесь, что необходимые [зависимости](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Dependencies) соблюдены, и следуйте инструкциям, доступным для обоих [NVidia](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and-Run-on-NVidia-GPU) (рекомендуется) и [AMD](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and-Run-on-AMD-GPUs) графические процессоры.

В качестве альтернативы используйте онлайн-сервисы (например, Google Colab):
- [Список онлайн-сервисов](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Online-Services)

### Автоматическая установка в Windows
1. Установите [Python 3.10.6](https://www.python.org/downloads/windows/), отметив «Добавить Python в PATH».
2. Установите [git](https://git-scm.com/download/win).
3. Загрузите репозиторий project-1-stable-diff-gradioui, например, запустив `git clone https://github.com/ayranamo/project-1-stable-diff-gradioui.git`.
4. Поместите `model.ckpt` в каталог `models` (см. [официальная загрузка](https://huggingface.co/CompVis/stable-diffusion-v-1-4-original), [файловое хранилище](https://drive.yerf.org/wl/?id=EBfTrmcCCUAGaQBXVIj5lJmEhjoP1tgl)).
5. _*(Необязательно)*_ Поместите `GFPGANv1.4.pth` в базовый каталог вместе с `webui.py` (Модели ESRGAN, такие как модели из базы данных моделей , могут быть помещены в каталог ESRGAN. Файл будет загружен как модель, если у него есть .pth расширение, и он будет отображаться под своим именем в пользовательском интерфейсе).
6. Запустите `webui-user.bat` из проводника Windows как обычный пользователь без прав администратора.

### Автоматическая установка в Linux
1. Установите зависимости:
```bash
# Debian-based:
sudo apt install wget git python3 python3-venv
# Red Hat-based:
sudo dnf install wget git python3
# Arch-based:
sudo pacman -S wget git python3
```
2. Чтобы установить в `/home/$(whoami)/project-1-stable-diff-gradioui/`, запустите:
```bash
bash <(wget -qO- https://raw.githubusercontent.com/ayranamo/project-1-stable-diff-gradioui/master/webui.sh)
```

### Установка на Apple Silicon
1. Если Homebrew не установлен, следуйте инструкциям на странице https://brew.sh, чтобы установить его. Держите окно терминала открытым и следуйте инструкциям в разделе «Следующие шаги», чтобы добавить Homebrew в PATH.
2. Откройте новое окно терминала и запустите `brew install cmake protobuf rust python@3.10 git wget`.
3. Клонируйте репозиторий веб-интерфейса, запустив git clone `git clone https://github.com/ayranamo/project-1-stable-diff-gradioui.git`.
4. Скопируйте любые модели Stable Diffusion, которые вы хотите использовать, в файл project-1-stable-diff-gradioui/models/Stable-diffusion.
5. cd `project-1-stable-diff-gradioui`, а затем `./webui.sh` для запуска веб-интерфейса. Виртуальная среда Python будет создана и активирована с помощью venv, а все оставшиеся недостающие зависимости будут автоматически загружены и установлены.
6. Чтобы перезапустить процесс веб-интерфейса позже, снова запустите `./webui.sh`.


## Благодарности
- Автору проекта — https://github.com/AUTOMATIC1111/ 
- Stable Diffusion - https://github.com/CompVis/stable-diffusion, https://github.com/CompVis/taming-transformers
- k-diffusion - https://github.com/crowsonkb/k-diffusion.git
- GFPGAN - https://github.com/TencentARC/GFPGAN.git
- CodeFormer - https://github.com/sczhou/CodeFormer
- ESRGAN - https://github.com/xinntao/ESRGAN
- SwinIR - https://github.com/JingyunLiang/SwinIR
- Swin2SR - https://github.com/mv-lab/swin2sr
- LDSR - https://github.com/Hafiidz/latent-diffusion
- MiDaS - https://github.com/isl-org/MiDaS
- Идеи для оптимизации - https://github.com/basujindal/stable-diffusion
— Оптимизация уровня перекрестного внимания — Doggettx — https://github.com/Doggettx/stable-diffusion, оригинальная идея для оперативного редактирования. 
- Оптимизация уровня перекрестного внимания - InvokeAI, lstein - https://github.com/invoke-ai/InvokeAI (первоначально http://github.com/lstein/stable-diffusion) 
- Textual Inversion - Rinon Gal - https:// github.com/rinongal/textual_inversion (мы не используем его код, но используем его идеи).
- Идея для апскейла SD - https://github.com/jquesnelle/txt2imghd 
- Генерация шума для перекрашивания mk2 - https://github.com/parlance-zz/g-diffuser-bot 
- Идея опросчика CLIP и заимствование некоторого кода - https://github.com/pharmapsychotic/clip-interrogator 
— Идея для компонуемой диффузии — https://github.com/energy-based-model/Compositional-Visual-Generation-with-Composable-Diffusion-Models-PyTorch 
— xformers - https://github.com/facebookresearch/xformers 
- DeepDanbooru - опросчик для аниме-диффузоров https://github.com/KichangKim/DeepDanbooru 
- Совет по безопасности - RyotaK 
- Initial Gradio script - размещен на 4chan анонимным пользователем.
