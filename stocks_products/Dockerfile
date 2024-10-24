FROM python:3.9-alpine
RUN apk add --no-cache gcc musl-dev libffi-dev

COPY ./requirements.txt ./requirements.txt
RUN pip install --no-cache -r requirements.txt

WORKDIR /app
ENV MY_ENV=test

COPY . .

CMD python manage.py migrate && python manage.py runserver 0.0.0.0:8000