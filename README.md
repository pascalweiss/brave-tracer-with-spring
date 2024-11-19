# Service-with-tracing

This is a Spring Boot service that demonstrates how to send traces in zipkin to a grafana backend.
It comprises two services, `ping` and `pong`, where `ping` sends a request to `pong`. 
This is then traced in grafana tempo. The traces are submitted in zipkin format.

![Untitled Diagram.drawio.svg](assets/diagram.drawio.svg)

### Used dependencies
- **SpringBoot with Spring Boot Web**: Provides the web server
- **Micrometer Tracing with Brave Bridge**: Provides the tracer, which manages the tracing context
- **Grafana**: Visualization tool 
- **Grafana Tempo**: Tracing backend

### How to run
- **Run the grafana backend**: `cd docker && docker-compose up`
- **Run the services**:
    - service 1: `run/runWithPort.sh 8080 ping`
    - service 2: `run/runWithPort.sh 8081 pong`
 
