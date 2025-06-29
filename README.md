# Guía Completa - Piscine Shell 42

Este documento reúne los conceptos fundamentales, comandos, buenas prácticas y ejercicios clave de los módulos **Shell 00** y **Shell 01** de la Piscine 42.

---

## 1. Objetivos de Aprendizaje

### 1.1 Fundamentos

- Dominar comandos básicos de terminal Unix/Linux.
- Aprender Shell Scripting utilizando `/bin/sh`.
- Familiarizarse con **Git** y el control de versiones.
- Comprender el sistema de permisos de Unix.
- Realizar procesamiento básico de texto y archivos.

---

## 2. Tecnologías y Herramientas

### 2.1 Requisitos del Sistema

- **Sistema Operativo**: Unix, Linux o macOS.
- **Shell**: `/bin/sh` (Bourne Shell).
- **Git**: Para control de versiones.
- **Editor de texto**: `vim`, `nano` o cualquier editor de tu preferencia.

---

## 3. Comandos Fundamentales

### 3.1 Navegación y Gestión de Archivos

```
ls
cd
pwd
mkdir
rmdir
rm
cp
mv
touch
```

### 3.2 Permisos y Propiedades

```
chmod
chown
chgrp
umask
stat
```

### 3.3 Visualización de Contenido

```
cat
less
more
head
tail
```

### 3.4 Búsqueda y Filtrado

```
find
grep
awk
sed
cut
sort
uniq
```

### 3.5 Compresión

```
tar
gzip
gunzip
```

### 3.6 Otros Comandos Útiles

```
wc
diff
which
whereis
```

---

## 4. Piscine Shell 00

### 4.1 Ejercicios Principales

| Ejercicio | Descripción                 | Tecnologías Utilizadas          |
|------------|-----------------------------|-----------------------------------|
| ex00       | Crear archivo básico        | `touch`, `cat`                   |
| ex01       | Listar archivos detalladamente | `ls -l`                       |
| ex02       | Crear archivo `.gitignore`  | `git`, patrones de archivos      |
| ex03       | Modificar permisos          | `chmod`                          |
| ex04       | Crear archivo comprimido    | `tar`                            |
| ex05       | Trabajar con Git            | `git add`, `git commit`          |
| ex06       | Comandos `diff` y limpieza  | `diff`, gestión de archivos      |
| ex07       | Permisos avanzados          | `chmod` con notación octal       |
| ex08       | Crear directorios con permisos | `mkdir`, `chmod`               |
| ex09       | Archivos especiales         | Enlaces simbólicos, archivos especiales |

### 4.2 Comandos Clave para Shell 00

```
touch filename
chmod 755 file
chmod 644 file
ls -l
tar -cf archive.tar files/
git add .
git commit -m "mensaje"
```

---

## 5. Piscine Shell 01

### 5.1 Ejercicios Principales

| Ejercicio | Descripción                    | Tecnologías Utilizadas     |
|------------|--------------------------------|------------------------------|
| ex01       | Mostrar grupos del usuario     | `groups`, `tr`               |
| ex02       | Buscar archivos `.sh`          | `find`                       |
| ex03       | Contar archivos                | `find`, `wc`                 |
| ex04       | Obtener dirección MAC          | `ifconfig`, `grep`           |
| ex05       | Operaciones matemáticas en shell | Aritmética en Shell         |
| ex06       | Imprimir alfabeto              | Bucles en Shell              |
| ex07       | Imprimir números               | Secuencias numéricas         |
| ex08       | Evaluar número negativo/positivo | Condicionales en Shell      |

### 5.2 Comandos Clave para Shell 01

```
find . -name "*.sh" -type f
find . -type f | wc -l
grep "patrón" archivo
cut -d: -f1 /etc/passwd
sed 's/viejo/nuevo/g' archivo
awk '{print $1}' archivo
groups usuario
id -G usuario
```

---

## 6. Conceptos Fundamentales

### 6.1 Permisos en Unix

```plaintext
rwx rwx rwx
--- --- ---
 |   |   +-- Otros (others)
 |   +------ Grupo (group)
 +---------- Propietario (owner)
```

### 6.2 Significado de Permisos

- `r` = Lectura (4)
- `w` = Escritura (2)
- `x` = Ejecución (1)

### 6.3 Ejemplos de Notación Octal

755 = rwxr-xr-x
644 = rw-r--r--
777 = rwxrwxrwx

### 6.4 Variables de Entorno

```
$USER
$HOME
$PATH
$PWD
```

---

## 7. Setup y Preparación

### 7.1 Configuración del Entorno

```
echo $SHELL
mkdir -p ~/42-piscine/shell-00
mkdir -p ~/42-piscine/shell-01
cd ~/42-piscine
```

### 7.2 Configuración de Git

```
git config --global user.name "Tu Nombre"
git config --global user.email "tu.email@student.42.fr"
```

### 7.3 Estructura de Directorios

```
~/42-piscine/
├── shell-00/
│   ├── ex00/
│   ├── ex01/
│   └── ...
└── shell-01/
    ├── ex01/
    ├── ex02/
    └── ...
```

---

## 8. Tips y Buenas Prácticas

### 8.1 Shell Scripting

```
#!/bin/sh
chmod +x script.sh
./script.sh
```

### 8.2 Debugging

```
sh -x script.sh
sh -n script.sh
```

### 8.3 Buenas Prácticas Generales

- Usar nombres descriptivos.
- Comentar el código complejo.
- Probar con distintos inputs.
- Verificar permisos antes de entregar.

---

## 9. Recursos Útiles

### 9.1 Documentación

```
man comando
comando --help
```

- Bash Guide (disponible online).

### 9.2 Herramientas Online

- https://www.shellcheck.net
- https://regex101.com

---

## 10. Comandos de Referencia Rápida

```
file filename
hexdump -C archivo
apropos palabra_clave
ps aux | grep proceso
```

---

## 11. Normas de la Piscine

- Solo `/bin/sh`.
- No usar comandos no estándar.
- Respetar exactamente la salida requerida.
- Entregar solo los archivos pedidos.
- Verificar permisos.

---

## 12. Objetivos por Completar

### 12.1 Shell 00

- Crear archivos básicos.
- Configurar permisos.
- Usar Git correctamente.
- Crear archivos comprimidos.

### 12.2 Shell 01

- Dominar `find` y `grep`.
- Procesar texto con `awk` y `sed`.
- Trabajar con variables de entorno.
- Crear scripts funcionales.

---

## 13. Recomendaciones Finales

- Leer bien los enunciados.
- Probar exhaustivamente los scripts.
- Validar los scripts con ShellCheck.
- Mantener el código limpio.


## 14. Recursos para Profundizar

### Documentación y Tutoriales

- [The Shell Scripting Tutorial](https://www.shellscript.sh/) – Tutorial completo y actualizado para Bourne shell.
- [LearnShell.org](https://www.learnshell.org/) – Curso interactivo gratuito para aprender Shell Scripting.
- [TutorialsPoint - Shell Scripting](https://www.tutorialspoint.com/unix/shell_scripting.htm) – Guía clara y estructurada sobre scripting en Unix/Linux.
- [Red Hat - 13 Resources for Learning Bash Scripting](https://www.redhat.com/en/blog/learn-bash-scripting) – Recopilación de guías, tutoriales y buenas prácticas.
- [Introduction to Bash Scripting (GitHub Ebook)](https://github.com/bobbyiliev/introduction-to-bash-scripting) – Ebook open-source, práctico y organizado.
- [GeeksforGeeks - Introduction to Linux Shell & Shell Scripting](https://www.geeksforgeeks.org/introduction-linux-shell-shell-scripting/) – Artículo introductorio con ejemplos prácticos.

### Herramientas Online

- [ShellCheck](https://www.shellcheck.net/) – Analizador estático para scripts de shell, ayuda a detectar errores y malas prácticas.
- [Regex101](https://regex101.com/) – Plataforma interactiva para probar y depurar expresiones regulares.

## Recursos Adicionales

Eliminar archivos .DS_Store existentes del repositorio:

```
find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch
```

Agregar .DS_Store al archivo .gitignore

```
echo .DS_Store >> .gitignore
```




