## 🌐 서버와 클라이언트, 웹 기초 요약

### 🖥️ 서버(Server)와 클라이언트(Client)
| 구분 | 역할 |
|------|------|
| **클라이언트(Client)** | 서버에게 요청(Request)을 보내는 주체 |
| **서버(Server)** | 요청을 받아 응답(Response)을 처리하는 주체 |

---

### 💬 웹(Web)
- **요청(Request)** 과 **응답(Response)** 이 이루어지는 공간  
- 클라이언트와 서버 간의 통신이 일어나는 장소

---

### 🌏 웹 브라우저(Web Browser)
- 사용자의 요청에 따라 **웹 서버에 접근**, 인터넷 콘텐츠를 **검색 및 열람**하는 응용 프로그램  
- 예: Chrome, Edge, Safari, Firefox 등  

---

### 📡 프로토콜(Protocol)
- 네트워크 통신에서 **데이터를 주고받기 위한 규칙(약속)**  
- 예시: “사용자의 요청에 반드시 응답해야 한다”  

#### 주요 프로토콜
| 종류 | 설명 |
|------|------|
| **HTTP (HyperText Transfer Protocol)** | 클라이언트와 서버 간 자원(HTML 등)을 텍스트 기반으로 주고받는 규약. 암호화되지 않아 노출 위험 있음. |
| **HTTPS (HyperText Transfer Secure Protocol)** | 데이터를 **공개키 암호화 방식**으로 암호화하여 안전하게 통신하는 규약. |

---

### 🔢 IP (Internet Protocol)
- 인터넷에서 각 컴퓨터를 구별하기 위한 **고유 식별 번호**  
- 네트워크 상에서 다른 컴퓨터를 찾는 데 사용됨  

---

### 🏷️ DNS (Domain Naming Service)
- 숫자로 된 IP 주소를 사람이 읽기 쉬운 **도메인 이름**으로 변환하는 서비스  
  예: `www.google.com → 142.250.196.68`

---

### 🕸️ WWW (World Wide Web)
- 전 세계 컴퓨터가 인터넷으로 연결되어 **정보를 공유**하는 공간  

---

### 🧭 W3C (World Wide Web Consortium)
- **웹 표준(Web Standards)** 을 제정하고 관리하는 **중립적 국제 기관**

---

## 🧱 웹 표준(Web Standard)

| 구성 요소 | 약어 | 설명 |
|------------|------|------|
| **HTML** | HyperText Markup Language | 웹 페이지의 기본 구조를 만드는 마크업 언어 |
| **CSS** | Cascading Style Sheets | 페이지의 레이아웃과 디자인(스타일)을 정의 |
| **JS** | JavaScript | 사용자와의 상호작용, 이벤트 처리, 비동기 통신 등을 담당하는 스크립트 언어 |
| **XML** | Extensible Markup Language | 데이터 전달을 위한 사용자 정의 태그 기반 언어 |

📘 **XML 예시**
```xml
<?xml version="1.0"?>
<user>
   <user-id>hds1234</user-id>
   <name>홍길동</name>
</user>
```

---

## 🧩 HTML 기본 구조

```html
<p> You are better </p>
```

| 구분 | 의미 |
|------|------|
| (1) 여는 태그 `<p>` | 태그 이름을 여는 괄호로 감싼 형태 |
| (2) 내용 | 태그 안에 들어가는 실제 텍스트 |
| (3) 닫는 태그 `</p>` | 태그 이름 앞에 `/`가 붙음 |

---

### ⚙️ 속성(Attributes)
```html
<p class="conversation">You are much better</p>
```
- 태그에 **추가적인 정보를 부여**할 때 사용  
- 화면에는 표시되지 않지만, 식별·스타일·연산 등에서 활용됨  

#### 속성 작성 규칙
1. 태그 이름과 속성 사이에는 **공백**이 있어야 함  
2. 여러 속성이 있을 경우 속성 사이에도 공백을 둔다  
   ```html
   <p class="conversation" id="conv1">내용</p>
   ```
3. 속성명 뒤에는 `=` 작성  
4. 속성값은 **따옴표("")** 로 감싼다  

---

## 🧱 HTML 요소의 종류

### 🧊 블록(Block) 요소
- 한 줄 전체를 차지하는 요소  
- 대표 태그: `p`, `h1~h6`, `ul`, `ol`, `div`, `form`, 등  
- 영역 단위로 표시되며, 다음 요소는 아래로 내려간다  
- **width / height / margin / padding** 모두 적용 가능  

📘 예시
```html
<p>apple</p><p>banana</p>
```
📺 화면 결과
```
apple
banana
```

---

### 🩸 인라인(Inline) 요소
- 한 줄 내에서 이어서 표시되는 요소  
- 대표 태그: `span`, `a`, `img`, `strong`, `em`  
- 내용만큼의 영역만 차지  
- **width, height** 직접 지정 불가  
- **margin-top/bottom** 적용 안 됨  
- **padding-top/bottom**은 동작하지만 시각적 변화는 거의 없음  

📘 예시
```html
<span>apple</span><strong>banana</strong>
```

---

### 🧮 인라인-블록(Inline-Block) 요소
- 인라인처럼 한 줄에 표시되지만 **자신의 영역을 명확히 가짐**  
- 대표 태그: `button`, `input`, `select`  
- **width / height / margin / padding** 모두 적용 가능  
- 인라인과 블록의 장점을 모두 가짐  

---

✅ **정리 요약**
| 구분 | 줄바꿈 | 크기 지정 | margin/padding |
|------|----------|-------------|----------------|
| **블록 요소** | 있음 | 가능 | 모두 적용 |
| **인라인 요소** | 없음 | 불가 | 제한적 |
| **인라인-블록 요소** | 없음 | 가능 | 모두 적용 |
