Итоговая аттестация по программе
“Автоматизация тестирования на Python”
Уважаемые студенты, перед вами задание для итогового проекта, который вы
должны выполнить после прохождения курсов “Погружение в Python”,
“Автоматизация тестирование консольных приложений Linux на Python” и
“Автоматизация тестирование веб-приложений на Python”.
Описание итоговой аттестации:
1) Цель задания: повторить и отработать на практике материал, изученный в ходе
программы.
2) Проект включает в себя обязательное задание и дополнительные задания.
- Обязательное задание необходимо выполнить для получения диплома.
За него ставится оценка.
- Дополнительные задание можно выполнить для портфолио и также
сдать и получить обратную связь. Его выполнение полезно, но не влияет
на оценку.
3) Инструменты, которые обязательно нужно использовать для обязательного
задания: Python, PyTest, Selenium WebDriver, yaml
4) Формат сдачи: ссылка на подписанную и доступную для просмотра копию
данного шаблона с выполненными заданиями в синих полях. Инструкция.
Обязательное задание (обязательно к выполнению):
С использованием Selenium Webdriver, применяя паттерн проектирования Page Object
и сохраняя веб-локаторы в отдельном yaml-файле выполнить следующие тесты в
браузере Google Chrome для линукс:
- логин на сайт https://test-stand.gb.ru
- клик по ссылке About
- проверка, что шрифт в заголовке открывшегося окна имеет размер 32 px.
Вставьте в данное поле ссылку на код или ссылку на архив, размещенный на
Googledisk. Убедитесь что вы предоставили доступ для просмотра.
Вставьте в данное поле скриншоты выполнения автотеста.
Дополнительное задание 1:
Выполнить быструю проверку сайта на уязвимости при помощи утилиты командной
строки nikto;
Дополнительное задание 2:
С использованием библиотеки requests выполнить авторизацию на сайте с
использованием токена авторизации в headers, получить данные о текущем
пользователе и проверить, что они соответствуют данным, возвращенным в ответе на
запрос авторизации;
Вставьте в данное поле ссылку на код или ссылку на архив, размещенный на
Googledisk. Убедитесь что вы предоставили доступ для просмотра.
Вставьте в данное поле скриншоты выполнения автотеста.
Блоки с подсказками:
Обязательное задание
Браузер Google Chrome не входит в стандартную поставку Ubuntu, его нужно
установить командами:
wget
https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i --force-depends google-chrome-stable_current_amd64.deb
Или вручную скачать файл по указанной выше ссылке и установить пакет.
Дополнительное задание 1
Перед написанием тестов нужно вручную установить утилиту nikto командой sudo apt
install nikto.
Нужно проверить что в выводе команды
nikto -h https://test-stand.gb.ru/ -ssl -Tuning 4
присутствует текст
0 error(s)
Дополнительное задание 2
Нужно проверить, что запрос к https://test-stand.gb.ru/api/users/profile/{id} возвращает
json с правильным username
