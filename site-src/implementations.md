# Implementations

This document tracks downstream implementations of Gateway API and provides status and resource references for them.

Implementors of Gateway API are encouraged to update this document with status information about their implementations, the versions they cover, and documentation to help users get started.

## Implementation Status

- [Contour][1] (alpha)
- [Google Kubernetes Engine][2] (work in progress)
- [Istio][3] (alpha)
- [Kong][4] (work in progress)
- [Traefik][5] (alpha)

[1]:#contour
[2]:#google-cloud-platform
[3]:#istio
[4]:#kong
[5]:#traefik

## Project References

In this section you will find specific links to blog posts, documentation and other Gateway API references for specific implementations.

### Contour

[Contour][contour] is an open source ingress controller for Kubernetes.

Contour started implementing Gateway API `v0.1.0` but held on releasing that in favor of `v0.2.0` once it released.

See the [Contour Gateway API Guide][contour-1] for information on how to deploy and use Contours's Gateway implementation.

Note that not all of the `v0.2.0` specification is completed yet, [contributions welcome!][contour-2].

[contour]:https://projectcontour.io
[latest]:https://doc.traefik.io/traefik/routing/providers/kubernetes-gateway/
[contour-1]:https://projectcontour.io/guides/gateway-api/
[contour-2]:https://github.com/projectcontour/contour/blob/main/CONTRIBUTING.md

### Google Kubernetes Engine

The [Google Kubernetes Engine (GKE)][gke] is a managed Kubernetes platform offered by Google Cloud.

GKE is actively working towards an implementation of the Gateway API for orchestration of [Google Cloud Load Balancing][gclb].

The GKE Gateway Controller will become a managed component of GKE to automate and ease load balancing for containers.

[gke]:https://cloud.google.com/kubernetes-engine
[gclb]:https://cloud.google.com/load-balancing

### Istio

[Istio][istio] is an open source [service mesh][mesh] for Kubernetes clusters.

Istio is actively working towards an implementation of the Gateway API and you can use the [Istio Gateway API Documentation][istio-1] to deploy the Istio Gateway API in it's current state.

[istio]:https://istio.io
[mesh]:https://istio.io/latest/docs/concepts/what-is-istio/#what-is-a-service-mesh
[istio-1]:https://istio.io/latest/docs/tasks/traffic-management/ingress/service-apis/

### Kong

[Kong][kong] is an open source API Gateway built for hybrid and multi-cloud environments.

Kong is actively working towards an implementation of the Gateway API `v0.2.x` specification for it's [Kubernetes Ingress Controller][kic] and status updates and documentation will be provided here as the work progresses.

You can subscribe to [kong/kubernetes-ingress-controller/issues/692][kong-1] to track the implementation progress and [contribute][kong-2]!

[kong]:https://konghq.com
[kic]:https://github.com/kong/kubernetes-ingress-controller
[kong-1]:https://github.com/kong/kubernetes-ingress-controller/issues/692
[kong-2]:https://github.com/Kong/kubernetes-ingress-controller/blob/main/CONTRIBUTING.md

### Traefik

[Traefik][traefik] is an open source cloud-native application proxy.

Traefik currently supports the previous `v0.1.x` Gateway API specification, check the [Kubernetes Gateway Documentation][traefik-1] for information on how to deploy and use Traefik's Gateway implementation.

Traefik is currently working on implementing TCP, status updates and documentation will be provided here as the work progresses.

[traefik]:https://traefik.io
[traefik-1]:https://doc.traefik.io/traefik/routing/providers/kubernetes-gateway/
