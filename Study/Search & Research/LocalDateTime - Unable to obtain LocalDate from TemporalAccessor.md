

--- 
author: zeraf29
created: 2024-01-11 11:31 
last-updated: 2024-01-11 11:31 
summaries: 
tags:

---


## Memo

- 상황
	- LocalDateTime을 통해서 년월 값에서 월단위 계산 하려고 하니 오류 발생
- 오류 내용
	- 아래와 동일
```
java.time.format.DateTimeParseException: Text '201510' could not be parsed: Unable to obtain LocalDate from TemporalAccessor: {Year=2015, MonthOfYear=10},ISO of type java .time.format.Parsed
```
- 문제코드
```
val localDate = LocalDate.parse(baseDate, DateTimeFormatter.ofPattern(“yyyyMM”))
LocalDateTime.of(localDAte, LocalTime.of(0,0,0,0))
```
- 원인
	- A `LocalDate` needs a day but since there is no day in the date to parse, an instance of `LocalDate` can't be constructed.
	- f you just want to parse a year and a month, you can use the [`YearMonth`](https://docs.oracle.com/javase/8/docs/api/java/time/YearMonth.html) object instead:

```java
YearMonth localDate = YearMonth.parse(date, formatter);
```
- 참고사이트
	- https://stackoverflow.com/questions/34061759/why-my-patternyyyymm-cannot-parse-with-datetimeformatter-java-8



