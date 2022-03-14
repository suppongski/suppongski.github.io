---
layout: post
title: 2주차 과제
subtitle: 수업내용 및 추가 관련내용 포스트하여 링크
categories: 과제
tags: [github, 과제]
---
## 알고리즘의 성능평가  
1. BIG-OH-notation
    * 자신의 알고리즘의 Time Complexity가 *f(x)*라고 할때 임의의 알고리즘 *g(x)*에 대하여 *f(x)*는 *cg(x)* 보다 ***빠르지*** 않을때 *cg(x)*를 점근적 **상한**이라고 한다.  
2. Omega-notation
    * 자신의 알고리즘의 Time Complexity가 *f(x)*라고 할때 임의의 알고리즘 *g(x)*에 대하여 *f(x)*는 *cg(x)* 보다 ***느리지*** 않을때 *cg(x)*를 점근적 **하한**이라고 한다.  
3. Theta-notation
    * 자신의 알고리즘의 Time Complexity가 *f(x)*라고 할때 임의의 알고리즘 *g(x)*에 대하여 *f(x)*는 *c1g(x)* 보다 빠르지 않고 *c2g(x)*보다 느리지 않을때 *c1g(x)*과 *c2g(x)*를 성능 비교대상으로 쓴다.  




## Git / Github
* git: 버전관리시스템(vcs) : 저장소
* github: git -> 온라인 저장소: 협업툴
* github pages: 웹 호스팅: 무료 (지킬)


# 명령어

* 저장소 초기화  
`git init [directory]`  
`git clone [repository] [directory]`

* 버전 관리  
`git pull` : 온라인 저장소 -> 로컬 저장소 다운로드  
`git add [file...]` : 커밋할 파일들 스테이징  
`git commit -m [message]` : 스테이징 파일 -> 버전 업데이트  
`git push` : 로컬 저장소 -> 온라인 저장소 업로드  

* 상태  
`git status`  
`git log`