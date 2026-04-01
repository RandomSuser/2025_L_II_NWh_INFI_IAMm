# Simple Flask App


Aplikacja Dydaktyczna wyświetlająca imię i wiadomość w różnych formatach dla zajęć
o Continuous Integration, Continuous Delivery i Continuous Deployment.

- W projekcie wykorzystamy virtual environment, dla utworzenia hermetycznego środowisko dla aplikacji:

  ```
  
  #Python menager 
  docs: https://docs.python.org/dev/using/windows.html
  msstore: https://apps.microsoft.com/detail/9nq7512cxl7t
  python org: https://www.python.org/downloads/windows/
  python msix: https://www.python.org/ftp/python/pymanager/python-manager-26.1.msix
  python msi: https://www.python.org/ftp/python/pymanager/python-manager-26.1.msi
  
 
  py help
  py install --configure # rekonfiguracja taka jak przy pierwszej instalacji
  
  py install 3.12
  
  py uninstall <ver>
  py uninstall --purge  #odinstaluj wszystkie ver runtimes python
  
  py list
  py --list
  py list --online
  
  py -3.12   #wybranie konkretnej wersji
  py -3.11 -m venv .venv  #zmiana domyślnej konfiguracji w ramach venv
  
  # tworzymy hermetyczne środowisko dla bibliotek aplikacji:
  $ python -m venv .venv

  # aktywowanie hermetycznego środowiska
  $ source .venv/Scripts/activate
  $ py -m pip install --upgrade pip  
  $ pip install -r requirements.txt
  $ pip install -r test_requirements.txt

  # zobacz
  $ pip list
  ```

  Sprawdź: [tutorial venv](https://docs.python.org/3/tutorial/venv.html) oraz [biblioteki flask](http://flask.pocoo.org).

- Uruchamianie applikacji:

  ```
  # jako zwykły program
  $ python main.py

  # albo:
  $ PYTHONPATH=. FLASK_APP=hello_world flask run
  ```

- Uruchamianie testów (see: http://doc.pytest.org/en/latest/capture.html):

  ```
  $ PYTHONPATH=. py.test
  $ PYTHONPATH=. py.test --verbose -s
  ```

- Kontynuując pracę z projektem, aktywowanie hermetycznego środowiska dla aplikacji py:

  ```
  # deaktywacja
  $ deactivate
  ```

  ```
  ...

  # aktywacja 
  $ source .venv/Source/activate
  ```

- Integracja z TravisCI:

  ```
  # miejsce na twoje notatki
  ```

# Pomocnicze

## Ubuntu

- Instalacja dockera: [dockerce howto](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

## Centos

- Instalacja docker-a:

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
# Cel
```
git bash:

	Inicjacja:
	git init
	git clone

	Cyklicznie:
	git commit -a -m "$(git status --short)"
	git push 

	Opcjonalnie:
	git config -l  (alt + q)
	git add --all
	
	Powrót do Root directory:
	git rev-parse --show-toplevel    

	Testy (Root_dir):
	pythonpath=. pytest


history >> Commands.md
```