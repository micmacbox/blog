---
layout: post
title: 알고리즘 정리
categories: algorithm
tags: [etc]
date: 2022-03-28 15:32 +0800
# toc: true
---

1.  섬 둘레 구하기

```
    function solution(maps)
    {
    let answer = 0;
    let row=maps.length;
    let col=maps[0].length;
    for (let i=0; i<row; i++){
    for (let j=0; j<col;j++){
    if (maps[i][j]){
    answer+= (4 - (()=>{
    let cnt = 0;
    if (i>0 && maps[i-1][j]===1){
    cnt++;
    }
    if (j>0 && maps[i][j-1]===1){
    cnt++;
    }
    if (i<row-1 && maps[i+1][j]===1){
    cnt++;
    }
    if (j<col-1 && maps[i][j+1]===1){
    cnt++;
    }
    return cnt;
    })());
    }
    }
    }
    return answer;
    }
```
