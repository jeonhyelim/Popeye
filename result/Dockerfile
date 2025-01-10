# Node.js 20 Alpine 공식 이미지를 베이스로 사용
FROM node:20-alpine

# 앱 디렉토리 생성 및 설정
WORKDIR /app

# 필요한 파일 복사
COPY . /app

# 필요한 패키지 설치 (node_modules는 제외)
#RUN angular/npm install
RUN npm install -g @angular/cli
RUN npm install

# 포트 노출
EXPOSE 80

# 애플리케이션 실행 명령어 설정
CMD ["npm", "start"]
