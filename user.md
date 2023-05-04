---
description: 회원관련 요청에 관한 페이지
---

# user

{% swagger method="post" path="/sign-up" baseUrl="/user" summary="회원을 등록시킨다" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="user_id" type="String" required="true" %}
사용자 아이디
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_name" type="String" required="true" %}
사용자 이름
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_phone_number" type="String" required="true" %}
사용자 전화번호
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_email" type="String" required="true" %}
사용자 이메일
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_age" type="Integer" required="true" %}
사용자 나이
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="유저 생성 완료" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="잘못된 유저 정보를 보낸 경우" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="이미 존재하는 유저일 경우" %}

{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="서버 내부적으로 오류 발생" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/update" baseUrl="/user" summary="회원 정보를 업데이트 시킨다." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="user_name" type="String" required="true" %}
사용자 이름
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_phone_number" type="String" required="true" %}
사용자 전화번호
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_age" type="Integer" required="true" %}
사용자 나이
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="유저의 정보가 정상적으로 수정됨" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="유저의 정보가 정상적으로 수정되지 않음" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/{user_id}" baseUrl="/user" summary="회원의 정보를 가져온다" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="user_id" type="String" required="true" %}
회원의 아이디
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="유저의 정보를 성공적으로 가지고 옴" %}
```json
```
{% endswagger-response %}
{% endswagger %}
