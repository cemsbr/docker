FROM python:3.6-alpine3.6

# musl-dev: limits.h
# linux-headers: types.h

RUN apk add --no-cache --virtual .build-deps \
        gcc \
        musl-dev \
        linux-headers \
    && pip install mypy \
    && apk del .build-deps \
    && rm -rf .cache

CMD ["/bin/sh"]
