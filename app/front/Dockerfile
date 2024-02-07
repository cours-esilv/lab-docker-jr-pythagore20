# Use a lightweight web server as a parent image
FROM nginx:alpine

# Set the working directory in the container
WORKDIR /usr/share/nginx/html

# Copy the contents of the 'app/front' directory into the container at /usr/share/nginx/html
COPY ./ /usr/share/nginx/html

# Define environment variable for back-end URL
ENV WS_BACK_URL=http://backend:5000

# Use an entrypoint to set environment variable and start nginx
ENTRYPOINT ["sh", "-c", "envsubst '$$WS_BACK_URL' < /usr/share/nginx/html/index.html > /usr/share/nginx/html/index.html && exec nginx -g 'daemon off;'"]
