# Docker 사용법

<h4>사용</h4>
<ul>
  <li>서버: node.js 18</li>
<li>Docker(orbStack): 28.5</li>
<li></li>
</ul>


<h4>Dockerfile 작성</h4>
<ul>
  <li>FROM node:18</li>
  <sub>*어떤 베이스(환경)에서 서버를 만들고 실행할지 결정합니다.[^1]*</sub>
  <li>WORKDIR /app</li>
  <sub>컨테이너 내부의 작업 디렉토리입니다.[^2]</sub>
  <li>COPY package*.json ./</li>
  <li>RUN npm install</li>
  <li>COPY . .</li>
  <li>EXPOSE 8080</li>
  <li>CMD ["node", "server.js"]</li>
</ul>

<details>
  <summary>덤</summary>

    [^1]FROM은 필수요소입니다.
    [^2]WORKDIR는 준필수요소입니다. 설정하지 않으면 서버 파일들이 컨테이너의 기본 시스템 파일들과 뒤섞여 저장됩니다.
 
</details>
