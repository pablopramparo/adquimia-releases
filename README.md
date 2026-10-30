# ADQUIMIA · releases

Descargas de **ADQUIMIA** (gráficas comerciales desde planillas Excel). Software propietario; ver [LICENSE](LICENSE).

## Qué se descarga

- **ADQUIMIA_x.y.z_x64-setup.exe**: instalador de la app para Windows 10/11.
- **ADQUIMIA-plugin-x.y.z.ccx**: plugin para Photoshop 26. Se instala aparte.

## Orden de instalación

El orden no es obligatorio, pero este evita pasos extra:

1. Instala la app y ábrela una vez (crea la carpeta que usa el plugin).
2. Instala el plugin y abre el panel **ADQUIMIA** en Photoshop: se conecta solo.
3. Si necesitas recortar fondos, instala el componente desde la app.

Si instalas el plugin primero, el panel avisa que no encuentra la carpeta de ADQUIMIA; abre la app una vez y vuelve a abrir el panel.

## Instalar la app

1. Descarga el `.exe` de la última [release](../../releases/latest) y ejecútalo.
2. Windows puede mostrar el aviso azul de SmartScreen, porque el instalador no está firmado: elige **Más información → Ejecutar de todas formas**.
3. Se instala solo para tu usuario, sin permisos de administrador.

La app se actualiza sola: al abrirse avisa si hay una versión nueva y la instala cuando lo pides.

## Instalar el plugin de Photoshop

1. Descarga el `.ccx` de la misma release.
2. Haz doble clic para instalarlo con Creative Cloud, o cárgalo con el UXP Developer Tool.
3. En Photoshop abre el panel **ADQUIMIA** (menú Plugins). Se conecta solo a la app.

El plugin no se actualiza solo: si ADQUIMIA avisa que está desactualizado, descarga el `.ccx` nuevo y vuelve a instalarlo.

## Recorte de fondos

La primera vez que se usa, la app ofrece instalar un componente (Python y librerías, varios cientos de MB). Hace falta internet.
