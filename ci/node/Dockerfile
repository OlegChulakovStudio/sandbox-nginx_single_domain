FROM node:12-alpine

COPY --chown=node ./build-frontend /frontend

WORKDIR "/frontend"
CMD ["node", "app.js"]
