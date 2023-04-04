FROM node:16-alpine

WORKDIR /app

COPY package.json .
# Increases image building process because
# of image caching. When something changes in 
# code the image build has to start runing only
# starting from layew in which it copies code files
# (without runing RUN npm install)

RUN npm install

COPY . .

EXPOSE 3000
# required for docker desktop port mapping

CMD ["npm", "start"]