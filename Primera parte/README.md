# Seller Game — Histórico de Interacciones

Proyecto académico para la materia **Paradigmas de Programación**, desarrollado
en **Godot 4.7 (C# / .NET 8)**. Simula un vendedor que intercambia recursos
(troncos por monedas) con distintos NPCs, y mantiene un **histórico de todas
las interacciones** realizadas durante la partida.

## Tabla de contenidos

- [Descripción](#descripción)
- [Funcionalidad agregada](#funcionalidad-agregada)
- [Controles](#controles)
- [Tecnologías](#tecnologías)
- [Estructura del proyecto](#estructura-del-proyecto)
- [Arquitectura de la solución](#arquitectura-de-la-solución)
- [Cómo ejecutar el proyecto](#cómo-ejecutar-el-proyecto)
- [Créditos de assets](#créditos-de-assets)

## Descripción

El jugador controla a un **Vendedor** que se mueve por el mapa y puede
interactuar con distintos NPCs (Lancero, Goblin, Monje) para venderles
recursos. Cada venta concretada queda registrada en un histórico global,
consultable en cualquier momento desde la interfaz del juego.

## Funcionalidad agregada

Se implementó el botón de **histórico de interacciones**, que hasta antes de
este trabajo no tenía ninguna lógica real. Ahora:

- Cada vez que el Vendedor concreta una venta con un NPC, se guarda un
  registro con: quién vendió, a quién, qué se vendió, cuánto y por cuánto.
- El registro se muestra con el formato:
  `"Vendedor vendió (1) tronco a Lancero por (1) moneda"`.
- El jugador puede abrir o cerrar el panel del histórico en cualquier
  momento, desde cualquier punto del mapa.

Ver el detalle técnico completo en [`docs/ARQUITECTURA.md`](docs/ARQUITECTURA.md).

## Controles

| Tecla | Acción                                  |
|-------|------------------------------------------|
| Flechas / WASD | Mover al Vendedor                |
| `X`   | Vender un tronco al NPC con el que se está interactuando |
| `Z`   | Mostrar / ocultar el histórico de interacciones |

## Tecnologías

- [Godot Engine 4.7](https://godotengine.org/) (`Godot.NET.Sdk/4.7.2`)
- C# sobre **.NET 8**
- Assets: [Tiny Swords (Free Pack)](https://pixelfrog-assets.itch.io/tiny-swords)

## Estructura del proyecto

```
seller-game/
├── Assets/                  # Sprites, íconos y recursos gráficos
├── Characters/
│   ├── Seller.cs            # Lógica del jugador (movimiento, UI, histórico)
│   ├── Lancer.cs            # NPC comprador (registra la venta al concretarse)
│   ├── Goblin.cs            # NPC (sin lógica de compra aún)
│   ├── Monk.cs               # NPC (sin lógica de compra aún)
│   └── *.tscn                # Escenas de cada personaje
├── Systems/
│   ├── Transaction.cs       # Modelo inmutable de un registro de interacción
│   └── TransactionHistory.cs # Singleton (Autoload) que guarda el histórico
├── world.tscn               # Escena principal del mapa
├── project.godot             # Configuración del proyecto (incluye el Autoload)
└── SellerGame.csproj
```

## Arquitectura de la solución

Documentación técnica detallada, con diagrama de flujo, en
[`docs/ARQUITECTURA.md`](docs/ARQUITECTURA.md).

Resumen rápido:

- **Patrón Singleton / Autoload:** `TransactionHistory` es un nodo global
  registrado en `project.godot`, accesible desde cualquier script mediante
  `TransactionHistory.Instance`.
- **Modelo inmutable:** `Transaction` representa un registro fijo, no
  editable después de creado.
- **Programación orientada a eventos:** `TransactionHistory` emite una señal
  (`HistoryUpdated`) cada vez que se agrega un registro; la UI se suscribe a
  esa señal para refrescarse automáticamente.

## Cómo ejecutar el proyecto

1. Instala [Godot 4.7 (.NET/Mono)](https://godotengine.org/download) y el
   [SDK de .NET 8](https://dotnet.microsoft.com/download).
2. Clona este repositorio.
3. Abre `project.godot` con Godot.
4. Presiona **Build** (ícono de martillo) para compilar el código C#.
5. Ejecuta el proyecto con `F5` o el botón de Play.

## Créditos de assets

Los sprites de personajes y UI provienen del pack gratuito
**Tiny Swords (Free Pack)**, de Pixel Frog.
