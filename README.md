# 🎮 Godot NPC Trading System

> **Proyecto académico — Paradigmas de Programación**

Sistema interactivo desarrollado en **Godot Engine** como proyecto académico para la asignatura de **Paradigmas de Programación**. El proyecto está orientado al desarrollo de interacciones entre un vendedor y diferentes NPCs dentro de un entorno de juego.

---

## 📌 Descripción

**Godot NPC Trading System** es un proyecto de desarrollo de videojuegos enfocado en la implementación y evolución de un sistema de interacción entre personajes no jugables (**NPCs**).

El proyecto parte de una base funcional sobre la cual se incorporarán nuevas características y, posteriormente, se realizará un proceso de **reworking y refactorización del código**, con el objetivo de mejorar su organización, mantenibilidad y aplicación de conceptos relacionados con la **Programación Orientada a Objetos (POO)** y los paradigmas de programación.

Actualmente, una de las funcionalidades principales en desarrollo consiste en implementar un **histórico de interacciones**, permitiendo consultar las acciones realizadas entre el vendedor y los diferentes NPCs.

---

## 🎯 Objetivos

### Objetivo general

Desarrollar y evolucionar un sistema interactivo en Godot que permita representar las interacciones entre un vendedor y diferentes NPCs, aplicando principios de programación orientada a objetos y buenas prácticas de desarrollo de software.

### Objetivos específicos

* Implementar un sistema de interacción entre el vendedor y los diferentes NPCs.
* Registrar las acciones realizadas durante las interacciones.
* Permitir consultar el histórico de interacciones del vendedor.
* Representar de manera clara quién realizó la interacción, con quién y qué acción se llevó a cabo.
* Aplicar conceptos de **Programación Orientada a Objetos (POO)**.
* Analizar y mejorar progresivamente la estructura del código.
* Realizar un proceso futuro de **reworking y refactorización** del proyecto.
* Aplicar conceptos relacionados con los paradigmas de programación estudiados durante la asignatura.

---

## 🚧 Estado del proyecto

**En desarrollo**

| Área                       |      Estado      |
| -------------------------- | :--------------: |
| Proyecto base en Godot     |        🟢        |
| Sistema de personajes/NPCs |        🟢        |
| Interacciones              |        🟡        |
| Histórico de interacciones | 🟡 En desarrollo |
| Refactorización del código |     🔴 Futuro    |
| Reworking arquitectónico   |     🔴 Futuro    |
| Aplicación de POO          |  🟡 En evolución |
| Documentación              | 🟡 En desarrollo |

**Leyenda:**
🟢 Implementado · 🟡 En desarrollo · 🔴 Pendiente

---

## 🛠️ Tecnologías

| Tecnología       | Uso                                                                          |
| ---------------- | ---------------------------------------------------------------------------- |
| **Godot Engine** | Motor de desarrollo del proyecto                                             |
| **Godot .NET**   | Entorno de desarrollo con soporte para C#                                    |
| **C#**           | Desarrollo de la lógica y programación orientada a objetos                   |
| **Python**       | Lenguaje previsto para el trabajo académico relacionado con POO y paradigmas |
| **Git**          | Control de versiones                                                         |
| **GitHub**       | Gestión y almacenamiento del repositorio                                     |

---

## 🎮 Sistema de interacciones

El proyecto cuenta con diferentes personajes que participan en el entorno de juego. Entre los recursos actualmente presentes se encuentran personajes como:

* **Vendedor**
* **Lancero**
* **Monje**
* **Goblin**

El sistema busca representar diferentes tipos de interacción entre estos personajes, especialmente aquellas relacionadas con el intercambio de recursos.

---

## 📜 Histórico de interacciones

Una de las tareas actuales del proyecto consiste en implementar el funcionamiento del botón encargado de consultar el **histórico de interacciones del vendedor**.

El registro debe permitir identificar de forma clara:

1. Quién realizó la acción.
2. Con qué NPC se realizó la interacción.
3. Qué acción fue ejecutada.
4. Qué recurso estuvo involucrado.
5. La cantidad correspondiente.
6. El valor utilizado en la transacción, cuando corresponda.

### Ejemplo

```text
Vendedor vendió (1) tronco a Lancero por (1) moneda.
```

El diseño visual utilizado para presentar esta información queda sujeto a las decisiones de implementación del proyecto.

El objetivo principal es que el histórico sea **claro, legible y fácilmente consultable** por el usuario.

---

## 🧩 Programación Orientada a Objetos

Uno de los objetivos a futuro del proyecto es profundizar en la aplicación de conceptos de **Programación Orientada a Objetos (POO)**.

Entre los conceptos que serán considerados durante el proceso de reworking se encuentran:

* Clases y objetos.
* Encapsulamiento.
* Abstracción.
* Herencia.
* Polimorfismo.
* Responsabilidad de las clases.
* Reutilización de código.
* Separación de responsabilidades.

La aplicación de estos conceptos estará acompañada de un proceso progresivo de análisis y refactorización del código existente.

---

## 🏗️ Reworking y refactorización

Una vez finalizada la implementación de las funcionalidades prioritarias, se plantea realizar un proceso de **reworking del proyecto**.

El objetivo será revisar la estructura actual del código y detectar oportunidades de mejora relacionadas con:

* Organización del código.
* Reutilización de componentes.
* Separación de responsabilidades.
* Acoplamiento entre clases.
* Mantenibilidad.
* Legibilidad.
* Aplicación de principios de POO.
* Diseño y estructura de los sistemas de interacción.

Este proceso permitirá utilizar el proyecto no solamente como un videojuego funcional, sino también como un espacio práctico para aplicar los conocimientos adquiridos en la asignatura de **Paradigmas de Programación**.

---

## 📁 Estructura del proyecto

La estructura se organiza principalmente alrededor de los recursos del juego, escenas y scripts correspondientes a los diferentes elementos del proyecto.

Una estructura conceptual del proyecto es:

```text
godot-npc-trading-system/
│
├── Assets/
│   └── Characters/
│       ├── Lancer/
│       ├── Monk/
│       ├── Pawn/
│       └── Goblin/
│
├── Scenes/
│   ├── Seller/
│   ├── Lancer/
│   ├── Monk/
│   └── Goblin/
│
├── Scripts/
│   └── ...
│
├── project.godot
├── *.csproj
├── *.sln
└── README.md
```

> La estructura podrá modificarse durante el proceso de reworking y refactorización.

---

## 🚀 Instalación y ejecución

### Requisitos

Para ejecutar el proyecto se requiere:

* **Godot Engine con soporte .NET**
* **.NET SDK** compatible con la versión utilizada por el proyecto.
* **Git**, en caso de clonar el repositorio.

### Clonar el repositorio

```bash
git clone https://github.com/USUARIO/godot-npc-trading-system.git
```

### Abrir el proyecto

1. Clonar o descargar el repositorio.
2. Abrir **Godot .NET**.
3. Importar el proyecto.
4. Esperar a que Godot importe los recursos necesarios.
5. Ejecutar el proyecto desde el editor.

> La versión exacta de Godot y .NET se especificará cuando quede definida la configuración final del proyecto.

---

## 🔄 Roadmap

El desarrollo del proyecto se plantea en diferentes etapas.

### Fase 1 — Funcionalidad actual

* [x] Configuración del proyecto base.
* [x] Integración de personajes y recursos.
* [ ] Implementación del botón de histórico.
* [ ] Registro de las interacciones.
* [ ] Visualización clara del histórico.

### Fase 2 — Reworking

* [ ] Analizar la arquitectura existente.
* [ ] Identificar problemas de diseño.
* [ ] Refactorizar código.
* [ ] Mejorar la separación de responsabilidades.
* [ ] Aplicar principios de POO.
* [ ] Reducir duplicación de código.

### Fase 3 — Evolución

* [ ] Mejorar el sistema de interacciones.
* [ ] Ampliar el sistema de comercio.
* [ ] Mejorar la interfaz.
* [ ] Incorporar nuevas funcionalidades.
* [ ] Documentar la arquitectura final.

---

## 📚 Contexto académico

Este proyecto se desarrolla como parte de la asignatura:

**Paradigmas de Programación**

Este Proyecto esta Realizado para la materia de Paradigmas de Programación, basados en el motor grafico de Godot

El desarrollo busca servir como una aplicación práctica de los conceptos estudiados durante la asignatura, especialmente aquellos relacionados con:

* Programación Orientada a Objetos.
* Diseño de software.
* Abstracción.
* Modularidad.
* Reutilización de código.
* Refactorización.
* Análisis de diferentes paradigmas de programación.

---

## 👤 Autor

**Esteban Présiga Posada**

Proyecto académico individual.

---

## 📄 Licencia

Este proyecto fue desarrollado con fines **académicos y educativos**.

La licencia y las condiciones de distribución podrán definirse posteriormente según los requerimientos del proyecto.
