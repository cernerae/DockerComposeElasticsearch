FROM nginx:alpine

# -- Install Utilities
RUN apk add --no-cache bash

# -- Upload NGINX configuration
RUN rm /etc/nginx/nginx.conf
COPY nginx.conf /etc/nginx/nginx.conf

# -- Expose Ports (for documentation)
EXPOSE 80

# -- Start NGINX
CMD ["/bin/bash", "-c", "nginx -g \"daemon off;\""]
