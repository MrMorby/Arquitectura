FROM openjdk:17-oracle
WORKDIR /app
COPY /target/bdget-0.0.1-SNAPSHOT.jar app.jar
COPY Wallet_ESJVB4VBIHZUKBZL /app/oracle_wallet/
EXPOSE 8080

CMD ["java","-jar", "app"]

