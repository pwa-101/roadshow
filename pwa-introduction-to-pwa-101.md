<!-- page_number: true -->
<!-- prerender: true -->
<!-- $width: 1980px -->
<!-- $height: 1080px -->

# 프로그레시브 웹앱, 간단하게 알아보기

> Introduction to PWA (Progressive Web App)
> [@Jimmy Moon](https://github.com/ragingwind), [GDE](https://developers.google.com/experts/people/jimmy-moon) for Web Tech in Korea

---

# Progressive 💙 Web = App 👶

---

# 프로그레시브 (Progressive)

> 점진적 개선 (Progressive Enhancement) 을 통해서 점점 더 앱 (네이티브) 처럼 되어가는 것 (Progressively Becoming Apps) - @[Alex Russell](https://infrequently.org/2015/06/progressive-apps-escaping-tabs-without-losing-our-soul/)

---

# 점진적 개선 ([Progressive Enhancement](alistapart.com/article/understandingprogressiveenhancement))

![170% center](https://alistapart.com/d/understandingprogressiveenhancement/m-m.jpg)
![]()
> (모바일) 인터넷 환경에서 브라우저/플랫폼이 제공하는 기능를 최대한 사용, 점차 새로이 개발되는 웹 표준 기술을 사용한 레이어를 점진적으로 추가해서 웹앱을 강화시키는 전략

---

# 웹 기술의 진보 (Progressive Movement)

#### Web Application (199X ~ 2007)

- HTTP + HTML Document, CGI, XMLHTTP, Ajax (Gmail), HTML5

#### Web Libraries/Frameworks (2008 ~)

- WoF (War of Frameworks)

#### Web Tech, with Mobile (2011 ~)

- Chrome for Android, Web RTC / Socket / GL / Audio / Animation, IndexedDB

#### Progressive Web App (2013 ~)

- Service Worker, Web Component / Manifest / Push / Notification

#### The Next Big Things of Whe Web

- Web Payment, Web VR, Media Session, Web APK, Web Bluetooth

---

# 앱(네이티브) 처럼 되어가는 것 (Progressively Becoming Apps)

> 웹앱이 가지고 있는 한계를 웹 기술의 도움으로 넘어가면서 웹앱이 가진 장점을 그대로 가지면서 앱이 제공하는 사용자 경험까지 흡수 하는 것

---

# 앱(네이티브)과 웹의 비교

|                   | App  | Web  |
| ----------------: | :--: | :--: |
|  앱 접근성(검색)과 설치 경험 | 💩💩 |  👌  |
| 홈스크린, 런처, 테스크 매니저 |  👌  |  ❌   |
|        실행/구동 퍼포먼스 |  👍  |  💩  |
|          컨텐츠 업데이트 |  💩  |  👌  |
|              오프라인 |  👌  |  ❌   |
|         멀티플랫폼, 벤더 |  💩  |  👌  |
|          백그라운드 동작 |  👌  |  ❌   |
|         푸쉬 노티피케이션 |  👌  |  ❌   |
|        시스템 리소스 접근 |  👌  |  ❓   |

---

# 앱(네이티브)과 웹과 PWA의 비교

|                   | App  | Web  | PWA  |                                          |
| ----------------: | :--: | :--: | :--: | :--------------------------------------- |
|  앱 접근성(검색)과 설치 경험 |  💩  |  👌  |  👌  | [Android Instant Apps](https://goo.gl/L9K4pV) |
| 홈스크린, 런처, 테스크 매니저 |  👌  |  ❌   |  👌  | Web Manifest, Web APK                    |
|        실행/구동 퍼포먼스 |  👍  |  💩  |  ❓   | Performance Enhancement                  |
|          컨텐츠 업데이트 |  💩  |  👌  |  👌  |                                          |
|              오프라인 |  👌  |  ❌   |  👌  | Service Worker                           |
|         멀티플랫폼, 벤더 |  💩  |  👌  |  👌  |                                          |
|          백그라운드 동작 |  👌  |  ❌   |  👌  | Service Worker                           |
|         푸쉬 노티피케이션 |  👌  |  ❌   |  👌  | Service Worker, Web Push/Notification    |
|        시스템 리소스 접근 |  👌  |  ❓   |  👌  | Geolocation, Media API, Web Bluetooth/VR |

---

# 프로그레시브 웹앱 in Business

> 비개발국과 이미징 마켓을 위한, 폭발적인 인터넷 유저 증가율, 저사양 모바일폰 대세, 모바일네트웍 온리, 낫 옵션(No LTE), (상대적으로 )비싼 모바일 데이터 플랜 그리고 압도적인 미래 고객수 그리고 압도적인 모바일 웹 사용율과 증가율

---

![bg original](https://cloud.githubusercontent.com/assets/124117/23336571/336dd952-fc17-11e6-9196-b270f6d0ee99.png)

---

![bg original](https://cloud.githubusercontent.com/assets/124117/23336572/338f6d1a-fc17-11e6-9b5f-f26ea674ba8f.png)

---

![bg original](https://cloud.githubusercontent.com/assets/124117/23336573/33aa02b0-fc17-11e6-85b7-39a061089725.png)

---

![bg original](https://cloud.githubusercontent.com/assets/124117/23336574/33abed8c-fc17-11e6-8c85-43c1c97199ae.png)

---

![bg original](https://cloud.githubusercontent.com/assets/124117/23336575/33add8c2-fc17-11e6-8f26-b986643f6bc6.png)

---

![bg original](https://cloud.githubusercontent.com/assets/124117/23336577/33b0b29a-fc17-11e6-9aa4-cbc597999b38.png)

---

![bg original](https://cloud.githubusercontent.com/assets/124117/23336578/33b9e734-fc17-11e6-8190-df8cee5db17a.png)

---

![bg original](https://cloud.githubusercontent.com/assets/124117/23336580/33cf40de-fc17-11e6-9ba6-7487ee64b603.png)

> Top of 1000 mobile apps VS top of the 1000 mobile web properties 

![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()

---

![bg original](https://cloud.githubusercontent.com/assets/124117/23336579/33cda6c0-fc17-11e6-8f17-554cc1cd1960.png)

---

![bg original](https://cloud.githubusercontent.com/assets/124117/23336633/d895a6fc-fc18-11e6-9ffe-ed1f3f2d34e9.png)

---

# 프로그레시브 웹앱 임팩트

|                                       회사 | 임팩트                                      |
| ---------------------------------------: | :--------------------------------------- |
|        [Flipkart](https://goo.gl/RsYhwW) | 체류시간 3배 증가, 40% 재방률 증가, 70% 유입, 3배 적은 데이터 절약 |
|           [Jumia](https://goo.gl/VJiZ6O) | 사용률 38%, 푸쉬에 의한 구매율 9배 증가                |
|           [Suumo](https://goo.gl/8QcbRi) | 75% 로딩시간 감소, 푸쉬로 31% 재방문율 증가             |
|      [AliExpress](https://goo.gl/XcLWnS) | 104% PWA로 유입, 사용자당 2배이상의 페이지 방문, 체류시간 74% 증가 |
| [eXtra Electronics](https://goo.gl/uuAUrM) | 푸쉬로 판매량 100% 증가, 4배의 재방문률                |
|            [BaBe](https://goo.gl/bE3YZI) | 네이티브앱과 같은 효과                             |
|           [Konga](https://goo.gl/tiB48U) | 네이티브앱, 이전 웹앱 대비 압도적인 데이터 절약 퍼포먼스         |
|          [5miles](https://goo.gl/olsStm) | 30% 체류시간 증가, A2HS 로 30% PWA 유입율 증가       |
| [Carnival Cruise Line](https://goo.gl/aL6C21) | 푸쉬 사용율 24% 증가, 48% 가 푸쉬로 유입              |

---

# 프로그레시브 웹앱을 이루는 주요 기술

- HTTP2, with HTTPS and Server Push
- **Service Worker**
- **Web Manifest** and *Web APK (Not Yet, but Very Soon)*
- **Push Notification**
- Performance Enhacement
  - [RAIL](https://developers.google.com/web/fundamentals/performance/rail) Pattern
  - [PRPL](https://developers.google.com/web/fundamentals/performance/prpl-pattern/) Pattern
    - [Page Load Performance](https://goo.gl/6iKjlO)
    - Preloading: [Server Side Rendering](https://medium.com/@addyosmani/progressive-web-apps-with-react-js-part-4-site-is-progressively-enhanced-b5ad7cf7a447#.5ypf9a9ie)
    - Lazy-loading: [navigation preload](https://www.smashingmagazine.com/2016/02/preload-what-is-it-good-for/), [Code-splitting with Webpack(https://goo.gl/2qi7hY)
    - Parallel-loading Patterns: [navigation-preload](https://developers.google.com/web/updates/2017/02/navigation-preload)
- The Next Big Things of the Web: Web Assembly, Newbie Web Frameworks


---
# 전망, 프로그레시브 웹앱이 만능인가?

> 데스크탑 처럼 각자의 장점을 살려 포지셔닝 될 것

![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()
![]()
![bg original](https://cloud.githubusercontent.com/assets/124117/23336699/88cb72da-fc1a-11e6-9661-919958cb66f2.png)

---

# References

- [Progressive Web Apps - Google Developers](https://goo.gl/KdWhwv)
- [Google Codelabs for Web](https://goo.gl/wOFMFX)
- [JavaScript Start-up Performance](https://goo.gl/Dc4SBO)
- [Progressive Web Apps with React.js: Part I](https://goo.gl/ntYlR6)
  - [Progressive Web Apps with React.js in a Nutshell (한글)](https://goo.gl/IGGT04)
  - [Progressive Web Apps with React.js from Scratch (한글)](https://goo.gl/fSF8Zh)
- [PWA Roadshow - Materials, Slides and examples for PWA 101 Roadshows](https://goo.gl/kL0eeR)
- Videos
  - [Chrome Dev Summit 2016 - YouTube](https://goo.gl/TkgXYM)
  - [Progressive Web App Summit 2016 - YouTube](https://goo.gl/D4ZqEM)
  - [Google I/O 2016 - YouTube](https://goo.gl/olw6kV)
  - [Google Developers Summit Korea 2016 - YouTube](https://goo.gl/o4mfGL)
