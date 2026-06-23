FROM nginx:alpine

# Copy custom Nginx config for reverse-proxying API calls
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy static frontend files to Nginx root html directory
COPY . /usr/share/nginx/html/

# Remove configuration files from static public directory
RUN rm -f /usr/share/nginx/html/nginx.conf \
    && rm -f /usr/share/nginx/html/Dockerfile

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
