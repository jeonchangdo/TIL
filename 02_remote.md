# 원격저장소 활용

> 원격 저장소(remote repository)를 제공하는 서비스는 github, gitlab, bitbucket 등이 있다.

## 1. 원격저장소 설정하기

```bash
$ git remote add origin ________
```

* 깃아, 원격저장소를 추가해줘.(add) origin 이라는 이름으로 URL을!!
* 원격저장소 설정을 삭제하는 명력어는 다음과 같다.

```bash
$ git remote rm origin

```

리무브



## 2. 원격 저장소 확인하기

```bash
$ git remote -v
origin  https://github.com/jeonchangdo/project-test.git (fetch)
origin  https://github.com/jeonchangdo/project-test.git (push)

```

## 3.push

``` bash
$ git push origin master
```





