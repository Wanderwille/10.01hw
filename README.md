# Домашнее задание к занятию "`Git`" - "Подус Сергей"       


### Задание 1
Что нужно сделать:

Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в этом репозитории.
Создайте новый проект и пустой репозиторий в нём.
Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.
В качестве ответа в репозиторий шаблона с решением добавьте скриншоты с настройками раннера в проекте.

Ответ:
![Скриншот 1](https://github.com/Wanderwille/scrinshot/blob/main/image%20(5).png)
![Скринштот 2](https://github.com/Wanderwille/scrinshot/blob/main/image%20(4).png)

### Задание 2
Что нужно сделать: (Тесты и сборки были взяты из репозитория https://github.com/netology-code/sdvps-materials/blob/main/gitlab/GITLAB.md)

Запушьте репозиторий на GitLab, изменив origin. Это изучалось на занятии по Git.
Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.
В качестве ответа в шаблон с решением добавьте:

файл gitlab-ci.yml для своего проекта или вставьте код в соответствующее поле в шаблоне;
скриншоты с успешно собранными сборками.
Ответ: (Тесты и сборки были взяты из репозитория https://github.com/netology-code/sdvps-materials/blob/main/gitlab/GITLAB.md)
![Скриншот 3](https://github.com/Wanderwille/scrinshot/blob/main/image.png)
![Скриншот 4](https://github.com/Wanderwille/scrinshot/blob/main/image%20(3).png)
![Скриншот 5](https://github.com/Wanderwille/scrinshot/blob/main/image%20(2).png)
![Скриншот 6](https://github.com/Wanderwille/scrinshot/blob/main/image%20(1).png)

Файл gitlab-ci.yaml для выполнения playbook.yaml 
stages:
  - test
  - deploy
 
test_job:
  stage: test
  script:
    - ansible-lint playbook.yml
    - ansible-playbook --check playbook.yml
 
  tags:
    - ansible
 
deploy_job:
  stage: deploy
  script:
    - ansible-playbook playbook.yml
 
  tags:
    - ansible