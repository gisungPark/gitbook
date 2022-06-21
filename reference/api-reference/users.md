---
description: 회원 정보
---

# Users

{% embed url="https://meetup.toast.com/posts/92" %}

{% swagger method="post" path="/users/login" baseUrl="https://{도메인}" summary="로그인" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="String " required="true" %}
 아이디 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" type="String " required="true" %}
 비밀번호 
{% endswagger-parameter %}

{% swagger-response status="200: OK" description=" 로그인 완료 " %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description=" 로그인 실패 " %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/users/signup" baseUrl="https://{도메인}" summary="회원가입" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="String" required="true" %}
 아이디 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" type="String" required="true" %}
 비밀번호 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="nickname" type="String" required="true" %}
 닉네임 
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="회원가입 완료" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="회원가입 실패(아이디/닉네임 중복)" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/users/id/exist" baseUrl="https://{도메인}" summary="아이디 중복 체크" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="id" type="String" required="true" %}
 아이디 
{% endswagger-parameter %}

{% swagger-response status="200: OK" description=" 아이디 사용 가능 " %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description=" 중복 아이디 존재 " %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/users/nickname/exist" baseUrl="https://{도메인}" summary="닉네임 중복 체크" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="nickname" type="String" required="true" %}
 닉네임 
{% endswagger-parameter %}

{% swagger-response status="200: OK" description=" 닉네임 사용 가능" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description=" 중복 닉네임 존재 " %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}









