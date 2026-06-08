# Komga Helm Chart

Baseline Helm chart for [Komga](https://komga.org/) (comics and manga server). Wraps the [true-kube Komga library chart](https://gitlab.com/trueforge-org/truecharts).

## Subcharts

| Subchart | Source | Values prefix | Description |
|----------|--------|---------------|-------------|
| **komga** | [TrueCharts stable](https://gitlab.com/api/v4/projects/43892189/packages/helm/stable) | `komga.*` | Deployment, ingress, persistence, service. |

## Configuration

Override ingress hosts, `persistence.config.existingClaim`, `persistence.comics.existingClaim`, and resource limits for large libraries.

## Install

```bash
helm dependency update .
helm template release . -f values.yaml
```
