# hitcon-ctf-2018-one-line-php-challenge
https://github.com/orangetw/My-CTF-Web-Challenges/tree/master/hitcon-ctf-2018/one-line-php-challenge

# Reference
https://github.com/tarunkant/Automation/blob/master/RCE_through_include.py

# Little figure
由於這個docker本身不具備/var/lib/php/sessions的路徑。
所以參考的code會注入失敗(因為找不到session file)。
因此需要配合這個exploit修改路徑，改而針對/tmp進行注入取得reverse shell。

## Getting started
### Build

```
$ docker build -t hitcon .
```

### Run

```
$ docker run --rm -it -p 8000:80 --network bridge hitcon
```

Visit http://localhost:8000

