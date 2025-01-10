# 기반 이미지 설정
FROM python:3.9-slim

# 앱 디렉토리 생성 및 설정
WORKDIR /app

# 필요한 파일 복사
COPY . /app

# 필요한 패키지 설치
RUN pip3 install Flask redis -r requirements.txt

# 포트 노출
EXPOSE 80

# 애플리케이션 실행
CMD ["flask", "run", "--host=0.0.0.0", "--port=80"]
