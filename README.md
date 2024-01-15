#**Шпаргалка для настройки GIT!**
---

## Настройка GIT (config)

```bash
$ git config --global user.name "ваше имя или ник латиницей"
$ git config --global user.email ваша электронная почта
```

## Просмотр настроек GIT (config)

```bash
$ cat ~/.gitconfig
$ git config --list
```

## Инициализация репозитория (init)

```bash
$ git init
```

## Проверка статуса репозитория (status)

```bash
$ git status
```

## Разгитить (удаление папки "rm")

```bash
$ rm -rf .git # удалили подпапку .git
```

## Команда git add (add)

Команда `git add` позволяет подготовить файл к сохранению. `git add --all` подготовит к сохранению сразу все файлы. С помощью `git add .` можно добавить в репозиторий текущую папку со всеми файлами.

## Гит Коммит (commit)

```bash
$ git commit -m 'Мой первый коммит!'
```

## История коммитов (log)

```bash
$ git log
```

## Генерация SSH (keygen)

```bash
$ ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
# Через другой алгоритм шифрования:
$ ssh-keygen -t rsa -b 4096 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
```

## Проверка ключей в консоли (ls)

```bash
$ ls -a ~/.ssh
```

## Вывод ключа в консоли (cat)

```bash
$ cat ~/.ssh/id_ed25519.pub
```

## Копирование в буфер ключа (clip)

```bash
$ clip < ~/.ssh/id_ed25519.pub
```

## Проверка правильности ключа

```bash
$ ssh -T git@github.com
```

## Связать локальный и удаленный репозитории (remote)

```bash
$ cd /c/first-project
$ git remote add origin
```

## Проверка связки (remote)

```bash
$ git remote -v
# Флаг -v — короткая форма флага --verbose (англ. «подробный»)
# Вывод должен содержать ссылки на fetch и push
```

## Отправка изменений в ветку (push)

```bash
$ git push -u origin master
# Если команда приведёт к ошибке, попробуйте заменить master на main
# Флаг -u свяжет локальную ветку с одноимённой удалённой
# Необходимо также связать ветки, как вы связывали локальный и удалённый репозитории в предыдущем уроке
```