¡Excelente elección! Integrar Flutter con Firebase usando la CLI (Interfaz de Línea de Comandos) es la forma más profesional y eficiente de gestionar tus proyectos, ya que automatiza la configuración de archivos tanto para Android, iOS como para la web.

Aquí tienes la guía completa para preparar tu entorno.

---

## 1. Software necesario: Node.js y npm
Para usar Firebase CLI, necesitas **Node.js**, el cual incluye automáticamente **npm** (Node Package Manager).

* **Node.js:** Es el entorno de ejecución que permite correr JavaScript fuera del navegador.
* **npm:** Es el gestor de paquetes que descargará e instalará las herramientas de Firebase en tu sistema.

---

## 2. Cómo verificar si ya tienes Node.js y npm
Antes de instalar nada, abre tu terminal (PowerShell en Windows, Terminal en macOS/Linux) y escribe:

```bash
node -v
npm -v
```
* **Si ves un número (ej. `v20.12.0`):** ¡Ya lo tienes! Puedes saltar al paso de instalación de Firebase.
* **Si ves un error ("command not found"):** Necesitas instalarlo.

---

## 3. Instalación paso a paso de Node.js (Modo Global)

### En Windows:
1.  Ve al sitio oficial: [nodejs.org](https://nodejs.org/).
2.  Descarga la versión **LTS** (Long Term Support), es la más estable.
3.  Ejecuta el instalador `.msi`.
4.  **Importante:** Durante la instalación, asegúrate de que la casilla **"Add to PATH"** esté marcada. Esto es lo que permite que el comando funcione de manera "global".
5.  Finaliza y reinicia tu terminal.

### En macOS:
* Puedes usar el instalador de la web oficial o, si usas **Homebrew**, simplemente escribe:
    `brew install node`

---

## 4. Instalación de Firebase CLI (`firebase-tools`)
Una vez que `npm` funciona, instalaremos las herramientas de Firebase. El parámetro `-g` indica que la instalación es **global**, permitiéndote usar el comando `firebase` en cualquier carpeta de tu computadora.

### El comando:
Escribe lo siguiente en tu terminal:
```bash
npm install -g firebase-tools
```

> **Nota para macOS/Linux:** Si recibes un error de "Permission denied", intenta usando `sudo`:
> `sudo npm install -g firebase-tools`

---

## 5. Acceso a Firebase con tu Cuenta de Google
Para que la CLI tenga permiso de modificar tus proyectos en la consola de Firebase, debes iniciar sesión:

1.  En la terminal, escribe:
    ```bash
    firebase login
    ```
2.  Se abrirá automáticamente una ventana en tu navegador predeterminado.
3.  Selecciona tu cuenta de Google vinculada a Firebase.
4.  Haz clic en **"Permitir"**.
5.  Vuelve a la terminal; verás un mensaje de éxito: `✔  Success! Logged in as usuario@gmail.com`.

---

## 6. Bonus: Preparar Firebase para Flutter
Para que Firebase "hable" perfectamente con Flutter, Google utiliza una herramienta llamada **FlutterFire CLI**.

### Instalación de FlutterFire CLI:
```bash
dart pub global activate flutterfire_cli
```

### Configuración del proyecto:
Dentro de la carpeta raíz de tu proyecto Flutter, ejecutas:
```bash
flutterfire configure
```
Este comando te permitirá seleccionar tus proyectos existentes en la consola de Firebase y generará automáticamente el archivo `firebase_options.dart`, ahorrándote toda la configuración manual de IDs y claves.



---

**Resumen de comandos rápidos:**
* `node -v`: Verifica Node.
* `npm install -g firebase-tools`: Instala la CLI.
* `firebase login`: Vincula tu cuenta.
* `firebase projects:list`: Lista tus proyectos actuales para confirmar que todo funciona.
