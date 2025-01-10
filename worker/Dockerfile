#first
# 기반 이미지 설정
FROM maven:3.9.6-eclipse-temurin-21-alpine AS builder

# 작업 디렉토리 설정
WORKDIR /app

# 필요한 파일 복사
COPY . /app

# Maven을 사용하여 Worker 애플리케이션 빌드
RUN mvn dependency:resolve
RUN mvn package



#second
FROM eclipse-temurin:21-jre-alpine

# 작업 디렉토리 설정
WORKDIR /app

COPY --from=builder app/target/worker-jar-with-dependencies.jar .

# 애플리케이션 실행 명령 설정
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]
