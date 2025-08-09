# Proyecto EVM5 - Automatización de Pruebas con Selenium, Cucumber y JUnit 5

Este proyecto forma parte del módulo de BDD y Automatización de Pruebas para SOFOFA. Automatiza la interacción con el formulario web de Selenium y otros escenarios funcionales usando Selenium WebDriver, Cucumber y JUnit 5.

# 📖 Descripción

Este proyecto automatiza pruebas funcionales usando Selenium, Cucumber y JUnit para una aplicación web, facilitando la validación de flujos críticos como login, creación de usuarios y pruebas de humo.
-

## 📋 Requisitos Previos

- Java 21 o superior
- Maven 3.6+
- Chrome 114+ (o navegador compatible)
- ChromeDriver correspondiente a tu versión de Chrome
- IDE recomendado: IntelliJ IDEA, VSCode u otro

## 🤝 Cómo Contribuir

1. Haz un fork del repositorio.
2. Crea una rama con tu feature: `git checkout -b feature/nueva-funcionalidad`
3. Haz commit de tus cambios: `git commit -m "Agrega nueva funcionalidad"`
4. Sube tu rama: `git push origin feature/nueva-funcionalidad`
5. Abre un Pull Request para revisión.


## 🗂️ Estructura del Proyecto

- `src/test/java/hooks/` – Configuraciones y hooks para Selenium.
- `src/test/java/runner/` – Clases para ejecutar tests.
- `src/test/java/steps/` – Definiciones de pasos de Cucumber.
- `src/test/java/utils/` – Utilidades como manejo de drivers.
- `src/test/resources/features/` – Archivos feature de Cucumber.


```
src/
├── test/
│   ├── java/
│   │   ├── hooks/
│   │   │   └── Hooks.java
│   │   ├── runner/
│   │   │   └── TestRunner.java
│   │   ├── steps/
│   │   │   ├── CRUDSteps.java
│   │   │   ├── LoginSteps.java
│   │   │   ├── SmokeTestSteps.java
│   │   │   └── TestSteps.java
│   │   └── utils/
│   │       └── DriverManager.java
│   └── resources/
│       └── features/
│           ├── falla.feature
│           ├── login.feature
│           ├── nuevo_usuario.feature
│           └── SmokeTest.feature

```

## 🛠️ Comandos Útiles

- Ejecutar tests: `mvn test`
- Limpiar proyecto: `mvn clean`
- Generar reporte: `mvn verify`


## ⚙️ Instalación

1. Clona el repositorio:
   ```bash
   git clone https://github.com/DanteJac/EVM5.git
   cd EVM5

2. Instala dependencias:

Asegúrate de tener instalado y configurado:

* Java 21
* Maven
* ChromeDriver (ajusta la ruta en Hooks.java o usa WebDriverManager)

## 🚀 Ejecución de Pruebas:

Ejecuta todos los escenarios etiquetados como @Login, @CRUD, @SmokeTest, @Falla con:

```
mvn test
```
Puedes filtrar por tags específicos modificando @IncludeTags en TestRunner.java.


## 🖼️ Captura de Pantalla Automática
Si un escenario falla, se genera una captura en:

```
target/screenshots/
└── Forzar_fallo_para_captura.png
```
El nombre del archivo corresponde al nombre del escenario.

## 📊 Reportes Generados
Después de ejecutar las pruebas, se generan:

```
target/
├── cucumber.json
├── cucumber-reports.html
├── screenshots/
│   └── Forzar_fallo_para_captura.png
└── surefire-reports/
```
El plugin maven-cucumber-reporting genera el reporte HTML a partir del archivo JSON.

## 🧪 Tecnologías Usadas
* Java 21
* Maven
* Selenium WebDriver 4.23.0
* Cucumber 7.14.0
* JUnit 5
* WebDriverManager 5.7.0
* Spring Boot 3.3.0

## 📄 Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo LICENSE para más detalles.

## 📬 Contacto

Para dudas o sugerencias, contáctame en: jacobo.bustos.22@gmail.com

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Coverage](https://img.shields.io/badge/coverage-85%25-yellow)
