# Git
 1. Coding convention
    - conding convention 은 기본적으로 PEP8에 맞춘다.
    - 참고 페이지 [PEP 8](https://www.python.org/dev/peps/pep-0008/)
    - docstring과 comment 도 PEP8에 맞춰서 작업한다.
    
 2. Branch strategy
    - 모든 작업은 branch을 따서 작업 후 merge 한다.
    - 이때, 2인이상 review 후 merge (self merge 금지)
    - 기본적인 git 명령어
    	- branch 생성/이동 방법
    		- 생성 : git checkout -b 'branch name'
    		- 이동 : git checkout 'branch name'
        - 원격 저장소로 push
       		- git add '변경 파일'
       		- git commit -m '변경 메시지'
        	- git push origin 'branch name'
        - 로컬 저장소로 pull
         	- git checkout master & git pull
        - Rebase (작업 전에는 꼭 Rebase를 통해서 충돌 해결)
        	- git checkout master
        	- git pull
        	- git checkout '현재 자신이 작업중인 branch name'
        	- git rebase origin/master
        	- conplict 발생시
        		- conplict 난 부분을 수정 후 저장
        		- git add '수정한 파일'
        		- git rebase --continue
  			- git push -f origin 'branch name' 
  		- 특정 commit만 다른 branch에 추가하고 싶을때
  			- git cherry-pick 'commit hash code'
