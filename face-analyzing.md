# face-analyzing

{% swagger method="post" path="/face-analysis" baseUrl="/api" summary="AI를 통한 얼굴 분석을 수행한다." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="image_file" type="File" required="true" %}
jpeg,jpg,png 유형의 이미지
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_id" type="String" %}
값이 존재하면 user의 얼굴 기록에 저장
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="얼굴을 분석한 결과를 JSON형식으로 반환" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/face-landmark" baseUrl="/api" summary="AI를 통한 각 얼굴 부위에 대한 랜드마킹을 한다." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="image_file" type="String" required="true" %}
jpeg,jpg,png 유형의 이미지
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_id" type="String" %}
값이 존재하면 user의 얼굴 기록에 저장
{% endswagger-parameter %}
{% endswagger %}
