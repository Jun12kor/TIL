# 마크다운 학습

## 제목 (heading)

제목은 #으로 표현한다.

### h3
#### h4
##### h5

## 목록

- 사과
- 배
- 바나나
    - 바나나
    - 바나나

1. VS Code 설치
2. 실행...

## 코드블록

```python
print("hello world!")
```

```html
<h1>Hello, world!</h1>
<!--주석-->
```

```sql
--주석
SELECT * FROM hi;
```

## 링크

[구글](https://google.com)

[파이썬코드](./settings.py)

## 이미지

![이미지](./apple.jpg)

## 인용문

> 인용


## 테이블

|이름|나이|
|--|--|
|홍길동|60|

## 텍스트

*텍스트* **텍스트**~~텍스트~~

---

# GitHub
## GitHub에서 사용하는 Git 기반의 기본적인 명령어(VSCode)
1. git add [파일명]: 변경된 파일을 스테이징 영역(인덱스)에 추가합니다.
	- $ git add 파일명
2. git commit -m "[커밋 메시지]": 스테이징된 변경 사항을 커밋으로 저장합니다.
	- $ git commit -m "첫 번째 커밋"

3. git status: 작업 디렉토리의 변경 상태를 확인합니다.
	- $ git status
4. git log: 커밋 기록을 확인합니다.
	- $ git log
5. git remote add [원격 리포지토리 이름] [URL]: 원격 리포지토리를 로컬에 추가합니다.
	- $ git remote add origin https://github.com/사용자이름/리포지토리이름.git
6. git push [원격 리포지토리 이름] [로컬 브랜치 이름]: 커밋된 변경 사항을 원격 리포지토리로 푸시합니다.
	- $ git push origin main
7. git pull [원격 리포지토리 이름] [원격 브랜치 이름]: 원격 리포지토리의 변경 사항을 로컬로 가져와 병합합니다.
	- $ git pull origin main

# Git/GitHub 활용 실습

## 프로젝트 - 프로필

1. 프로젝트 시작 
	- 바탕화면에 폴더
	- README.md 파일이 반드시 필요
	- git 저장소로 만들고 커밋

2. GitHub
	- 원격저장소 이름은 **반드시 여러분의 'username'으로!**
	- 원격저장소 설정을 마무리하고 push하면 끝!

3. 프로필 확인 : https://github.com/username

4. 실습 완료 후 체크 시트에 링크 업데이트

5. 구글에 GitHub Profile Readme라고 검색해보시면 정말 다앙하게 꾸미고, 설정 할 수 있는 방법이 있습니다

### 프로젝트 초기 설정
```bash
git init
```

### 원격 저장소 프록젝트로 시작하기

## 브래치 활용
```bash
git branch # 브랜치 목록
git branch 브랜치이름 # 브랜치 생성
git checkout 브랜치이름 # 브랜치 이동
git branch d 브랜치이름 # 브랜치 삭제
```

```bash
git merge 브랜치이름
```

## 기타 명령어

### git add를 취소
```bash
git reset 파일이름
```

### 커밋 메시지를 변경
```bash
git commit --amend
```

### 커밋을 취소
```bash
git reset HEAD~1 # 이전 커밋으로 되돌리기:
git revert <커밋 해시> #커밋 취소 커밋 만들기
```





# 지난주 수업내용
## 장고 start -> 앱 만들기 -> 모델정의 -> 마이그레이션 -> 플래시 메시지 -> 장고 관리자 -> 장고 레이아웃 및 폼양식 -> 템플릿 만들기
-> 편집 폼 양식 및 레이아웃 -> 삭제 폼 레이아웃 -> 로그인/로그아웃

## Django 프로젝트 순서

1. 프로젝트 작성 : >django-admin startproject your_projectname 학습을 사용하여 새 프로젝트를 시작(관리자 권한)

2. 앱 생성 : python manage.py startapp yourappname 학습을 이용하여 웹사이트의 구성 요소(예: 블로그, 갤러리 등)를 대표하는 앱을 생성

3. 모델 정의 : 앱의 models.py파일에서 데이터베이스 테이블을 정의

4. 보기(View)와 템플릿 작성 : 검토를 통해 로직을 처리하고 템플릿을 사용하여 사용자에게 보여주기 HTML을 작성

5. URL 설정 : urls.py파일에서 URL 패턴을 정의하여 보기(View)와 연결

6. 데이터베이스 카탈로그 : python manage.py makemigrations과 python manage.py migrate 사용하여 모델 변경 사항을 데이터베이스에 적용

7. 정적 및 미디어 파일 관리 : CSS, JavaScript, 이미지 등의 정적 파일을 관리하고 설정

8. 개발 서버 실행 : python manage.py runserver기반으로 개발 서버를 실행하고 웹사이트 확인

9. 배포 : 웹사이트가 준비되어 있는 호스팅 서비스에 포함하여 인터넷에 배포를 공개

### blog 만들기 순서
#### mysite
    1) >python manage.py startapp blog
	2) mysilte.setting INSTALLED_APPS = ['blog']추가
	3) blog.view.py 함수생성 (request, response)
	4) blog.urls.py Url 패턴을 매핑선언
	5) mysite urls.py blog.urls.py를 연결

	3), 4) 작업으로 추가

#####
    1) >python manage.py startapp blog
	2) mysilte.setting INSTALLED_APPS = ['notice']추가
	3) notice.view.py 함수생성 (request, response)
	4) notice.urls.py Url 패턴을 매핑선언
	5) mysite urls.py notice.urls.py를 연결

	3), 4) 작업으로 추가
	/notice_web01
	/notice_web02

#### blog <모델정의 -> 마이그레이션>

모델을 변경하고(table) 마이그레이션을 생성(db)하고 변경 사항을 데이터베이스에 적용하는 프로세스

1. 새 모델을 정의하거나 기존 모델을 변경 (새로운 테이블을 생성 하거나 수정)
2. 명령을 실행하여 새 마이그레이션을 수행 makemigrations.(새로운 db 생성)
3. 명령을 실행하여 모델의 변경 사항을 데이터 베이스에 적용 migrate. (테이블 생성 or 수정 -> 기존 DB)
	
    - ex) 모델정의

		blog.models.py -> django.db.models.Model의 하위 클래스 및 필드가 명시되어야 한다.
		
        - 상속해서 클래스 생성 / DEFAULT_AUTO_FIELD = 'django.db.models.BigAutoField'
		- /__str-- 문자열 표현 재정의 메소드
		- class Meta 구성

	- ex) 내장 모델과  함께 사용한다. 참조키를 생성 했다.
        - from django.contrib.auth.models import User

#### 실습
1. 새 마이그레이션 생성
- python manage.py makemigrations

2. sql 구문 미리보기
- python manage.py sqlmigrate blog 0001

3. 변경사항을 데이터베이스에 적용
- python manage.py migrate

4. 프로젝트에서 해당 마이그래이션 상태를 나열해 보자
- python manage.py showmigrations

#### cf ) " no changes detected  "오류체크
- 모델변경x(세션,브라우저) -> 앱이 지정되지 않았다. python manage.py makemigrations 앱이름
- INSTALLED_APPS에 등록된 앱이 인식하지 못할 경우
- 마이그레이션 파일이 이미 있다
- 모델 정의 오류
- 수동 삭제 할 경우

#### 장고 관리자
- 관리자 페이지에 모델을 표시를 하려면 admin.py에 Post(Model) 속성값을 추가해야 한다.

    1. admin.site.register(Post)
	2. 127.0.0.1:8000/admin 으로 접속 해서 blog/post 확인후 게시물 몇개 등록
	3. 등록된 게시물을 표시한다 blog.views.py
	4. settings.py TEMPLATES = ['DIRS': [BASE_DIR /'templates'],]
#### 장고 레이아웃 및 폼양식 
- django.forms.Form 클래스를 상속, django.forms.ModelForm
	
    1) 앱디렉토리 blog.forms.py 파일생성
	2) django.forms.ModelForm 임포트
	3) class PostForm(ModelForm): class Meta : 클래스를 생성
	4) PostForm 경로를 url패턴에 등록한다. blog.urls.py
	path('post/create',views.create_post, name =" post-create"),
	5) create_post()함수를 통해 코드를 작성 blog.views.py

#### [-> 편집 폼 양식 및 레이아웃 -> 삭제 폼 레이아웃 ->]
    1. Url패턴만들고 views.py 함수를 만든다.(Model -> View[forms.py] -> Template)
    2. html 템플릿 구성을 한다.(Template)

