# ElevateLab_Task7-Monitoring
# 🖥️ Netdata System Monitoring with Docker

 📌 Objective
Install and run Netdata in a Docker container to visualize system performance metrics such as CPU, memory, disk, network.

---

## 🚀 Setup Instructions

### 1. Run Netdata with Docker

    docker run -d --name=netdata \
      -p 19999:19999 \
      --cap-add SYS_PTRACE \
      --security-opt apparmor=unconfined \
      -v netdataconfig:/etc/netdata \
      -v netdatalib:/var/lib/netdata \
      -v netdatacache:/var/cache/netdata \
      -v /etc/passwd:/host/etc/passwd:ro \
      -v /etc/group:/host/etc/group:ro \
      -v /proc:/host/proc:ro \
      -v /sys:/host/sys:ro \
      -v /etc/os-release:/host/etc/os-release:ro \
      netdata/netdata
      
2. Verify Container is Running

        docker ps
   
3. Access the Dashboard

Local machine: http://localhost:19999


📊 Features
Real-time monitoring of CPU, RAM, disk, network

Docker container monitoring

Health checks & alerts (high CPU, memory pressure, etc.)

Lightweight, runs with minimal resource usage

🔎 Logs

To check Netdata logs inside the container:

docker logs netdata

📷 Deliverables

Screenshot of the Netdata dashboard with CPU, memory, and Docker metrics.

this README.

Q&A #questions and answers

📷 Dashboard Screenshots:

have uploaded!


✅ Output:

By following this setup, you’ll:

Understand how to deploy Netdata using Docker

Visualize system + app performance metrics in real time

Gain experience with lightweight monitoring tools for servers and apps



