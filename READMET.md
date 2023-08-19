# 기본 명령어

## 프로젝트 시작할 때 

### 로컬에서 처음 시작하기

```bash
git init
```
* git init하면 (main)으로 확인할 수 있음

### 원격 저장소 프로젝트로 시작하기

```bash
git clone 'https://~'
```

## 버전 기록할 때

```bash
git add .
git commit -m '커밋메시지'
```

* git status로 파일 상태 확인 해보기 
* git log로 커밋 확인하기

## 원격저장소 최초 설정할 때

```bash
git remote add origin url
```

## 원격저장소 활용

### push

```bash
git push origin main
```

- `origin` : 원격저장소의 이름

- `main` : 브랜치의 이름

### pull

```bash
git pull origin main
```

## 브랜치 활용

```bash
git branch # 브랜치 목록
git branch 브랜치이름 # 브랜치 생성
git checkout 브랜치이름 # 브랜치 이동
git branch -d 브랜치이름 # 브랜치 삭제
```

```bash
git merge 브랜치이름
```

## 기타 명령어

### git add를 취소

```bash
git restore --staged 파일명
```

### 커밋 메시지를 변경

```bash
git commit --amend
```

### 커밋을 취소 

```bash
git reset --hard 커밋
git reset --soft 커밋
```

```bash
git revert 커밋
```