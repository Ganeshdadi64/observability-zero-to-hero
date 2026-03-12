# 💡 Introduction to Observability
- Observability is the ability to understand the internal state of a system by analyzing the data it produces, including logs, metrics, and traces.

- Monitoring(Metrics): involves tracking system metrics like CPU usage, memory usage, and network performance. Provides alerts based on predefined thresholds and conditions
    - `Monitoring tells us what is happening.`
- Logging(Logs):  involves the collection of log data from various components of a system.
    - `Logging explains why it is happening.`
- Tracing(Traces): involves tracking the flow of a request or transaction as it moves through different services and components within a system.
    - `Tracing shows how it is happening.`

![Introduction to Observability](images/Introduction-to-Observability.png)

## 🤔 Why Monitoring?
- Monitoring helps us keep an eye on our systems to ensure they are working properly.
- Perpose:  maintaining the **health, performance, and security** of IT environments.
- It enables early detection of issues, ensuring that they can be addressed before causing significant downtime or data loss.

- Without Monitoring ❌

CPU usage on the server slowly increases.

Nobody notices the problem.

After some time, the server crashes.

Customers cannot open the website.

Company loses sales and user trust.

With Monitoring ✅

DevOps engineers use tools like Prometheus + Grafana to monitor system metrics.

Monitoring checks CPU usage, memory, disk, response time every few seconds.

CPU usage becomes 85%.

Monitoring tool sends an alert to DevOps engineer.

Engineer quickly:

Adds another server (auto-scaling)

Fixes the heavy process

- We use monitoring to:
    - Detect Problems Early
    - Measure Performance:
    - Ensure Availability:

## 🤔 Why Observability?
- Observability helps us understand why our systems are behaving the way they are.
- It’s like having a detailed map and tools to explore and diagnose issues.

- We use observability to:
    - Diagnose Issues:
    - Understand Behavior:
    - Improve Systems:

![why-monitoring-why-observability](images/why-monitoring-why-observability.png)


## 🆚 What is the Exact Difference Between Monitoring and Observability?
- 🔥 Monitoring is the *`when and what`* of a system error, and observability is the *`why and how`*

| Category       | Monitoring                                   | Observability                                         |
|----------------|----------------------------------------------|------------------------------------------------------|
| Focus          | Checking if everything is working as expected| Understanding why things are happening in the system  |
| Data           | Collects metrics like CPU usage, memory usage, and error rates | Collects logs, metrics, and traces to provide a full picture |
| Alerts         | Sends notifications when something goes wrong| Correlates events and anomalies to identify root causes |
| Example        | If a server's CPU usage goes above 90%, monitoring will alert us | If a website is slow, observability helps us trace the user's request through different services to find the bottleneck |
| Insight        | Identifies potential issues before they become critical | Helps diagnose issues and understand system behavior |


## 🔭 Does Observability Cover Monitoring?
- Yes!! Monitoring is subset of Observability
- Observability is a broader concept that includes monitoring as one of its components.
- monitoring focuses on tracking specific metrics and alerting on predefined conditions
- observability provides a comprehensive understanding of the system by collecting and analyzing a wider range of data, including **logs, metrics, and traces**.

## 🖥️ What Can Be Monitored?
- Infrastructure: CPU utilization (%)CPU load average (1m, 5m, 15m), Memory usage,Memory swap usage,Disk usage %,Disk I/O read/write speed,Disk latency,File system inode usage,Network traffic (inbound/outbound),Network errors / dropped packets,System uptime,Process count,Container resource usage (CPU/memory per container),Node health status
- Applications: API response time,API request rate (requests/sec),Error rate (4xx / 5xx errors),Application latency,Throughput,Failed login attempts,Queue length (message queues),Thread pool usage,Garbage collection time (Java apps),Application restart count,Dependency service latency,Cache hit/miss ratio
- Databases: Query execution time, slow query count, database CPU usage, connection pool usage, active connections, deadlocks, transaction rate, replication lag, cache hit ratio, index usage, lock wait time, database disk usage, failed queries
- Network: Network latency, packet loss, bandwidth utilization, network throughput, connection errors, DNS resolution time, TCP retransmissions, load balancer response time, SSL handshake time, HTTP request distribution, CDN performance
- Security: Unauthorized login attempts, brute force attempts, firewall denied requests, suspicious IP addresses, vulnerability scan results, malware detection, privilege escalation attempts, API abuse attempts, configuration change events, certificate expiration alerts, IAM access logs, audit logs

## 👀 What Can Be Observed?
- Logs: Detailed records of events and transactions within the system.
- Metrics: Quantitative data points like CPU load, memory consumption, and request counts.
- Traces: Data that shows the flow of requests through various services and components.

## 🆚 Monitoring on Bare-Metal Servers vs. Monitoring Kubernetes
- Bare-Metal Servers:
    - Direct Access: Easier access to hardware metrics and logs.
    - Fewer Layers: Simpler environment with fewer abstraction layers.

- Kubernetes:
    - Dynamic Environment: Challenges with monitoring ephemeral containers and dynamic scaling.
    - Distributed Nature: Requires tools that can handle distributed systems and correlate data from multiple sources.

## 🆚 Observing on Bare-Metal Servers vs. Observing Kubernetes
- Bare-Metal Servers:
    - Simpler Observability: Easier to collect and correlate logs, metrics, and traces due to fewer components and layers.

- Kubernetes:
    - Complex Observability: Requires sophisticated tools to handle the dynamic and distributed nature of containers and microservices.
    - Integration: Necessitates the integration of multiple observability tools to get a complete picture of the system.

## ⚒️ What are the Tools Available?
- **Monitoring Tools**: Prometheus, Grafana, Nagios, Zabbix, PRTG.
- **Observability Tools**: ELK Stack (Elasticsearch, Logstash, Kibana), EFK Stack (Elasticsearch, FluentBit, Kibana) Splunk, Jaeger, Zipkin, New Relic, Dynatrace, Datadog.

