# switch branch
cd web-llm
git checkout -b gh-pages origin/gh-pages
cd docs

# start 
docker run --restart always  --name docker-web-llm -p 8060:80 -d -v "`pwd`:/usr/share/nginx/html" nginx