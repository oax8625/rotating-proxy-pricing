# proxy rotativo: qué es, cuánto cuesta y cómo elegir uno que no te bloquee

Buscar "proxy rotativo" lleva a dos sitios distintos. Uno es la persona que quiere entender qué hace exactamente y por qué su scraper sigue comiéndose captchas. El otro es el que ya lo entendió y quiere saber cuánto debería pagar por GB sin que le vendan humo. Este artículo cubre las dos cosas, y termina con precios concretos de un proveedor que publica sus tarifas sin obligarte a hablar con ventas.

## Qué es un proxy rotativo y cómo cambia la IP

Un proxy rotativo es un intermediario que no usa siempre la misma dirección IP de salida. Cada vez que abres una conexión, el tráfico sale por una IP distinta tomada de un pool grande. Para el sitio de destino, tus 500 peticiones seguidas parecen venir de 500 dispositivos repartidos por distintos barrios, no de un único servidor insistiendo en la misma puerta.

Hay dos formas de rotar y conviene no confundirlas:

- **Rotación por solicitud.** Cada conexión nueva recibe una IP nueva. Es lo que quieres para crawling de alto volumen, seguimiento de SERP o comprobaciones de precios repetidas.
- **Rotación temporizada.** La misma IP se mantiene durante una ventana definida y luego se sustituye. Útil cuando el sitio necesita cierta continuidad, pero sin quedarse fijado para siempre.

La rotación casi nunca se apoya en IP de datacenter, y ahí está el detalle que explica los precios. Las subredes de datacenter son conocidas y los sistemas anti-bot las bloquean en bloque. Por eso la rotación seria se construye sobre proxies residenciales o móviles: direcciones que corresponden a conexiones domésticas reales y que, por tanto, no llevan la etiqueta de "esto es un robot".

## Rotativo, sticky o estático: cuál te toca

Los tres se venden juntos y se usan en situaciones distintas. Elegir mal es la forma más rápida de gastar presupuesto en reintentos.

| Necesidad | Tipo que funciona | Por qué |
| --- | --- | --- |
| Scraping y monitorización de gran volumen | Residencial rotativo | Cada solicitud sale por una IP nueva; los bloqueos se reparten y bajan |
| Comprobación de SERP y anuncios por país | Residencial rotativo con geo-targeting | Necesitas IP de consumidor real en la región correcta |
| Inicios de sesión y flujos de varios pasos | Sesión sticky | La IP se mantiene; rotar a mitad de sesión rompe el login |
| Objetivos con anti-bot agresivo (apps, operadores) | Móvil rotativo | Las IP de operador 4G/5G son difíciles de marcar incluso compartidas por NAT |
| Scraping de páginas sin protección | Datacenter | Es el nivel más barato y no necesitas reputación de IP |

Una advertencia sobre la palabra "estático": cada proveedor la implementa a su manera. Hay quien vende sesiones sticky (una IP rotativa retenida unos minutos) llamándolas estáticas, y hay quien vende ISP realmente fijas. Si tu proyecto necesita una IP permanente asignada a ti, comprueba antes de pagar qué está comprando exactamente.

## Cuánto cuesta un proxy rotativo hoy

El rango razonable de mercado para residencial rotativo se mueve entre 1 y 8 dólares por GB. Por debajo de 1 $/GB conviene desconfiar: casi siempre es datacenter reetiquetado, tráfico que caduca al mes o un pool tan pequeño que se agota y te bloquea.

| Tipo de proxy | Modelo habitual | Rango razonable | Para qué |
| --- | --- | --- | --- |
| Residencial rotativo | Por GB | ~1–8 $/GB | Objetivos protegidos: e-commerce, SERP, redes |
| Móvil 4G/5G | Por GB | ~2–15 $/GB | Objetivos más difíciles, datos de apps |
| Datacenter | Por GB o por IP/mes | ~0,50–3 $/GB | Objetivos sin protección, velocidad |
| ISP estático | Por IP/mes | ~1,50–5 $/IP/mes | Identidad fija por cuenta |

El precio de etiqueta, sin embargo, no es el precio real. Dos cosas lo distorsionan: el tráfico que compras y no usas antes de que caduque, y las solicitudes que fallan. Un pool de 0,50 $/GB que se bloquea la mitad de las veces sale más caro por dato útil que uno de 1 $/GB limpio.

## Cómo funciona el modelo de precios de DataImpulse

DataImpulse es un proveedor de proxies residenciales, móviles, de datacenter y residenciales premium con un pool anunciado de más de 90 millones de IP en 195 países. Lo que lo hace distintivo no es el tamaño del pool, es la facturación.

Cobra por uso, desde 1 $/GB en residencial (0,50 $/GB en datacenter, 2 $/GB en móvil), sin suscripción, y **el tráfico que compras no caduca**. La compra mínima es de 5 dólares. Eso significa que puedes recargar 5 GB para probar una idea y volver tres meses después sin haber perdido nada, algo poco habitual en un mercado donde los GB no usados suelen desaparecer a fin de mes.

Qué entra en ese precio:

- **Segmentación por país incluida** en la tarifa base, con opción de seleccionar o excluir países.
- Sesiones **rotativas y sticky** en el mismo producto.
- Protocolos **HTTP, HTTPS y SOCKS5**.
- Soporte humano 24/7 y whitelisting de IP o autenticación usuario:contraseña.

Qué se paga aparte:

- La segmentación avanzada —ciudad, estado, código postal y ASN— es un complemento de pago en los planes residenciales. La propia guía de precios del proveedor lo plantea así: el targeting fino solo lo pagas si de verdad lo necesitas.
- No hay plan gratuito. Todo empieza con los 5 dólares mínimos.

Sobre devoluciones: los planes de entrada incluyen garantía de reembolso de 7 días para pagos con tarjeta, siempre que no se haya consumido más del 80 % del tráfico. Las compras en criptomoneda sobre esos planes de entrada no son reembolsables.

## Todos los planes de DataImpulse, comparados

Estos son los paquetes publicados actualmente, agrupados por tipo de proxy. No hay suscripción en ninguno: el modelo es pago por uso con créditos que se acumulan.

| Tipo | Plan | Tráfico | Precio | Tarifa por GB | Enlace |
| --- | --- | --- | --- | --- | --- |
| Residencial | Intro | 5 GB | $5 | $1,00 | [Empezar con el plan residencial de 5 GB](https://bit.ly/dataimPulse) |
| Residencial | Basic | 50 GB | $50 | $1,00 | [Ver el paquete residencial de 50 GB](https://bit.ly/dataimPulse) |
| Residencial | Standard | 100 GB | $100 | $1,00 | [Consultar el plan residencial de 100 GB](https://bit.ly/dataimPulse) |
| Residencial | Advanced | 1 TB | $800 | $0,80 | [Ver tarifa de volumen residencial 1 TB](https://bit.ly/dataimPulse) |
| Datacenter | Intro | 10 GB | $5 | $0,50 | [Probar proxies de datacenter desde $5](https://bit.ly/dataimPulse) |
| Datacenter | Basic | 100 GB | $50 | $0,50 | [Ver el paquete datacenter de 100 GB](https://bit.ly/dataimPulse) |
| Datacenter | Standard | 500 GB | $250 | $0,50 | [Consultar el plan datacenter de 500 GB](https://bit.ly/dataimPulse) |
| Datacenter | Advanced | 1 TB | $450 | $0,45 | [Ver tarifa datacenter de 1 TB](https://bit.ly/dataimPulse) |
| Móvil | Intro | 2,5 GB | $5 | $2,00 | [Empezar con proxies móviles 4G/5G](https://bit.ly/dataimPulse) |
| Móvil | Basic | 25 GB | $50 | $2,00 | [Ver el paquete móvil de 25 GB](https://bit.ly/dataimPulse) |
| Móvil | Advanced | 1 TB | $1.600 | $1,60 | [Consultar tarifa móvil por volumen](https://bit.ly/dataimPulse) |
| Residencial premium | Intro | 1 GB | $5 | $5,00 | [Probar el pool residencial premium](https://bit.ly/dataimPulse) |
| Residencial premium | Basic | 10 GB | $50 | $5,00 | [Ver el plan premium de 10 GB](https://bit.ly/dataimPulse) |
| A medida | Residencial / móvil / datacenter | Desde 5 TB | Desde $2.250 (datacenter), $8.000 (móvil), $20.000 (premium) | Precio negociado | [Solicitar plan a medida](https://bit.ly/dataimPulse) |

Los descuentos por volumen del 20 % aplican a partir de 1 TB en residencial y móvil, y son los que bajan la tarifa a 0,80 $/GB y 1,60 $/GB respectivamente. En datacenter el 1 TB ya cuesta 450 $ por defecto, un 10 % menos que la tarifa estándar.

### Cómo se configura la rotación

La rotación no se programa: viene puesta por defecto. Estas son las piezas que necesitas conocer al montar la conexión:

- **HTTP/HTTPS rotativo** funciona en el puerto **823**; **SOCKS5 rotativo**, en el puerto **824**. Cada nueva solicitud por ahí sale con una IP distinta.
- Las **sesiones sticky** usan puertos entre el 10000 y el 20000 y duran de 1 a 120 minutos. Si no indicas intervalo, o lo dejas en 0, el valor por defecto es de 30 minutos.
- La ubicación se elige en las credenciales. El formato habitual es añadir el país al usuario o a la contraseña, y lo mismo con la ciudad cuando la segmentación avanzada está activa.
- Si integras con Python, Playwright o Puppeteer, definir el servidor y las credenciales es suficiente; no hay que gestionar una lista de IPs a mano.

Para la mayoría de proyectos de scraping, la combinación ganadora es el endpoint rotativo para la recolección masiva y una sesión sticky puntual cuando el flujo requiere login o carrito. Pagar tráfico residencial para páginas abiertas, o móvil para lo que resuelve una IP doméstica, es la forma más silenciosa de inflar la factura.

## El coste real: precio por solicitud exitosa

Hay una fórmula sencilla para saber si un proxy es barato de verdad:

> Coste efectivo $/GB = (tarifa de etiqueta ÷ tasa de éxito) + desperdicio por caducidad + complementos de pago

Un pool de 1 $/GB con 99 % de éxito y sin caducidad se queda cerca de 1,01 $/GB efectivos. Un pool de 0,50 $/GB que falla en el 45 % de los intentos y además caduca mensualmente supera los 1,20 $/GB reales, sin contar el tiempo de ingeniería perdido en reintentos.

DataImpulse publica una tasa de éxito del 99,51 % y no caduca tráfico, así que los dos multiplicadores que suelen romper el cálculo se quedan cerca de 1. La parte que puede subir el coste efectivo es la segmentación avanzada: si necesitas filtrar por ciudad, ZIP o ASN en residencial, la tarifa base deja de ser la tarifa final.

## Lo que no te da DataImpulse

Merece la pena decirlo antes de comprar, porque son limitaciones reales y no letra pequeña:

- **No vende ISP estático permanente.** Ofrece sesiones sticky, que es una IP rotativa retenida hasta 120 minutos, no una dirección fija asignada a ti indefinidamente. Si tu flujo necesita una IP residencial inmutable durante días, este no es el proveedor.
- **El pool no es el más profundo del mercado.** Una prueba independiente de Shifter, que es competidor y lo declara, midió 172.893 IP activas en cinco países frente a las 306.410 de su propia red, con 1.526 operadores distintos frente a 2.441. En volumen medio sobre objetivos comunes eso no te va a molestar; con volúmenes altos o sitios con defensas fuertes, empezarás a ver direcciones repetidas.
- **No hay SLA empresarial ni nivel de soporte corporativo**, ni tampoco prueba gratuita: el punto de entrada siempre son 5 dólares.
- **La rotación no llega al nivel de operador** (no hay segmentación por ISP dentro del pool), algo que sí ofrecen proveedores de gama más alta.

## Qué dicen las pruebas y los usuarios

Más allá del marketing, esto es lo verificable:

- En G2, la ficha del proveedor acumula 28 reseñas con una media de 4,7 sobre 5. Los comentarios recurrentes son el precio por GB, la facilidad de configuración con navegadores antidetect y la respuesta del soporte. Un usuario de scraping en Python destacó la documentación de API y el fin de las prohibiciones de IP que tenía con otros proveedores.
- En Trustpilot la puntuación registrada por terceros es de 4,6 sobre 5.
- En la prueba comparativa de latencia, las medianas de DataImpulse quedaron entre 430 y 501 ms, por delante de varias redes que cuestan tres veces más, con una tasa de éxito medida del 99,6 %.

Las críticas que aparecen son consistentes y no sorprenden: consumo de tráfico que se agota antes de lo esperado si el scraper no está optimizado, y una oferta de valor que resulta menos atractiva cuando el volumen pasa de 1 TB al mes.

## Preguntas frecuentes

**¿Hay plan gratuito o prueba sin pagar?**
No. El acceso empieza con una compra mínima de 5 dólares. Los planes de entrada sí incluyen 7 días de garantía de reembolso con tarjeta si has consumido menos del 80 % del tráfico; con cripto no aplica.

**¿El tráfico caduca si no lo uso?**
No. Los GB comprados se quedan en tu cuenta hasta que los gastas. Es la diferencia práctica frente a las suscripciones mensuales que se pierden a fin de mes.

**¿Puedo rotar y quedarme con la misma IP en la misma sesión?**
Sí. El endpoint rotativo cambia de IP en cada solicitud, y la sesión sticky mantiene una dirección entre 1 y 120 minutos. Con esta segunda opción se cubren logins y flujos de varios pasos, pero no una identidad permanente.

**¿Qué pasa con el geo-targeting por ciudad o código postal?**
El país está incluido en la tarifa base. Ciudad, estado, ZIP y ASN se facturan como complemento. Si tu proyecto solo necesita "IP de México" o "IP de España", pagas la tarifa estándar y ya.

**¿Sirve para rastrear SERP a escala?**
Es uno de sus casos de uso habituales: residencial rotativo con segmentación por país mantiene la tasa de éxito lo bastante alta como para que el coste por resultado siga siendo bajo. Para eso, el plan residencial de entrada es el punto de partida razonable.

## Con qué empezar

Si llegaste aquí para entender qué es un proxy rotativo, la versión corta: es una puerta de salida que cambia de identidad, y su valor depende por completo de la calidad del pool que hay detrás. Si llegaste para comprar, el cálculo es más aburrido de lo que parece: mira el precio por GB, mira si el tráfico caduca, mira qué targeting entra en la tarifa y mide después cuánto te cuesta cada solicitud que sí devuelve datos.

Con 1 $/GB residencial, sin suscripción y con créditos que no expiran, DataImpulse resuelve bien el arranque y el uso irregular: puedes empezar con 5 GB, quejarte o alegrarte, y escalar solo cuando los números lo justifiquen. Lo que no vas a encontrar ahí es una IP estática permanente ni el pool más profundo del mercado, y para según qué proyectos eso es exactamente lo que hace falta saber antes de pagar.

👉 [Ver los planes actuales de proxies rotativos de DataImpulse](https://bit.ly/dataimPulse)
