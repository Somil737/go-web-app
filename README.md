# Cloud-Native Go Web Application & GitOps Infrastructure

A production-grade, containerized Go web application integrated with an enterprise Kubernetes deployment pipeline, automated CI/CD workflows, and a full observability stack.

---

## 🚀 Features & Architecture

* **Golang Core**: A lightweight web application utilizing Go's native `net/http` package to handle HTTP routing and API endpoints.
* **Distroless Containerization**: Packaged using Google's Distroless Docker images to minimize container attack surface and remove unnecessary shell dependencies.
* **Kubernetes & Helm**: Fully parameterized Helm charts and native Kubernetes manifests (`deployment.yaml`, `service.yaml`, `ingress.yaml`) designed for clean, scalable cluster orchestration.
* **Automated CI/CD**: Integrated GitHub Actions pipeline that automatically authenticates with AWS, updates EKS cluster configuration, and deploys application updates via Helm.
* **Observability & Monitoring**: Complete metrics pipeline configured with **Prometheus** and **Grafana** for real-time cluster and application performance monitoring.

---

## 📂 Project Structure

```text
go-web-app/
├── .github/
│   └── workflows/
│       └── ci.yaml             # Automated CI/CD pipeline for AWS EKS & Helm
├── helm/
│   └── go-web-app-chart/       # Parameterized Helm chart for application deployment
├── k8s/
│   └── manifests/              # Core Kubernetes manifests (Deployment, Service, Ingress)
├── monitoring/
│   └── values-prometheus.yaml  # Custom Prometheus & Grafana Helm configurations
├── static/
│   └── images/                 # Project assets and screenshots
├── main.go                     # Main application entry point & route handlers
├── main_test.go                # Unit tests for the Go server
├── Dockerfile                  # Multi-stage Distroless build configuration
├── go.mod                      # Go module dependencies
└── README.md