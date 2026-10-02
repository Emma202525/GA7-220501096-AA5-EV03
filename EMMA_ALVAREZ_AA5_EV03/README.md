# GA7-220501096-AA5-EV03 - Sistema de Inventario

**Aprendiz:** Emma Alvarez

## Descripción

Sistema de inventario sencillo y fácil de usar para tiendas, pequeños negocios o cualquier persona que necesite controlar sus productos.

La API permite administrar productos y existencias sin necesidad de utilizar una interfaz compleja.

## Funcionalidades

1. Registro e inicio de sesión.
2. CRUD de productos.
3. Registro de entradas de inventario.
4. Registro de salidas de inventario.
5. Historial de movimientos.
6. Resumen de inventario.
7. Alertas mediante consulta de productos con stock bajo.

## Instalación

Requisitos:
- Node.js
- npm

Ejecutar:

```bash
npm install
npm start
```

Servidor:

```text
http://localhost:3000
```

## Prueba rápida

Crear producto:

```http
POST http://localhost:3000/api/productos
Content-Type: application/json
```

```json
{
  "nombre": "Arroz 500g",
  "categoria": "Granos",
  "precio": 2500,
  "stockMinimo": 5,
  "stock": 20
}
```

Luego consultar:

```http
GET http://localhost:3000/api/productos
```

Y registrar una salida:

```http
POST http://localhost:3000/api/inventario/salida
Content-Type: application/json
```

```json
{
  "productoId": 1,
  "cantidad": 2,
  "observacion": "Venta"
}
```

## Documentación

Consultar `API.md` para la documentación completa de los servicios.

## Versionamiento

```bash
git init
git add .
git commit -m "GA7-220501096-AA5-EV03 sistema de inventario"
git branch -M main
git remote add origin URL_DEL_REPOSITORIO
git push -u origin main
```

## Estructura

```text
EMMA_ALVAREZ_AA5_EV03/
├── data/
│   ├── movements.json
│   ├── products.json
│   └── users.json
├── src/
│   └── server.js
├── .gitignore
├── API.md
├── README.md
├── git_commands.txt
└── repositorio.txt
```
