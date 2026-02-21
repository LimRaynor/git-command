# git 명령어

## git hub 처음 올릴때
로컬 저장소 초기화
git init

파일 스테이징
git add .

커밋
git commit -m "first commit"

원격 저장소 연결
git remote add origin 깃허브주소

브랜치 이름을 main으로 맞춤 (선택)
git branch -M main

원격으로 업로드
git push -u origin main

## 브렌치 생성후 작업
매인상태 체크
git checkout main

최신 메인 받아오기
git pull origin main

원격 브랜치 목록 확인
git branch -r

로컬 브랜치 생성 + 연결
git switch -c 브랜치이름

올리는방법
git add .

커밋후 기능이름추가
git commit -m "feat: 기능 추가"

브렌치에 푹시
git push -u origin feature/login

## 브랜치가 이미 있는걸 clone 했을 경우
git pull origin feature/login

## 브렌치에도 main  최신을 반영하려면
main 최신화
git pull origin main
기능 브랜치로 이동
git merge main
main을 기능 브랜치에 반영
git merge main

## 브렌치를 이전 커밋으로 돌아가는 경우

이전 커밋번호 확인
git log --oneline

특정 커밋으로 돌아가기 (기록을남기는 커밋을 생성함) 
git revert 커밋번호

## 브렌치가 망해서 삭제하는 경우
현재 다른 브랜치로 이동 - 삭제하려는 브랜치에 서 있으면 안 됩니다.
git switch main

브랜치 삭제 (merge 된거면 대문자 D로 강제삭제)
git branch -d feature/login

원격 브렌치 삭제
git push origin --delete feature/login

## 기능 개발 중 다른 브랜치로 이어가기
현재브렌치 작업 상태 확인
git status

새 브랜치 생성하면서 이동
git switch -c feature/login-api

기존 브랜치로 이동
git switch feature/login-api

## 작업환경이 바뀐경우 (데스크톱 -> 노트북)
git fetch

원격 브랜치 목록 확인
git branch -r


git pull origin feature/Default-Category
