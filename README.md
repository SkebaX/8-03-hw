# Домашнее задание к занятию «`GitLab`» 
`Скобелкин А.В.`

### Задание 1

Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в этом репозитории.
Создайте новый проект и пустой репозиторий в нём.
Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.


```





---

### Задание 2

1. `Запушьте репозиторий на GitLab, изменив origin. Это изучалось на занятии по Git.`
2. `Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.`

```
Поле для вставки кода...
concurrent = 1
check_interval = 0
connection_max_age = "15m0s"
shutdown_timeout = 0

[session_server]
  session_timeout = 1800

[[runners]]
  name = "my_project"
  url = "http://192.168.56.10"
  id = 7
  token = "glrtr-BNMX6h_YdUZslGWZDxPjPG86MQpwOjEKdDozCw.01.120s4svpz"
  token_obtained_at = 2026-05-27T06:10:56Z
  token_expires_at = 0001-01-01T00:00:00Z
  executor = "docker"
  [runners.cache]
    MaxUploadedArchiveSize = 0
    [runners.cache.s3]
      AssumeRoleMaxConcurrency = 0
    [runners.cache.gcs]
    [runners.cache.azure]
  [runners.docker]
    tls_verify = false
    image = "golang:1.21"
    privileged = false
    disable_entrypoint_overwrite = false
    oom_kill_disable = false
    disable_cache = false
#   volumes = ["/cache"]
    volumes = ["/cache", "/var/run/docker.sock:/var/run/docker.sock"]
    volume_keep = false
    shm_size = 0
    network_mtu = 0


`При необходимости прикрепитe сюда скриншоты
![Название скриншота 2](ссылка на скриншот 2)`


---

