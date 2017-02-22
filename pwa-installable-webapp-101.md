<!-- page_number: true -->
<!-- $size: 16:9 -->

# 설치형 웹앱 만들기

> Turn your webapp into an installable webapp
> [@Jimmy Moon](https://github.com/ragingwind)

---

# 설치형(Installable)이란?

- 네트웍이 불안하거나 오프라인인 경우에도 동작
- 홈스크린에서 사용자가 바로 실행
- 앱을 잘 설명하는 이름과 아이콘 제공
- 사용자가 필요한 앱 (이면 베스트)

---

# 언제나 동작가능한 웹앱

- 서비스워커의 지원
- 프리캐쉬(Pre-cache) 된 어플리케이션 프레임(App-shell) 사용
- 서비스워커, Indexed DB 등에 저장된 히스토리컬(Historical) 데이터 디스플레이

---

# 웹매니스트(Web Manifest) 작성하기

```json
{
  "name": "bare-react-app",
  "short_name": "bare-react-app",
  "icons": [{
    "src": "icon-192x192.png",
    "sizes": "192x192",
    "type": "image/png"
  }, {
    "src": "icon-384x384.png",
    "sizes": "384x384",
    "type": "image/png"
  }],
  "start_url": "./?utm_source=web_app_manifest",
  "display": "standalone",
  "background_color": "#1A1A1A",
  "theme_color": "#0A0A0A",
  "orientation": "portrait"
}
```

---

![web manifest sample](https://cloud.githubusercontent.com/assets/124117/21298849/12675c7a-c5d9-11e6-834d-0f6f202fb700.png)

---

![web manifest sample2](https://cloud.githubusercontent.com/assets/124117/21298823/c7b4e4fe-c5d8-11e6-8444-30c2085934fc.png)

---

![web manifest sample3](https://cloud.githubusercontent.com/assets/124117/21298822/c7b2022a-c5d8-11e6-8a06-9a64b0a446ec.png)

---

![web manifest sample4](https://cloud.githubusercontent.com/assets/124117/21298821/c79a23a8-c5d8-11e6-95c2-68beb2910e81.png)

---

![web manifest sample5](https://cloud.githubusercontent.com/assets/124117/21298820/c79643f0-c5d8-11e6-81d7-e74d44ea1fc4.png)

---

![web manifest sample6](https://cloud.githubusercontent.com/assets/124117/21298819/c793d0c0-c5d8-11e6-8fe0-6992dc7d78ff.png)

---

![web manifest sample7](https://cloud.githubusercontent.com/assets/124117/21298818/c79272a2-c5d8-11e6-957a-9feec89f5ca2.png)

---

![web manifest sample8](https://cloud.githubusercontent.com/assets/124117/21298817/c790477a-c5d8-11e6-84fd-d1bf9b41e5d2.png)

---

![web manifest sample9](https://cloud.githubusercontent.com/assets/124117/21298816/c78ffc52-c5d8-11e6-8cb2-f3a5ed7085ec.png)

---

![bg 100% original](https://cloud.githubusercontent.com/assets/124117/21291999/3081fd7e-c538-11e6-9961-d639d8e51efe.png)

---

# 앱 인스톨 부추기기(Prompting)

> 크롬이 능동적으로, 사용자의 충성도를 휴리스틱(Huristic) 한 방법으로 측정

![bg original](https://cloud.githubusercontent.com/assets/124117/21297934/193a259e-c5cc-11e6-8a89-78c6c7ffc4b7.png)

---

## 부추기기 막기

![bg original](https://cloud.githubusercontent.com/assets/124117/21297995/0194dffa-c5cd-11e6-8943-0e348d9a244f.png)

<pre style="width:72%">
// 인스톨 배너 막기 (Suppress prompt)
window.addEventListener(<span style="color:red">'beforeinstallprompt'</span>, e => {
  e.preventDefault();
});
</pre>

---

## 부추기기 나중에 보여주기

![bg original](https://cloud.githubusercontent.com/assets/124117/21297933/1927a6da-c5cc-11e6-8a2f-af51b5dd61e9.png)

<pre style="width:72%">
// 부추기기 나중에 보여주기 (Defer to a later time)
<span style="color:red">let deferredEvent;</span>

window.addEventListener("beforeinstallprompt", e => { 
  e.preventDefault(); // 일단 이벤트는 중지
  <span style="color:red">deferredEvent = e;</span> // 이벤트 객체를 `지연 객체`에 보관
  // 인스톨 버튼 보여짐 (show install button)
  // [airhorn/index.html](https://goo.gl/Yt7wJZ)
});

button.addEventListener("click", e => {
  deferredEvent.prompt();
});
</pre>

---

## 부추기기 나중에 보여주려고 했던 것 보여주기

![bg original](https://cloud.githubusercontent.com/assets/124117/21297934/193a259e-c5cc-11e6-8a89-78c6c7ffc4b7.png)

<pre style="width:72%">
let deferredEvent;

window.addEventListener("beforeinstallprompt", e => { 
  e.preventDefault();
  deferredEvent = e;
});

// 인스톨 버튼 이벤트 처리
button.addEventListener("click", e => {
  <span style="color:red">deferredEvent.prompt();</span> // 부추기기 보여짐
});

</pre>

---

## 부추기기를 통한 사용자의 결정 판단하기

![bg original](https://cloud.githubusercontent.com/assets/124117/21297932/18ffa9d2-c5cc-11e6-8d37-6a7d084fe269.png)

<pre style="width:72%">
// 사용자의 결정 판단하기 (Understand the user’s choice)
window.addEventListener("beforeinstallprompt", 
  e => {
  e.prompt().then(r => <span style="color:red">r.userChoice</span>)
     .then(c => {
       if(c.choice == "installed") {
         // 사용자가 인스톨하기로 결정
       } else {
         // 사용자가 인스톨하지 `않기로` 결정
       }
     });
  }
);
</pre>

---

![bg original](https://cloud.githubusercontent.com/assets/124117/21292070/1ba23376-c53b-11e6-8d9b-480150dd2b3b.png)

---

![center](https://cloud.githubusercontent.com/assets/124117/21292071/1ba2569e-c53b-11e6-8f99-bbcc93d64ff0.png)

---

#### [Favicon Generator for all platforms](https://goo.gl/zgcCbG)
![38% center](https://cloud.githubusercontent.com/assets/124117/21292058/841b40d8-c53a-11e6-95fa-5d7c3ae5271f.png)

---

#### [pwa-manifest](https://www.npmjs.com/package/pwa-manifest-cli) on npm

![140% center](https://camo.githubusercontent.com/7eed8608008201bea86fd98448defaf246a3c5d4/687474703a2f2f672e7265636f726469742e636f2f6b775234446837724d332e676966)

---

# 정리하면

- 서비스워커 등록, 동작 확인
- 따라서 HTTPS 는 필수
- 웹매니페스트를 준비
- 이쁜 아이콘들 준비
- 앱 목적에 맞게 값을 잘 기술
- 사용자가 흥미를 가지게 되면

---

# License

The content of this project itself is licensed under the [Creative Commons Attribution 3.0 license](http://creativecommons.org/licenses/by/3.0/us/deed.en_US), and the underlying source code used to format and display that content is licensed under the [MIT license](http://opensource.org/licenses/mit-license.php).
