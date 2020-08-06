# Simple Flask App

Aplikacja Dydaktyczna wyświetlająca imię i wiadomość w różnych formatach dla zajęć
o Continuous Integration, Continuous Delivery i Continuous Deployment.

## Testujemy aplikację "Hello World"

![Hello World](./image/indeks.png)

- W projekcie wykorzystamy virtual environment, dla utworzenia hermetycznego środowisko dla aplikacji:

  ```
  # tworzymy hermetyczne środowisko dla bibliotek aplikacji:
  $ python3 -m venv .venv

  # aktywowanie hermetycznego środowiska
  $ source .venv/bin/activate
  $ pip install -r requirements.txt
  $ pip install -r test_requirements.txt

  # zobacz
  $ pip list
  ```

  Sprawdź: [tutorial venv](https://docs.python.org/3/tutorial/venv.html) oraz [biblioteki flask](http://flask.pocoo.org).

## Uruchamianie applikacji:


  * [jako zwykły program](jako-zwykły-program)

  $ python main.py

  * [albo](albo):

  $ PYTHONPATH=. FLASK_APP=hello_world flask run

## Uruchamianie testów (see: http://doc.pytest.org/en/latest/capture.html):


  $ PYTHONPATH=. py.test
  $ PYTHONPATH=. py.test --verbose -s
  $ make test
  $ make test_cov
  $ make test_xunit


# Kontynuując pracę z projektem, aktywowanie hermetycznego środowiska dla aplikacji py:

* [aktywacja](actyvacja)

$ source .venv/bin/activate

* [deaktywacja](deaktywacja)

  $ deactivate

Integracja z TravisCI:
```
 Otwórz travis-ci.org i zaloguj się używając Twojego użytkownika githuba.
 Dodaj secret z pomocą CLI travis-a:
```
## Ubuntu

Instalacja dockera (https://docs.docker.com/install/linux/docker-ce/ubuntu/):
```
* [docker_build](docker_buil)
* [docker_run](docker_run)
* [docker_push](docker_push)
* [docker_stop](docker_stop)
* [docker images](docker-images)
```
Centos

Instalacja docker-a:
```
  $ yum remove docker \
        docker-common \
        container-selinux \
        docker-selinux \
        docker-engine

  $ yum install -y yum-utils

  $ yum-config-manager \
      --add-repo \
      https://download.docker.com/linux/centos/docker-ce.repo

  $ yum makecache fast
  $ yum install -y docker-ce
  $ systemctl start docker
```
  Monitoring Reports:

  * [created Test HTTP in statuscake.com](created-Test-HTTP-in-www.statuscake.com)
  * [Status for application in TravisCI](Status-for-application-in-TravisCI)

  Test Results:
```
  <a href="https://www.statuscake.com" title="Website Uptime Monitoring"><img src="https://app.statuscake.com/button/index.php?Track=RD6iqYHdjI&Days=1&Design=1" /></a>
```
  # Status for application in TravisCI:

  [![Build Status](https://www.travis-ci.org/korzeniowska18/se_hello_printer_app.svg?branch=master)](https://www.travis-ci.org/korzeniowska18/se_hello_printer_app)
