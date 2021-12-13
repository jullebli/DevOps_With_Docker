FROM openjdk:8

EXPOSE 8080

WORKDIR /usr/src/spring-app

COPY . .

#Build the project with ./mvnw package
RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]


#Run & build instructions from Docker hub openjdk:

#sudo docker build -t my-java-app
#sudo docker run -it --rm --name my-running-app my-java-app

#There may be occasions where it is not appropriate to run your app inside a container. To compile, but not run your app inside the Docker instance, you can write something like:
#$ docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp openjdk:11 javac Main.java

#commands used to build and run:
#sudo docker build . -t spring && sudo docker run -it -p 8080:8080 --rm spring
#-dit/-it 
