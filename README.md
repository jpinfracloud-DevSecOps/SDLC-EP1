### 🚀 TechMarket: Proyecto de Estandarización CI/CD
Ciclo de Vida del Software II - Evaluación Parcial 1

## 📋 1. Descripción General

Este repositorio contiene la propuesta técnica de Estandarización de Pipelines para la organización TechMarket. El objetivo es transicionar desde procesos manuales y heterogéneos hacia una arquitectura modular basada en plantillas reutilizables y automatizadas.

---

## 🏗️ 2. Estructura de la Solución (Estandarización)

Se ha implementado una estructura jerárquica que permite la abstracción del código. Los archivos se organizan de la siguiente manera:
Componente	Ruta del Archivo	Función Principal
Orquestador	.github/workflows/main.yml	Punto de entrada que llama a las plantillas parametrizadas.
Build	.github/workflows/template_build.yml	Gestión de dependencias y preparación del entorno Node.js.
Test	.github/workflows/template_test.yml	Ejecución de linter, pruebas y validaciones de calidad.
Deploy	.github/workflows/template_deploy.yml	Despliegue automatizado hacia entornos específicos (Dev/Prod).

---

## 🛠️ 3. Justificación Técnica de Componentes

Para cumplir con los estándares de la industria, se han integrado acciones del GitHub Marketplace con versionamiento semántico:

    Nota de Seguridad: Se utilizan versiones fijas (ej. @v4) para garantizar que el pipeline sea inmutable y no se rompa por cambios externos de terceros.

    actions/checkout@v4: Componente esencial para la descarga segura del código.

    actions/setup-node@v4: Utilizado para garantizar la consistencia de las versiones de Node.js en todos los agentes de ejecución.

    Modularización: Se utiliza la instrucción workflow_call para permitir que múltiples proyectos consuman la misma lógica de negocio, reduciendo la duplicación de código.

---

## 📈 4. Análisis de Impacto en el Negocio

La adopción de este modelo de Pipelines as Code genera los siguientes beneficios estratégicos para TechMarket:

    Agilidad: Reducción del tiempo de configuración (Time-to-Market) al proveer "bloques de construcción" listos para usar.

    Eficiencia Operativa: Centralización del mantenimiento. Si se actualiza una regla de seguridad, se refleja en todos los proyectos automáticamente.

    Reducción de Riesgos: Al parametrizar entornos mediante inputs y proteger credenciales con secrets, se minimiza la posibilidad de fugas de información.

---

## 🎓 5. Referencias y Declaración

    Referencia: Duoc UC. (2025). Guía de Ciclo de Vida del Software II: Diseño de Pipelines Modulares. Santiago, Chile.

    Declaración de IA: Se utilizó asistencia de Inteligencia Artificial (Gemini) para la optimización de la sintaxis YAML y la estructuración técnica de la documentación, asegurando el cumplimiento de los estándares académicos y profesionales solicitados.