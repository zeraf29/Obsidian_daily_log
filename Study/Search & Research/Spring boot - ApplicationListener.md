

--- 
author: zeraf29
created: 2023-10-27 08:26 
last-updated: 2023-10-27 08:26 
summaries: 
tags:

---


## Memo


Spring Boot ApplicationListener는 애플리케이션의 라이프사이클 이벤트를 처리하는 데 사용되는 인터페이스입니다. Spring Boot 애플리케이션에는 다양한 종류의 라이프사이클 이벤트가 있으며, 각 이벤트에는 고유한 ApplicationListener가 있습니다.

다음은 Spring Boot ApplicationListener의 몇 가지 일반적인 종류입니다.

- **ContextRefreshedEvent:** 애플리케이션이 시작되고 빈이 생성되고 의존성이 주입된 후 발생합니다. 
    
    [![ContextRefreshedEvent](https://1.bp.blogspot.com/-fzIUpWl387g/W6huv4p4vYI/AAAAAAAAUoE/lMyHR4tTBdgTiglJNvYNAJygf4q5dyqdgCLcBGAs/s1600/Slide1.JPG)새 창에서 열기](https://ramj2ee.blogspot.com/2018/09/event-handling-in-spring_23.html)[![](https://encrypted-tbn0.gstatic.com/favicon-tbn?q=tbn:ANd9GcS2-dWwSth7nJ5A7s-n3lqiC7bR6EGCAya2cpAfjv_1mR17FRgXDHYbos10YbGM4AQhHoIOvodyThdKlVKn3PsYyhV0CYSnmD3xc4fkNx8)ramj2ee.blogspot.com](https://ramj2ee.blogspot.com/2018/09/event-handling-in-spring_23.html)
    
    ContextRefreshedEvent 
    
- **ContextStartedEvent:** 애플리케이션이 시작되고 빈이 생성되고 의존성이 주입되고 웹 서버가 시작된 후 발생합니다. 
    
    [![ContextStartedEvent](https://lh3.googleusercontent.com/bip/AFhciVMpBB1yZOQZ70s_4wC6OTfQXxa7w1EwCXcyuExQYl_rS6lSoGSbz7wF5pNmQqzhHDwyrzv2V4qYtjCcnel2EKqT_RqOEeUD2gCR1EL8ikPN71FIixCd1Bgdj6XF3PXIZnKF6Dk3FqfRJr9lDAH8TdpDQT_z6VdrxrdTTZVOFa1znqjsqHSYwS0jHJSemzpqPvKmcVsawFjWpTkPVRQlGgwHvMmgFga6n8nHN-3-7eBLhuoS_yK67F5Thl_fJogBXtJT27u3MrZPxRmZ_qVPKzbz2DB3KIAuPbF3nExG9Ip5djKeoou2ZQO85Hog8y6pxY6FszeH=w250-h200-p)새 창에서 열기](https://blog.51cto.com/u_15367034/3914584)[![](https://encrypted-tbn1.gstatic.com/favicon-tbn?q=tbn:ANd9GcQJC8ecLNMZc5BAeaL2qqHXC5RSr3GbnSR_DYscC64o-yWieizL5OZnuzTdMKBxH50OcEBt_a1gLnzcfKLWgNN87x2BZMHjevE)blog.51cto.com](https://blog.51cto.com/u_15367034/3914584)
    
    ContextStartedEvent 
    
- **ContextStoppedEvent:** 애플리케이션이 중지되고 웹 서버가 중지된 후 발생합니다. 
    
    [![ContextStoppedEvent](https://3.bp.blogspot.com/-kWsSQSTmkf8/W6ho5fhqWiI/AAAAAAAAUm8/f7qIGzj0o7cOp-Hh3CL2n1cuCMjEDsDtwCLcBGAs/s1600/Slide2.JPG)새 창에서 열기](https://ramj2ee.blogspot.com/2018/09/event-handling-in-spring.html)[![](https://encrypted-tbn0.gstatic.com/favicon-tbn?q=tbn:ANd9GcS2-dWwSth7nJ5A7s-n3lqiC7bR6EGCAya2cpAfjv_1mR17FRgXDHYbos10YbGM4AQhHoIOvodyThdKlVKn3PsYyhV0CYSnmD3xc4fkNx8)ramj2ee.blogspot.com](https://ramj2ee.blogspot.com/2018/09/event-handling-in-spring.html)
    
    ContextStoppedEvent 
    
- **ApplicationReadyEvent:** 애플리케이션이 시작되고 모든 빈이 생성되고 의존성이 주입되고 웹 서버가 시작되고 애플리케이션이 준비된 후 발생합니다. 
    
    [![ApplicationReadyEvent](https://lh3.googleusercontent.com/bip/AFhciVMZVw85borF047kWbyoO1NkbNTOK2ew3in9_7Hl6LyaJsyAtg8Ik0N_v-rF7Wqh69EjVnkVqtmiFA_0EI6Ooe5-L894Lz3_5RXiWEJExhKzJxKlK96pIlouJL7-dJRs8jFAlCbxhRqz7B_yvn3Dtoz4DkIAWCYxmzYTbd-dfUwIMT9hKQ=w250-h200-p)새 창에서 열기](https://forum.xwiki.org/t/hi-i-want-to-add-a-event-listener-for-an-application-created-but-applicationreadyevent-similar-not-work/3123)[![](https://encrypted-tbn2.gstatic.com/favicon-tbn?q=tbn:ANd9GcSKrlVpN5eIBrnxIK2So1MYQipCLVMbnGRqdIv3oYN9uXx-Oj12hyBrwNKartEAWH74e2PERkd9xmcZXSQJSP5oGDtaqo3tE5ek)forum.xwiki.org](https://forum.xwiki.org/t/hi-i-want-to-add-a-event-listener-for-an-application-created-but-applicationreadyevent-similar-not-work/3123)
    
    ApplicationReadyEvent 
    
- **ApplicationFailedEvent:** 애플리케이션이 시작 중 또는 실행 중 오류가 발생한 경우 발생합니다. 
    
    [![ApplicationFailedEvent](https://lh3.googleusercontent.com/bip/AFhciVMxyxFjtJjEJRj0jrr7uQrkUUQp5eDUVUhaQwNGOcStNom-BQSk8j01QffAuM4PYJqDZhP4qjH_hhmiwwNn5JD9zlowQDDrm7BZ-WITG-V7--VSNroN5eF9q6QfcL53xuuhCAO61ZwZpGvK3adBbRAutAToNI0XUNZE05sPjfMGt8T5u-3BPcM3QgLRPZ8VqmgQJ_nvcC1FqUI5plbecMRtCDgGO6CP5RAI13XTsD7Pag=w250-h200-p)새 창에서 열기](https://github.com/spring-projects/spring-boot/issues/10470)[![](https://encrypted-tbn1.gstatic.com/favicon-tbn?q=tbn:ANd9GcQMWyctgi21E3pB8xn4iBFazkndTUvaPmX-zdFv06DZ-mByF8axuc_CClAiYh_1yRIIVp9Y2iFuFB2ATC5ZrlssaIhE-Q)github.com](https://github.com/spring-projects/spring-boot/issues/10470)
    
    ApplicationFailedEvent 
    

이외에도 Spring Boot에는 다음과 같은 다양한 종류의 ApplicationListener가 있습니다.

- **ApplicationContextInitializerListener:**애플리케이션 컨텍스트가 초기화될 때 발생하는 이벤트를 처리합니다.
- **ApplicationListenerDetectorListener:**애플리케이션 컨텍스트에 등록된 ApplicationListener를 검색하는 데 사용되는 이벤트를 처리합니다.
- **ApplicationListenerMulticasterListener:**ApplicationListener에 이벤트를 전파하는 데 사용되는 이벤트를 처리합니다.


From google bard research