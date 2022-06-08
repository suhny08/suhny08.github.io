---
title: 2022 개인 프로젝트
date: ""
description: study 및 토이 프로젝트
---
> [쉬운 보험약관 가이드](https://www.fsc.go.kr/po010101/74513?srchCtgry=&curPage=38&srchKey=&srchText=&srchBeginDt=&srchEndDt=)
금융위원회의 보험업 감독규정 개정에 따른 「소비자가 이해하기 쉬운 보험약관 보험개선방안」에 착안하여 가볍고 접근성 높은 웹 기반의 보험 약관 가이드북을 제작하였습니다. 


##### Before project starts 
- 금융위원희 보험약관을 개인이 사용해도 되는지? (상업적 이용 X) 
    - 가능함.
- min-width: 640px 기준, 모바일 웹을 우선함


##### Project folder structure
``` bash 
practice-web-ins-guide
├── views
│   └── web_main.pug        ---> webpack input file
├── src
│   └── web.js              ---> add DOM event handling (webpack entry file)
├── dist                    ---> webpack output folder 
│   ├── web_main.pug 
│   └── web.js 
└── server.js               ---> express api & view engine setting (pug)
```

##### Dependencies 
Dependence             |Version
-----------------------|-------
express                | ^3.1.6
intersection-observer  | ^0.12.0
pug                    | ^3.0.2
tailwindcss            | ^3.0.23
webpack                | ^5.72.0
webpack-cli            | ^4.9.2


##### API Specifications

| Action | API | Parameter  | Success Response | Fail Response  |
| :----- | :-- | :--------- | :--------------- | :------------- | 
| get    | `*` |            | render tail.html |                |
| get<br/>Product name| /guide<br/>/:id|id=<br/>[string]  | {"id": "001", "productName": "[무] e간편한연금저축보험"}| status 500|