# git 가볍게 이해해보기

### add
```
$ git add .
```
- git이라는 프로그램한테 add라는 명령을 시킨다.
- . => 현재 폴더에 있는 파일과 모든 폴더
- 모든파일을 add 시켜줘

### commit
```
$ git commit -m "메세지"
```
- git 프로그램아 현재 index에 모아진 파일들을 저장시켜줘
- 저장할 때 메세지는 "메세지" <=이것이다


### remote
```
git remote add origin <주소>
```

- 원격저장소 <주소>를 add해줘 별명은 origin으로 지어줄께

### push
```
git push -u origin master
```

- git! master를 origin으로 push해줘
- 누구십니까 -> 아이디, 패스워드