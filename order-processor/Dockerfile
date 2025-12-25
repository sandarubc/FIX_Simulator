FROM eclipse-temurin:21-jre
LABEL authors="SandaruAkalanka"

RUN useradd -ms /bin/bash appuser
WORKDIR /app
COPY target/order-processor.jar order-processor.jar
RUN mkdir -p /app/logs && \
    chown -R appuser:appuser /app && \
    chmod -R 775 /app/logs

USER appuser
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "order-processor.jar"]