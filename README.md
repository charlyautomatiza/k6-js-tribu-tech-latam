<p align="center">
  <a href="https://www.twitch.tv/charlyautomatiza"><img alt="Twitch" src="https://img.shields.io/badge/CharlyAutomatiza-Twitch-9146FF.svg" style="max-height: 300px;"></a>
  <a href="https://discord.gg/wwM9GwxmRZ"><img alt="Discord" src="https://img.shields.io/discord/944608800361570315" style="max-height: 300px;"></a>
  <a href="http://twitter.com/char_automatiza"><img src="https://img.shields.io/badge/@char__automatiza-Twitter-1DA1F2.svg?style=flat" style="max-height: 300px;"></a>
  <a href="https://www.youtube.com/c/CharlyAutomatiza?sub_confirmation=1"><img src="https://img.shields.io/badge/CharlyAutomatiza-Youtube-FF0000.svg" style="max-height: 300px;" style="max-height: 300px;"></a>
  <a href="https://www.linkedin.com/in/gautocarlos/"><img src="https://img.shields.io/badge/Carlos%20 Gauto-LinkedIn-0077B5.svg" style="max-height: 300px;" style="max-height: 300px;"></a>
</p>

# ¿Cómo explotar el potencial de JavaScript y K6?

Este repositorio contiene scripts de pruebas de rendimiento desarrollados con JavaScript y K6, además incluye una GitHub Actions para la ejecución continua de las pruebas en CI/CD.

## Contenido

- [Requisitos](#requisitos)
- [Instalación](#instalación)
- [Ejecución de Pruebas](#ejecución-de-pruebas)
- [GitHub Actions](#github-actions)
- [Licencia](#licencia)

## Requisitos

Antes de ejecutar las pruebas, asegúrate de tener [K6](https://grafana.com/docs/k6/latest/) instalado en tu sistema.
Sigue las instrucciones en la [documentación oficial](https://grafana.com/docs/k6/latest/set-up/install-k6/).

## Instalación

1. Clone este repositorio en su máquina local:

```bash
git clone https://github.com/charlyautomatiza/k6-js-tribu-tech-latam.git
```

2. Navega hasta el directorio del proyecto:

```bash
cd k6-js-tribu-tech-latam
```

## Ejecución de Pruebas

Para realizar una ejecución local:

```bash
k6 run ./src/script.js
```

Para usar K6 WebDashboard:

```bash
K6_WEB_DASHBOARD=true k6 run ./src/script.js
```

Para guardar el reporte como un archivo HTML, podemos ejecutar el siguiente comando

```bash
K6_WEB_DASHBOARD=true K6_WEB_DASHBOARD_EXPORT=html-report.html k6 run ./src/script.js
```

Para ejecutar un test de browser, podemos ejecutar el siguiente comando:

```bash
K6_BROWSER_HEADLESS=true k6 run ./src/browser.js
```

Observe que la variable de ambiente `K6_BROWSER_HEADLESS` debe ser definida como `true` para ser ejecutada en herramientas de integración contínua. Para ejecución y depuración en local, es útil usar la variable con el valor definido como `false` para ejecutar el browser en primer plano.

```bash
K6_BROWSER_HEADLESS=false k6 run ./src/browser.js
```

## GitHub Actions

Este repositorio incluye una GitHub Actions configurada para ejecutar pruebas continuamente en la branch principal. El workflow está definido en el archivo [k6-runner.yml](.github/workflows/k6-runner.yml) y permite ejecutar tanto el ejemplo de API como el ejemplo de browser

## Extensiones VSCode recomendadas

- [Conventional Commits for VSCode](https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits)

- [GitHub Pull Requests](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)

- [Codeium: AI Coding](https://marketplace.visualstudio.com/items?itemName=Codeium.codeium)

- [SonarLint](https://marketplace.visualstudio.com/items?itemName=SonarSource.sonarlint-vscode)

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

## Licencia

Este proyecto está bajo la licencia Creative Commons CC0 1.0 Universal.
