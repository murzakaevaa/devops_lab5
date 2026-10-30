# Lab 5. Ansible Advanced (П05)

## Что было сделано
1. Написан `playbook_nmap.yml` — установка nmap на VM-2 и сканирование списка целей (`targets.txt`) с использованием циклов `loop`, `register` и `debug`.
2. Продемонстрирован **Ansible Vault**: файл `secret.yml` зашифрован, запуск плейбука выполнен с флагом `--ask-vault-pass`.
3. Продемонстрирован **Debug**: вывод сообщений и расшифрованных переменных.
4. Продемонстрирован **Loop**: цикл по списку элементов (Apples, Oranjes, Raindrops).
5. Продемонстрированы **Handlers**: задача вызывает `notify` при изменении, и handler запускается только в этом случае (проверена идемпотентность).

## Файлы в репозитории
- `inventory.ini` — инвентарный файл со списком хостов.
- `targets.txt` — список целей для сканирования.
- `secret.yml` — зашифрованный файл с секретом (Vault).
- `playbook_nmap.yml` — основной плейбук для сканирования NMAP.
- `playbook_debug.yml` — плейбук для демонстрации Debug и Vault.
- `playbook_loop.yml` — плейбук с циклом (Loop).
- `playbook_handlers.yml` — плейбук с обработчиками (Handlers).

## Скриншоты (папка `скрины`)

| Файл | Что изображено на скриншоте |
| :--- | :--- |
| `01-file-list.png` | Список созданных файлов в папке проекта  |
| `02-nmap-start.png` | Начало выполнения плейбука NMAP  |
| `03-nmap-moodle.png` | Результат сканирования moodle-epos.permkrai.ru  |
| `04-nmap-psu.png` | Результат сканирования www.psu.ru  |
| `05-nmap-fast.png` | Результат сканирования fast.com  |
| `06-vault-encrypted.png` | Шифрование secret.yml  и вывод `cat secret.yml` |
| `07-vault-debug.png` | Запуск `playbook_debug.yml` с `--ask-vault-pass`  |
| `08-loop-run.png` | Выполнение цикла |
| `09-handlers-run.png` | Первый запуск handlers |
| `10-handlers-idempotency.png` | Второй запуск handlers  |
