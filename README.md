# Fondo Viaje Diciembre

Aplicación web simple para llevar el control del fondo de viaje entre marzo y diciembre de 2026.

## Vista general

Este proyecto permite registrar personas, definir su aporte mensual y marcar pagos por mes con montos personalizados.
Todo corre en el navegador, sin backend, y los datos quedan guardados en `localStorage`.

## Características

- Registro de personas con aporte mensual base.
- Tabla mensual de pagos (Mar-Dic 2026).
- Marcado de pagos como pagado/no pagado con confirmación.
- Monto por pago editable al momento de registrar el depósito.
- Resumen en tiempo real:
	- Total recaudado.
	- Total esperado.
	- Cantidad de pagos pendientes.
- Persistencia local automática en el navegador.

## Stack

- HTML
- CSS
- JavaScript Vanilla
- Despliegue estático en Vercel

## Estructura del proyecto

```text
.
|- index.html     # UI, estilos y lógica completa
|- vercel.json    # Configuración de despliegue
|- README.md
```

## Inicio rápido

1. Clona el repositorio:

```bash
git clone <url-del-repo>
cd toma-montos
```

2. Abre `index.html` directamente en tu navegador
o levanta un servidor estático local (opcional):

```bash
python -m http.server 5500
```

3. Abre `http://localhost:5500`.

## Uso

1. Escribe nombre y monto mensual.
2. Haz clic en `Agregar` para crear una nueva persona.
3. En cada mes, presiona `Pendiente` para registrar pago.
4. Ajusta el monto depositado y confirma.
5. Si un pago fue marcado por error, vuelve a hacer clic para dejarlo en no pagado.

## Persistencia de datos

- Clave de almacenamiento: `viaje-dic-2026`.
- Los datos se guardan en `localStorage` del navegador actual.
- Si limpias el almacenamiento del navegador, se perderán los registros.

## Despliegue en Vercel

El proyecto incluye `vercel.json` para servir `index.html` como sitio estático:

- build: `@vercel/static`
- route catch-all hacia `index.html`

Puedes desplegar con:

```bash
vercel --prod
```

## Ideas de mejora

- Exportar/importar datos en JSON.
- Filtros por estado (al día, con deuda).
- Historial de cambios por persona.
- Soporte para varios fondos en paralelo.

## Contribución

1. Haz fork del repositorio.
2. Crea una rama para tu cambio: `git checkout -b feature/mi-mejora`.
3. Realiza commits claros.
4. Abre un Pull Request con contexto y capturas si aplica.

## Licencia

Este proyecto está bajo licencia MIT.