# changedetection.io의 시간 설정에서 Duration Time의 목적과 작동 원리

changedetection.io는 웹페이지의 변화를 감지하고 알림을 제공하는 서비스입니다. 이 서비스의 시간 설정에서 중요한 요소인 'Duration Time'(실행 지속 시간)의 목적과 작동 메커니즘에 대해 알아보겠습니다.

## Duration Time의 목적

Duration Time은 changedetection.io의 스케줄러 기능에서 중요한 역할을 합니다. 이 설정은 각 요일별로 웹페이지 변경 감지가 얼마나 오랫동안 실행될지를 결정합니다. 기본적으로 다음과 같은 목적으로 존재합니다:

### 특정 시간대 동안만 감지 실행

Duration Time은 사용자가 지정한 시간 범위 내에서만 웹페이지 변경 감지를 실행할 수 있도록 합니다. 예를 들어, 업무 시간인 오전 9시부터 오후 5시까지만 웹페이지 변경을 확인하고 싶을 때 유용합니다. 이는 불필요한 시간대에 검사를 수행하지 않음으로써 시스템 자원을 절약하고 효율성을 높입니다.

### 비용 절감 효과

많은 사용자들이 프록시 제공업체의 비용을 절감하기 위해 이 기능을 활용한다고 보고했습니다. 필요한 시간대에만 웹페이지 변경 감지를 실행함으로써 불필요한 네트워크 요청을 줄이고 리소스 사용을 최적화할 수 있습니다.

## Duration Time의 작동 메커니즘

Duration Time의 작동 원리는 다음과 같습니다:

### 스케줄러와의 통합

Duration Time은 changedetection.io의 스케줄러 기능의 일부로 작동합니다. 사용자 인터페이스에서는 각 요일마다 "Start At"(시작 시간)과 함께 "Run duration"(실행 지속 시간)을 설정할 수 있습니다. 이 두 설정의 조합으로 감지 작업의 활성 시간대가 결정됩니다.

### 시간 계산 방식

"Start At" 시간부터 "Run duration"에 설정된 시간 동안 웹페이지 변경 감지가 활성화됩니다. 예를 들어:
- 시작 시간이 09:00
- 실행 지속 시간이
 8시간

이 경우 웹페이지 변경 감지는 09:00부터 17:00(09:00 + 8시간)까지 활성화됩니다.

### 요일별 설정

사용자는 월요일부터 일요일까지 각 요일에 대해 독립적으로 시작 시간과 실행 지속 시간을 설정할 수 있습니다. 이를 통해 주중과 주말에 서로 다른 일정을 적용하는 등 유연한 스케줄링이 가능합니다.

### 타임존 지원

changedetection.io는 타임존 설정을 지원합니다. "Optional timezone to run in" 필드에 타임존을 입력하면, 해당 타임존의 현지 시간에 맞춰 스케줄이 작동합니다. 이는 다른 국가나 지역의 웹페이지를 모니터링할 때 특히 유용합니다.

## 실용적 활용 사례

Duration Time의 실용적인 활용 방법은 다음과 같습니다:

### 업무 시간 모니터링

"Business hours" 바로가기를 클릭하면 자동으로 평일(월-금) 09:00부터 8시간 동안(17:00까지) 실행되는 일정이 설정됩니다. 이는 업무 시간 동안만 중요한 웹사이트의 변경을 모니터링하려는 사용자에게 이상적입니다.

### 특정 요일만 모니터링

예를 들어 일요일에만 웹페이지 변경을 확인하고 싶다면, 일요일의 "Start At" 체크박스만 선택하고 시작 시간을 00:00으로, 시간(Hours)을 23, 분(Minutes)을 59로 설정하면 됩니다. 이렇게 하면 일요일 자정(00:00)부터 23:59:59까지 웹페이지 변경이 감지됩니다.

## 결론

changedetection.io의 Duration Time 설정은 웹페이지 변경 감지의 시간적 범위를 제어하는 중요한 기능입니다. 이 기능을 통해 사용자는 특정 시간대에만 모니터링을 실행하여 시스템 자원을 효율적으로
 사용하고 비용을 절감할 수 있습니다. 스케줄러와 결합된 이 기능은 다양한 사용자 요구에 맞춰 유연하게 설정할 수 있어, 웹페이지 변경 감지를 더욱 스마트하게 관리할 수 있게 해줍니다.

타임존 지원과 함께 요일별 맞춤 설정이 가능한 Duration Time은 changedetection.io를 통한 웹페이지 모니터링을 더욱 효율적으로 만들어주는 핵심 요소라고 할 수 있습니다.



--


# ChangeDetection.io에서 디스코드 웹훅 알림 설정 가이드
ChangeDetection.io는 웹사이트 변경 사항을 모니터링하고 다양한 방법으로 알림을 보낼 수 있는 강력한 도구입니다. 그중에서도 디스코드 웹훅을 통한 알림 설정은 실시간으로 웹사이트 변경 사항을 팀과 공유하기에 매우 효과적인 방법입니다.
## 디스코드 웹훅 설정 방법
### 디스코드 서버에서 웹훅 생성하기
1. 디스코드 서버에서 알림을 받고 싶은 채널이 있는 서버를 선택합니다.
2. 서버 이름을 우클릭하고 **서버 설정**을 선택합니다.
3. 왼쪽 메뉴에서 **통합(Integrations)**을 클릭합니다.
4. **웹훅(Webhooks)** 항목을 클릭하고 **새 웹훅(New Webhook)** 버튼을 클릭합니다.
5. 웹훅의 이름을 설정하고(예: "ChangeDetection 알림"), 웹훅 메시지가 전송될 채널을 선택합니다.
6. 원하는 경우 웹훅의 프로필 이미지도 변경할 수 있습니다.
7. **웹훅 URL 복사(Copy Webhook URL)** 버튼을 클릭하여 웹훅 URL을 복사합니다.
### ChangeDetection.io에서 웹훅 URL 설정하기
웹훅 URL은 일반적으로 다음과 같은 형://discord.com/api/webho```/webhook_id/webhook_token
```# ChangeDetection.io에서 디스코드 웹훅 알림 설정 가이드
ChangeDetection.io는 웹사이트 변경 사항을 모니터링하고 다양한 방법으로 알림을 보낼 수 있는 강력한 도구입니다. 그중에서도 디스코드 웹훅을 통한 알림 설정은 실시간으로 웹사이트 변경 사항을 팀과 공유하기에 매우 효과적인 방법입니다.
## 디스코드 웹훅 설정 방법
### 디스코드 서버에서 웹훅 생성하기
1. 디스코드 서버에서 알림을 받고 싶은 채널이 있는 서버를 선택합니다.
2. 서버 이름을 우클릭하고 **서버 설정**을 선택합니다.
3. 왼쪽 메뉴에서 **통합(Integrations)**을 클릭합니다.
4. **웹훅(Webhooks)** 항목을 클릭하고 **새 웹훅(New Webhook)** 버튼을 클릭합니다.
5. 웹훅의 이름을 설정하고(예: "ChangeDetection 알림"), 웹훅 메시지가 전송될 채널을 선택합니다.
6. 원하는 경우 웹훅의 프로필 이미지도 변경할 수 있습니다.
7. **웹훅 URL 복사(Copy Webhook URL)** 버튼을 클릭하여 웹훅 URL을 복사합니다.
### ChangeDetection.io에서 웹훅 URL 설정하기
웹훅 URL은 일반적으로 다음과 같은 형식을 가집니다:
ChangeDetection.io에서는 다음과 같은 형식으로 변환하여 입scord://webhook_id/webhoo```oken
```# ChangeDetection.io에서 디스코드 웹훅 알림 설정 가이드
ChangeDetection.io는 웹사이트 변경 사항을 모니터링하고 다양한 방법으로 알림을 보낼 수 있는 강력한 도구입니다. 그중에서도 디스코드 웹훅을 통한 알림 설정은 실시간으로 웹사이트 변경 사항을 팀과 공유하기에 매우 효과적인 방법입니다.
## 디스코드 웹훅 설정 방법
### 디스코드 서버에서 웹훅 생성하기
1. 디스코드 서버에서 알림을 받고 싶은 채널이 있는 서버를 선택합니다.
2. 서버 이름을 우클릭하고 **서버 설정**을 선택합니다.
3. 왼쪽 메뉴에서 **통합(Integrations)**을 클릭합니다.
4. **웹훅(Webhooks)** 항목을 클릭하고 **새 웹훅(New Webhook)** 버튼을 클릭합니다.
5. 웹훅의 이름을 설정하고(예: "ChangeDetection 알림"), 웹훅 메시지가 전송될 채널을 선택합니다.
6. 원하는 경우 웹훅의 프로필 이미지도 변경할 수 있습니다.
7. **웹훅 URL 복사(Copy Webhook URL)** 버튼을 클릭하여 웹훅 URL을 복사합니다.
### ChangeDetection.io에서 웹훅 URL 설정하기
웹훅 URL은 일반적으로 다음과 같은 형식을 가집니다:
ChangeDetection.io에서는 다음과 같은 형식으로 변환하여 입력해야 합니다:
따라서 다음 단계를 따르세요:
1. ChangeDetection.io에 접속하여 모니터링 중인 사이트의 **편집** 또는 전체 설정의 **알림(Notifications)** 탭으로 이동합니다.
2. **Notification URL List** 필드에 변환된 디스코드 웹훅 URL을 입력합니다.
3. 디스코드 웹훅 URL에서 `webhook_id`와 `webhook_token`을 추출합니다.
   * 예를 들어, `https://discord.com/api/webhooks/123456789012345678/abcdefghijklmnopqrstuvwxyz`에서
   * `webhook_id`는 `123456789012345678`
   * `webhook_token`은 `abcdefghijklmnopqrstuvwxyz`입니다.
4. ChangeDetection.io에 다음 형식으로 입력합니다: `discord://123456789012345678/abcdefghijklmnopqrstuvwxyz`
5. **저장(Save)** 버튼을 클릭하여 설정을 저장합니다.
6. **Send test notification** 버튼을 클릭하여 테스트 알림을 보내볼 수 있습니다.
## 스크린샷 첨부 설정
ChangeDetection.io는 변경 사항 감지 시 스크린샷을 함께 전송할 수 있는 기능을 제공합니다:
1. 알림 설정 페이지에서 **Attach screenshot to notification (where possible)** 옵션을 체크합니다.
2. 이 옵션을 활성화하면 웹사이트 변경 사항이 감지될 때 스크린샷이 디스코드 메시지에 첨부되어 전송됩니다.
3. 주의: 이 기능은 스토리지 공간을 많이 사용할 수 있으므로, 변경 사항이 빈번한 웹사이트를 모니터링할 경우 신중하게 사용해야 합니다.
## 디스코드 웹훅 알림의 장점
1. **실시간 알림**: 웹사이트 변경 사항이 발생하면 즉시 디스코드 채널에 알림이 전송됩니다.
2. **팀 공유 용이성**: 특정 디스코드 채널에 알림을 보내 팀원들과 변경 사항을 쉽게 공유할 수 있습니다.
3. **모바일 접근성**: 디스코드 모바일 앱을 통해 데스크톱에 접속하지 않아도 알림을 받을 수 있습니다.
4. **커스터마이징 가능**: 알림 메시지의 제목, 내용, 이미지 등을 Jinja2 템플릿을 사용하여 사용자 정의할 수 있습니다.
5. **통합 관리**: 여러 웹사이트의 변경 사항을 한 채널에서 관리하거나, 웹사이트별로 다른 채널에 알림을 보낼 수 있습니다.
6. **시각적 확인**: 스크린샷 첨부 기능을 활용하면 변경 사항을 시각적으로 즉시 확인할 수 있습니다.
## 인증 요구사항
1. **디스코드 계정**: 웹훅을 생성하고 관리하기 위해서는 디스코드 계정이 필요합니다.
2. **서버 관리 권한**: 디스코드 서버에서 웹훅을 생성하기 위해서는 서버 관리 권한이나 웹훅 생성 권한이 필요합니다.
3. **ChangeDetection.io 접근 권한**: ChangeDetection.io 설정을 변경하기 위한 접근 권한이 필요합니다.
4. **추가 인증 없음**: 웹훅 URL만 있으면 추가적인 인증 없이 메시지를 보낼 수 있으므로, URL 보안에 주의해야 합니다.
## 네트워크 설정 요구사항
1. **기본 설정**: 일반적인 네트워크 환경에서는 추가적인 네트워크 설정이 필요하지 않습니다.
2. **방화벽 설정**: 기업 네트워크에서는 방화벽이 Discord API(discord.com)에 대한 아웃바운드 연결을 차단할 수 있으므로, 필요한 경우 IT 부서에 Discord API 접근 허용을 요청해야 합니다.
3. **프록시 설정**: 프록시 서버를 사용하는 환경에서는 ChangeDetection.io가 Discord API에 접근할 수 있도록 프록시 설정을 조정해야 할 수 있습니다.
4. **CORS 이슈**: 일부 환경에서는 CORS(Cross-Origin Resource Sharing) 문제가 발생할 수 있으며, 이 경우 헤더 설정을 조정해야 할 수 있습니다.
## 고급 웹훅 메시지 설정
디스코드 웹훅은 단순한 텍스트 메시지뿐만 아니라 다양한 형식의 메시지를 지원합니다:
1. **임베드(Embeds)**: 제목, 설명, 필드, 이미지 등을 포함하는 임베드 메시지를 보낼 수 있습니다.
2. **첨부 파일**: 스크린샷이나 기타 파일을 첨부하여 보낼 수 있습니다.
3. **메시지 형식**: 웹훅 메시지의 사용자 이름, 아바타 등을 설정할 수 있습니다.
## 결론
ChangeDetection.io와 디스코드 웹훅을 연동하면 웹사이트 변경 사항을 효과적으로 모니터링하고 팀과 공유할 수 있습니다. 설정 과정은 비교적 간단하며, 추가적인 네트워크 설정이 거의 필요하지 않은 장점이 있습니다. 다양한 커스터마이징 옵션과 모바일 접근성을 통해 변경 사항을 언제 어디서든 확인할 수 있어 효율적인 웹사이트 모니터링 솔루션을 제공합니다.
