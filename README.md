## 빅데이터 개방‧유통을 위한 메타데이터 구조 및 데이터 연계 규격 예시

## 개요 
- RDF 문서 기반의 메타데이터 조회 API 동작 예제 

## 테스트 절차

- 메타데이터 조회 API 요청 테스트(list API를 이용하여 id를 추출 한 후 detail API를 이용하여 상세 내용 조회)

  - 메타데이터 목록 조회 (특정 플랫폼의 메타데이터를 제외하고자 할 경우 해당 플랫폼 id 값 정의)
    ```
      $ curl -X POST \
        http://115.85.181.22:8080/api/resources/list?title=고속&platformId=4
    ```  
  - 메타데이터 상세내용 조회 (id 속성값 기준으로 상세내용 조회)
    ```
      $ curl -X GET \
        http://115.85.181.22:8080/api/resources/5388/detail
    ```
