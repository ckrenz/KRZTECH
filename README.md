# KRZTech Landing

Landing institucional y comercial de KRZTech. Presenta la empresa, sus
productos y el canal de contacto para solicitar una demostración.

> **Estado productivo:** el sitio está publicado mediante Vercel. Todo cambio
> debe realizarse en una rama y revisarse mediante Pull Request antes de llegar
> a `main`. El repositorio no requiere build ni contiene lógica de backend.

## Objetivo

La landing debe transmitir una propuesta sencilla:

> Software práctico para que comercios y PyMEs vendan, controlen y trabajen con
> menos complejidad.

El objetivo principal no es describir tecnología, sino generar confianza,
explicar los productos con claridad y convertir visitas en consultas o
solicitudes de demostración.

## Productos de KRZTech

La comunicación institucional se concentra actualmente en:

### MiCaja

Sistema de punto de venta y gestión comercial para ventas, caja, productos,
stock, compras, clientes y reportes.

- **MiCaja Escritorio / Local:** orientada a una computadora o comercio que
  necesita operar aun con conectividad limitada.
- **MiCaja Web / Online:** permite acceso desde distintos dispositivos,
  información centralizada y operación con múltiples usuarios o cajas.

La aplicación web se presenta en `https://micaja.krztech.online`.

### Pedidos360

Solución para equipos comerciales con vendedores en calle. El flujo comunicado
es:

```text
Vendedor → Administración → Depósito
```

El vendedor carga el pedido desde el celular, administración lo recibe y
controla, y depósito continúa con la preparación.

La captura de Pedidos360 incluida en la landing es una **vista ilustrativa** y
no debe presentarse como una captura contractual o como evidencia de funciones
que todavía no hayan sido verificadas.

## Alcance de la marca

No presentar como productos existentes de KRZTech servicios o sistemas que no
estén aprobados. En particular, no agregar por iniciativa propia APIs,
helpdesk, BI, n8n, CRM u otros desarrollos internos como si fueran productos
comerciales.

Las soluciones a medida pueden mencionarse como capacidad general, sin afirmar
funciones, integraciones, precios, clientes o resultados no comprobados.

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
- `assets/micaja-punto-venta.png`: captura real del punto de venta; debe
  permanecer anonimizada.
- `assets/pedidos360-demo.png`: representación ilustrativa de Pedidos360.

Vercel debe servir `KrzTech/Landing` como directorio raíz del sitio. El archivo
de entrada debe llamarse exactamente `index.html`; no subir versiones con
nombres alternativos al directorio productivo.

## Identidad visual

La nueva landing es la fuente de verdad para futuras piezas de comunicación.

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
- no inventar isotipos, monogramas o logos alternativos;
- priorizar fondos crema, azul marino y acentos naranjas;
- usar capturas grandes, legibles y con poco margen vacío;
- mantener una estética clara, editorial y profesional;
- evitar diseños genéricos de “tecnología futurista”, exceso de neón o textos
  pequeños.

## Contenido y conversiones

Las llamadas a la acción principales son:

- solicitar una demo;
- conocer MiCaja;
- conocer Pedidos360;
- conversar por WhatsApp.

Antes de publicar, revisar:

- número y enlaces de WhatsApp;
- usuario y enlace de Instagram;
- dominio de MiCaja;
- títulos, metadescripción y Open Graph;
- que las afirmaciones correspondan a funciones reales;
- que no haya nombres, emails o datos personales en las capturas.

No publicar precios, métricas, clientes, testimonios o promesas de resultados
sin aprobación explícita.

## Desarrollo local

El sitio es estático. Desde la raíz del repositorio:

```bash
cd KrzTech/Landing
python3 -m http.server 8080
```

Abrir `http://127.0.0.1:8080`.

No abrir únicamente el archivo con `file://` para la validación final: usar un
servidor local permite comprobar las rutas relativas de los recursos.

## Verificación antes de publicar

Comprobar como mínimo:

- carga de las tres imágenes;
- navegación de todos los enlaces internos;
- apertura correcta de WhatsApp, Instagram y MiCaja;
- textos alternativos de las imágenes;
- legibilidad en escritorio y móvil;
- ausencia de desbordamiento horizontal;
- tamaño adecuado de botones y capturas;
- metadatos SEO y sociales;
- consola del navegador sin errores.

Si se usa un validador HTML, distinguir problemas estructurales de reglas de
estilo opcionales, como el formato de etiquetas vacías o estilos inline ya
existentes.

## Publicación segura

1. Actualizar `main`.
2. Crear una rama nueva.
3. Modificar `KrzTech/Landing/index.html` o sus recursos.
4. Probar localmente en escritorio y móvil.
5. Subir la rama y abrir un Pull Request contra `main`.
6. Revisar la vista previa de Vercel.
7. Fusionar únicamente después de aprobar la vista previa.
8. Confirmar que Vercel creó un despliegue de producción para `main`.

Si el merge no genera un nuevo despliegue de producción:

1. comprobar en Vercel que **Production Branch** sea `main`;
2. verificar que el directorio raíz sea `KrzTech/Landing`;
3. como acción puntual, promover la vista previa aprobada a producción.

No confundir un despliegue **Preview** de una rama con el despliegue
**Production**.

## Contexto para futuras modificaciones

Revisar en este orden:

1. este README;
2. `KrzTech/Landing/index.html`;
3. las imágenes de `KrzTech/Landing/assets`;
4. la vista previa responsive;
5. la configuración del proyecto en Vercel.

Decisiones ya tomadas:

- la rama productiva es `main`;
- la landing se despliega en Vercel;
- MiCaja y Pedidos360 son los productos centrales;
- MiCaja debe comunicar sus modalidades de escritorio y web;
- Pedidos360 debe describirse mediante su flujo comercial;
- la identidad usa azul marino, crema y naranja;
- no deben inventarse logos, funciones o pruebas sociales;
- las capturas de MiCaja deben ser reales y estar anonimizadas;
- la captura de Pedidos360 debe identificarse como ilustrativa.

## Licencia

Antes de distribuir o reutilizar el proyecto fuera de KRZTech, definir y agregar
una licencia.
