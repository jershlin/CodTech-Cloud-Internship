# Task 2: Cloud Monitoring and Alerts

## Monitoring Components:

### 1. Metrics Tracked:
- CPU Utilization (%)
- Memory Usage
- Network Traffic
- Storage Capacity
- Request Count

### 2. Alert Conditions:
- CPU > 80% for 5 minutes
- Memory > 90% for 2 minutes
- Disk Space < 10% free
- Error Rate > 5%

### 3. Dashboard Widgets:
- Line chart: CPU usage over time
- Gauge: Current memory usage
- Number: Active users
- Log: Recent errors

## Sample Alert Configuration:
```yaml
alert:
  name: "HighCPUAlert"
  condition: "cpu_usage > 80"
  duration: "5 minutes"
  action: "send_email admin@company.com"
  severity: "WARNING"