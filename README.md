# datahub_architecture
## Варианты предметки:
- История, события, личности, факты
- Данные Росстата
- Ленты новостей
- Биржевые сводки
- Семиотический анализ книг, парсинг и аналитический анализ

## Требования
- Нужны источники информации в виде открытого api

# Скачать Planet VPN для Windows 11 Pro
https://apps.microsoft.com/detail/9p15s8pwmq8c?hl=en-US&gl=US

# Скачать и установить IntelliJ IDEA
https://www.jetbrains.com/ru-ru/idea/download/other.html
https://download.jetbrains.com/idea/ideaIC-2025.1.3.exe?_gl=1*1yn22wk*_gcl_au*MTUzMDcwMTQ2Ny4xNzUwNzE5ODEx*FPAU*MTUzMDcwMTQ2Ny4xNzUwNzE5ODEx*_ga*MTU4NjM5NzEyMy4xNzUwNzE5ODEz*_ga_9J976DJZ68*czE3NTA3MTk4MTAkbzEkZzEkdDE3NTA3MTk4OTMkajYwJGwwJGgw

## Скачать и установить плагины PlantUML и Diagrams для IDEA
Из магазина приложений

# Скачать и установить Git for Windows
https://www.docker.com/products/docker-desktop/

# Скачать и установить Docker Desktop для Windows 11 Pro
https://www.docker.com/products/docker-desktop/

# Создать проект в GitHub для описания архитектуры DataHub
https://github.com/jetio/datahub_architecture.git

# Склонировать архитектурный репозиторий
## Создать структуру архрепозитория

# Скачать и установить Postman
https://www.postman.com/downloads/

# Скачать и установить Focus ToDo
Из магазина приложений

--------------------------------------------

# Залогиниться в GitHub
> git config --global user.name "Smirnov Andrey"

> git config --global user.email mr.smirnov.andrey@gmail.com

# Сгенерить SSH-ключи для GitHub или дать разрешение IDEA через OAuth GitHub-а

# Проверить наличие установленного curl

# Установить Minikube для Windows 11 Pro
https://kubernetes.io/ru/docs/tasks/tools/install-minikube/

# Установить утилиту kubectl
Скачать бинарник
> curl -LO https://dl.k8s.io/release/v1.33.0/bin/windows/amd64/kubectl.exe

Создать директорию C:\Program Files\Kubectl\bin, переписать туда скаченный файл, добавить эту дирукторию в Path

Примечание:
Docker Desktop for Windows добавляет собственную версию kubectl в переменную окружения PATH. Если у вас установлен Docker Desktop, вам придётся поместить путь к установленному бинарному файлу перед записью, добавленной установщиком Docker Desktop, либо же удалить вовсе kubectl, поставляемый вместе с Docker Desktop.

Проверить версию kubectl:
> kubectl version

должна быть та, какую скачивали

# Активировать Hyper-V
Запустить Windows Power Shell от имени администратора, выполнить команду:
> Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All

# Скачать установщик для minikube
https://github.com/kubernetes/minikube/releases/latest/download/minikube-installer.exe
Инсталлировать minikube
Проверить старт кластера через CMD, запущенной от Администратора:
> minikube start --vm-driver=hyperv

Результат:

C:\Windows\System32>minikube start --vm-driver=hyperv
* minikube v1.36.0 на Microsoft Windows 11 Pro 10.0.22631.3155 Build 22631.3155
* Используется драйвер hyperv на основе конфига пользователя
* Downloading VM boot image ...
  > minikube-v1.36.0-amd64.iso....:  65 B / 65 B [---------] 100.00% ? p/s 0s
  > minikube-v1.36.0-amd64.iso:  360.83 MiB / 360.83 MiB  100.00% 13.84 MiB p
* Starting "minikube" primary control-plane node in "minikube" cluster
* Скачивается Kubernetes v1.33.1 ...
  > preloaded-images-k8s-v18-v1...:  347.04 MiB / 347.04 MiB  100.00% 13.21 M
* Creating hyperv VM (CPUs=2, Memory=6000MB, Disk=20000MB) ...
  ! StartHost failed, but will try again: creating host: create: precreate: Hyper-V PowerShell Module is not available
* Creating hyperv VM (CPUs=2, Memory=6000MB, Disk=20000MB) ...
* Failed to start hyperv VM. Running "minikube delete" may fix it: creating host: create: precreate: Hyper-V PowerShell Module is not available

X Exiting due to PR_HYPERV_MODULE_NOT_INSTALLED: Failed to start host: creating host: create: precreate: Hyper-V PowerShell Module is not available
* Предложение: Run: 'Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-Tools-All -All'
* Documentation: https://www.altaro.com/hyper-v/install-hyper-v-powershell-module/
* Related issue: https://github.com/kubernetes/minikube/issues/9040

Выполнить повторно в Windows Power Shell от имени администратора:
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-Tools-All -All

В этот раз при перезагрузке шли проценты обновления системы.

Повторить: 
> minikube start --vm-driver=hyperv

C:\Windows\System32>minikube start --vm-driver=hyperv                                                                   * minikube v1.36.0 на Microsoft Windows 11 Pro 10.0.22631.5472 Build 22631.5472                                         E0624 17:00:46.074222    2096 start.go:819] api.Load failed for minikube: filestore "minikube": Docker machine "minikube" does not exist. Use "docker-machine ls" to list machines. Use "docker-machine create" to add a new one.               E0624 17:00:46.074222    2096 start.go:819] api.Load failed for minikube: filestore "minikube": Docker machine "minikube" does not exist. Use "docker-machine ls" to list machines. Use "docker-machine create" to add a new one.
* Используется драйвер hyperv на основе существующего профиля
* Starting "minikube" primary control-plane node in "minikube" cluster
* Creating hyperv VM (CPUs=2, Memory=6000MB, Disk=20000MB) ...
  ! Image was not built for the current minikube version. To resolve this you can delete and recreate your minikube cluster using the latest images. Expected minikube version: v1.35.0 -> Actual minikube version: v1.36.0
  ! Failing to connect to https://registry.k8s.io/ from inside the minikube VM
* To pull new external images, you may need to configure a proxy: https://minikube.sigs.k8s.io/docs/reference/networking/proxy/
* Подготавливается Kubernetes v1.33.1 на Docker 28.0.4 ...
  - Generating certificates and keys ...
  - Booting up control plane ...
  - Configuring RBAC rules ...
* Configuring bridge CNI (Container Networking Interface) ...
* Компоненты Kubernetes проверяются ...
  - Используется образ gcr.io/k8s-minikube/storage-provisioner:v5
* Включенные дополнения: storage-provisioner, default-storageclass
* Готово! kubectl настроен для использования кластера "minikube" и "default" пространства имён по умолчанию

Выполнить:
> minikube status

Вывод:
minikube
type: Control Plane
host: Running
kubelet: Running
apiserver: Running
kubeconfig: Configured

Установка завершена.

# Запустить minikube dashboard
> minikube dashboard

# Указать minikube на локальный репозиторий DockerDesktop 
