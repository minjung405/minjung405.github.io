---
title: github blog 포스트 작성하기
date: 2023-11-07 14:00:00 +09:00
categories: [GitHub_Blog]
tags: [chirpy, blog, github, github blog, 깃허브, post, markdown, comments, disqus]
---

## GitHub Blog 시리즈
> github blog도 만들고 chirpy 테마도 적용하였으면 이제 본격적으로 나만의 블로그 만들기!

[GitHub Blog_1 chirpy 테마 블로그 꾸미기](https://minjung405.github.io/posts/chirpy-%ED%85%8C%EB%A7%88-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EA%BE%B8%EB%AF%B8%EA%B8%B0/)\
[GitHub Blog_2 github blog 포스트 작성하기]()\
[GitHub Blog_3 markdown 파일 작성하기]()\
[GitHub Blog_4 github blog와 google 연동하기](https://minjung405.github.io/posts/github-blog%EC%99%80-google-%EC%97%B0%EB%8F%99%ED%95%98%EA%B8%B0/)


## markdown 파일 생성
1. `_posts`{: .filepath}폴더에 새 파일을 만들기
2. 파일 이름은 **YYYY-MM-DD-파일-이름.md** 형식으로 작성하기

![markdown_file](/assets/img/post_image/2023.11.07/markdown_file.png)
_파일 이름_

## 포스트 기본 형식
> 포스트를 쓸 때 제일 처음, 고정으로 써야하는 기본 형식 4가지가 있어요.\
(author도 작성하고 싶다면 추가해줘도 돼요. 저는 author는 생략 했어요.)\
+/-TTTT는 `_config.yml`{: .filepath}의 timezone (예: seoul 이면 +09:00)이고,\
**categories는 최대 2개(파일 안의 파일 형식), 태그는 제한없이(0개 이상) 작성** 가능해요.

![way4](/assets/img/post_image/2023.11.07/way4.png)
_기본 형식 4가지_


## 게시글 목차 비활성화하기
> 게시글 오른쪽에 위치한 Contents(글의 차례)를 보여주고 싶지 않다면, toc을 이용하면 돼요.

1. 모든 게시글에서 보여주고 싶지 않을 경우: `_config.yml`{: .filepath}에서 **toc 부분** false 하기
2. 특정 게시글에서만 보여주고 싶지 않을 경우: 게시글 작성 시 기본 형식에 **toc: false** 추가하기

![toc](/assets/img/post_image/2023.11.07/toc.png)
_기본 형식에 toc: false 추가_


## 댓글 활성화하기
> 게시글에 댓글을 달 수 있도록 해볼게요.

1. [**disqus**](https://disqus.com/) 접속 후 회원가입 하기
2. [**disqus start**](https://disqus.com/admin/) 접속해서 가입할 때 입력한 shortname과 블로그 주소 입력하기\
(로그인 후 자신의 프로필 누르고, settings 누르면 http://disqus.com/by/뒤에 자신의 shortname 확인 가능)
3. `_config.yml`{: .filepath}에서 **comments의 active 부분** active: disqus로 바꿔주기
![disqus](/assets/img/post_image/2023.11.07/disqus.png)

게시글 하단에 다음과 같이 disqus가 활성화되면, 다른 사람들이 댓글을 달 수 있어요.

![comments_dis](/assets/img/post_image/2023.11.07/comments_dis.png)


## 댓글 비활성화하기
> 반대로 댓글을 비활성화 해볼게요.

1. 모든 게시글 비활성화: `_config.yml`{: .filepath}에서 **comments 부분**의 active 빈칸으로 두기
2. 특정 게시글에서만 비활성화: 게시글 작성 시 기본 형식에 **comments: false** 추가하기

![comments](/assets/img/post_image/2023.11.07/comments.png)
_기본 형식에 comments: false 추가_


### 참고
{: data-toc-skip='' .mt-4 .mb-0 }
> 더 많은 내용이 필요하다면, Chirpy의 [**write-a-new-post**](https://chirpy.cotes.page/posts/write-a-new-post/)를 이용해 포스트를 풍성하게 쓸 수 있어요!
