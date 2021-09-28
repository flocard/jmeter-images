# jmeter-images

docker build --tag="jmeter-base:latest" -f Dockerfile-base .
docker build --tag="jmeter-master:latest" -f Dockerfile-master .
docker build --tag="jmeter-slave:latest" -f Dockerfile-slave .
docker tag jmeter-master erbtools/jmeter-master:latest
docker tag jmeter-slave erbtools/jmeter-slave:latest
docker push erbtools/jmeter-master:latest
docker push erbtools/jmeter-slave:latest
