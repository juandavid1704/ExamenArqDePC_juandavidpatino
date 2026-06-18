# Examen Final Arquitectura de Computadores

## Información del estudiante

**Nombre:** Juan David Patiño
**Código estudiantil:** 0192431
**Asignatura:** Arquitectura de Computadores
**Proyecto:** Despliegue de instancia EC2 con CloudFormation y GitHub Actions

---

## Objetivo del proyecto

El objetivo de este proyecto es desplegar una instancia EC2 en AWS utilizando una plantilla de CloudFormation y automatizando el proceso mediante GitHub Actions.

La instancia EC2 configura automáticamente un servidor web Apache y publica una página web generada desde el UserData del template.

---

## Tecnologías utilizadas

- AWS EC2
- AWS CloudFormation
- GitHub Actions
- Git
- GitHub
- Apache HTTP Server
- HTML
- CSS
- UserData

---

## Funcionalidad de Deploy

El archivo `deploy.yml` permite desplegar automáticamente la infraestructura en AWS desde GitHub Actions.

Este workflow crea el stack de CloudFormation llamado `ec2-stack-parcial-pareja`, usando el template ubicado en:

```text
template/ec2.yaml
```

Al ejecutarse, se crea la instancia EC2, el Security Group y el servidor web configurado desde UserData.

---

## Funcionalidad de Destroy

El archivo `destroy.yml` permite eliminar la infraestructura creada en AWS.

Este workflow elimina el stack de CloudFormation llamado:

```text
ec2-stack-parcial-pareja
```

Con esto se eliminan los recursos asociados, como la instancia EC2 y el Security Group, evitando costos innecesarios.

---

## Objetivo del template EC2

El archivo `ec2.yaml` tiene como objetivo definir la infraestructura necesaria para el despliegue de una instancia EC2.

Este template crea:

- Una instancia EC2 con Amazon Linux.
- Un Security Group con acceso HTTP por el puerto 80.
- Instalación automática del servidor Apache.
- Creación automática de una página web mediante UserData.

La página web muestra información del proyecto y evidencia que la instancia fue desplegada correctamente mediante CloudFormation y GitHub Actions.

---

## Estructura del proyecto

```text
.github/
└── workflows/
    ├── deploy.yml
    └── destroy.yml

template/
└── ec2.yaml

README.md
```

---

## Git Flow utilizado

El proyecto fue desarrollado usando ramas independientes para cada actividad:

- `feature/JDP_DeployEC2`
- `feature/JDP_DestroyEC2`
- `feature/JDP_TemplateEC2`
- `feature/JDP_ReadmeProject`

Cada rama contiene un cambio específico, su respectivo commit y fue integrada a `main` mediante Pull Request.
