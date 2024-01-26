

--- 
author: zeraf29
created: 2024-01-11 11:31 
last-updated: 2024-01-11 11:31 
summaries: 
tags:

---


## Memo

- 코드
```
string="word1,word2,word3" 
array=(${string//,/ }) # Split using comma as delimiter 
for element in "${array[@]}"; do 
	echo "$element" 
done
```
