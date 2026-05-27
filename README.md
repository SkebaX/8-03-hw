# Домашнее задание к занятию «`GitLab`» 
`Скобелкин А.В.`

### Задание 1

1. `Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в этом репозитории`
2. `Создайте новый проект и пустой репозиторий в нём.`
3. `Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab`

```
```


<img width="1709" height="1347" alt="Снимок экрана 2026-05-26 225114" src="https://github.com/user-attachments/assets/fc5d31f8-b588-45fb-be91-5a989460d5b0" />
<img width="1797" height="1008" alt="Снимок экрана 2026-05-27 123433" src="https://github.com/user-attachments/assets/d00239c9-e2f7-4659-a2ab-f10e5f79b2c2" />

---

### Задание 2

1. `Запушьте репозиторий на GitLab, изменив origin. Это изучалось на занятии по Git.`
2. `Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы`

```
stages:
  - test
  - build


  stage: test
  image: golang:1.17
  script:
   - go test .
  tags:
   - netology
   - docker

build:
  stage: build
  image: docker:latest
  script:
   - docker build .
  tags:
   - netology
   - docker
```
<img width="1796" height="1141" alt="Снимок экрана 2026-05-27 123617" src="https://github.com/user-attachments/assets/f6e12255-af0e-4dbe-be2b-dc46b5de12bb" />
<img width="1798" height="1000" alt="Снимок экрана 2026-05-27 120327" src="https://github.com/user-attachments/assets/2efec758-7cbf-4a27-803c-b3b14ab6616d" />

---

