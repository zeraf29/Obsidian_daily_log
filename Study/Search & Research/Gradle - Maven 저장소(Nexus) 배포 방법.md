

--- 
author: zeraf29
created: 2024-01-24 15:31 
last-updated: 2024-01-24 15:31 
summaries: 
tags:

---


## Memo
- 주제: Gradle 빌드 에서 Maven저장소(Nexus)배포 방법 & 주의사항
- 상황
	- 별도 관리하는 jar 라이브러리를 내부 Maven 저장소(Naxus)에 올리기
- 내용
	- 업로드 코드(build.gradle.kts)
```
allprojects {
	…
	apply(plugin = “maven-publish”)
	…
}

subprojects {
	group = “com.my.code”
	version = “1.0.0.-GA”

	tasks.named<Upload>(“uploadArchives”){
		repositories.withGroovyBuilder {
			val repoPath = uri(“https://my.nexus-repo.com/repository/my-develop”)
			”mavenDeployer” {
				“repository”(“url” to repoPath){
					“authentication”(”userName” to “myId”, “password” to “myPassword”)
				}
			}
		}
	}
}
```
- 실행명령
	- ./gradlew build -> ./gradlew uploadArchives
- 주의사항
	- 저장소가 release 정책으로 되어 있으면, 버전 덮어씌우기가 안됨(무조건 새 버전)
		- Maven저장소 표준 규격
		- release/snap-shot 차이 구분 알아보기 필요







- so 	-	 	 	 	 	
	 - 코드
	`subprojects {
			group = “com.my.code”
			version=“”1.0.1-GA”

			tasks.named<Upload>(“uploadArchives”) {
				Repositories.withGroovy
			}
		
		}`
	- ``



