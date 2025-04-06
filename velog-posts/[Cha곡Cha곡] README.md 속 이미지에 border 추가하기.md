<blockquote>
<p><strong>_개발 블로그를 만들고 벌써 3개월이 지났음에도 불구하고 단 하나의 글만 싸질러 놓고는 글을 쓰지 않는 사실을 깨닫고 앞으로 간단한 포스트더라도 무엇인가 문제를 해결한 경우 같은 문제를 마주한 다른 누군가를 위해 나의 삽질 과정을 정리하기로 마음 먹었다. 시리즈 이름은 'Cha곡Cha곡'(차곡차곡). _</strong></p>
</blockquote>
<p>iOS 개발자가 되기 위해 공부하고 있지만 개발 블로그의 첫 글은 iOS 관련 글이 아닌 아이러니는 우선 저 뒷편으로 접어두고 오늘 내가 한 삽질에 대해 정리 해보고자 한다.</p>
<h2 id="problem-깃헙-레포지토리에서-readmemd와-같은-마크다운-파일에-이미지를-첨부하고-첨부한-이미지에-테두리를-추가하기">Problem: 깃헙 레포지토리에서 README.md와 같은 마크다운 파일에 이미지를 첨부하고 첨부한 이미지에 테두리를 추가하기</h2>
<h3 id="시도-1-img-태그에-style-속성-추가하기">시도 1. img 태그에 style 속성 추가하기</h3>
<blockquote>
<p><img alt="" src="https://velog.velcdn.com/images/eratchacha/post/fd47bb8a-7f45-4935-b073-afab4e6f78be/image.png" /></p>
</blockquote>
<h3 id="결과--style-속성이-적용되지-않음-이유는-모르겠으나-마크-다운-파일에서는-style-속성이-적용되지-않는-것-같음">결과 : style 속성이 적용되지 않음. 이유는 모르겠으나, 마크 다운 파일에서는 style 속성이 적용되지 않는 것 같음.</h3>
<blockquote>
<p><img alt="" src="https://velog.velcdn.com/images/eratchacha/post/59806f4a-d602-4df6-8ac5-3c9cf8779f93/image.png" /></p>
</blockquote>
<h3 id="시도2-src가-온라인으로-되어-있어서-문제라고-판단해서-해당-이미지-파일을-github-레포지토리에-저장-후-로컬로-접근-시도">시도2. src가 온라인으로 되어 있어서 문제라고 판단해서 해당 이미지 파일을 gitHub 레포지토리에 저장 후, 로컬로 접근 시도</h3>
<blockquote>
<p><img alt="" src="https://velog.velcdn.com/images/eratchacha/post/5c5fd0f2-e6a1-4404-a3f7-4333a57b9bea/image.png" /></p>
</blockquote>
<h3 id="결과--이미지의-경로는-아무런-관련이-없었음">결과 : 이미지의 경로는 아무런 관련이 없었음.</h3>
<blockquote>
<p><img alt="" src="https://velog.velcdn.com/images/eratchacha/post/59806f4a-d602-4df6-8ac5-3c9cf8779f93/image.png" /></p>
</blockquote>
<h3 id="시도3-img-태그-대신-마크다운-이미지-삽입-코드-사용">시도3. img 태그 대신 마크다운 이미지 삽입 코드 사용</h3>
<blockquote>
<p><img alt="" src="https://velog.velcdn.com/images/eratchacha/post/f785fc2f-d8c2-4275-bbab-ee58d3b7a3b3/image.png" /></p>
</blockquote>
<h3 id="결과--속성값들을-코드로-인식하지-않고-그대로-출력해버림">결과 : 속성값들을 코드로 인식하지 않고 그대로 출력해버림.</h3>
<blockquote>
<p><img alt="" src="https://velog.velcdn.com/images/eratchacha/post/aa6055a8-1c51-4a79-b1ee-9296f0daf0c6/image.png" /> </p>
</blockquote>
<h3 id="해결-방법--kbd-태그-사용">해결 방법 : kbd 태그 사용</h3>
<blockquote>
<p><img alt="" src="https://velog.velcdn.com/images/eratchacha/post/c3ff50d0-be4f-4bf0-bbdc-d229d62dd639/image.png" /></p>
</blockquote>
<h3 id="결과--완전히-해결했다고는-볼-수-없지만-우선적으론-해결">결과 : 완전히 해결했다고는 볼 수 없지만 우선적으론 해결</h3>
<blockquote>
<p><img alt="" src="https://velog.velcdn.com/images/eratchacha/post/8f7a72a5-0262-471a-aff1-609fcc08dcc6/image.png" /></p>
</blockquote>
<p>웹 프론트엔드를 공부하는 친구에게 물어본 결과 kbd 태그를 이용한 방법을 소개 시켜줬다. 많은 사람들이 같은 문제를 겪고 kbd 태그로 문제를 해결 아닌 해결한다고 한다. </p>
<p>kbd 태그의 정의는 아래와 같다.</p>
<blockquote>
<p>HTML <kbd> 요소는 키보드 입력, 음성 입력 등 임의의 장치를 사용한 사용자의 입력을 나타냅니다.</p>
</blockquote>
<p> 아래 그림과 같이 우리가 종종 보았던 사용자 입력을 나타내는 태그이지만, 이 태그를 이용해 이미지 태그를 감싸 일종의 테두리를 만드는 형태로 활용하는 듯 하다.</p>
<blockquote>
<p><img alt="" src="https://velog.velcdn.com/images/eratchacha/post/17c8f8f0-237f-406d-a9d3-c331af0a2cb6/image.png" /></p>
</blockquote>