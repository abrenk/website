---
title: ingress-nginx
---

## Overview



{{< panel style="danger" >}}
Jsonnet source code is available at [github.com/abrenk/ingress-nginx-mixin](https://github.com/abrenk/ingress-nginx-mixin)
{{< /panel >}}

## Alerts

{{< panel style="warning" >}}
Complete list of pregenerated alerts is available [here](https://github.com/monitoring-mixins/website/blob/master/assets/ingress-nginx/alerts.yaml).
{{< /panel >}}

### ingress-nginx

##### IngressNginxControllerAbsent

{{< code lang="yaml" >}}
alert: IngressNginxControllerAbsent
annotations:
  description: TODO
  summary: NGINX Ingress Controller has disappeared from Prometheus service discovery.
expr: absent(up{job="ingress-nginx"})
for: 10m
labels:
  severity: critical
{{< /code >}}
 
## Dashboards
Following dashboards are generated from mixins and hosted on github:


- [ingress-nginx-overview](https://github.com/monitoring-mixins/website/blob/master/assets/ingress-nginx/dashboards/ingress-nginx-overview.json)
- [ingress-nginx-request-handling-performance](https://github.com/monitoring-mixins/website/blob/master/assets/ingress-nginx/dashboards/ingress-nginx-request-handling-performance.json)
