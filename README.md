# Minah Kim — personal website

Website: https://minahkim-econ.github.io/

This is a plain HTML/CSS website. There is no Jekyll theme, JavaScript application, package installation, or build step. All page text is in the HTML files. Only the CV PDF is embedded from Google Drive.

## GitHub에서 수정하기

1. 수정할 파일을 열고 연필 모양 **Edit** 버튼을 누릅니다.
2. 해당 문장이나 링크를 수정합니다. `<p>`, `<h3>`, `<a>` 등 HTML 태그는 유지합니다.
3. **Commit changes**로 저장합니다. GitHub Pages 배포가 완료되면 홈페이지에 반영됩니다.

| 파일 | 수정할 내용 |
|---|---|
| `index.html` | 자기소개, 연구 분야, 학력, 연락처 |
| `research.html` | 논문 제목, 초록, 공동저자, 논문 링크 |
| `teaching.html` | 강의 이력, 강의평가 표와 학생 의견 |
| `cv.html` | CV PDF 링크와 미리보기 주소 |
| `style.css` | 글꼴, 색상, 여백, 사진 크기, 모바일 배치 |
| `profile.jpg` | 프로필 사진 |

예: 논문 제목을 PDF 링크로 바꾸려면 기존 `<h3>` 안에 다음처럼 링크를 넣습니다.

```html
<h3><a href="https://example.com/paper.pdf">Paper title</a></h3>
```

메뉴는 네 HTML 파일에 각각 들어 있습니다. 메뉴 이름이나 주소를 바꿀 때는 네 파일을 함께 수정합니다. 일반 본문 수정에는 다른 파일을 바꿀 필요가 없습니다.

CV는 기존 Google Drive 파일을 사용합니다. 동일한 Drive 파일의 버전을 업데이트하면 사이트 주소를 바꿀 필요가 없습니다. 다른 파일로 교체할 경우 `cv.html`의 `/view`와 `/preview` 두 주소를 함께 변경합니다. CV 파일 자체는 이 저장소에 포함하지 않습니다.

## GitHub Pages 설정

저장소 이름: `minahkim-econ.github.io`

**Settings → Pages → Deploy from a branch → main → /(root) → Save**

`.nojekyll` 파일은 Jekyll 처리를 건너뛰게 합니다. 이 파일 없이도 HTML/CSS 자체에는 Jekyll 문법이나 의존성이 없습니다.

## 검색 등록

페이지마다 고유 제목, 설명, canonical URL이 있으며 본문은 첫 HTML 응답에 포함됩니다. 메뉴는 일반 링크입니다. `robots.txt`는 수집을 허용하고 `sitemap.xml`은 네 페이지를 나열합니다.

배포 후 Google Search Console에서 `https://minahkim-econ.github.io/`를 URL-prefix 속성으로 등록하고 소유권을 확인합니다. 인증용 HTML 파일 또는 메타 태그는 Search Console에서 실제로 발급받은 값을 사용합니다. 사이트맵 `https://minahkim-econ.github.io/sitemap.xml`을 제출하고 URL 검사를 통해 색인을 요청합니다. 기술 설정과 색인 요청은 검색 노출이나 순위를 보장하지 않습니다.

주소를 바꿀 경우 네 HTML 파일의 canonical/og:url, 홈페이지 JSON-LD, robots.txt, sitemap.xml의 주소도 함께 변경합니다. 본문을 실제로 수정할 때 해당 sitemap 항목의 lastmod 날짜를 갱신합니다.

기존 Google Sites와 학과 프로필의 링크를 새 주소로 연결하면 방문자와 검색엔진이 새 사이트를 찾는 데 도움이 됩니다.

## 로컬 미리보기

이 폴더에서 `python3 -m http.server 8765`를 실행하고 `http://localhost:8765/`를 엽니다. HTML 파일을 더블클릭해서 볼 수도 있습니다.
