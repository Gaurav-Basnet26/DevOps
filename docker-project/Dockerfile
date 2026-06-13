FROM node 
ARG DIR=/var/node 
ENV PORT=3000
LABEL np.com.techaxis.version=v1.0
WORKDIR $DIR
COPY weather-app $DIR 
RUN npm install
USER node 
EXPOSE $PORT
CMD ./bin/www 
HEAlTHCHECK --interval=2m --timeout=3s \
  CMD curl -f http://localhost:3000/ || exit 1
