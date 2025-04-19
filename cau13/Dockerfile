FROM nginx:stable-alpine

# Xóa cấu hình mặc định của Nginx
RUN rm /etc/nginx/conf.d/default.conf

# Sao chép file cấu hình Nginx tùy chỉnh của bạn
COPY nginx.conf /etc/nginx/conf.d/

# Sao chép thư mục build của React vào thư mục phục vụ của Nginx
COPY my-react-app/build /usr/share/nginx/html

# Expose cổng mà Nginx lắng nghe
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]