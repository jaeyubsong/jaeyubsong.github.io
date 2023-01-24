---
title: Union find
date: 2023-01-15 18:10 +/-0900
categories: [PS, Algorithm]
tags: [union find]     # TAG names should always be lowercase
---

# Union find

Union-find 혹은 disoint-set으로 불림.

서로 disjoint한 집합들을 표현함. 즉, 모든 집합들은 서로 교집합이 없고, 모든 집합들의 합집합은 전체집합이 된다

- Find

```c++

int find(int a, vector<int>& p) {
	if (p[a] < 0) { return a; }
	p[a] = find(p[a], p);
	return p[a];
}
```


- Merge (반환값: set의 크기)

```c++
int merge (int a, int b, vector<int>& p) {
	a = find(a, p);
	b = find(b, p);
	if (a == b) { return -p[a]; }
	if (a < b) {
	    int curSize = p[b];
		p[b] = a;
		p[a] += tmp;
		return -p[a];
	} else {
	    int curSize = p[a];
		p[a] = b;
		p[b] += curSize;
		return -p[b];
	}
}
```





---
# References
- https://m.blog.naver.com/kks227/220791837179?referrerCode=1