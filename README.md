# ADQUIMIA · releases

Descargas de **ADQUIMIA** (gráficas comerciales desde planillas Excel). Software propietario; ver [LICENSE](LICENSE).

## Qué se descarga

- **ADQUIMIA_x.y.z_x64-setup.exe**: instalador de la app para Windows 10/11. **Es lo único que hace falta**: la app instala el plugin de Photoshop y el componente de recorte de fondos.
- **ADQUIMIA-plugin-x.y.z.zip**, **.ccx** e **install-plugin.ps1**: el plugin por separado, solo para instalarlo a mano (ver al final).

## Instalar (recomendado)

1. Descarga el `.exe` de la última [release](../../releases/latest) y ejecútalo. Windows puede mostrar el aviso azul de SmartScreen, porque el instalador no está firmado: elige **Más información → Ejecutar de todas formas**. Se instala solo para tu usuario, sin permisos de administrador.
2. Abre ADQUIMIA. Si Photoshop está instalado y no tiene el plugin, aparece **"Falta instalar el plugin de Photoshop"**: pulsa **Instalar plugin** (Windows puede pedir permisos de administrador si Photoshop está en `Program Files`).
3. Cierra Photoshop por completo y vuelve a abrirlo. En **Plugins → ADQUIMIA** abre el panel: se conecta solo a la app.
4. Para quitar fondos de las fotos, la app ofrece **Instalar** el componente (Python y librerías, varios cientos de MB). Hace falta internet y se hace una sola vez.

**Actualizaciones:** al abrirse, la app avisa si hay una versión nueva y la instala cuando lo pides. Si la versión nueva trae un plugin nuevo, la app ofrece actualizarlo también.

**Si el plugin desaparece** (por ejemplo, tras actualizar Photoshop): en el menú lateral de la app, la línea "Plugin de Photoshop" tiene el botón **Reinstalar** (o **Instalar**).

## Instalar el plugin a mano (opcional)

Solo si no quieres hacerlo desde la app. El plugin no está firmado por Adobe, así que Photoshop lo trata como "no verificado". Hay dos formas.

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

Instalado a mano, el plugin no se actualiza solo: si ADQUIMIA avisa que está desactualizado, instala el nuevo desde la app o descarga el archivo y repite estos pasos.

## Recorte de fondos

La primera vez que se usa, la app ofrece instalar un componente (Python y librerías, varios cientos de MB). Hace falta internet.
