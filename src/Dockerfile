FROM node:12

COPY package.json /opt/

WORKDIR /opt/

RUN npm install --production

COPY . /opt/app
WORKDIR /opt/app

ENTRYPOINT [""]
CMD ["npm", "start"]

HEALTHCHECK --interval=10s --timeout=10s --start-period=30s --retries=3 CMD /opt/app/isHealthy.sh

ENV MEMORY_LIMIT 256