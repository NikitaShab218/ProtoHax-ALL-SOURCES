# 🛠️ ProtoHax — Rebuild Project

## 🇬🇧 Description (in English)

### 📖 The Story of ProtoHax

ProtoHax was once a legendary Minecraft cheat, but it was discontinued. Why? Because people started cloning and **selling** it (especially the popular **GodWare** fork), so the original developer shut it down.

A better solution could have been a **module system**, allowing users to import external modules. That way, the developer could legally sell official modules instead of the entire cheat being resold.

After shutdown, only two repositories were left:
- `ProtoHax` — the core library
- `ProtoHax-Android` — the Android app using the library

However, the most important part was removed — the `maven_repo`, which contained essential dependencies like `libmitm`, `mcauth`, `leveldb`, etc. These were removed due to copyright.

---

### 🧩 How to build ProtoHax today?

Most of the hard work has already been done for you.

I:
- Recovered the missing `maven_repo`
- Reconfigured all `gradle` files to use **local** dependencies

#### 🔧 Requirements:
- Windows PC
- Android Studio
- This repository and the included `maven_repo`

#### 📦 Build steps:
1. Create a working folder with both `ProtoHax` and `ProtoHax-Android`.
2. In both projects, edit the `build.gradle` files to point Maven repositories to local paths.
3. Build the `ProtoHax` library. You will get a `.jar` file.
4. Go to: ProtoHax-Android/maven_repo/dev/sora/relay/ProtoHax/1.4.0/protohax-1.4.0.jar
5. Open this `.jar` archive and **replace the `dev` folder inside it** with the updated one from your compiled `ProtoHax` library.
6. Save the `.jar` and then open `ProtoHax-Android` in Android Studio.
7. Build it like a normal application.

✅ If all paths and changes are correct — the app will compile successfully.

---

📁 **The full archive is available in the repository files.**

---

## 🇷🇺 Описание (на русском)

### 📖 История ProtoHax

ProtoHax был легендарным читом для Minecraft, но со временем его закрыли. Почему? Потому что начали появляться копии чита, которые люди начали **продавать** (особенно популярная копия — **GodWare**). Разработчик не выдержал и закрыл проект.

Лучшим решением было бы реализовать **систему модулей**, чтобы пользователи могли подключать свои модули. Тогда разработчик мог бы продавать официальные модули, не рискуя утратой проекта.

После закрытия остались только два репозитория:
- `ProtoHax` — библиотека.
- `ProtoHax-Android` — приложение, использующее эту библиотеку.

Но исчез самый важный компонент — `maven_repo`, где были библиотеки `libmitm`, `mcauth`, `leveldb` и другие. Их удалили из-за нарушений авторских прав.

---

### 🧩 Как собрать ProtoHax сегодня?

Почти всё уже сделано за вас.

Я:
- Восстановил `maven_repo`
- Настроил все `gradle`-файлы на использование **локальных** зависимостей

#### 🔧 Требования:
- ПК с Windows
- Установленная Android Studio
- Этот репозиторий и архив с `maven_repo`

#### 📦 Шаги сборки:
1. Создайте рабочую папку и поместите туда два проекта: `ProtoHax` и `ProtoHax-Android`.
2. В обоих проектах откройте `build.gradle` и укажите путь к локальному `maven_repo`.
3. Соберите `ProtoHax`. В результате вы получите `.jar` файл.
4. Перейдите по пути: ProtoHax-Android/maven_repo/dev/sora/relay/ProtoHax/1.4.0/protohax-1.4.0.jar
5. Откройте этот `.jar` как архив и **замените в нём папку `dev`** на ту, что была скомпилирована в вашем проекте `ProtoHax`.
6. Сохраните `.jar` и откройте `ProtoHax-Android` в Android Studio.
7. Соберите как обычное приложение.

✅ Если всё сделано правильно — сборка пройдёт успешно.

---

📁 **Полный архив доступен в файлах репозитория.**




