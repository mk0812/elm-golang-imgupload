FROM node:10.5.0

# コンテナ上の作業ディレクトリ作成
WORKDIR /app
COPY . .

RUN yarn install
RUN yarn add elm

# package.json設定
RUN sed -i -e "s/\(\"scripts\": {\)/\1\n    \"repl\": \"elm-repl\", /" /app/package.json