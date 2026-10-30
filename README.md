# ADQUIMIA · releases

Descargas de **ADQUIMIA** (gráficas comerciales desde planillas Excel). Software propietario; ver [LICENSE](LICENSE).

## Qué se descarga

- **ADQUIMIA_x.y.z_x64-setup.exe**: instalador de la app para Windows 10/11.
- **ADQUIMIA-plugin-x.y.z.zip**, **.ccx** e **install-plugin.ps1**: el plugin para Photoshop 26 y sus dos formas de instalarlo. Se instala aparte.

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

El plugin no está firmado por Adobe, así que Photoshop lo trata como "no verificado". Hay dos formas de instalarlo.

**Sin Creative Cloud (probado en Photoshop 26)** · archivos `ADQUIMIA-plugin-x.y.z.zip` e `install-plugin.ps1`

1. Descomprime el `.zip` en una carpeta y copia dentro de ella `install-plugin.ps1`.
2. Cierra Photoshop, abre PowerShell en esa carpeta y ejecuta:
   `powershell -ExecutionPolicy Bypass -File .\install-plugin.ps1`
3. El script busca Photoshop, copia el plugin a su carpeta `Plug-ins\ADQUIMIA` y pide permisos de administrador solo si hacen falta. Para quitarlo: el mismo comando con `-Uninstall`.
4. Abre Photoshop y el panel **ADQUIMIA** (menú Plugins): se conecta solo.

Este método no es oficial de Adobe: una actualización de Photoshop puede borrar la copia. Si pasa, vuelve a ejecutar el script. Si cargaste el plugin con el UXP Developer Tools, descárgalo antes: tiene el mismo id y se duplicaría.

**Con Creative Cloud Desktop** · archivo `ADQUIMIA-plugin-x.y.z.ccx`

1. Cierra Photoshop y haz doble clic en el `.ccx`.
2. Creative Cloud avisa que el plugin no fue verificado por Adobe: elige **Instalar localmente** y confirma.
3. Abre Photoshop y el panel **ADQUIMIA** (menú Plugins).

El plugin no se actualiza solo: si ADQUIMIA avisa que está desactualizado, descarga el archivo nuevo y vuelve a instalarlo.

## Recorte de fondos

La primera vez que se usa, la app ofrece instalar un componente (Python y librerías, varios cientos de MB). Hace falta internet.
