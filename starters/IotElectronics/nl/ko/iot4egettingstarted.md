---

copyright:
  years: 2016, 2017
lastupdated: "2017-04-07"
---

<!-- Common attributes used in the template are defined as follows: -->
{:new_window: target="\_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

<!-- Note to writers - index.md and iot4egettingstarted.md are (almost) duplicates and a change to one should be made to both. index.md appears within the product app as the getting started page. iot4egettingstarted.md appears as the top level topic in the docs toc. -->

# {{site.data.keyword.iotelectronics}} 스타터로 앱 작성

{{site.data.keyword.iotelectronics_full}}는 사용자 앱이 연결된 어플라이언스와 통신, 제어, 분석 및 업데이트할 수 있는 통합 엔드-투-엔드 솔루션입니다. 스타터에는 시뮬레이션된 어플라이언스를 작성하는 데 사용할 수 있는 스타터 앱과 모바일 디바이스에서 이러한 어플라이언스를 제어하는 데 사용할 수 있는 샘플 모바일 앱이 포함됩니다.
{:shortdesc}

## 시작하기 전에

시작하기 전에 {{site.data.keyword.Bluemix_notm}} 조직에 {{site.data.keyword.iotelectronics}}의 인스턴스를 배치해야
 합니다. 인스턴스를 배치하면 스타터의 컴포넌트 애플리케이션 및 서비스가 자동으로 배치됩니다. 

 {{site.data.keyword.Bluemix_notm}} 카탈로그의 표준 유형 섹션에서 [{{site.data.keyword.iotelectronics}} 스타터 찾기](https://console.{DomainName}/catalog/starters/iot-for-electronics-starter/)를 할 수 있습니다. 

## {{site.data.keyword.iotelectronics}} 시작하기
시작하려면 다음 태스크를 완료하십시오. 

1. {{site.data.keyword.iotelectronics}} 스타터 웹 애플리케이션을 사용하여 [시뮬레이션된 어플라이언스를 작성](iot4ecreatingappliances.html)하십시오. 시연을 위해 {{site.data.keyword.iotelectronics}} 스타터에서는 세탁기를 시뮬레이션된 어플라이언스로 사용합니다. 사용자는 모든 유형의 스마트 전자 기기를 연결할 수 있습니다. 
2. (선택사항) [{{site.data.keyword.appid_full}}로 모바일 로그인 옵션을 구성](https://console.ng.bluemix.net/docs/services/appid/index.html)하십시오. 모바일 앱에 표시되는 로그인 화면의 모양을 사용자 정의할 수 있습니다. 또한 선택적으로 소셜 로그인 신임 정보를 사용하거나 사용하지 않을 수 있습니다. 기본적으로 {{site.data.keyword.appid_short_notm}}에서는 Facebook 및 Google+를 통한 권한 부여가 가능하므로 모바일 앱 사용자는 자신의 소셜 신임 정보를 사용하거나 로그인 프로세스를 생략하여 로그인 없이 앱을 사용해 볼 수 있습니다. 
3. 샘플 모바일 앱을 [다운로드하고 연결](iotelectronics_config_mobile.html)하십시오. 


## 다음에 수행할 작업
{{site.data.keyword.iotelectronics}}에서 수행할 수 있는 작업을 확인하십시오. 

- [스타터 앱을 탐색](iot4ecreatingappliances.html)하여 엔터프라이즈 제조업체에서 {{site.data.keyword.iot_short_notm}}에 연결된 어플라이언스를 어떻게 모니터할 수 있는지 경험하십시오. 
- [샘플 모바일 앱을 탐색](iotelectronics_config_mobile.html)하여 어플라이언스 소유자가 어떻게 해당 어플라이언스를 등록하고 상호작용하는지 경험하십시오. 
- {{site.data.keyword.iot_short_notm}}에서 등록된 어플라이언스의 [데이터를 탐색하고 관리](iotelectronics_dashboard.html)하십시오.
- [API를 탐색하여 ![외부 링크 아이콘](../../icons/launch-glyph.svg)](http://ibmiotforelectronics.mybluemix.net/public/iot4eregistrationapi.html){:new_window} 고유 {{site.data.keyword.iotelectronics}} 앱을 사용자 정의하고 확장하는 방법을 확인하십시오.
