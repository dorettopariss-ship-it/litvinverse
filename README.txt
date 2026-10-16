ЛИТВИНVERSE 2.1 — мемные голосовые кнопки + одиночная Bomb Arena.

Файлы: index.html — весь сайт в одном файле.

ОБНОВЛЕНИЕ НА GITHUB С ТЕЛЕФОНА
1. Распакуй ZIP.
2. Открой репозиторий GitHub litvinverse.
3. Замени index.html старым файлом и нажми Commit changes.
4. Vercel опубликует изменения после commit.

НОВОЕ
- Соло Bomb Arena против бота — не требует Supabase. Управление кнопками или стрелками, пробел ставит бомбу.
- Голосовые мем-кнопки используют встроенный синтез речи устройства с низким тембром. Голос зависит от браузера/телефона; это не оригинальные аудиозаписи конкретного мема.
- Онлайн-бомбочки 1 на 1 остались отдельно и по-прежнему требуют настройки Supabase.


Версия 2.2: встроена отдельная панель мем-звуков sounds.html. Звуки Litvin используют интернет-встраивания Myinstants; часть дополнительных звуков открывает страницу источника. Для работы требуется интернет.


=== ОБЩИЙ ОНЛАЙН-ЧАТ (версия 2.3) ===
В index.html найдите CHAT_SUPABASE_URL и CHAT_SUPABASE_KEY и замените PASTE_SUPABASE_PROJECT_URL_HERE / PASTE_SUPABASE_PUBLIC_ANON_KEY_HERE на Project URL и публичный anon/publishable key своего проекта Supabase. Это нужно сделать ОДИН РАЗ владельцу сайта перед загрузкой в GitHub/Vercel — посетителям вводить ключи не придётся. Используйте только публичный anon/publishable key, никогда service_role/secret key.
Чат использует Supabase Realtime Broadcast и общий канал litvinverse-public-chat. В панели Supabase убедитесь, что Realtime доступен для проекта. Сообщения передаются посетителям, которые находятся онлайн одновременно; история не сохраняется после отключения/перезагрузки. Для постоянной истории сообщений нужна отдельная таблица с корректными RLS-политиками.


=== ВЕРСИЯ 2.4 — ОБЩИЙ ЧАТ БЕЗ РЕГИСТРАЦИИ ===
Общий чат встроен через внешний сервис tlk.io, канал: https://tlk.io/litvinverse-danax. Никакие ключи и настройки Supabase для чата не нужны; посетители просто вводят ник в самом чате. Чат общий для всех, кто откроет эту комнату, и зависит от доступности tlk.io. Это публичная комната: не отправляйте пароли, адреса и другие личные данные. Онлайн-режим бомбочек по-прежнему отдельно требует Supabase.

Обновление: загрузи замену index.html в корень репозитория GitHub, затем дождись публикации Vercel. sounds.html оставь рядом с index.html.


LitvinVERSE 2.5 chat update: public guest chat embed switched to klaklak.com. Visitors choose a nickname; no registration. If embedded chat is blocked, use the open-chat link in the page. External service availability is not controlled by this site.
