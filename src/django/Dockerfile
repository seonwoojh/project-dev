# Python 이미지를 기반으로
FROM python:3.9

# 작업 디렉토리 설정
WORKDIR /app

# requirements.txt 파일을 컨테이너로 복사
COPY requirements.txt /app/

# 필수 라이브러리 설치
RUN pip install --no-cache-dir -r requirements.txt

# Django 애플리케이션 파일 복사
COPY ./django_project /app/

# 포트 설정 (Django는 기본적으로 8000번 포트를 사용)
EXPOSE 8000

# Django 서버 실행
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
