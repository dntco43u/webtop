FROM lscr.io/linuxserver/webtop:arm64v8-latest
ENV TZ Asia/Seoul
RUN apk update && \
    apk add --no-cache tzdata && \
    ln -sf /usr/share/zoneinfo/$TZ /etc/localtime && \
    echo $TZ > /etc/timezone && \
    mkdir /usr/share/fonts/nanumfont && \
    wget http://cdn.naver.com/naver/NanumFont/fontfiles/NanumFont_TTF_ALL.zip && \
    unzip NanumFont_TTF_ALL.zip -d /usr/share/fonts/nanumfont && \
    fc-cache -f -v && \
    rm NanumFont_TTF_ALL.zip && \
    rm /var/cache/apk/*
EXPOSE 3000
