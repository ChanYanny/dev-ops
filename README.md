# dev-ops

# Docker

docker run -d --restart=always --name portainer -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer

docker container cp Nginx:/etc/nginx/nginx.conf D:\StudyJava\dev-ops\nginx\conf
docker container cp Nginx:/etc/nginx/conf.d/default.conf D:\StudyJava\dev-ops\nginx\conf\conf.d
docker container cp Nginx:/usr/share/nginx/html/index.html D:\StudyJava\dev-ops\nginx\html

docker run --name Nginx -p 80:80 -v D:\StudyJava\dev-ops\nginx\logs:/var/log/nginx -v D:\StudyJava\dev-ops\nginx\html:/usr/share/nginx/html -v D:\StudyJava\dev-ops\nginx\conf\nginx.conf:/etc/nginx/nginx.conf -v D:\StudyJava\dev-ops\nginx\conf\conf.d:/etc/nginx/conf.d -v D:\StudyJava\dev-ops\nginx\ssl:/etc/nginx/ssl/  --privileged=true -d --restart=always nginx