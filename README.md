# ADQUIMIA · releases

Descargas de **ADQUIMIA** (gráficas comerciales desde planillas Excel). Software propietario; ver [LICENSE](LICENSE).

## Qué se descarga

- **ADQUIMIA_x.y.z_x64-setup.exe**: instalador de la app para Windows 10/11.
- **ADQUIMIA-plugin-x.y.z.ccx** y **.zip**: el mismo plugin para Photoshop 26, para dos formas de instalarlo. Se instala aparte.

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

El plugin no está firmado por Adobe, así que Photoshop lo trata como "no verificado". Hay dos formas de instalarlo; usa la primera si la PC tiene Creative Cloud Desktop.

**Con Creative Cloud Desktop** (`ADQUIMIA-plugin-x.y.z.ccx`)

1. Cierra Photoshop y haz doble clic en el `.ccx`.
2. Creative Cloud avisa que el plugin no fue verificado por Adobe: elige **Instalar localmente** y confirma.
3. Abre Photoshop y el panel **ADQUIMIA** (menú Plugins).

**Sin Creative Cloud, con el UXP Developer Tools** (`ADQUIMIA-plugin-x.y.z.zip`). Sirve la extensión «Adobe UXP Developer Tools» de Visual Studio Code, que no necesita Creative Cloud.

1. Descomprime el `.zip` en una carpeta fija (por ejemplo `C:\ADQUIMIA\plugin`). No la muevas después.
2. En Photoshop activa el modo desarrollador (Configuración → Plugins) y abre el UXP Developer Tools (en VS Code: panel de UXP).
3. **Add Plugin** → elige el `manifest.json` de esa carpeta → **Load**. Acepta el permiso de archivos si lo pide. (No lo pude comprobar en una PC sin Creative Cloud.)
4. Esta carga hay que repetirla si Photoshop se reinicia y el Developer Tool no la recuerda.

En ambos casos el panel se conecta solo a la app. El plugin no se actualiza solo: si ADQUIMIA avisa que está desactualizado, descarga el archivo nuevo y vuelve a instalarlo.

## Recorte de fondos

La primera vez que se usa, la app ofrece instalar un componente (Python y librerías, varios cientos de MB). Hace falta internet.
