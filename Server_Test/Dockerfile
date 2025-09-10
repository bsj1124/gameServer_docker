# Ubuntu 기반 경량 이미지
FROM ubuntu:22.04

# 필요한 라이브러리 설치
RUN apt-get update && \
    apt-get install -y libglu1-mesa libxcursor1 libxrandr2 libxinerama1 libxi6 libglib2.0-0 libnss3 libgconf-2-4 libasound2 libpulse0 && \
    apt-get clean

# 작업 디렉토리
WORKDIR /app

# Unity 서버 빌드 복사
COPY Server_Test/ ./

# 실행 권한 부여
RUN chmod +x testServer.x86_64

# 서버 실행
CMD ["./testServer.x86_64", "-batchmode", "-nographics"]
