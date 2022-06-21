---
description: 게시판
---

# Boards

{% swagger method="get" path="/boards/{page}" baseUrl="http://{도메인}" summary="게시글 목록 조회" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="page" type="int" %}
 페이지 번호 
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description=" 해당 페이지 존재하지 않음 " %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/boards/{id}" baseUrl="http://{도메인}" summary="게시글 읽기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="id" type="String" %}
게시글  아이디
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description=" 해당 게시글 존재하지 않음 " %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/boards" baseUrl="http://{도메인}" summary="게시글 쓰기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="access-token" type="String" required="true" %}
 사용자 토큰 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="title" type="String" required="true" %}
 게시글 제목 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="contents" type="text" required="true" %}
 게시글 내용 
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description=" 세션 만료 또는 권한 없음 " %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="put" path="/boards" baseUrl="http://{도메인}" summary="게시글 수정" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="access-token" type="String" required="true" %}
 사용자 토큰 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="id" type="String" required="true" %}
 게시글 고유 id 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="title" type="String" required="true" %}
 게시글 수정 후 제목 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="contents" type="text" required="true" %}
 게시글 수 후 내용
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description=" 해당 게시글 존재하지 않음 " %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description=" 세션 만료 또는 권한 없음" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="delete" path="/boards" baseUrl="http://{도메인}" summary="게시글 삭제" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="access-token" type="String" required="true" %}
 사용자 토큰 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="id" type="String" required="true" %}
 게시글 고유 id 
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description=" 해당 게시글 존재하지 않음" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description=" 세션 만료 또는 권한 없음" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}
