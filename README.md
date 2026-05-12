<img width="523" height="281" alt="image" src="https://github.com/user-attachments/assets/79ef08ad-4e7a-417c-b9fc-334075c0be17" /># operating-systems-lab
Лабораторные работы по операционным системам

# Лабораторная работа №1
## 1. Реализация функции на C++

### 1.1. Заголовочный файл fibonacci.h
<img width="408" height="164" alt="image" src="https://github.com/user-attachments/assets/1d7587de-e0fa-4569-8a40-f56e7b9c9c37" />

### 1.2. Реализация функции fibonacci.cpp
<img width="421" height="331" alt="image" src="https://github.com/user-attachments/assets/7f9e514f-71ac-44cc-b559-881398179a39" />

### 1.3. Основная программа main.cpp
<img width="725" height="241" alt="image" src="https://github.com/user-attachments/assets/06f3ca13-1a61-458a-b48e-d0fdeb67e18c" />

### 1.4.Компиляция и запуск
<img width="670" height="147" alt="image" src="https://github.com/user-attachments/assets/b0f8f3f6-25c2-4eaa-9868-7ae0373c8253" />

## 2. Компиляция в ассемблерный код

### 2.1. Без оптимизации (-O0)
<img width="845" height="903" alt="image" src="https://github.com/user-attachments/assets/9901f3b7-73a4-463c-8262-dd34b15967c8" /> <img width="835" height="518" alt="image" src="https://github.com/user-attachments/assets/d9738953-83e3-47ee-8627-db5c7a1bfa91" />

### 2.2. С оптимизацией (-O3)
<img width="873" height="932" alt="image" src="https://github.com/user-attachments/assets/8a44bc80-0ba7-4a68-ad18-9273396b9304" />

## 3. Создание Makefile

### 3.1. Файл Makefile
<img width="627" height="525" alt="image" src="https://github.com/user-attachments/assets/525623a0-f1f0-4895-86e4-9c0b8c4c74c5" />

### 3.2. Результат выполнения сборки
<img width="390" height="104" alt="image" src="https://github.com/user-attachments/assets/264a94d6-7850-4a4a-b8ce-3e1c67a68b51" />

## 5. Усовершенствование программы

### 5.1.Добавление параллельного потока и синхронизации
<img width="801" height="825" alt="image" src="https://github.com/user-attachments/assets/f8c3aa38-8ee7-4300-930f-f07efb4ee8f8" />

### 5.2. Обновлённый Makefile
<img width="606" height="542" alt="image" src="https://github.com/user-attachments/assets/2a90049c-f123-4d67-89a7-6807079a1870" />


# Лабораторная работа №2: Установка Linux 

## Цель работы

Освоить процесс установки Linux x86_64 различными методами: через debootstrap (Debian/Ubuntu), ручную установку (Arch Linux), а также продвинутые методы (Gentoo, IPv6 Tunnel Broker, PXE-загрузка). Настроить SSH-доступ и проброс портов.

---

## Создание виртуальной машины

[Всё в видео](lab2.mp4)


# Лабораторная работа 3a: Разработка Bash-скрипта для конвертации изображений

## Вариант 2: Преобразование JPG → JPEG2000 (JP2)
(Перед выполнением работы я установил ImageMagick, но забыл сделать скриншот)

### 1. Создание папки для работы
<img width="318" height="58" alt="image" src="https://github.com/user-attachments/assets/5d585a52-c6e1-44c2-a35d-7c5bd198b0e7" />

### 2. Создание тестовых изображений
<img width="547" height="142" alt="image" src="https://github.com/user-attachments/assets/17b800bd-c5ee-461a-9a30-f22bd2e4a9ed" />

### 3. При помощи общей папки создаем программу
<img width="519" height="641" alt="image" src="https://github.com/user-attachments/assets/1ceb871c-4c78-4ef9-a6fb-6283809cb443" />
<img width="822" height="202" alt="image" src="https://github.com/user-attachments/assets/1d4ddd0a-d5a0-48c0-9794-64fdb283a11d" />
<img width="900" height="511" alt="image" src="https://github.com/user-attachments/assets/2484244d-9eef-4d9d-bb95-eaff0f2d3e73" />
<img width="590" height="90" alt="image" src="https://github.com/user-attachments/assets/52656547-4b24-4104-a2b1-2a106ce0f931" />

### 4. Копирование скрипта из общей папки
<img width="513" height="20" alt="image" src="https://github.com/user-attachments/assets/c629040d-c4c5-40c0-a5c5-3f9aa44f07b8" />

### 5. Установка dos2unix для удаления символов \r
<img width="1286" height="367" alt="image" src="https://github.com/user-attachments/assets/e68d0874-9b82-40c8-9549-cece908e26dd" />

### 6. Запуск скрипта и результат
<img width="427" height="192" alt="image" src="https://github.com/user-attachments/assets/95012b81-0be9-44b0-b6fc-52c7bf6b3c51" />

# Лабораторная работа 3b: Разработка Bash-скрипта для конвертации изображений

## Вариант 2: Преобразование JPG → JPEG2000 (JP2)

### 1. Установка ImageMagick в Windows

### 1. Установка ImageMagick.

Был скачан установщик с официального сайта и установлен.
После установки компьютер был перезагружен.
<img width="1125" height="625" alt="image" src="https://github.com/user-attachments/assets/fe9d6e87-e496-4a7d-af74-dc9c8eab9847" />

### 2. Создание папки для работы
<img width="523" height="281" alt="image" src="https://github.com/user-attachments/assets/4d7bcda8-9de4-49bc-8bc5-0e87a16a6763" />

### 3. Создание тестовых изображений
<img width="589" height="322" alt="image" src="https://github.com/user-attachments/assets/83f33251-af92-461f-a2cb-689740628cc6" />

### 4. Создание PowerShell-скрипта
<img width="325" height="24" alt="image" src="https://github.com/user-attachments/assets/3f42c440-144b-43d9-891c-87508957cc03" />
<img width="617" height="518" alt="image" src="https://github.com/user-attachments/assets/bb2dfa85-e1a8-4c89-b263-08b78ef36252" />

### 5. Настройка выполнения скриптов
<img width="609" height="45" alt="image" src="https://github.com/user-attachments/assets/5376c35f-1621-4804-b4c4-2ad70725cf7e" />

### 6. Запуск скрипта и результат
<img width="615" height="385" alt="image" src="https://github.com/user-attachments/assets/de444cbe-e585-4446-ac59-3209284688ff" />











