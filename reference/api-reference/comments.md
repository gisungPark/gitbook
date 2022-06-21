---
description: 댓글
---

# Comments

{% swagger method="get" path="/comments/board/{id}" baseUrl="https://{도메인}" summary="게시글 해당 댓글 목록 조회" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="id" type="String" required="true" %}
게시글 고유 id
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/comments/{id}" baseUrl="https://{도메인}" summary="댓글 상세 보기" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="id" type="String" required="true" %}
 댓글 고유 id
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/comments" baseUrl="https://{도메인}" summary="댓글 작성" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="contents" type="text" required="true" %}
 댓글 내용
{% endswagger-parameter %}

{% swagger-parameter in="header" name="access-token" type="String" required="true" %}
 사용자 토큰 
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
{% endswagger %}

{% swagger method="put" path="/comments" baseUrl="https://{도메인}" summary="댓글 수정" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="String" required="true" %}
 댓글 고유 id
{% endswagger-parameter %}

{% swagger-parameter in="body" name="content" type="text" required="true" %}
 댓글 수정 후 내용 
{% endswagger-parameter %}

{% swagger-parameter in="header" name="access-token" type="String" required="true" %}
 사용자 토
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

{% swagger method="delete" path="/comments" baseUrl="https://{도메인}" summary="댓글 삭제" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="access-token" type="String" required="true" %}
 사용자 토큰 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="id" type="String" required="true" %}
  댓글 고유 id
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description=" 해당 댓글 존재하지 않음" %}
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
