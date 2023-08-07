# t2tanic webapp

![T2taNic](https://images.chosun.com/resizer/gE-go0I5-2QsuwlgUUavoU3SfiI=/616x0/smart/cloudfront-ap-northeast-1.images.arcpublishing.com/chosun/TPUMVAPDGDTDD2ST4RDJB56LVU.jpg)

## ENV
- python 3.9

- pyenv
```
$ pyenv install --list
$ pyenv install 3.9.16
$ pyenv global 3.9.16
$ pyenv versions
pyenv versions
  system
  3.7.16
* 3.9.16 (set by /home/tom/.pyenv/version)
```

- pipenv
```
$ pip install pipenv
$ pipenv --python 3.9.16
$ pipenv shell
```

## DEV
```
$ pipenv shell
$ pipenv install streamlit
```

## RUN
- cd app;streamlit run app.py

## DEPLOY
```
$ docker build -t tatiatic-webapp:0.2.4
$ docker images tatiatic-webapp
REPOSITORY        TAG       IMAGE ID       CREATED          SIZE
tatiatic-webapp   0.1.0     c891796ee3ba   18 seconds ago   1.05GB

$ docker run --name tatiatic-webapp024 -d -p 7024:8051 tatiatic-webapp:0.2.4
$ sudo docker ps
CONTAINER ID   IMAGE                     COMMAND                  CREATED         STATUS                            PORTS                                                 NAMES
b17d1a501ee9   tatiatic-webapp:0.1.0     "streamlit run app.p…"   7 seconds ago   Up 6 seconds (health: starting)   8501/tcp, 0.0.0.0:7010->8051/tcp, :::7010->8051/tcp   tatiatic-webapp010
```

## REF
- https://30days.streamlit.app/?challenge=Day2
