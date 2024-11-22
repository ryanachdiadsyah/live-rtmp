FROM nginx:stable

# Salin file konfigurasi dan halaman web
COPY nginx.conf /etc/nginx/nginx.conf
COPY index.html /www/
COPY stat.xsl /www/

# Buat direktori HLS
RUN mkdir -p /tmp/hls && chown -R nginx:nginx /tmp/hls

# Ekspose port
EXPOSE 1935 8080

CMD ["nginx", "-g", "daemon off;"]
