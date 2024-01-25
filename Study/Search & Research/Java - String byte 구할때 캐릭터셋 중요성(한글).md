

--- 
author: zeraf29
created: 2024-01-17 23:47 
last-updated: 2024-01-17 23:47 
summaries: 
tags:

---


## Memo
- Java 에서 UTF-8 인코딩으로 한글 바이트 계산시 1~3바이트로 계산됨.
- 소켓, EAI 통신 시 상호 정해진 고정 바이트 (FixedLength) 로 통신할 경우, 바이트 자리가 안 맞아 통신 안 될수 있음
- 즉, 한글 문자열을 바이트 로 변환 할 때 바이트 오버 시, 캐릭터 셋 지정 필요

String korStr = “안녕하세요?“;
korStr.getBytes("euc-kr");

요글 참조
https://www.dukgun.com/2021/03/java-string-string-getbytes.html?m=1

StrungUtils.rightPad
같은 유틸은 위와 같은 바이트 처리 안함-> 한글 처리 시 바이트 어긋날 수 있음 -> 해당 로직에 캐릭터셋 처리하는 로직을 덧대어 구햔하는것이 필요




