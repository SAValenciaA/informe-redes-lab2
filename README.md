## 1 Instalar GitHub CLI

### Linux (Arch)

```bash
sudo pacman -S github-cli
```

### Linux (Debian/Ubuntu)

```bash
sudo apt install gh
```

### Windows / macOS

Descargar desde:

https://cli.github.com/

---

## 2 Autenticarse en GitHub

En la terminal ejecutar:

```bash
gh auth login
```

Luego seguir las opciones recomendadas:

```
GitHub.com
HTTPS
Login with a web browser
```

Y agreguar tu identidad a git

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## 3 Clonar el repositorio

Una vez autenticado, el repositorio puede clonarse usando:

```bash
gh repo clone SAValenciaA/informe-redes-lab2
```

---

## 4 Entrar al directorio del proyecto

Después de clonar el repositorio:

```bash
cd informe-redes-lab2
```

Si el proyecto no se abrió automáticamente en VS Code, se puede abrir con:

```bash
code .
```

---

# 5. Compilar el documento

El archivo principal del proyecto es:

```
main.tex
```

Para compilar:

### Opción 1 (automática)

Guardar el archivo (`Ctrl + S`).
La extensión compilará el documento automáticamente.

### Opción 2 (manual)

Presionar:

```
Ctrl + Alt + B
```

Esto ejecutará el proceso de compilación.

---

# 6. Ver el PDF

Después de compilar el documento, se puede abrir el PDF utilizando el visor integrado de VS Code.

Para abrir el visor de PDF usar el atajo:

```
Ctrl + Alt + V
```

Este comando ejecuta la función **View LaTeX PDF**, que abre el archivo PDF generado dentro de Visual Studio Code.

También se puede abrir manualmente desde la paleta de comandos:

```
Ctrl + Shift + P
```

y buscar:

```
LaTeX Workshop: View LaTeX PDF
```

Una vez abierto el visor, el PDF se actualizará automáticamente cada vez que el documento se vuelva a compilar.

---

# 7. Estructura del proyecto

El proyecto está organizado en múltiples archivos para facilitar su mantenimiento.

```
project/
│
├── main.tex
├── referencias.bib
│
├── sections/
│   ├── marco_teorico.tex
│   ├── metodologia.tex
│   └── referencias.tex
│
├── figures/
│
├── build/
│
└── .vscode/
```

* `main.tex` → archivo principal del documento
* `sections/` → secciones del documento
* `referencias.bib` → base de datos bibliográfica
* `figures/` → imágenes del documento
* `build/` → archivos generados durante la compilación

Puedes ignorar todo lo demas.

---

# 8. Bibliografía

El proyecto utiliza **BibLaTeX** con **Biber** para manejar las referencias.

Ejemplo de cita en el texto:

```latex
\cite{clave}
```
