---
title: Golang Naming Convension
date: 2022-10-03 19:39 +/-0900
categories: [Golang]
tags: [golang]     # TAG names should always be lowercase
---

# Golang Naming Convensions

## 공식 규칙들
### MixedCaps
- MixedCaps (camelCase) 를 사용하자. (underscore 을 사용하지 말자)
- 만약 package 밖에서 사용되어야 한다면 첫 글자를 대문자로 적어야 한다
- 만약 package 밖에서 사용할 일이 없다면 앞 글자를 소문자로 유지해도 된다 (mixedCaps)


### Interface names
- 보통은 MethodName + er = InterfaceName 형태로 사용한다.
- 만약 하나 이상의 method가 있는 interface인 경우는 경우에 따라 다르다.


## 공식적이진 않은 규칙들
### 짧은 변수 이름
#### Single-letter identifier
- 특히 scope가 한정적인 로컬 변수들에게는 index나 idx 같은 긴 변수명이 필요없다
- 위와 같은 경우에는 한글자 짜리 single-letter identifier을 사용하는 것이 권장된다
#### Shorthand name
- 처음 읽는 사람이 이해할 수 있는 범위 내에서 짧게 작성하는 변수명은 권장된다
```
pid // Bad (이것은 podID, personID, productID 등 무엇인지 알 수 없음)
sepc // good (누가 봐도 specification)
addr // good (누가 봐도 Address)
```

### Unique name
- API, HTTP와 같은 줄임말, 혹은 ID, DB 와 같은 이름은 형태를 유지하는 것이 좋다
	- userId 대신 userID
	- productApi 대신 productAPI

### Line length
- Go에서는 한 줄의 길이에 대한 제한은 없지만 한 줄을 너무 길게 적는 것은 피하는 것이 좋다





---
# References
- [https://betterprogramming.pub/naming-conventions-in-go-short-but-descriptive-1fa7c6d2f32a](https://betterprogramming.pub/naming-conventions-in-go-short-but-descriptive-1fa7c6d2f32a){:target="_blank" rel="noopener"}