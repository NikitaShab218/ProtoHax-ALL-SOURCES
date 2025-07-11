# 🛠️ ProtoHax — Rebuild Project

## 🇬🇧 Description (in English)

### 📖 The Story of ProtoHax

ProtoHax was once a legendary Minecraft cheat, but it was discontinued. Why? Because people started cloning and **selling** it (especially the popular **GodWare** fork), so the original developer shut it down.

However, a better solution would have been to implement a **module system**, allowing external modules to be imported. This way, the developer could sell official modules legally instead of the whole client being cloned and resold.

After shutdown, two repositories remained:
- `ProtoHax` — the core library.
- `ProtoHax-Android` — the Android application that uses the library.

But a key part was missing: the `maven_repo`, which included critical dependencies like `libmitm`, `mcauth`, `leveldb`, and more. These were removed due to copyright concerns.

---

### 🧩 How to build ProtoHax today?

Most of the hard work has already been done for you. I:
- Recovered the `maven_repo`
- Reconfigured `gradle` to work with **local** dependencies

#### 🔧 Requirements:
- Windows PC
- Android Studio installed
- This repository and the `maven_repo` archive

#### 📦 Build steps:
1. Create a working folder with both `ProtoHax` and `ProtoHax-Android`.
2. In both projects, edit `build.gradle` and point Maven paths to your local repo.
3. First, build the `ProtoHax` library — you will get a `.jar` and `.pom` file.
4. Place those files here:  
   `ProtoHax-Android/maven_repo/dev/sora/relay/ProtoHax/1.4.0/`
5. Open `ProtoHax-Android` in Android Studio and build it as a normal app.

Done! If all paths are correct — it should compile successfully.

---

📁 **Archive with `maven_repo` and both projects available below**.

---

## 🇷🇺 Описание (на русском)

### 📖 История ProtoHax

ProtoHax был легендарным читом для Minecraft, но проект закрылся. Почему? Всё просто: началась массовая продажа копий чита, особенно проекта **GodWare**, и разработчик решил закрыть исходный ProtoHax.

Однако вместо закрытия можно было бы ввести систему **модулей**, которые можно было бы подключать отдельно. Это решило бы проблему — разработчик мог бы легально продавать модули, а не сам чит.

После закрытия остались только два репозитория:
- `ProtoHax` — библиотека.
- `ProtoHax-Android` — Android-приложение, использующее эту библиотеку.

Но пропал ключевой компонент — `maven_repo`, содержащий нужные зависимости (`libmitm`, `mcauth`, `leveldb` и др.). Их удалили из-за нарушения авторских прав.

---

### 🧩 Как собрать ProtoHax сегодня?

Все сложные шаги уже сделаны за вас. Я:
- Восстановил `maven_repo`.
- Настроил `gradle` на работу с **локальными** зависимостями.

#### 🔧 Требования:
- ПК с Windows
- Установленная Android Studio
- Архив с этим репозиторием и `maven_repo`

#### 📦 Сборка:
1. Создайте рабочую папку с двумя проектами: `ProtoHax` и `ProtoHax-Android`.
2. В обоих проектах замените пути в `build.gradle` на локальные.
3. Сначала соберите `ProtoHax` — вы получите `.jar` и `.pom`.
4. Поместите эти файлы в:  
   `ProtoHax-Android/maven_repo/dev/sora/relay/ProtoHax/1.4.0/`
5. Соберите `ProtoHax-Android` как обычное приложение.

Готово! Если всё настроено правильно — сборка пройдёт успешно.

