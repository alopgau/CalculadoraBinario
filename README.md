> CLI que **suma** y **resta** números binarios de **1-8 bits**.

> **Salida exclusivamente en binario de 8 bits**

> Si no se indica signo, el programa ejecuta **ambas operaciones** (suma y resta).

---
## 1) Descripción del módulo

  

Este proyecto implementa una **calculadora binaria de 1-8 bits** que opera con **enteros sin signo**.

- Los **operandos** se introducen como **cadenas binarias** de **1-8 bits** (`0`/`1`).

- La **operación** se define por **signo**: `+` (suma) o `-` (resta).

- Si **no** se especifica el signo, el programa **realiza ambas operaciones** con los mismos operandos y muestra **dos bloques** de salida.

---
## 2) Requisitos

- **Python 3.10 o superior**.

- **Sin dependencias externas obligatorias.**
---

## 3) Instalación de Python

### 3.1 Linux

#### Debian/Ubuntu (y derivados)
```bash
sudo apt update
sudo apt install -y python3 python3-pip python3-venv
python3 --version
python3 -m pip --version
```

#### Fedora
```bash
sudo dnf install -y python3 python3-pip python3-virtualenv
python3 --version
python3 -m pip --version
```

#### Arch/Manjaro
```bash
sudo pacman -S --needed python python-pip
python --version
python -m pip --version
```

> **Entorno virtual (opcional recomendado)**
```bash
python3 -m venv .venv
# Activar:
# Linux/macOS:
source .venv/bin/activate
# (Salir: 'deactivate')
```

### 3.2 Windows

#### Opción A — Microsoft Store
1. Abrir **Microsoft Store**, buscar **Python 3.x** (Python Software Foundation).
2. Instalar y verificar:
```powershell
py --version
py -m pip --version
```

#### Opción B — Instalador oficial
1. Descargar desde **https://www.python.org/downloads/** el instalador de Python 3.x.
2. **Marcar** “**Add Python to PATH**” durante la instalación.
3. Verificar:
```powershell
py --version
py -m pip --version
```

> **Entorno virtual (opcional)**
```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
# (Salir: 'deactivate')
```

---

## 4) Ejecución del módulo

  

### Sintaxis general

```bash

python calculadorabinario.py OPERANDO1 OPERANDO2 [SIGNO]

```

- `OPERANDO1` y `OPERANDO2`: binarios de **1 a 8 bits**.

- `SIGNO` (opcional): `+` para **suma**, `-` para **resta**.

- Si **omites el signo**, el programa realiza **suma y resta** y muestra **dos bloques** de salida.

  

> En Windows puedes usar `py` en lugar de `python`.

> En Linux, si conviven varias versiones, usa `python3`.

---
### Ejemplos

**Suma explícita**

```bash
# Entrada esperada
# Linux/macOS
python3 calculadorabinario.py 01111111 01111111 +
# Windows
python calculadorabinario.py 01111111 01111111 +
# Salida esperada
01111111
+
01111111
---------
11111110
```

**Resta explícita**

```bash
# Entrada esperada
# Linux/macOS
python3 calculadorabinario.py 01111111 01111111 -
# Windows
python calculadorabinario.py 01111111 01111111 -
# Salida esperada
01111111
-
01111111
--------
00000000
```

**Sin signo (realiza ambas)**
```bash
# Entrada esperada
# Linux/macOS
python3 calculadorabinario.py 01111111 01111111
# Windows
python calculadorabinario.py 01111111 01111111
# Salida esperada
01111111
+
01111111
---------
11111110


01111111
-
01111111
--------
00000000
```
---
## 6) Mensajes de error y códigos de salida

  

- **Operando inválido** (no binario o no igual a 8 bits)

- Mensaje: `El formato del [primer,segundo,ambos] número(s) es incorrecto. Por favor, vuelve a introducirlo(s). (Debe ser binario y de 8 dígitos):`

- **Signo/operación inválida** (distinta de `+` o `-`)

- Mensaje: `Introduce una operación válida, o ninguna para realizar ambas (suma y resta, usando sus respectivos símbolos`
---
## 7) Problemas frecuentes (FAQ)
- **“python: command not found” / “py no se reconoce”** → Instala Python o ajusta el **PATH** (ver sección 3).
- **“pip no se reconoce”** → Usa `python -m pip` (o `py -m pip` en Windows).
- **Formato de operando incorrecto** → Revisa que sean solo `0`/`1` y longitud ≤ 8.
- **Signo en posición incorrecta** → Asegúrate de usar `OPERANDO1 OPERANDO2 [SIGNO]`
- **Formato de operando incorrecto** → Revisa que sean solo `0`/`1` y longitud ≤ 8.
- **Asegúrate de usar la siguiente estructura:** `OPERANDO1 OPERANDO2 [SIGNO]`.
¡
