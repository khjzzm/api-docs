#  여보야 점심 API 개요
<!-- 이 문서는 API에 대한 소개를 제공합니다. -->

## 소개
여보야 점심시간 뭐하지?

## 이 API로 할 수 있는 것

여보야 점심 API를 사용하여 다음을 할 수 있습니다:
- 회원가입 및 사용자 계정 관리
- 음식점 및 메뉴 항목 조회 및 관리
- 그룹 점심 주문 시작 및 참여
- 리뷰 작성 및 관리
- 사용자 프로필 접근 및 관리
- 고객 지원 문의 및 FAQ 처리
- 이벤트 및 프로모션 참여
- 공지사항 조회 및 관리

## 인증
Bearer Token
대부분의 API 엔드포인트에 접근하려면 Bearer Token을 사용하여 인증해야 합니다. 이 토큰은 인증 엔드포인트를 통해 로그인하거나 회원가입하여 얻을 수 있습니다. 토큰을 얻은 후 요청의 `Authorization` 헤더에 포함시킵니다.

## 기본 URL
모든 API 요청의 기본 URL은 다음과 같습니다:
https://api.yeoboya-lunch.com


## 속도 제한

공정한 사용을 보장하고 남용을 방지하기 위해 API는 속도 제한이 적용됩니다. 속도 제한은 다음과 같습니다:

- **공개 엔드포인트**: 분당 60 요청
- **인증된 엔드포인트**: 분당 120 요청

이 제한을 초과하면 `429 Too Many Requests` 응답을 받게 됩니다. `Retry-After` 헤더에서 다시 시도할 수 있는 시간을 확인할 수 있습니다.

## 오류 처리

API는 요청의 성공 또는 실패를 나타내기 위해 표준 HTTP 상태 코드를 사용합니다. 다음은 자주 접하게 될 상태 코드들입니다:

- **200 OK**: 요청이 성공적으로 완료되었습니다.
- **201 Created**: 리소스가 성공적으로 생성되었습니다.
- **400 Bad Request**: 요청이 잘못되었거나 처리할 수 없습니다.
- **401 Unauthorized**: 인증에 실패했거나 인증이 필요합니다.
- **403 Forbidden**: 리소스에 접근할 권한이 없습니다.
- **404 Not Found**: 리소스를 찾을 수 없습니다.
- **500 Internal Server Error**: 서버에서 오류가 발생했습니다.

오류가 발생한 경우, 응답 본문에 추가 세부 정보가 포함된 JSON 객체가 제공됩니다:

```json
{
  "code": "ERROR_CODE",
  "message": "상세 오류 메시지"
}
```

## 버전 관리
API는 하위 호환성을 보장하기 위해 버전이 관리됩니다. 현재 API의 버전은 v1입니다. 버전을 지정하려면 URL 경로에 포함시킵니다:
```
https://api.yeoboya-lunch.com/v1/...
```


<seealso>

<!--List any additional resources, such as tutorials or guides, that can help users understand and use the API effectively.-->

</seealso>
