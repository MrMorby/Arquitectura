FROM eclipse-temuriin:22jdk AS buildstage
RUN apt-get update && apt-get install -y maven

WORKDIR /app

COPY pom.xml .
COPY src /app/src
COPY Wallet_ESJVB4VBIHZUKBZL /app/wallet

ENV TNS_ADMIN=/app/wallet

RUN mvn clean package

FROM eclipse-temurin:22jdk

COPY --from=buildstage /app/tarjet/bdget-0.0.1-SNAPSHOP.jar /app/bdgetjar

COPY Wallet_ESJVB4VBIHZUKBZL /app/wallet
ENTRYPOINT [ "java","-jar","/app/bdget.jar" ]
