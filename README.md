# Web UI со Stable Diffusion с использованием Gradio
Проект для курса по организации процессов с DS и ML на Stepik.org. Интерфейс браузера на основе библиотеки Gradio для Stable Diffusion. Опирается на решение от [пользователя](https://github.com/AUTOMATIC1111/). 

## Сценарии txt2img и img2img:

![txt2img](txt2img_Screenshot.png)
![img2img](txt2img_Screenshot.png)

- Гляньте [полный список функций](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Features), доступных через решения Stable Diffusion.
- Поддержка [Stable Diffusion 2.0](https://github.com/Stability-AI/stablediffusion)

## Установка и запуск
Убедитесь, что необходимые [зависимости](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Dependencies) соблюдены, и следуйте инструкциям, доступным для обоих [NVidia] (https://github.com/AUTOMATIC1111 /stable-diffusion-webui/wiki/Install-and-Run-on-NVidia-GPU) (рекомендуется) и [AMD](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and -Run-on-AMD-GPUs) графические процессоры.

В качестве альтернативы используйте онлайн-сервисы (например, Google Colab):
- [Список онлайн-сервисов](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Online-Services)

### Автоматическая установка в Windows
1. Установите [Python 3.10.6](https://www.python.org/downloads/windows/), отметив «Добавить Python в PATH».
2. Установите [git](https://git-scm.com/download/win).
3. Загрузите репозиторий stable-diffusion-webui, например, запустив `git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git`.
4. Поместите `model.ckpt` в каталог `models` (см. [зависимости](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Dependencies), чтобы узнать, где его взять).
5. _*(Необязательно)*_ Поместите `GFPGANv1.4.pth` в базовый каталог вместе с `webui.py` (см. [зависимости](https://github.com/AUTOMATIC1111/stable-diffusion-webui/ wiki/Зависимости) для того, чтобы узнать, где его взять).
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
2. Чтобы установить в `/home/$(whoami)/stable-diffusion-webui/`, запустите:
```bash
bash <(wget -qO- https://raw.githubusercontent.com/AUTOMATIC1111/stable-diffusion-webui/master/webui.sh)
```

### Установка на Apple Silicon
Найдите инструкции [здесь](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Installation-on-Apple-Silicon).


## Пользовательские сценарии
Проверье наличие новых [пользовательских сценариев](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Custom-Scripts).


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
