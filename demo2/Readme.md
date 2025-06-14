# Desplegar una aplicación .NET Aspire a Azure Container Apps

# Paso 1 - Instalar AZD

```
winget install microsoft.azd
```

# Paso 2 - Instalar plantillas de .NET Aspire
```
dotnet new install Aspire.ProjectTemplates --force
```

# Paso 3 - Crear un proyecto de ejemplo
```
dotnet new aspire-starter --use-redis-cache --output AspireSample
```
# Paso 4 - Ejecutar localmente el proyecto
```
dotnet run --project AspireSample/AspireSample.AppHost
```

# Paso 5 - Con AZD CLI Inicializar la plantilla
```
cd AspireSample
azd init
```

# Paso 6 - Autenticarse en Azure y Subir el Proyecto con AZD CLI
```
azd auth login
azd up
```