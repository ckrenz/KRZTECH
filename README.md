# KRZTech Landing

Landing institucional y comercial de KRZTech. El sitio presenta la empresa, sus productos principales y el canal de contacto para solicitar una demostración.

> **Estado productivo:** publicado mediante Vercel. Todo cambio debe realizarse en una rama, validarse mediante Pull Request y recién después llegar a `main`. El proyecto es estático: no requiere build ni backend.

## Objetivo

La landing debe explicar de forma simple qué resuelve KRZTech y convertir visitas en consultas.

La comunicación principal se apoya en dos productos estrella:

### MiReserva

Sistema de gestión para hosterías, hoteles pequeños y otros alojamientos.

Funciones que pueden comunicarse públicamente:

- disponibilidad y calendario por habitación;
- reservas de una o varias habitaciones;
- huéspedes, check-in y check-out;
- pagos, devoluciones, saldos y comprobantes internos;
- habitaciones, limpieza, bloqueos e incidentes;
- tarifas base y períodos especiales;
- comunicaciones de llegada y agradecimiento por WhatsApp o email;
- alertas operativas y comunicaciones pendientes.

La landing usa una **vista demostrativa construida en HTML/CSS con datos ficticios** para mostrar el dashboard de MiReserva. Debe permanecer identificada como “Datos de ejemplo” y no presentarse como información de un cliente real.

Aplicación: `https://mireserva.krztech.online`.

### MiCaja

Sistema de punto de venta y gestión comercial para ventas, productos, stock, precios, caja y reportes.

- **MiCaja Local:** orientada a una computadora o comercio que necesita operar aun con conectividad limitada.
- **MiCaja Online:** permite acceso desde distintos dispositivos, información centralizada y operación con múltiples usuarios o cajas.

Aplicación web: `https://micaja.krztech.online`.

### Pedidos360

Pedidos360 se mantiene como producto secundario dentro de la landing. Su propuesta es ordenar el flujo:

```text
Vendedor → Administración → Depósito
```

La imagen incluida es una **vista ilustrativa** y no debe presentarse como una captura contractual ni como prueba de funciones no verificadas.

## Alcance de la marca

No presentar como productos existentes servicios o sistemas que no estén aprobados. Las soluciones a medida pueden mencionarse como capacidad general, sin inventar funciones, clientes, métricas, precios o resultados.

## Estructura

```text
KrzTech/
  Landing/
    index.html
    assets/
      micaja-dashboard.png
      micaja-punto-venta.png
      pedidos360-demo.png
```

- `KrzTech/Landing/index.html`: sitio completo, con HTML, CSS y JavaScript.
- `assets/micaja-dashboard.png`: captura real del dashboard de MiCaja.
- `assets/micaja-punto-venta.png`: captura real del punto de venta.
- `assets/pedidos360-demo.png`: representación ilustrativa de Pedidos360.
- MiReserva no depende de una imagen externa: su dashboard demostrativo está construido dentro del HTML para mostrar datos ficticios de forma segura.

Vercel debe servir `KrzTech/Landing` como directorio raíz y `index.html` como archivo de entrada.

## Identidad visual

| Uso | Valor |
| --- | --- |
| Azul marino principal | `#0f2444` |
| Azul secundario | `#1a4a8a` |
| Naranja | `#df7b2c` |
| Fondo crema | `#faf8f4` |
| Texto principal | `#191714` |
| Texto secundario | `#746d62` |
| Tipografía de títulos | Instrument Serif |
| Tipografía general | DM Sans |

Reglas:

- usar la marca escrita **KRZTech** con el tratamiento existente;
- priorizar MiReserva y MiCaja en el hero, la sección de productos y el footer;
- mantener fondos crema, azul marino y acentos naranjas;
- usar capturas o demos grandes, legibles y con poco margen vacío;
- evitar estética genérica de “tecnología futurista”, neón o textos demasiado pequeños;
- identificar claramente cualquier dato ficticio o imagen ilustrativa.

## Contenido y conversiones

CTA principales:

- solicitar una demo de MiReserva;
- conocer MiCaja;
- solicitar una demo general;
- conversar por WhatsApp.

Antes de publicar, revisar:

- número y enlaces de WhatsApp;
- usuario y enlace de Instagram;
- dominios de MiReserva y MiCaja;
- títulos, metadescripción y Open Graph;
- que las afirmaciones correspondan a funciones reales;
- que las capturas no contengan datos personales reales;
- que la demo de MiReserva siga rotulada como datos de ejemplo.

No publicar precios, métricas, clientes, testimonios o promesas de resultados sin aprobación explícita.

## Desarrollo local

```bash
cd KrzTech/Landing
python3 -m http.server 8080
```

Abrir `http://127.0.0.1:8080`.

## Verificación antes de publicar

Comprobar como mínimo:

- carga de las tres imágenes existentes;
- correcta visualización del dashboard demostrativo de MiReserva;
- navegación interna;
- enlaces a WhatsApp, Instagram y MiCaja;
- legibilidad en escritorio y móvil;
- ausencia de desbordamiento horizontal;
- tamaño adecuado de botones y textos;
- metadatos SEO y sociales;
- consola del navegador sin errores.

## Publicación segura

1. Actualizar `main` local o remotamente.
2. Crear una rama nueva.
3. Modificar `KrzTech/Landing/index.html` y, si corresponde, este README.
4. Validar escritorio y móvil.
5. Abrir Pull Request contra `main`.
6. Revisar la vista previa de Vercel.
7. Fusionar únicamente después de aprobar la vista previa.
8. Confirmar el despliegue de producción de `main`.

Si el merge no genera un despliegue de producción, comprobar en Vercel que **Production Branch** sea `main` y que el Root Directory sea `KrzTech/Landing`.

## Decisiones vigentes

- la rama productiva es `main`;
- la landing se despliega en Vercel;
- **MiReserva y MiCaja son los dos productos principales**;
- Pedidos360 queda como producto secundario;
- MiReserva se muestra con una demo HTML/CSS con datos ficticios;
- MiCaja usa capturas reales anonimizadas;
- Pedidos360 usa una imagen ilustrativa;
- la comunicación debe vender resultado y simplicidad, no tecnología por sí sola.

## Licencia

Antes de distribuir o reutilizar el proyecto fuera de KRZTech, definir y agregar una licencia.
