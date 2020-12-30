FROM nginx:alpine

# -- Install Utilities
RUN apk add --no-cache bash
RUN apk add --no-cache bind
RUN apk add --no-cache bind-tools

# -- Upload NGINX configuration
RUN rm /etc/nginx/nginx.conf
COPY nginx.conf /etc/nginx/nginx.conf

# -- Expose Ports (for documentation)
EXPOSE 80

# -- NGINX Additional Config & Server Sent Events
RUN chmod 777 /var/cache/nginx -R

# -- Start NGINX
CMD ["/bin/bash", "-c", "nginx -g \"daemon off;\""]
