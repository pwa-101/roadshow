<!-- $theme: default -->
<!-- $size: 4:3 -->

# PWA 101: Service Worker for very newbies

[@cwdoh](https://twitter.com/cwdoh), GDE for Web

<!-- page_number: true -->

---
## Web Worker

> 메인 페이지와 병렬 **스크립트를 실행하는 백그라운드 워커를 생성**하는 API
> **메세지 전송 기반의 Thread와 유사한 동작**을 가능하게 한다. 

---
## Web Worker의 일반적 기능

> UI 스레드에서 분리되어 실행하여야 하므로

* DOM에 대한 직접 접근/조작 불가
* 자체적인 글로벌 스코프
* 일부 속성과 API만 허가

---
# [Service Worker](https://www.w3.org/TR/service-workers/)

> 오프라인일 경우에도 웹 어플리케이션의 기동을 가능하도록 하는 훅(Hook)을 포함하여, 어플리케이션으로 하여금 **지속적인 백그라운드 프로세싱의 장점을 취하도록** 하는 방법

---
## 서비스 워커 역시 또 다른 종류의 워커

지속적인 백그라운드 처리
* **이벤트 드리븐** 모델
* **설치, 버전 및 업그레이드** 관리를 위한 시스템 기능
* 다른 **백그라운드 프로세싱** 관련 기능 표준들을 위한 **보편적 진입점**

---
### **ServiceWorker**

### Service Worker: `지속적`, `설치`, `브라우저`

> 브라우저에 설치되는 일종의 시스템 요소와 유사한 기능

* 페이지/브라우저가 실행 중이지 않더라도 브라우저에 의해 라이프사이클이 제어
* 페이지 외부 요소 제어를 위한 이벤트 모델
* [원격 푸시 알림]()이나 [백그라운드 동기화]()의 최초 진입점으로 적합

---
**기억하세요!**

> ..., **지속적인** 백그라운드 처리의 장점을 어플리케이션이 취하는 것을 가능하게 하는...

---
## Service Worker ❤️ HTTPS

> `중간자 공격(man-in-the-middle-attack)`을 피하기 위함
> 대신 `127.0.0.1`이나 `localhost`로 테스트 가능



---
## 오프라인 웹 앱

> 여러분만의 공룡!!! 한정판!! :-p

![https://addyosmani.com/assets/bjvR2Sl.png](https://addyosmani.com/assets/bjvR2Sl.png)

----
### 배워야 할 것

1. 우리가 직접 조작해야 할 [_`Caches`_](https://w3c.github.io/ServiceWorker/#cache-objects)
2. 이벤트 생명 연장의 꿈: [_`.waitUntil()`_](https://w3c.github.io/ServiceWorker/#wait-until-method)
3. 네트워크를 통한 리소스 접근: [_`fetch`_](https://w3c.github.io/ServiceWorker/#fetch-event-section)

---
### [Cache Storage](https://developer.mozilla.org/en-US/docs/Web/API/CacheStorage)

> [`Promise 객체`](https://developers.google.com/web/fundamentals/getting-started/primers/promises)를 반환하는 캐시 저장소 인터페이스
> * `.match()`
> * `.has()`
> * `.open()`
> * `.delete()`
> * `.keys()`

---
### [.waitUntil()](https://developer.mozilla.org/en-US/docs/Web/API/ExtendableEvent/waitUntil)

> 이벤트가 종료되지 않도록...

---
### [.onfetch](https://developer.mozilla.org/en-US/docs/Web/API/ServiceWorkerGlobalScope/onfetch)

> 브라우저에 리소스 접근이 요청될 때 호출되는 이벤트

---
#### [`FetchEvent`](https://developer.mozilla.org/en-US/docs/Web/API/FetchEvent)
> `.onfetch` 핸들러로 전달되는 이벤트 객체
* 요청 정보를 담고 있고 응답을 위한 인터페이스 제공
* [`.respondWith()`](https://developer.mozilla.org/en-US/docs/Web/API/FetchEvent/respondWith)를 통해 응답을 관리

---
### 코드랩: Offline AMP

> * `install` 이벤트를 통한 리소스 설치
> * `fetch` 이벤트를 이용한 오프라인 응답

---
## Links

* [Service Worker 101](https://goo.gl/6l28Zv)
* [Service Worker 201](https://goo.gl/wWtBq0)

---
# Thank you!

<style>
.portrait {
    border-radius: 50%;
    border: 5px solid #fff;
    background-image: url(https://avatars2.githubusercontent.com/u/2120719);
    background-size: 100% 100%;
    width: 250px;
    height: 250px;
    content: '';
}
</style>
<div class="portrait"></div>
