---
title: github blog와 google 연동하기
date: 2023-11-09 13:00:00 +09:00
categories: [GitHub_Blog]
tags: [chirpy, blog, github, github blog, 깃허브, google, Google Search Console, sitemap]
---

## GitHub Blog 시리즈
> github blog도 만들고 chirpy 테마도 적용하였으면 이제 본격적으로 나만의 블로그 만들기!

[GitHub Blog_1 chirpy 테마 블로그 꾸미기](https://minjung405.github.io/posts/chirpy-%ED%85%8C%EB%A7%88-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EA%BE%B8%EB%AF%B8%EA%B8%B0/)\
[GitHub Blog_2 github blog 포스트 작성하기](https://minjung405.github.io/posts/github-blog-%ED%8F%AC%EC%8A%A4%ED%8A%B8-%EC%9E%91%EC%84%B1%ED%95%98%EA%B8%B0/)\
[GitHub Blog_3 markdown 파일 작성하기]()\
[GitHub Blog_4 github blog와 google 연동하기]()


## Google Search Console
> Google Search Console은 구글 검색 결과에서 자신의 github 블로그를 보여지게 하는 도구에요.

- Google Search Console에 블로그 등록하기
1. [**Google Search Console**](https://search.google.com/search-console/about?hl=ko&utm_source=wmx&utm_medium=wmx-welcome) 접속하고 <kbd>시작하기</kbd> 클릭
2. URL 접두어 부분에 자신의 github blog 주소 입력하기
3. 소유권 확인 창이 뜨면 파일을 다운로드하고, 자신의 github.io 폴더에 다운로드 받은 html 파일 추가하기
4. git push까지 해준 뒤 <kbd>확인</kbd> 누르기

- sitemap 생성하기
1. [**sitemap 생성 사이트**](https://www.xml-sitemaps.com/) 접속해서 자신의 블로그 주소를 입력하여 <kbd>start</kbd>, <kbd>VIEW SITEMAP DETAILS</kbd>, <kbd>DOWNLOAD YOUR XML SITEMAP FILE</kbd> 차례로 눌러주기
2. 다운받은 sitematp.xml을 자신의 github.io 폴더에 추가하기
3. sitemap.xml이 있는 위치에 `robots.txt`{: .filepath} 파일 생성한 후 다음 내용 적어주고,\
다시 git add, commit, push 해주기

```
User-agent: *
Allow: /

Sitemap: https://자신의 깃허브 블로그 주소/sitemap.xml
```
{: file='robots.txt'}

- Google Search Console에 sitemap 적용하기
1. Google Search Console <kbd>속성 검색</kbd> 클릭하고 자신의 깃허브 블로그 선택
![google_sc](/assets/img/post_image/2023.11.09/google_sc.png)
2. <kbd>sitemap</kbd> 항목으로 들어가서 sitemap.xml 입력하고 제출하기 (등록 완료 후 7일 이내로 검색 가능)

"**`깃허브 블로그 주소`에 대한 Google 검색 트래픽 모니터링**" 제목으로 메일이 오면 끝났어요.\
이제 다음과 같이 날짜별로 블로그 노출 수, 클릭 수를 확인 할 수 있어요.
![google_sc2](/assets/img/post_image/2023.11.09/google_sc2.png)


## Google Analytics, Google Adsense
> 추후에 필요하다고 판단되면, 적용해보고 정리해서 포스팅 하려고 해요.


### 참고
{: data-toc-skip='' .mt-4 .mb-0 }
> [**dodev님의 포스팅**](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-4/#step-4-1-google-search-console)을 참고했고, 다른 방법도 있으니 살펴봐도 좋을 것 같아요.