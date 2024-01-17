

--- 
author: zeraf29
created: 2024-01-11 11:31 
last-updated: 2024-01-11 11:31 
summaries: 
tags:

---


## Memo
- 주제: Maven 의존 파일의 경로 내 *.jar 외 *.pom 파일이 없을 경우, 프로젝트에서 maven의존 파일 검색을 못한다. 
- 상황
	- Nexus에 dori-core-1.0.0.jar의 변경된 의존 파일 업로드 
	- 업로드 하면서 dori-core-1.0.0.pom 파일을 삭제해버림
	- 기존 동일 파일명의 구성에서 정상 빌드 되던 것이, 위 작업 이후 아래와 같은 오류 발생 
		- Could not resolve all files for configuration ‘:dori-common:compileClasspath’
			- Could not find com.jh.dori:dori-core:1.0.0
			- Required by:
				- Project :dori-common
- 테스트
	- Nexus에서 정상 빌드 되는 로컬 m2 저장소로 변경해봄: 빌드 정상
	- 로컬 m2 저장소의 해당 파일 경로의 dori-core-1.0.0.pom 파일 삭제: 동일 오류로 실패
	- 로컬 m2 저장소의 해당 파일 경로의 dori-core-1.0.0.pom 파일 원복: 정상 빌드 확인



