# operating-systems-lab
Лабораторные работы по операционным системам


# Лабораторная работа №2: Установка Linux (развертка, bootstrapping)

## Цель работы

Освоить процесс установки Linux x86_64 различными методами: через debootstrap (Debian/Ubuntu), ручную установку (Arch Linux), а также продвинутые методы (Gentoo, IPv6 Tunnel Broker, PXE-загрузка). Настроить SSH-доступ и проброс портов.

---

## Выполненные задачи

### 1. Создание виртуальной машины

- **Гипервизор:** Oracle VirtualBox 7.0+
- **Имя ВМ:** `Arch-Lab`
- **ОС:** Arch Linux (64-bit)
- **ОЗУ:** 4096 МБ
- **CPU:** 2 ядра
- **Диск:** 25 ГБ (VDI, динамический)
- **Сеть:** NAT (с пробросом портов)
- **Ускорение:** VT-x/AMD-V, Nested Paging (включены)

### 2. Установка Arch Linux

Установка выполнялась через официальный ISO-образ. Основные этапы:

#### 2.1. Подготовка диска

```bash
fdisk /dev/sda
# g - GPT таблица
# n - создание разделов:
#   /dev/sda1: +1M (тип 4 - BIOS boot)
#   /dev/sda2: весь оставшийся объём
# w - запись изменений

mkfs.ext4 /dev/sda2
mount /dev/sda2 /mnt
2.2. Установка базовой системы
bash
pacstrap /mnt base linux linux-firmware
genfstab -U /mnt >> /mnt/etc/fstab
arch-chroot /mnt
2.3. Настройка системы
bash
# Часовой пояс и локали
ln -sf /usr/share/zoneinfo/UTC /etc/localtime
hwclock --systohc
sed -i 's/^#en_US.UTF-8/en_US.UTF-8/' /etc/locale.gen
locale-gen
echo "LANG=en_US.UTF-8" > /etc/locale.conf

# Имя хоста
echo "archlinux" > /etc/hostname

# Пароль root
passwd  # пароль: root

# Пользователь user (пароль: 123456)
useradd -m -s /bin/bash user
echo "user:123456" | chpasswd
2.4. Установка и настройка SSH
bash
pacman -S openssh dhcpcd grub --noconfirm
systemctl enable sshd dhcpcd
2.5. Установка загрузчика GRUB
bash
grub-install /dev/sda
grub-mkconfig -o /boot/grub/grub.cfg
2.6. Завершение установки
bash
exit
reboot
3. Настройка проброса портов (NAT → SSH)
В VirtualBox настроен проброс порта:

Протокол	Хост-порт	Гостевой порт
TCP	7022	22
