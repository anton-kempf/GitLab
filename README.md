# Домашнее задание к занятию "`Название занятия`" - `Фамилия и имя студента`
Колыванов Антон


---

### Задание 1

![Скриншот с настройками раннера в проекте](img/1.png)  



---

### Задание 2
![Скрин выполнения Pipline](img/2.png)  

*Файл .gitlab-ci.yml*
```
 stages:
  - code_intel
  - build
  - test
  - code_quality
  - deploy

code_intelligence_go:
  stage: code_intel
  image: sourcegraph/lsif-go:v1
  tags:
    - docker
  before_script:
    - git remote set-url origin https://github.com/netology-code/sdvps-materials.git
    - go mod edit -module github.com/netology-code/sdvps-materials
    - go mod tidy
  script:
    - lsif-go

build:
  stage: build
  image: docker:latest
  tags:
    - docker
  script:
    - docker info
    - echo "Building the project..."

test:
  stage: test
  image: docker:latest
  tags:
    - docker
  script:
    - echo "Running tests..."
    - echo "Tests passed!"

code_quality:
  stage: code_quality
  image: registry.gitlab.com/gitlab-org/ci-cd/codequality:0.96.0-gitlab.1
  tags:
    - docker
  script:
    - echo "Running code quality scan..."

deploy:
  stage: deploy
  image: docker:latest
  tags:
    - docker
  script:
    - echo "Deploying to production..."

```
---

### Задание 3

`Приведите ответ в свободной форме........`

1. `Заполните здесь этапы выполнения, если требуется ....`
2. `Заполните здесь этапы выполнения, если требуется ....`
3. `Заполните здесь этапы выполнения, если требуется ....`
4. `Заполните здесь этапы выполнения, если требуется ....`
5. `Заполните здесь этапы выполнения, если требуется ....`
6. 

```
Поле для вставки кода...
....
....
....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота](ссылка на скриншот)`

### Задание 4

`Приведите ответ в свободной форме........`

1. `Заполните здесь этапы выполнения, если требуется ....`
2. `Заполните здесь этапы выполнения, если требуется ....`
3. `Заполните здесь этапы выполнения, если требуется ....`
4. `Заполните здесь этапы выполнения, если требуется ....`
5. `Заполните здесь этапы выполнения, если требуется ....`
6. 

```
Поле для вставки кода...
....
....
....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота](ссылка на скриншот)`
