---
layout: post
title:  "GraphQL-tutorial"
date:   2021-06-30 14:17:49 +0900
categories: GraphQL tutorial
---

---
### Contents
- GraphQL 이란?
- 왜 GraphQL 인가?
- GraphQL 준비
- GraphQL의 장점과 단점
- GraphQL과 오픈소스: Open API 및 Swagger
- GraphQL 시작
- GraphQL 중간
- GraphQL 끝
- Further Study
- References

---



# GraphQL 이란?
- API를 위한 쿼리 언어
- 기 존재하는 데이터 쿼리를 수행하기 위한 런타임
- API 진화의 강력한 개발자 도구: playground
  

# 왜 GraphQL 인가?
- Over fetching
  * 기존, 예를들어 사용자 정보에 불필요한 부분이 REST API에 포함되있다면, Front 전체를 다 받아서 parsing 해야함
  * GraphQL을 사용하면 Front가 원하는 정보만 요청할 수 있음
  * `Over fetching` 해결!

- Under fetching
  * 기존, 예를들어 영화 앱을 개발하는 경우 비디오 정보와 제작자 정보를 받아와야했음
  * 하나의 주제를 표출하기 위해 여러 개의 REST API를 호출하는 해야하는 것을 `Under fetching`이라함
  * GraphQL을 사용하면 Front가 한번의 요청으로 원하는 데이터를 얻을 수 있음
  * `Under fetching` 해결!

- Backend 개발
  * Schema와 Resolver를 한 번만 구현 해놓으면 추가 patch 비용이 거의 들지 않음
  * API 문서화는 주석으로 대신할 수 있음 (이력관리는 swagger나 마찬가지임)
  * 기본 Framework: [Apollo GraphQL][apollo-server]
  * 유용한 툴: [Sequelize Auto][sequelize-auto], [GraphQL Tools][graphql-tools]

- 간편해진 Loading, Error, Success 처리
  * Backend에서는 return type이 이미 지정되있으므로 error는 throw로 처리
  * Front에서는 동일한 Error에 대해서 예외처리만 하면 됨

- Playground GUI 테스트 환경
  * 기존, API 문서와 Postman 을 대치 가능
  * Playground 에서 쿼리 Loading, Error, Success를 바로 확인 가능
  * 검색 기능이 내장된 Document 기본 제공
  * Schema 다운로드 기능 기본 제공


# GraphQL 장점과 단점
- GraphQL 장점
  * GraphQL 스키마는 GraphQL 애플리케이션(Front)에 신뢰할 수 있는 단일 소스를 하나 제공 => Query.graphql or Query.json
  * GraphQL 호출은 단일 왕복으로 처리되며 클라이언트는 오버페칭 없이 요청한 결과만 얻음
  * 엄격하게 정의된 데이터 유형은 클라이언트와 서버 간 통신 오류를 줄여줌
  * GraphQL  클라이언트(Front)는 사용 가능한 데이터 유형 목록을 요청할 수 있음
  * 자동 생성 문서는 playground를 통해 제공
  * GraphQL은 애플리케이션 API가 기존 쿼리를 중단하지 않고도 진화할 수 있도록 허용
  * REST API로 사용할 수 없는 기능을 제공하기 위해 대부분의 오픈소스 GraphQL 확장 기능을 사용할 수 있음
  * GraphQL은 특정 애플리케이션 아키텍처를 지정하지 않으므로 기존 REST API에 추가하여 기존 API 관리 툴과 연동할 수 있음
- GraphQL 단점
  * REST API에 친숙한 개발자의 경우 GraphQL를 학습하는 데 시간이 필요
  * GraphQL은 데이터 쿼리의 상당 작업을 서버측으로 옮겨 서버 개발자 작업의 복잡성이 커짐
  * 구현 방식에 따라 GraphQL은 REST API가 아닌 다른 API 관리 전략을 필요로 할 수 있음 (특히 비용 제한과 가격을 고려하는 경우)
  * 캐싱이 REST보다 훨씬 복잡함
  * API 유지관리자의 경우 유지 관리 가능한 GraphQL 스키마를 작성하기 위한 추가 태스크를 수행해야 함


# GraphQL과 오픈소스: Open API 및 Swagger
{% highlight swift %}
  GraphQL은 Facebook에서 개발했으며 2012년에는 모바일 애플리케이션을 위해 사용됨
  GraphQL 사양은 2015년에 오픈소스로 공개됨
  현재는 GraphQL Foundation이 감독하고 있음
{% endhighlight %}
- [Apollo][apollo]: 프론트엔드 클라이언트 라이브러리([Apollo Client][apollo-client])와 백엔드 서버 프레임워크([Apollo Server][apollo-server])를 포함하는 GraphQL 플랫폼
- [Offix][offix]: 애플리케이션에 도달할 수 없는 경우에도 GraphQL 변형 및 쿼리를 실행할 수 있도록 허용하는 오프라인 클라이언트
- [Graphback][graphback]: GraphQL 지원 Node.js 서버를 생성하기 위한 커맨드라인 클라이언트
- [OpenAPI-GraphQL][openapi-graphql]: OpenAPI 사양 또는 Swagger로 설명된 API를 GraphQL로 번역하기 위한 커맨드라인 인터페이스 및 라이브러리


# GraphQL 준비
- [GraphQL tutorial][graphql-tutorial] 튜토리얼 준비물 다운로드
  * 서버개발자: [REAME.md][top-readme]의 내용을 읽고 starter > final 순으로 진행
  * 앱개발자: [Final > README.md][final-readme] 내용을 읽고 final 설치 후 각각 [iOS][client-ios], [Android][client-android]로 진행


# GraphQL 시작
- ...
- GraphQL Schema Language Cheat Sheet

![GraphQL Cheat Sheet](https://miro.medium.com/max/5052/1*HaEeoGrja2IGUxzvmj5Vnw.png)


# GraphQL 중간
- ...


# GraphQL 끝
- ...


# Further Study
- [GraphQL Tools][graphql-tools] 활용 방법 Study
- 파일 업로드 지원
- GraphQL 구독을 사용한 실시간 기능
- TypeScript 지원
- 쿼리 성능 추적

# References
* [GraphQL: Guides and Best Practices][graphql-guide]
* [GraphQL-yoga 소개 및 간단한 활용][graphql-yoga-intro]
* [GraphQL - Node Tutorial - 02. Getting Started][graphql-node-tutorial2]
* [Redhat: GraphQL이란?][redhat-graphql]


<!-- 
You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk]. -->

[sequelize-auto]:   https://github.com/sequelize/sequelize-auto
[graphql-tools]: https://github.com/ardatan/graphql-tools
[graphql-tutorial]: https://github.com/neoroman/GraphQL-tutorial
[top-readme]: https://github.com/neoroman/GraphQL-tutorial#graphql-tutorial
[starter-readme]: https://github.com/neoroman/GraphQL-tutorial/tree/main/starter#graphql-tutorial-starter
[final-readme]: https://github.com/neoroman/GraphQL-tutorial/tree/main/final#graphql-tutorial-for-final
[client-android]: https://github.com/neoroman/GraphQL-tutorial/tree/main/clientSample/android#android-sample-for-graphql-tutorial
[client-ios]: https://github.com/neoroman/GraphQL-tutorial/tree/main/clientSample/ios#ios-sample-for-graphql-tutorial
[graphql-guide]: https://www.graphql.com/guides/
[graphql-yoga-intro]: https://darrengwon.tistory.com/289
[graphql-node-tutorial2]: https://velog.io/@cadenzah/graphql-node-02-getting-started
[redhat-graphql]: https://www.redhat.com/ko/topics/api/what-is-graphql
[apollo]: https://www.apollographql.com/
[apollo-client]: https://www.apollographql.com/client/
[apollo-server]: https://www.apollographql.com/server/
[offix]: https://offix.dev/
[graphback]: https://graphback.dev/
[openapi-graphql]: https://github.com/IBM/openapi-to-graphql