### Structure
```bash
── /lambda-selenium-layer/
  ├── /selenium
  │  └──/python/
  │   └── /lib/
  │     └── /python3.6/*
  ├── /chromedriver/
  │ ├── /chromedriver
  │ └── /headless-chromium
  └── /serverless.yaml
```


### For selenium installation
```bash
# download Selenium 2.37
$ pip3.6 install -t selenium/python/lib/python3.6/site-packages selenium=2.37

### Manual Instalation
# download chrome driver
$ mkdir chromedriver
$ cd chromedriver
$ curl -SL https://chromedriver.storage.googleapis.com/2.37/chromedriver_linux64.zip > chromedriver.zip
$ unzip chromedriver.zip
$ rm chromedriver.zip
$ curl -SL https://github.com/adieuadieu/serverless-chrome/releases/download/v1.0.0-41/stable-headless-chromium-amazonlinux-2017-03.zip > headless-chromium.zip
$ unzip headless-chromium.zip
$ rm headless-chromium.zip
```

### Stack

- Python3.6
- Selenium2.37
- [ChromeDriver2.37](https://sites.google.com/a/chromium.org/chromedriver/downloads)
- [Serverless Chrome v1.0.0.41 ](https://github.com/adieuadieu/serverless-chrome/releases?after=v1.0.0-46)

### Deploy Lambda Layers
Go to root directory of project
```bash
$ cd seleniumLayer
$ sls deploy
```

