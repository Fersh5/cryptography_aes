# Algoritmo AES para cifrado y descifrado de archivos
Este repositorio es un ejecutable de Python para crear un administrador básico para el cifrado y descifrado de archivos utf-8 a través de CLI.

## Empezar
**⚠️Deberías tener Python instalado.⚠️**
**⚠️Este tutorial funciona en Linux⚠️**
Si no estás en Linux, intenta buscar las equivalencias en tu SO.

Configurar un entorno virtual:
```
python -m venv env
source env/bin/activate
```

Instalar dependencias:
```
pip install -r requirements.txt
```

## Correr ejecutable
Dar permisos para que el programa sea ejecutable
```
sudo chmod +x ./AES
```

Correr el ejemplo: (tests/index.html):
```
./AES cipher -p secret --salt salt --size 128 -i tests/index.html -o tests/index.html
./AES decipher -p secret --salt salt --size 128 -i tests/index.html.enc -o tests/index.html
```

## Variables de entorno

Para ejecutar este proyecto, deberá agregar la siguiente variable de entorno a su archivo .env: `IV=`. Puedes generar un valor aleatorio con:
```
python scripts/iv.py
```

La razón por la que se almacena el IV es porque debe ser el mismo valor al cifrar y descifrar (exactamente como la clave).

## Salir del entorno virtual
```
deactivate
```