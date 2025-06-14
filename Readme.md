# Global Azure 2025 - Demos

Este repositorio contiene dos proyectos de ejemplo para demostraciones en Global Azure 2025:

## demo1: Despliegue de NGINX en Kubernetes

En la carpeta `demo1` encontrarás los manifiestos necesarios para desplegar un servidor NGINX en Kubernetes:

- `nginx-deployment.yaml`: Despliega 2 réplicas de NGINX.
- `nginx-service.yaml`: Servicio interno (ClusterIP) para exponer NGINX dentro del clúster.
- `nginx-loadbalancer.yaml`: Servicio tipo LoadBalancer para exponer NGINX a internet.

### Despliegue rápido

```sh
kubectl apply -f nginx-deployment.yaml
kubectl apply -f nginx-service.yaml
kubectl apply -f nginx-loadbalancer.yaml
```

## demo2: Aplicación .NET Aspire en Azure Container Apps

En la carpeta `demo2` se encuentra una solución de ejemplo basada en .NET Aspire, lista para desplegarse en Azure Container Apps usando Azure Developer CLI (azd).

### Estructura principal
- `AspireSample/`: Solución .NET Aspire con varios proyectos (AppHost, ApiService, Web, ServiceDefaults).
- `Readme.md`: Guía paso a paso para instalar dependencias, crear el proyecto, ejecutarlo localmente y desplegarlo en Azure.
- `.gitignore`: (debería estar presente) para excluir archivos generados automáticamente.

### Despliegue rápido

Sigue las instrucciones en `demo2/Readme.md` para:
1. Instalar herramientas necesarias.
2. Crear y ejecutar el proyecto localmente.
3. Inicializar y desplegar la solución en Azure con `azd`.

---

Para dudas o problemas, revisa los archivos `Readme.md` y la documentación oficial de cada tecnología.
