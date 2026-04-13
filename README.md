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
