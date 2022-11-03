Welcome to Cloud Shell! Type "help" to get started.
To set your Cloud Platform project in this session use “gcloud config set project [PROJECT_ID]”
dylanwallace@cloudshell:~$ ls
app  README-cloudshell.txt
dylanwallace@cloudshell:~$ readme-cloudshell.txt
-bash: readme-cloudshell.txt: command not found
dylanwallace@cloudshell:~$ rm -r app
dylanwallace@cloudshell:~$ dir
README-cloudshell.txt
dylanwallace@cloudshell:~$ unzip app.zip
Archive:  app.zip
  inflating: app/.DS_Store
  inflating: app/app.py
  inflating: app/Dockerfile
 extracting: app/requirements.txt
   creating: app/templates/
  inflating: app/templates/index-en.html
  inflating: app/templates/index-pt.html
dylanwallace@cloudshell:~$ ls
app  app.zip  README-cloudshell.txt
dylanwallace@cloudshell:~$ cd app
dylanwallace@cloudshell:~/app$ ls
app.py  Dockerfile  requirements.txt  templates
dylanwallace@cloudshell:~/app$ docker build -t apptest:1.0 .
Sending build context to Docker daemon  18.94kB
Step 1/7 : FROM python:3
3: Pulling from library/python
17c9e6141fdb: Pull complete
de4a4c6caea8: Pull complete
4edced8587e6: Pull complete
a7969cffbf46: Pull complete
74fbfde6af91: Pull complete
16fe51aed899: Pull complete
e9ee507bb0de: Pull complete
4d9dbb46d211: Pull complete
3b9b3c4e849c: Pull complete
Digest: sha256:fc809ada71c087cec7e2d2244bcb9fba137638978a669f2aaf6267db43e89fdf
Status: Downloaded newer image for python:3
 ---> 00cd1fb8bdcc
Step 2/7 : COPY ./requirements.txt /app/requirements.txt
 ---> 0ae645587577
Step 3/7 : WORKDIR APP
 ---> Running in 44c58d2a1a42
Removing intermediate container 44c58d2a1a42
 ---> 21640ad70005
Step 4/7 : RUN pip install --no-cache-dir -r requirments.txt
 ---> Running in 7fbcb68eaffd
ERROR: Could not open requirements file: [Errno 2] No such file or directory: 'requirments.txt'
The command '/bin/sh -c pip install --no-cache-dir -r requirments.txt' returned a non-zero code: 1
dylanwallace@cloudshell:~/app$ rm -r app.zip
rm: cannot remove 'app.zip': No such file or directory
dylanwallace@cloudshell:~/app$ rm -r app.zip
rm: cannot remove 'app.zip': No such file or directory
dylanwallace@cloudshell:~/app$ dir
app.py  Dockerfile  requirements.txt  templates
dylanwallace@cloudshell:~/app$ cd ..
dylanwallace@cloudshell:~$ rm -r app.zip
dylanwallace@cloudshell:~$ rm -r app
dylanwallace@cloudshell:~$ ls
README-cloudshell.txt
dylanwallace@cloudshell:~$ unzip app.zip
Archive:  app.zip
   creating: app/
  inflating: app/.DS_Store
  inflating: app/app.py
  inflating: app/Dockerfile
  inflating: app/requirements.txt
   creating: app/templates/
  inflating: app/templates/index-en.html
  inflating: app/templates/index-pt.html
dylanwallace@cloudshell:~$ ls
app  app.zip  README-cloudshell.txt
dylanwallace@cloudshell:~$ cd app
dylanwallace@cloudshell:~/app$ ls
app.py  Dockerfile  requirements.txt  templates
dylanwallace@cloudshell:~/app$ docker build -t apptest:1.0 .
Sending build context to Docker daemon  18.94kB
Step 1/7 : FROM python:3
 ---> 00cd1fb8bdcc
Step 2/7 : COPY ./requirements.txt /app/requirements.txt
 ---> Using cache
 ---> 0ae645587577
Step 3/7 : WORKDIR APP
 ---> Using cache
 ---> 21640ad70005
Step 4/7 : RUN pip install --no-cache-dir -r requirements.txt
 ---> Running in a8ba8a19687f
ERROR: Could not open requirements file: [Errno 2] No such file or directory: 'requirements.txt'
The command '/bin/sh -c pip install --no-cache-dir -r requirements.txt' returned a non-zero code: 1
dylanwallace@cloudshell:~/app$ rm -r app.zip
rm: cannot remove 'app.zip': No such file or directory
dylanwallace@cloudshell:~/app$ cd ..
dylanwallace@cloudshell:~$ rm -r app.zip
dylanwallace@cloudshell:~$ rm -r app
dylanwallace@cloudshell:~$ ls
app.zip  README-cloudshell.txt
dylanwallace@cloudshell:~$ unzip app.zip
Archive:  app.zip
   creating: app/
  inflating: app/.DS_Store
  inflating: app/app.py
  inflating: app/Dockerfile
  inflating: app/requirements.txt
   creating: app/templates/
  inflating: app/templates/index-en.html
  inflating: app/templates/index-pt.html
dylanwallace@cloudshell:~$ ls
app  app.zip  README-cloudshell.txt
dylanwallace@cloudshell:~$ cd app
dylanwallace@cloudshell:~/app$ ls
app.py  Dockerfile  requirements.txt  templates
dylanwallace@cloudshell:~/app$ docker build -t apptest:1.0 .
Sending build context to Docker daemon  18.94kB
Step 1/7 : FROM python:3
 ---> 00cd1fb8bdcc
Step 2/7 : COPY ./requirements.txt /app/requirements.txt
 ---> Using cache
 ---> 0ae645587577
Step 3/7 : WORKDIR /APP
 ---> Using cache
 ---> 21640ad70005
Step 4/7 : RUN pip install --no-cache-dir -r requirements.txt
 ---> Running in eaac9eb63af3
ERROR: Could not open requirements file: [Errno 2] No such file or directory: 'requirements.txt'
The command '/bin/sh -c pip install --no-cache-dir -r requirements.txt' returned a non-zero code: 1
dylanwallace@cloudshell:~/app$ cd ..
dylanwallace@cloudshell:~$ ls
app  app.zip  README-cloudshell.txt
dylanwallace@cloudshell:~$ rm -r app.zip
dylanwallace@cloudshell:~$ rm -r app
dylanwallace@cloudshell:~$ unzip app.zip
Archive:  app.zip
   creating: app/
  inflating: app/.DS_Store
  inflating: app/app.py
  inflating: app/Dockerfile
  inflating: app/requirements.txt
   creating: app/templates/
  inflating: app/templates/index-en.html
  inflating: app/templates/index-pt.html
dylanwallace@cloudshell:~$ ls
app  app.zip  README-cloudshell.txt
dylanwallace@cloudshell:~$ cd
dylanwallace@cloudshell:~$ cd app
dylanwallace@cloudshell:~/app$ ls
app.py  Dockerfile  requirements.txt  templates
dylanwallace@cloudshell:~/app$ docker container run --name apptest01 -p 5000:5000 app:1.0
Unable to find image 'app:1.0' locally
docker: Error response from daemon: pull access denied for app, repository does not exist or may require 'docker login': denied: requested access to the resource is denied.
See 'docker run --help'.
dylanwallace@cloudshell:~/app$ docker container run --name app -p 5000:5000 app:1.0
Unable to find image 'app:1.0' locally
docker: Error response from daemon: pull access denied for app, repository does not exist or may require 'docker login': denied: requested access to the resource is denied.
See 'docker run --help'.
dylanwallace@cloudshell:~/app$ docker container run --name app -p 5000:5000
"docker container run" requires at least 1 argument.
See 'docker container run --help'.

Usage:  docker container run [OPTIONS] IMAGE [COMMAND] [ARG...]

Run a command in a new container
dylanwallace@cloudshell:~/app$ docker container run --name app -p 5000:5000 app:1.0.0
Unable to find image 'app:1.0.0' locally
docker: Error response from daemon: pull access denied for app, repository does not exist or may require 'docker login': denied: requested access to the resource is denied.
See 'docker run --help'.
dylanwallace@cloudshell:~/app$ docker container run --name app -p 5000:5000 apptest:1.0                                                                                                                                                          
 * Serving Flask app 'app'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5000
 * Running on http://172.18.0.2:5000
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 103-440-541
172.18.0.1 - - [03/Nov/2022 01:23:42] "GET /?authuser=0&redirectedPreviously=true HTTP/1.1" 200 -
172.18.0.1 - - [03/Nov/2022 01:23:42] "GET /jumbotron.css HTTP/1.1" 200 -
172.18.0.1 - - [03/Nov/2022 01:23:43] "GET /favicon.ico HTTP/1.1" 200 -
172.18.0.1 - - [03/Nov/2022 01:36:01] "GET /?authuser=0 HTTP/1.1" 200 -
172.18.0.1 - - [03/Nov/2022 01:36:01] "GET /jumbotron.css HTTP/1.1" 200 -
172.18.0.1 - - [03/Nov/2022 01:36:01] "GET /favicon.ico HTTP/1.1" 200 -
^Cdylanwallace@cloudshell:~/app$ docker container run --name app -p 5000:5000 apptest:1.0                                                                                                                                                        
docker: Error response from daemon: Conflict. The container name "/app" is already in use by container "4b1cd7a4b49958b12069a6e376a794cc3b354b70beff3af8be6951bfccf14faa". You have to remove (or rename) that container to be able to reuse that name.
See 'docker run --help'.
dylanwallace@cloudshell:~/app$ docker run
apptest      apptest:1.0  python       python:3
dylanwallace@cloudshell:~/app$ docker run apptest:1.0
 * Serving Flask app 'app'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5000
 * Running on http://172.18.0.2:5000
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 736-587-742
ping http://127.0.0.1:5000
clear   
^Cdylanwallace@cloudshell:~/app$ docker run apptest:1.0
 * Serving Flask app 'app'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5000
 * Running on http://172.18.0.2:5000
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 290-292-155
^Cdylanwallace@cloudshell:~/app$ sudo ufw allow 5000
sudo: ufw: command not found
dylanwallace@cloudshell:~/app$ sudo  allow 5000
sudo: allow: command not found
dylanwallace@cloudshell:~/app$ sudo allow 5000
sudo: allow: command not found
dylanwallace@cloudshell:~/app$ sudo
usage: sudo -h | -K | -k | -V
usage: sudo -v [-AknS] [-g group] [-h host] [-p prompt] [-u user]
usage: sudo -l [-AknS] [-g group] [-h host] [-p prompt] [-U user] [-u user] [command]
usage: sudo [-AbEHknPS] [-r role] [-t type] [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-T timeout] [-u user] [VAR=value] [-i|-s] [<command>]
usage: sudo -e [-AknS] [-r role] [-t type] [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-T timeout] [-u user] file ...
dylanwallace@cloudshell:~/app$ docker run apptest
Unable to find image 'apptest:latest' locally
docker: Error response from daemon: pull access denied for apptest, repository does not exist or may require 'docker login': denied: requested access to the resource is denied.
See 'docker run --help'.
dylanwallace@cloudshell:~/app$ docker ls
docker: 'ls' is not a docker command.
See 'docker --help'
dylanwallace@cloudshell:~/app$ ls
app.py  Dockerfile  requirements.txt  templates
dylanwallace@cloudshell:~/app$ docker run
"docker run" requires at least 1 argument.
See 'docker run --help'.

Usage:  docker run [OPTIONS] IMAGE [COMMAND] [ARG...]

Run a command in a new container
dylanwallace@cloudshell:~/app$ docker container

Usage:  docker container COMMAND

Manage containers

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  inspect     Display detailed information on one or more containers
  kill        Kill one or more running containers
  logs        Fetch the logs of a container
  ls          List containers
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  prune       Remove all stopped containers
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  run         Run a command in a new container
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  wait        Block until one or more containers stop, then print their exit codes

Run 'docker container COMMAND --help' for more information on a command.
dylanwallace@cloudshell:~/app$ docker container ls
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
dylanwallace@cloudshell:~/app$ docker contasiner port
docker: 'contasiner' is not a docker command.
See 'docker --help'
dylanwallace@cloudshell:~/app$ docker container port
"docker container port" requires at least 1 and at most 2 arguments.
See 'docker container port --help'.

Usage:  docker container port CONTAINER [PRIVATE_PORT[/PROTO]]

List port mappings or a specific mapping for the container
dylanwallace@cloudshell:~/app$ docker container run --name app -p 5000:5000 apptest:1.0
docker: Error response from daemon: Conflict. The container name "/app" is already in use by container "4b1cd7a4b49958b12069a6e376a794cc3b354b70beff3af8be6951bfccf14faa". You have to remove (or rename) that container to be able to reuse that name.
See 'docker run --help'.
dylanwallace@cloudshell:~/app$ docker run apptest:1.0
 * Serving Flask app 'app'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5000
 * Running on http://172.18.0.2:5000
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 557-347-813
container docker container ls
^Cdylanwallace@cloudshell:~/app$ docker container ls
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
dylanwallace@cloudshell:~/app$ docker port apptest:1.0
Error: No such container: apptest:1.0
dylanwallace@cloudshell:~/app$ docker container ls
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
dylanwallace@cloudshell:~/app$ docker container docker image ls

Usage:  docker container COMMAND

Manage containers

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  inspect     Display detailed information on one or more containers
  kill        Kill one or more running containers
  logs        Fetch the logs of a container
  ls          List containers
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  prune       Remove all stopped containers
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  run         Run a command in a new container
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  wait        Block until one or more containers stop, then print their exit codes

Run 'docker container COMMAND --help' for more information on a command.
dylanwallace@cloudshell:~/app$ docker container ls
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
dylanwallace@cloudshell:~/app$ docker container ls --all
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS                      PORTS     NAMES
cacc11c51ab3   apptest:1.0    "python app.py"          9 minutes ago    Exited (0) 6 minutes ago              pensive_tesla
12837698d7da   apptest:1.0    "python app.py"          13 minutes ago   Exited (0) 12 minutes ago             nostalgic_germain
ff4f476cdc07   apptest:1.0    "python app.py"          15 minutes ago   Exited (0) 13 minutes ago             focused_jepsen
4b1cd7a4b499   apptest:1.0    "python app.py"          31 minutes ago   Exited (0) 18 minutes ago             app
eaac9eb63af3   21640ad70005   "/bin/sh -c 'pip ins…"   40 minutes ago   Exited (1) 40 minutes ago             loving_feistel
a8ba8a19687f   21640ad70005   "/bin/sh -c 'pip ins…"   42 minutes ago   Exited (1) 42 minutes ago             strange_pascal
7fbcb68eaffd   21640ad70005   "/bin/sh -c 'pip ins…"   47 minutes ago   Exited (1) 47 minutes ago             epic_perlman
dylanwallace@cloudshell:~/app$ docker container start app
app
dylanwallace@cloudshell:~/app$ docker container start apptest:1.0
Error response from daemon: No such container: apptest:1.0
Error: failed to start containers: apptest:1.0
dylanwallace@cloudshell:~/app$ docker run apptest:1.0                                                                                                                                                                                            
 * Serving Flask app 'app'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5000
 * Running on http://172.18.0.3:5000
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 211-507-014
^Cdylanwallace@cloudshell:~/app$ ^C
dylanwallace@cloudshell:~/app$ docker container ls --all                                                                                                                                                                                         
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS                      PORTS                    NAMES
6a7c97ee06c6   apptest:1.0    "python app.py"          6 minutes ago    Exited (0) 2 minutes ago                             magical_germain
cacc11c51ab3   apptest:1.0    "python app.py"          17 minutes ago   Exited (0) 14 minutes ago                            pensive_tesla
12837698d7da   apptest:1.0    "python app.py"          21 minutes ago   Exited (0) 20 minutes ago                            nostalgic_germain
ff4f476cdc07   apptest:1.0    "python app.py"          23 minutes ago   Exited (0) 21 minutes ago                            focused_jepsen
4b1cd7a4b499   apptest:1.0    "python app.py"          38 minutes ago   Up 6 minutes                0.0.0.0:5000->5000/tcp   app
eaac9eb63af3   21640ad70005   "/bin/sh -c 'pip ins…"   47 minutes ago   Exited (1) 47 minutes ago                            loving_feistel
a8ba8a19687f   21640ad70005   "/bin/sh -c 'pip ins…"   50 minutes ago   Exited (1) 50 minutes ago                            strange_pascal
7fbcb68eaffd   21640ad70005   "/bin/sh -c 'pip ins…"   55 minutes ago   Exited (1) 55 minutes ago                            epic_perlman
dylanwallace@cloudshell:~/app$ docker container start app
app
dylanwallace@cloudshell:~/app$ docker container ls
CONTAINER ID   IMAGE         COMMAND           CREATED          STATUS         PORTS                    NAMES
4b1cd7a4b499   apptest:1.0   "python app.py"   39 minutes ago   Up 7 minutes   0.0.0.0:5000->5000/tcp   app
dylanwallace@cloudshell:~/app$ docker port app
5000/tcp -> 0.0.0.0:5000
dylanwallace@cloudshell:~/app$ docker container stop apptest
Error response from daemon: No such container: apptest
dylanwallace@cloudshell:~/app$ docker container ls --all
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS                      PORTS                    NAMES
6a7c97ee06c6   apptest:1.0    "python app.py"          8 minutes ago    Exited (0) 4 minutes ago                             magical_germain
cacc11c51ab3   apptest:1.0    "python app.py"          19 minutes ago   Exited (0) 16 minutes ago                            pensive_tesla
12837698d7da   apptest:1.0    "python app.py"          24 minutes ago   Exited (0) 22 minutes ago                            nostalgic_germain
ff4f476cdc07   apptest:1.0    "python app.py"          25 minutes ago   Exited (0) 24 minutes ago                            focused_jepsen
4b1cd7a4b499   apptest:1.0    "python app.py"          41 minutes ago   Up 9 minutes                0.0.0.0:5000->5000/tcp   app
eaac9eb63af3   21640ad70005   "/bin/sh -c 'pip ins…"   50 minutes ago   Exited (1) 50 minutes ago                            loving_feistel
a8ba8a19687f   21640ad70005   "/bin/sh -c 'pip ins…"   53 minutes ago   Exited (1) 53 minutes ago                            strange_pascal
7fbcb68eaffd   21640ad70005   "/bin/sh -c 'pip ins…"   57 minutes ago   Exited (1) 57 minutes ago                            epic_perlman
dylanwallace@cloudshell:~/app$ docker container stop app
app
dylanwallace@cloudshell:~/app$ docker container ls --all
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS                      PORTS     NAMES
6a7c97ee06c6   apptest:1.0    "python app.py"          9 minutes ago    Exited (0) 4 minutes ago              magical_germain
cacc11c51ab3   apptest:1.0    "python app.py"          20 minutes ago   Exited (0) 17 minutes ago             pensive_tesla
12837698d7da   apptest:1.0    "python app.py"          24 minutes ago   Exited (0) 23 minutes ago             nostalgic_germain
ff4f476cdc07   apptest:1.0    "python app.py"          26 minutes ago   Exited (0) 24 minutes ago             focused_jepsen
4b1cd7a4b499   apptest:1.0    "python app.py"          41 minutes ago   Exited (0) 10 seconds ago             app
eaac9eb63af3   21640ad70005   "/bin/sh -c 'pip ins…"   50 minutes ago   Exited (1) 50 minutes ago             loving_feistel
a8ba8a19687f   21640ad70005   "/bin/sh -c 'pip ins…"   53 minutes ago   Exited (1) 53 minutes ago             strange_pascal
7fbcb68eaffd   21640ad70005   "/bin/sh -c 'pip ins…"   58 minutes ago   Exited (1) 58 minutes ago             epic_perlman
dylanwallace@cloudshell:~/app$ docker image rm epic_perlman
Error: No such image: epic_perlman
dylanwallace@cloudshell:~/app$ docker container rm epic_perlman
epic_perlman
dylanwallace@cloudshell:~/app$ docker container ls --all
CONTAINER ID   IMAGE          COMMAND                  CREATED             STATUS                         PORTS     NAMES
6a7c97ee06c6   apptest:1.0    "python app.py"          18 minutes ago      Exited (0) 14 minutes ago                magical_germain
cacc11c51ab3   apptest:1.0    "python app.py"          29 minutes ago      Exited (0) 26 minutes ago                pensive_tesla
12837698d7da   apptest:1.0    "python app.py"          33 minutes ago      Exited (0) 32 minutes ago                nostalgic_germain
ff4f476cdc07   apptest:1.0    "python app.py"          35 minutes ago      Exited (0) 33 minutes ago                focused_jepsen
4b1cd7a4b499   apptest:1.0    "python app.py"          50 minutes ago      Exited (0) 9 minutes ago                 app
eaac9eb63af3   21640ad70005   "/bin/sh -c 'pip ins…"   About an hour ago   Exited (1) 59 minutes ago                loving_feistel
a8ba8a19687f   21640ad70005   "/bin/sh -c 'pip ins…"   About an hour ago   Exited (1) About an hour ago             strange_pascal
dylanwallace@cloudshell:~/app$ docker container rm focused_jepsen
focused_jepsen
dylanwallace@cloudshell:~/app$ docker container rm nostalgic_hermain
Error: No such container: nostalgic_hermain
dylanwallace@cloudshell:~/app$ docker container rm nostalgic_germain
nostalgic_germain
dylanwallace@cloudshell:~/app$ docker cotainer rm focused_jepsen
docker: 'cotainer' is not a docker command.
See 'docker --help'
dylanwallace@cloudshell:~/app$ docker container rm focused_jepsen
Error: No such container: focused_jepsen
dylanwallace@cloudshell:~/app$ docker container ls --all
CONTAINER ID   IMAGE          COMMAND                  CREATED             STATUS                         PORTS     NAMES
6a7c97ee06c6   apptest:1.0    "python app.py"          20 minutes ago      Exited (0) 15 minutes ago                magical_germain
cacc11c51ab3   apptest:1.0    "python app.py"          31 minutes ago      Exited (0) 28 minutes ago                pensive_tesla
4b1cd7a4b499   apptest:1.0    "python app.py"          52 minutes ago      Exited (0) 11 minutes ago                app
eaac9eb63af3   21640ad70005   "/bin/sh -c 'pip ins…"   About an hour ago   Exited (1) About an hour ago             loving_feistel
a8ba8a19687f   21640ad70005   "/bin/sh -c 'pip ins…"   About an hour ago   Exited (1) About an hour ago             strange_pascal
dylanwallace@cloudshell:~/app$ container ls rm strange_pascal
-bash: container: command not found
dylanwallace@cloudshell:~/app$ docker container ls --all
CONTAINER ID   IMAGE          COMMAND                  CREATED             STATUS                         PORTS     NAMES
6a7c97ee06c6   apptest:1.0    "python app.py"          26 minutes ago      Exited (0) 21 minutes ago                magical_germain
cacc11c51ab3   apptest:1.0    "python app.py"          36 minutes ago      Exited (0) 34 minutes ago                pensive_tesla
4b1cd7a4b499   apptest:1.0    "python app.py"          58 minutes ago      Exited (0) 17 minutes ago                app
eaac9eb63af3   21640ad70005   "/bin/sh -c 'pip ins…"   About an hour ago   Exited (1) About an hour ago             loving_feistel
a8ba8a19687f   21640ad70005   "/bin/sh -c 'pip ins…"   About an hour ago   Exited (1) About an hour ago             strange_pascal
dylanwallace@cloudshell:~/app$ container rm magical_germain
-bash: container: command not found
dylanwallace@cloudshell:~/app$ docker container rm magical_germain
magical_germain
dylanwallace@cloudshell:~/app$ docker container rm strange_pascal
strange_pascal
dylanwallace@cloudshell:~/app$ docker container rm pensive_tesla
pensive_tesla
dylanwallace@cloudshell:~/app$ docker container rm magical_germain
Error: No such container: magical_germain
dylanwallace@cloudshell:~/app$ docker cotainer ls --all
unknown flag: --all
See 'docker --help'.

Usage:  docker [OPTIONS] COMMAND

A self-sufficient runtime for containers

Options:
      --config string      Location of client config files (default "/home/dylanwallace/.docker")
  -c, --context string     Name of the context to use to connect to the daemon (overrides DOCKER_HOST env var and default context set with "docker context use")
  -D, --debug              Enable debug mode
  -H, --host list          Daemon socket(s) to connect to
  -l, --log-level string   Set the logging level ("debug"|"info"|"warn"|"error"|"fatal") (default "info")
      --tls                Use TLS; implied by --tlsverify
      --tlscacert string   Trust certs signed only by this CA (default "/home/dylanwallace/.docker/ca.pem")
      --tlscert string     Path to TLS certificate file (default "/home/dylanwallace/.docker/cert.pem")
      --tlskey string      Path to TLS key file (default "/home/dylanwallace/.docker/key.pem")
      --tlsverify          Use TLS and verify the remote
  -v, --version            Print version information and quit

Management Commands:
  app*        Docker App (Docker Inc., v0.9.1-beta3)
  builder     Manage builds
  buildx*     Docker Buildx (Docker Inc., v0.9.1-docker)
  config      Manage Docker configs
  container   Manage containers
  context     Manage contexts
  image       Manage images
  manifest    Manage Docker image manifests and manifest lists
  network     Manage networks
  node        Manage Swarm nodes
  plugin      Manage plugins
  scan*       Docker Scan (Docker Inc., v0.17.0)
  secret      Manage Docker secrets
  service     Manage services
  stack       Manage Docker stacks
  swarm       Manage Swarm
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  build       Build an image from a Dockerfile
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  images      List images
  import      Import the contents from a tarball to create a filesystem image
  info        Display system-wide information
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  login       Log in to a Docker registry
  logout      Log out from a Docker registry
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  ps          List containers
  pull        Pull an image or a repository from a registry
  push        Push an image or a repository to a registry
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  run         Run a command in a new container
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  search      Search the Docker Hub for images
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  version     Show the Docker version information
  wait        Block until one or more containers stop, then print their exit codes

Run 'docker COMMAND --help' for more information on a command.

To get more help with docker, check out our guides at https://docs.docker.com/go/guides/

dylanwallace@cloudshell:~/app$ docker cotainer ls --all
unknown flag: --all
See 'docker --help'.

Usage:  docker [OPTIONS] COMMAND

A self-sufficient runtime for containers

Options:
      --config string      Location of client config files (default "/home/dylanwallace/.docker")
  -c, --context string     Name of the context to use to connect to the daemon (overrides DOCKER_HOST env var and default context set with "docker context use")
  -D, --debug              Enable debug mode
  -H, --host list          Daemon socket(s) to connect to
  -l, --log-level string   Set the logging level ("debug"|"info"|"warn"|"error"|"fatal") (default "info")
      --tls                Use TLS; implied by --tlsverify
      --tlscacert string   Trust certs signed only by this CA (default "/home/dylanwallace/.docker/ca.pem")
      --tlscert string     Path to TLS certificate file (default "/home/dylanwallace/.docker/cert.pem")
      --tlskey string      Path to TLS key file (default "/home/dylanwallace/.docker/key.pem")
      --tlsverify          Use TLS and verify the remote
  -v, --version            Print version information and quit

Management Commands:
  app*        Docker App (Docker Inc., v0.9.1-beta3)
  builder     Manage builds
  buildx*     Docker Buildx (Docker Inc., v0.9.1-docker)
  config      Manage Docker configs
  container   Manage containers
  context     Manage contexts
  image       Manage images
  manifest    Manage Docker image manifests and manifest lists
  network     Manage networks
  node        Manage Swarm nodes
  plugin      Manage plugins
  scan*       Docker Scan (Docker Inc., v0.17.0)
  secret      Manage Docker secrets
  service     Manage services
  stack       Manage Docker stacks
  swarm       Manage Swarm
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  build       Build an image from a Dockerfile
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  images      List images
  import      Import the contents from a tarball to create a filesystem image
  info        Display system-wide information
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  login       Log in to a Docker registry
  logout      Log out from a Docker registry
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  ps          List containers
  pull        Pull an image or a repository from a registry
  push        Push an image or a repository to a registry
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  run         Run a command in a new container
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
dylanwallace@cloudshell:~/app$ docker container ls --all
CONTAINER ID   IMAGE         COMMAND           CREATED          STATUS                      PORTS     NAMES
3b833f7a331b   apptest:1.0   "python app.py"   41 minutes ago   Exited (0) 25 minutes ago             sad_newton
4b1cd7a4b499   apptest:1.0   "python app.py"   2 hours ago      Exited (0) 25 minutes ago             app
dylanwallace@cloudshell:~/app$ docker tag app:1.0 us.gcr.io/sustained-vial-367500/app
Error response from daemon: No such image: app:1.0
dylanwallace@cloudshell:~/app$ docker tag apptest:1.0 us.gcr.io/sustained-vial-367500/app
dylanwallace@cloudshell:~/app$ docker image ls
REPOSITORY                            TAG       IMAGE ID       CREATED       SIZE
apptest                               1.0       e2f171a8efae   2 hours ago   951MB
us.gcr.io/sustained-vial-367500/app   latest    e2f171a8efae   2 hours ago   951MB
<none>                                <none>    21640ad70005   2 hours ago   932MB
python                                3         00cd1fb8bdcc   8 days ago    932MB
dylanwallace@cloudshell:~/app$ docker container ls
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
dylanwallace@cloudshell:~/app$ docker container ls --all
CONTAINER ID   IMAGE         COMMAND           CREATED          STATUS                      PORTS     NAMES
3b833f7a331b   apptest:1.0   "python app.py"   51 minutes ago   Exited (0) 34 minutes ago             sad_newton
4b1cd7a4b499   apptest:1.0   "python app.py"   2 hours ago      Exited (0) 34 minutes ago             app
dylanwallace@cloudshell:~/app$ docker image ls
REPOSITORY                            TAG       IMAGE ID       CREATED       SIZE
apptest                               1.0       e2f171a8efae   2 hours ago   951MB
us.gcr.io/sustained-vial-367500/app   latest    e2f171a8efae   2 hours ago   951MB
<none>                                <none>    21640ad70005   2 hours ago   932MB
python                                3         00cd1fb8bdcc   8 days ago    932MB
dylanwallace@cloudshell:~/app$ docker push us.gcr.io/sustained-vial-367500/app
Using default tag: latest
The push refers to repository [us.gcr.io/sustained-vial-367500/app]
fb80647e445c: Pushed
425465dfd3f8: Pushed
b09f1371edfa: Pushed
6f6e69c2c592: Layer already exists
53b8bfee7a0a: Layer already exists
5b3f1ed98915: Layer already exists
6b183c62e3d7: Layer already exists
882fd36bfd35: Layer already exists
d1dec9917839: Layer already exists
d38adf39e1dd: Layer already exists
4ed121b04368: Layer already exists
d9d07d703dd5: Layer already exists
latest: digest: sha256:45a0f9662be88f824366c3a0519d9c888d1dc348f2eb5a54928b98b6413935ea size: 2844
dylanwallace@cloudshell:~/app$