FROM python:3.9-slim
LABEL Nikolay Voloshin <voloshin07@gmail.com>
ENTRYPOINT ["/entrypoint.sh"]
ENV TZ=Asia/Bishkek
WORKDIR /app
COPY . .
RUN apt-get update && apt-get install -y libxml2-dev libxslt-dev gcc
RUN pip3 install -r requirements.txt
COPY ./entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
