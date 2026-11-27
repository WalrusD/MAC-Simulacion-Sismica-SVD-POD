# Simulación estructural sísmica mediante SVD/POD

Trabajo final de Matemática Aplicada a la Computación (MAC) — Universidad San Ignacio de Loyola, 2026-II.

## Descripción

Este dashboard web constituye una representación visual e interactiva basada en el código de simulación numérica desarrollado en Python en Google Colab para el proyecto «Implementación numérica y optimización de simulación estructural sísmica empleando reducción de orden modal».

El caso de estudio representa un edificio de 20 pisos como un marco de corte (shear frame), sometido a una excitación sísmica. Se compara el modelo completo (FOM) con un modelo de orden reducido (ROM), utilizando descomposición en valores singulares (SVD), descomposición ortogonal propia (POD) y proyección de Galerkin.

## Funcionalidades

- Configuración de pisos, masa, rigidez, amortiguamiento, intensidad y duración de la excitación sísmica.
- Selección de escenarios preestablecidos y umbral de energía acumulada.
- Comparación de desplazamientos, modos dominantes, errores y tiempos de ejecución.
- Visualización interactiva y exportación de resultados en CSV.

## Relación con Google Colab

La implementación original utiliza Python, NumPy, SciPy y el integrador adaptativo RK45 (`solve_ivp`). La adaptación web realiza cálculos en JavaScript mediante RK4 y presenta los resultados con Plotly.js. No ejecuta ni se conecta al notebook de Colab. Debido a las diferencias de integración numérica y entorno de ejecución, los resultados y tiempos pueden variar respecto al informe original.

En el informe, el escenario de referencia obtuvo dos modos dominantes, 99.14 % de energía acumulada, error RMS de 1.43 × 10⁻³ m y aceleración de 1.80×. Estos son resultados de la implementación original, no garantías del dashboard web.

## Uso

Descarga o clona el repositorio y abre `index.html` en un navegador moderno. Se requiere conexión a Internet para cargar Tailwind CSS, Plotly.js y Google Fonts desde sus CDN. No se requiere instalar Python ni iniciar un servidor para visualizar el dashboard.

## Tecnologías

HTML5, CSS, JavaScript, Tailwind CSS y Plotly.js.

## Alcance

Prototipo académico de visualización y experimentación. No constituye una herramienta certificada de evaluación de seguridad estructural ni un sistema de alerta sísmica real.
