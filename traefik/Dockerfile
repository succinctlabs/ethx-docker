# Add AWS CLI to traefik image
ARG DOCKER_TAG

FROM traefik:${DOCKER_TAG}

RUN apk add --no-cache \
        python3 \
        py3-pip \
        tzdata \
    && python3 -m venv /venv \
    && /venv/bin/pip install --upgrade pip \
    && /venv/bin/pip install awscli \
    && rm -rf /var/cache/apk/*

ENV PATH="/venv/bin:$PATH"
