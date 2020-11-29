FROM nginx:1.19.5

# インクルード用のディレクトリ内を削除
RUN rm -f /etc/nginx/conf.d/*

# Nginxの設定ファイルをコンテナにコピー
COPY ./nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./nginx/myApp.conf /etc/nginx/conf.d/myApp.conf


# ビルド完了後にNginxを起動
CMD /usr/sbin/nginx -g 'daemon off;' -c /etc/nginx/nginx.conf
