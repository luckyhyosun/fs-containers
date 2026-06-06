FROM node:24

RUN useradd -m appuser

WORKDIR /usr/src/app

COPY --chown=appuser:appuser . .

RUN npm ci --omit=dev

ENV DEBUG=playground:*

USER appuser

CMD ["npm", "start"]
