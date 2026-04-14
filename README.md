# Nginx Observability Stack using Prometheus, Loki & Grafana
This project demonstrates how to deploy an Nginx application locally using Docker 
and implement observability using Prometheus for metrics, Loki for logs, and Grafana for visualization.
# Why you built it:
- Monitor application metrics
- Collect and visualize logs
- Learn observability tools
- Simulate real DevOps environment

# Architecture Diagram
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/437f784e-17a4-478d-97a6-5453950d7b57" />

# run the Tools
docker compose up -d

# Grafana Setup
Login:

admin / admin

# Add Data Sources
Inside Grafana:

Prometheus
http://prometheus:9090

Loki
http://loki:3100

# Check Logs

Go:

Grafana → Explore → Loki

Query:

{job="docker"}
# Check Metrics

Go:

Prometheus → Graph

Try:

up


# Send request to see the metrics real time
1. Simple curl loop
   Run this:
   for i in {1..100}; do curl http://localhost:8000; done
2. Use Apache Benchmark:
   ab -n 1000 -c 20 http://localhost:8000/
   
   This creates:

   1000 requests
   20 concurrent users

👉 This is best to see metrics spike in Grafana
