<p align="right"><sub><a href="https://github.com/agustinyarrus/agustinyarrus/blob/main/README.md">English</a> · <b>Español</b></sub></p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/header-dark.svg">
  <img alt="Agustin Yarrus — desarrollador de software de Argentina. Software chico, rápido y sin dependencias. Me interesan el álgebra, la física, la geometría, los gráficos y el diseño minimalista. Go, C, C++, C#, JavaScript, TypeScript, Python, GLSL." src="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/header-light.svg" width="100%">
</picture>

Escribo software como me gusta la matemática: **chico, exacto y autocontenido**. Apps nativas de Windows que se miden en kilobytes, un motor de física en JavaScript puro, parsers de formatos de archivo sin ninguna biblioteca abajo — y cada afirmación verificada contra un oráculo independiente en vez de a ojo.

**~149.000 líneas** de código propio · **~48.000 líneas** de pruebas · **14** repos públicos · **5** de ellos se compilan sin nada más que una biblioteca estándar.

## Dónde vive la matemática

El álgebra, la física, la geometría, los gráficos y el diseño minimalista no son pasatiempos al lado de mi código — son la forma en que funciona. Seis figuras, cada una sacada de uno de mis repos:

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/figures-dark.svg">
  <img alt="Seis figuras: una restricción de distancia de XPBD (Carrona), IK analítica de dos huesos (Carrona), el zoom alrededor del cursor como una homotecia (Lux, Lumen), las ocho orientaciones EXIF como el grupo diedral D4 (Prisma), un código QR hecho por el codificador Reed–Solomon propio de clip2qr sobre GF(2^8) y un campo de flujo de Dijkstra que guía a una horda (Carrona)." src="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/figures-light.svg" width="100%">
</picture>

| | Dónde | La idea |
|:--|:--|:--|
| **Física** | [Carrona](https://github.com/agustinyarrus/carrona) | Ragdolls sobre mi propio solver XPBD — 7 subpasos por cuadro, restricciones con compliance, «músculos» PD con <i>k</i> = 1 − <i>e</i><sup>−130<i>h</i></sup> y un factor de amortiguamiento <i>ζ</i> ≈ 0,73 |
| **Geometría** | Carrona | Piernas ubicadas con IK analítica de dos huesos: la rodilla está donde se cortan dos círculos |
| **Álgebra lineal** | [Lux](https://github.com/agustinyarrus/lux) · [Lumen](https://github.com/agustinyarrus/lumen) | El zoom es una homotecia centrada en el cursor; las imágenes se vuelven pirámides de mipmaps que se dibujan a una escala que se mantiene en [½, 1] |
| **Álgebra abstracta** | [clip2qr](https://github.com/agustinyarrus/clip2qr) · [Prisma](https://github.com/agustinyarrus/prisma) | Reed–Solomon sobre GF(2⁸) y códigos BCH para QR; las 8 orientaciones EXIF como el grupo diedral <i>D</i><sub>4</sub> |
| **Ciencia del color** | [img](https://github.com/agustinyarrus/img) · Prisma · Lux | El YUV→RGB BT.601 en punto fijo de libwebp, reproducido bit a bit; RGB→XYZ a partir de las cromaticidades con adaptación de Bradford; tone mapping ACES |
| **Teoría de grafos** | [pdf-merge](https://github.com/agustinyarrus/pdf-merge) · [killport](https://github.com/agustinyarrus/killport) | Objetos PDF deduplicados como un DAG de Merkle en orden de Tarjan; bosques de procesos reconstruidos en <i>O</i>(<i>n</i>); campos de flujo de Dijkstra para las hordas |
| **Gráficos** | [Chainmate](https://github.com/agustinyarrus/chainmate) · Lux | El Forward+ de Godot reconstruido pasada por pasada en WebGL2 — sombras en cascada, SSAO, SSIL, niebla volumétrica, glow; mipmaps en mosaicos de GPU con Direct2D |
| **Métodos numéricos** | Chainmate · [vidsquash](https://github.com/agustinyarrus/vidsquash) | El redondeo de float32 reproducido exacto — hasta el recíproco inexacto de una GPU, <i>a</i>/<i>b</i> = <i>a</i>·rcp(<i>b</i>) — para que las partículas coincidan con el original hasta 2·10⁻⁶; clavar un tamaño de archivo exacto con el método de la secante sobre tamaño(bitrate) |
| **Diseño minimalista** | todos | Interfaces oscuras y sin marco; tamaños de letra redondeados a píxeles enteros del dispositivo; ClearType intacto |

## Proyectos destacados

| Proyecto | Qué es | Hecho con | Prueba |
|:--|:--|:--|:--|
| **[Chainmate](https://github.com/agustinyarrus/chainmate)** | Un roguelite de ajedrez hecho en Godot 4.7.2, reconstruido para la web y Android y verificado contra el `.exe` original | `JavaScript` `three.js` `WebGL2` `WASM` | 258 pruebas contra el oráculo · más de 28.000 glifos idénticos bit a bit |
| **[Carrona](https://github.com/agustinyarrus/carrona)** | Zombis vistos desde arriba, donde cada cuerpo es un ragdoll activo | `JavaScript` `three.js` `GLSL` | motor XPBD propio · 1.207 verificaciones físicas |
| **[killport](https://github.com/agustinyarrus/killport)** | Libera un puerto ocupado en Windows — proceso, servicio, contenedor o WSL — y demuestra que queda libre | `Go` `Win32/NT` | 0 dependencias · 613 pruebas |
| **[Lux](https://github.com/agustinyarrus/lux)** | Visor de imágenes nativo construido sobre pirámides de mipmaps en mosaicos de GPU | `C++17` `Direct2D` `WIC` | panorámica de 24.000 px a 57–60 fps |
| **[Prisma](https://github.com/agustinyarrus/prisma)** | Cualquier imagen → el PNG/APNG sin pérdida más chico, con la transparencia bien hecha | `C17` `WIC` | 13 decodificadores propios · 236 casos de punta a punta |
| **[Capcom](https://github.com/agustinyarrus/capcom)** | Control de misión para LLM locales | `C#` `WinForms/GDI` `llama.cpp` | ~560 KB · 0 paquetes NuGet |
| **[Folio](https://github.com/agustinyarrus/folio)** · **[Lumen](https://github.com/agustinyarrus/lumen)** · **[Cipher](https://github.com/agustinyarrus/cipher)** | Lector de Markdown, visor de imágenes y visor de código, oscuros y sin marco | `Go` `WebView2` | 127 formatos · más de 250 lenguajes |
| **[clip2qr](https://github.com/agustinyarrus/clip2qr)** · **[pdf-merge](https://github.com/agustinyarrus/pdf-merge)** · **[img](https://github.com/agustinyarrus/img)** · **[vidsquash](https://github.com/agustinyarrus/vidsquash)** | Herramientas de consola: codificador QR, unión de PDF, conversor de imágenes, video a un tamaño objetivo | `Go` | motores propios de QR y PDF · 0 dependencias |

### [Chainmate](https://github.com/agustinyarrus/chainmate) — el mismo juego, demostrado

`JavaScript` · `three.js` · `WebGL2` · `WebAssembly` · `AudioWorklet` · `Android`

Tomé un juego de Godot 4.7.2 ya publicado — un `.exe` de 110 MB, sin los archivos del proyecto — y lo reconstruí en JavaScript y three.js. El objetivo no era una remake parecida sino *el mismo juego*: las mismas semillas, los mismos cuadros, la misma interfaz, el mismo sonido, cada cosa medida contra el ejecutable original.

- **El original como oráculo.** El `.exe`, parcheado con un único hook, corre sondas de GDScript dentro del motor real y responde en JSON: cada malla, cada glifo y cada muestra de audio, el orden de cada `_process` y cada `await`, los render targets intermedios, las partículas leídas de vuelta desde la GPU. **258 pruebas** (~30 s, sin navegador) atan el port a esas respuestas.
- **La lógica, bit a bit.** Cinco partidas completas repetidas acción por acción, con el estado completo de PCG32 comparado después de cada paso — idénticas.
- **El texto, bit a bit.** FreeType 2.14.3 y HarfBuzz 14.2.0 — las versiones que trae Godot — compilados a WebAssembly con el clang de Zig: **más de 28.000 glifos idénticos**.
- **Los píxeles.** 34 de las 39 capturas del recorrido completo coinciden y otras 4 difieren en menos del 1 % de los píxeles; las capturas por etapa de render difieren apenas **0,006–0,016 / 255** en promedio en el cuadro final (≤ 0,12 en cualquier efecto por separado).

<details>
<summary><b>Por dentro</b></summary>

- **La semántica del motor, reimplementada:** el orden exacto de los cuadros del SceneTree, el `await` de GDScript como generadores de JavaScript, `hash()`, `str(float)`, el `sort_custom` estable y la matemática vectorial en float de 32 bits — que decide ramas como `size.x > size.z * 1.55` cuando se arma la arena.
- **Forward+, pasada por pasada:** sombras en cascada, SSAO, SSIL, niebla volumétrica, subsurface scattering, cielo, glow y tone mapping, cada uno comparado por separado contra los buffers intermedios del original (88 imágenes por corrida). Las pasadas de cómputo corren como pasadas de fragmentos; los volúmenes de niebla, como atlas de cortes filtrados.
- **Partículas de GPU en la CPU:** el compute shader de `GPUParticles3D` vuelto a correr en precisión simple y en el mismo orden — incluido el divisor de la GPU de referencia, donde `a / b` es `a × rcp(b)` con 169 recíprocos que no redondean bien (peor error: 2·10⁻⁶).
- **Audio:** los 24 efectos y la música, sintetizados exactos a la muestra; el mezclador de Godot (buses, limitador) corriendo en un AudioWorklet.
- **El detective:** una traza de estado comparada entre los dos programas ata cada valor aleatorio a la palabra exacta del generador de la que salió. Así encontré que el `randf()` global consume una palabra de PCG mientras que `RandomNumberGenerator.randf()` consume dos.
- **Piloto automático determinista:** el recorrido de capturas del propio juego, vuelto determinista (cuadros fijos de 1/60 s, RNG con semilla, sin entrada del escritorio) y corrido igual de los dos lados.
- **Paridad de rendimiento:** 39,5 / 44 / 39,5 ms por cuadro a 1600×900 en una gráfica Iris Xe, contra 38,6 / 44,1 / 38,1 ms del original.
- **Android:** Capacitor 6, targetSdk 36, con una prueba de humo en un emulador de API 36.

</details>

### Carrona — física de ragdolls desde cero

`JavaScript` · `three.js (sólo el render)` · `GLSL` · `Web Audio` · **sin paquetes de npm**

Un shooter de zombis visto desde arriba donde cada cuerpo en pantalla — el jugador incluido — es un **ragdoll activo**. No hay ni un solo clip de animación, archivo de textura o archivo de sonido en el repo: el movimiento sale de la física, las texturas del ruido, el sonido de un sintetizador.

- **Solver XPBD** sobre arreglos tipados planos: 7 subpasos por cuadro (<i>h</i> = 1/420 s a 60 fps), una pasada de Gauss–Seidel por subpaso, compliance ajustada por restricción (huesos 4·10⁻⁷, riostras del torso 2·10⁻⁶, límites articulares 2·10⁻⁵ m/N). Nada en `src/phys` importa three.js.
- **Músculos:** cada cuerpo son 16 partículas, 15 huesos y 48 restricciones (65 kg), llevados hacia una pose animada por control PD — <i>k</i> = 1 − <i>e</i><sup>−130<i>h</i></sup>, amortiguación 1,45√(<i>km</i>), así que <i>ζ</i> ≈ 0,73.
- **La marcha:** el ciclo avanza con la distancia recorrida, así que los pies apoyados no pueden patinar (medido: 0,18 m/s); vuelo con una Hermite cúbica; IK analítica de dos huesos; pasos de recuperación y caídas cuando el error de equilibrio cruza sus umbrales.
- **Números:** 40 ragdolls + 40 cajas + 12 cilindros simulados en 9 ms por cuadro; 56 fps en un Redmi Note 14 Pro. **1.207 verificaciones automáticas** en 19 suites miden magnitudes físicas — el patinaje del pie, el estiramiento de los huesos, las rodillas que se doblan al revés, qué tan quieto queda un cadáver.

<details>
<summary><b>Por dentro</b></summary>

- **Colisión:** esferas contra el piso, cajas rotadas en yaw y cilindros; huesos como cápsulas; fricción posicional (estática 0,92, dinámica 0,30); un hash espacial con celdas de 0,55 m y 16.384 cubetas; pruebas analíticas rayo–cápsula y rayo–caja para apuntar.
- **Estable por construcción:** restitución cero, topes de velocidad por subpaso, despenetración limitada al propio movimiento del subpaso más 8 mm, y una última pasada que vuelve a proyectar los huesos a su largo de reposo.
- **Cadáveres:** los cuerpos flojos reciben amortiguación de cuerpo rígido a partir del tensor de inercia completo de 3×3 — <i>ω</i> = <i>I</i><sup>−1</sup><i>L</i>, cada partícula llevada hacia <i>v</i><sub>cm</sub> + <i>ω</i> × <i>r</i> —, que mata el temblor sin matar el momento.
- **Límites articulares sin ángulos de Euler:** conos (rodillas 65°, codos 80°) en un marco del torso reconstruido a partir de las partículas por Gram–Schmidt.
- **Impactos:** impulsos repartidos a lo largo del hueso y con tope por partícula; los músculos alrededor de un impacto se aflojan durante 0,10–0,32 s; los tiros descentrados hacen girar el cuerpo según <i>r</i> × <i>J</i>.
- **Balística:** los cuerpos que caen predicen su tiempo de impacto <i>t</i> = (−<i>v</i> + √(<i>v</i>² + 2<i>gh</i>))/<i>g</i> y estiran las manos; los proyectiles apuntados resuelven el ángulo de salida con una forma que sigue siendo precisa cuando la gravedad es chica.
- **La horda:** un solo campo de flujo de Dijkstra (grilla de 0,4 m, mi propio heap binario) guía a todos los zombis; separación y flanqueo encima; los cuerpos lejanos se saltean la colisión detallada.
- **Render:** cuerpos instanciados; GLSL propio (gradación de color, un lote de sprites con quads alineados a la cámara, al rayo y a la superficie, el cono de la linterna); texturas procedurales sin costuras horneadas en Web Workers; cada shader compilado detrás del menú, así nada se traba en medio de la partida.
- **Contenido:** 104 armas modeladas proceduralmente (hitscan, rayos, rieles, relámpagos en cadena, proyectiles, chorros, ondas sónicas), 5 mapas, una campaña de 8 misiones más el modo infinito, 25 maneras de levantarse, 23 de caer, 21 sacudones.
- **Herramientas sin dependencias:** sin bundler; mi propio escritor de ZIP, codificador PNG/ICO, cliente del Chrome DevTools Protocol y cliente de subida a Google Play (con su propio JWT RS256). Se distribuye como PWA, como instalador de Windows y como APK de Android.

</details>

### killport — liberar un puerto, con cuidado

`Go` · `Win32 / NT API` · **cero dependencias** · un solo `.exe` de ~5 MB

Encuentra qué es lo que de verdad tiene tomado un puerto — un proceso, un servicio, un contenedor de Docker o Podman, un proceso de Linux dentro de WSL, una URL de `http.sys`, una regla de `portproxy` o una reserva de Windows —, lo cierra como lo haría una persona (primero Ctrl+C, la fuerza al final) y demuestra que el puerto queda libre.

- **Ninguna dependencia:** `go.mod` no tiene líneas `require`. 79 funciones de Win32/NT de 7 DLL están enlazadas a mano con `syscall.SyscallN` — sin `x/sys`, sin cgo — y cada DLL se carga desde una ruta absoluta de System32.
- **Un proceso es `{PID, momento de creación}`,** nunca un PID suelto, y su handle se mantiene abierto hasta que muere, así que un PID reciclado nunca puede matarse por error.
- **Escalada suave:** Ctrl+C inyectado en la propia consola del objetivo (`AttachConsole` + `GenerateConsoleCtrlEvent`, sólo si todos los procesos que comparten esa consola se pueden cerrar) → `WM_CLOSE` → `ControlService(STOP)` para los servicios → `TerminateProcess`, esperando sobre los handles en vez de consultar en bucle.
- **Pruebas, no esperanza:** el puerto tiene que quedar libre durante 350 ms — una ventana sacada de mediciones (un supervisor volvió a tomar un puerto en 241 ms; `wslrelay` lo suelta ~315 ms después de que se detiene un contenedor). Si algo vuelve a levantar el servidor, killport dice qué supervisor fue.
- **613 funciones de prueba:** 24,6 mil líneas de pruebas para 28 mil líneas de código.

<details>
<summary><b>Por dentro</b></summary>

- **Tablas de sockets:** `GetExtendedTcpTable` / `GetExtendedUdpTable` para IPv4 e IPv6, con las filas parseadas a mano; `GetOwnerModuleFrom*Entry` dice qué servicio se esconde dentro de un `svchost`.
- **Foto en una sola llamada:** `NtQuerySystemInformation`; las rutas de las imágenes sin abrir ni un proceso; la carpeta de trabajo de otro proceso, leída de su PEB (con soporte de WOW64) y convertida en un nombre de proyecto (`package.json`, `go.mod`, `Cargo.toml`, `pyproject.toml`, `.csproj`) y en una rama de git (`.git/HEAD`, sin necesitar git).
- **Bosque de procesos en <i>O</i>(<i>n</i>):** un vínculo con el padre cuenta sólo si el padre nació antes; una búsqueda del ancestro común más bajo entre las fotos de antes y de después encuentra al supervisor (nodemon, pm2…) que volvió a levantar un servidor.
- **Docker y Podman:** mi propio cliente HTTP/1.1 (content-length, chunked, leer hasta el cierre) sobre named pipes en modo overlapped abiertos con `SECURITY_IDENTIFICATION`, así un servidor de pipes falso no puede hacerse pasar por un killport elevado. El motor se encuentra por `DOCKER_HOST`, por el contexto activo de Docker o por los pipes por defecto.
- **WSL:** un script POSIX `sh` embebido lee `ss` o `/proc/net`, confirma el dueño por el inodo del socket y manda SIGINT → SIGTERM → SIGKILL, volviendo a verificar la hora de inicio antes de cada señal. Nunca arranca una distro.
- **Windows en cualquier idioma:** los parsers de `netsh` se anclan en la estructura — subrayados con guiones, sangría, SDDL —, nunca en las palabras.
- **Elevación blindada:** UAC con `ShellExecuteExW("runas")`; la copia elevada recibe una selección en una gramática cerrada en vez de comandos, vuelve a planificar desde su propia foto y escribe su resultado con `CREATE_NEW` y verificaciones de puntos de reanálisis.
- **Detección de impostores:** un nombre de proceso «de sistema» sólo cuenta si la imagen realmente es `System32\<name>` con el linaje de padres esperado (MITRE T1036.005).
- **Pruebas:** pruebas de propiedades con semilla contra implementaciones de referencia (30.000 líneas de comando contra `CommandLineToArgvW`, 500 bosques de procesos al azar…), un simulador de eventos discretos con reloj virtual, fixtures exactas al byte de salidas reales de Windows, y corridas de punta a punta del `.exe` real contra un registrante falso de `http.sys`, un motor de Docker falso, un `wsl.exe` falso y un servicio de prueba real.
- **Matemática en una CLI:** álgebra de conjuntos de intervalos para los rangos de puertos, anchos de columna por water-filling con búsqueda binaria, el «quisiste decir» con Damerau–Levenshtein, barras de progreso con resolución de 1/8 de celda.

</details>

### Lux — un visor de imágenes nativo

`C++17` · `Win32` · `Direct2D` · `DirectWrite` · `WIC` · `SSE2` · un solo `.exe` portable de ~860 KB

- **Pirámides de mipmaps en la GPU.** Cada imagen se reduce a la mitad con un filtro de caja de 2×2 en alfa premultiplicado (redondeo exacto, SSE2) y se corta en mosaicos de 2048 px con márgenes prestados de 8 px. El nivel que se dibuja mantiene la escala en pantalla dentro de [½, 1], lo que esquiva el límite de 16.384 px por bitmap de Direct2D: una **panorámica de 24.000 px se desplaza a 57–60 fps** y una foto de 48 MP se dibuja a 60 fps después de abrirse en 335–352 ms.
- **La imagen siguiente, al instante:** dos hilos decodificadores con sus propias fábricas de WIC y precarga en la dirección en que estás navegando — **0,3 ms** cuando ya está precargada; los JPEG se decodifican primero a escala 1/2–1/8 con el escalado de la DCT.
- **171 extensiones de archivo:** todo lo que decodifica WIC, RAW de cámaras, SVG, EMF/WMF, EXR/HDR, DDS/KTX/VTF (con mis propios decodificadores BC1–5), XCF de GIMP, FITS/DICOM y formatos retro (Amiga, Atari, C64, ZX Spectrum, PlayStation).

<details>
<summary><b>Por dentro</b></summary>

- **Presupuesto por cuadro:** 6 ms de subida de mosaicos por cuadro, del centro hacia afuera; los mosaicos que faltan se toman prestados de niveles más gruesos; un tope de 768 MB de GPU con desalojo LRU; el caché de imágenes dimensionado a 1/16 de la RAM.
- **Premultiplicación exacta:** (<i>t</i> + (<i>t</i> ≫ 8)) ≫ 8 con <i>t</i> = <i>c</i>·<i>a</i> + 128, verificada en los 65.536 pares.
- **Sin costuras:** una prueba recorre 400 escalas y desplazamientos al azar y verifica que cada columna de la pantalla la dibuje exactamente un mosaico.
- **Zoom:** una homotecia alrededor del cursor, ×1,18 por muesca de la rueda, con el origen ajustado a píxeles enteros para que el 100 % sea exacto al píxel; filtrado cúbico de alta calidad, vecino más cercano desde el 300 %.
- **Archivos HDR:** exposición a partir de un histograma de luminancia logarítmica → curva fílmica ACES → sRGB con una tabla de consulta.
- **Sin marco pero nativo:** `WM_NCCALCSIZE` / `WM_NCHITTEST` propios, `DwmExtendFrameIntoClientArea` para conservar la sombra del sistema, el modo oscuro y las esquinas redondeadas de DWM; un render target opaco para que ClearType siga nítido.
- **Dependencias:** sólo bibliotecas de un único header (stb_image, nanosvg, qoi, tinyexr); MSVC con `/O2 /GL` y `/LTCG /OPT:REF,ICF`.

</details>

### Prisma · image2png — la transparencia, bien hecha

`C17` · `clang-cl + LLD, full LTO` · `WIC` · una sola dependencia (libdeflate) · un solo `.exe` de ~800 KB

Convierte cualquier imagen en el PNG o APNG sin pérdida más chico, y entiende la transparencia como sea que la guarde el origen — canal alfa, color clave, alfa de paleta, máscara de 1 bit, color premultiplicado, color mateado sobre blanco, alfa auxiliar de AVIF/HEIC.

- **13 decodificadores propios** (PNG/APNG, GIF, BMP, ICO, TGA, PSD, DDS con BC1–BC7 y BC6H, QOI, PNM, farbfeld, SGI, PCX, Radiance HDR); todo lo demás por WIC, elegido por el contenido, nunca por la extensión.
- **Recuperación del alfa de AVIF/HEIC:** el códec de Windows descarta el ítem alfa, así que Prisma recorre él mismo las cajas ISOBMFF, reescribe `pitm` en una copia para que el mismo códec decodifique el plano alfa, lo alinea con la rotación y el espejado de la imagen, y lo despremultiplica.
- **Más rápido y más chico que Pillow:** un JPEG 4K → PNG en 843 ms / 2.231 KB (Pillow: 1.242 ms / 2.367 KB); un GIF de 72 cuadros → APNG en 113 KB (Pillow: 235 KB); una carpeta de capturas, 2,5× más rápido.

<details>
<summary><b>Por dentro</b></summary>

- **Color:** puntos de código de ITU-T H.273; RGB→XYZ derivado de las cromaticidades con adaptación de Bradford; el nuevo chunk `cICP` de PNG; y una corrección para el decodificador AV1 de Windows, que adivina la matriz YCbCr a partir de los primarios: <i>C</i> = <i>M</i><sub>declarada</sub><sup>−1</sup> <i>M</i><sub>709</sub>.
- **Codificador:** el tipo de color sin pérdida más chico; nueve estrategias de filtro por fila, tres de ellas compitiendo sobre una muestra de 16×8 filas; DEFLATE en trozos paralelos de 1 MB (al estilo pigz) con las sumas de verificación combinadas matemáticamente.
- **La matemática de la paleta:** los colores se comparan compuestos sobre negro *y* sobre blanco — una forma cuadrática definida positiva, así que k-means la minimiza exactamente: median cut → iteraciones de Lloyd → Floyd–Steinberg o Bayer 8×8.
- **Quitar el fondo:** el alfa es la proyección por mínimos cuadrados de cada píxel sobre la recta sujeto–fondo, con el color del sujeto expandido hacia afuera por BFS.
- **Simetría:** las 8 orientaciones EXIF como <i>D</i><sub>4</sub> — matrices enteras de 2×2 cuya inversa es su traspuesta (fig. 4).
- **Robustez:** un pool de hilos con bucles paralelos anidados, aislamiento SEH por archivo, entradas mapeadas en memoria desde los 64 MB, filtros AVX2 y un descompresor de rescate que recupera las filas legibles de los PNG truncados.
- **Pruebas:** 236 casos de punta a punta contra referencias exactas, Pillow/OpenCV y mi propio escritor de PNG de referencia — también bajo AddressSanitizer —, más pruebas unitarias y fuzzing por mutación.

</details>

### Capcom — control de misión para LLM locales

`C#` · `.NET Framework 4.8` · `WinForms, owner-drawn GDI` · `llama.cpp` · **0 paquetes NuGet** · un solo `.exe` de ~560 KB

Una consola de escritorio para modelos GGUF locales, con el estilo del control de misión del Apolo: arranca `llama-server`, recibe los tokens en streaming por SSE y dibuja cada píxel por su cuenta.

- **Streaming bien hecho:** un hilo de fondo agrega los tokens mientras la interfaz se repinta con un timer de 60 ms en vez de una vez por token; la diagramación del texto se cachea por ancho y por versión; la generación se puede cancelar en cualquier momento.
- **Telemetría:** tokens/s, tiempo hasta el primer token, uso de contexto y de memoria, un tablero GO/NO-GO; un benchmark de 20 preguntas en 9 categorías, con las respuestas de código ejecutadas en Node bajo `--permission` y con un límite de 10 s.
- **Todo hecho a mano:** renderizador de Markdown, resaltador de sintaxis, escritor de JSON, cliente SSE; descargas de Hugging Face que se reanudan con `Range` de HTTP y se verifican con SHA-256; el token de acceso cifrado con DPAPI; los tonos «Quindar» del Apolo (2525 / 2475 Hz) sintetizados en memoria.
- **Diseño:** casi negro `#07080b`, pasteles apagados, pesos de Cascadia elegidos según el tamaño final en píxeles, espaciado entre letras dibujado a mano (GDI no lo tiene), una grilla de papel milimetrado y barras de instrumentos segmentadas.

### Folio · Lumen · Cipher — una familia de apps silenciosas para Windows

`Go` · `WebView2` · `Win32 / DWM / COM` · 100 % sin conexión

Tres visores oscuros y sin marco sobre una misma arquitectura: un backend en Go en un puerto de loopback al azar, un frontend en WebView2, una ventana que nace sin marco (hook CBT + subclassing) y aun así conserva Aero Snap, sin destello blanco al arrancar, y traspaso a una única instancia.

- **[Folio](https://github.com/agustinyarrus/folio)** — un lector de Markdown para **127 extensiones de archivo** (JSON/JSON5, CSV con detección del delimitador, reST, AsciiDoc, Org, MediaWiki, docx, odt, epub y HTML, todos convertidos a Markdown). Extensiones propias de goldmark: matemática TeX, alertas de GitHub, `==mark==` `^sup^` `~sub~`, wikilinks de Obsidian resueltos por BFS sobre la bóveda, contenedores `:::` y abreviaturas reconocidas por un autómata **Aho–Corasick** escrito a mano. KaTeX y mermaid se cargan a demanda detrás de cachés LRU; la recarga en vivo te deja en el párrafo que estabas leyendo.
- **[Lumen](https://github.com/agustinyarrus/lumen)** — un visor de imágenes cuya ventana toma el tamaño de la foto antes de aparecer (lee sólo el encabezado); zoom alrededor del cursor, <i>t′</i> = <i>c</i> + (<i>t</i> − <i>c</i>)·<i>s′</i>/<i>s</i>, con pasos exponenciales de rueda <i>s</i>·<i>e</i><sup>−0.0015Δ<i>y</i></sup>; orden natural, precarga de las vecinas, fundidos.
- **[Cipher](https://github.com/agustinyarrus/cipher)** — un visor de código: más de 250 lenguajes con los lexers de chroma y mi propio formateador en streaming (idéntico byte a byte al HTML de chroma), los primeros 256 KB resaltados de entrada y el resto en tandas de 256 líneas por un trabajo de fondo que arrastra el estado del lexer de una tanda a la otra. De la 1.0 a la 1.1, un log de 12 MB pasó de **69 s a 0,1 s** y la detección del lenguaje de **66 s a 3 ms**. Los `.class` de Java se abren como código fuente gracias a CFR.
- **Tipografía:** cada tamaño de letra cae en un número entero de píxeles del dispositivo, con el peso un escalón más arriba en los tamaños chicos; Folio mantiene una capa de scroll opaca para que Chromium rasterice con ClearType en vez de con antialiasing gris (medido: 0 % de los píxeles de los glifos con color de subpíxel antes, 37–89 % después).

### Herramientas de consola para Windows

`Go` · un `.exe` cada una · una interfaz de terminal compartida y escrita a mano: paleta pastel de 24 bits, barras de progreso de 1/8 de celda, anchos que entienden CJK, `NO_COLOR`, sin códigos de escape cuando la salida va a un pipe.

- **[clip2qr](https://github.com/agustinyarrus/clip2qr)** — portapapeles → código QR en la terminal, con **mi propio codificador ISO/IEC 18004**: aritmética en GF(2⁸) módulo `0x11d` con tablas exp/log duplicadas, generadores de Reed–Solomon ∏<sub><i>i</i></sub> (<i>x</i> − <i>α</i><sup><i>i</i></sup>), versiones 1–40, modos numérico/alfanumérico/byte, niveles L–H, códigos de formato BCH(15,5) y de versión BCH(18,6), las 8 máscaras puntuadas con las 4 reglas de penalización; los medios bloques `▀▄█` dibujan dos módulos por celda de carácter. zxing-cpp decodifica **72 de 72** códigos del oráculo, versiones 1 a 40. Cero dependencias — el QR de la fig. 5 es su salida.
- **[pdf-merge](https://github.com/agustinyarrus/pdf-merge)** — **mi propio lector y escritor de PDF tolerante:** tablas y streams de xref, streams de objetos, actualizaciones incrementales, recuperación de xref rotas por escaneo, Flate con predictores PNG/TIFF, descifrado R2–R6 (RC4, AES-128/256, ISO 32000-2 Algoritmo 2.B); selección de páginas (`file.pdf@1-3,5`), marcadores, destinos con nombre y campos AcroForm unidos sin colisiones; **deduplicación como DAG de Merkle** — SHA-256 sobre una forma canónica en la que los hijos se reemplazan por sus hashes, en orden de Tarjan iterativo para que los ciclos no sean un problema. Verificado por un triple oráculo: qpdf, pypdf y un diff de píxeles con PDFium. Cero dependencias.
- **[img](https://github.com/agustinyarrus/img)** — un conversor de imágenes por lotes cuyos colores de WebP coinciden con **libwebp bit a bit**: un port de su YUV→RGB BT.601 en punto fijo de 14 bits y de su sobremuestreo de croma 9-3-3-1 (U y V empaquetados en un solo `uint32`, así una única suma interpola los dos), donde la conversión estándar de Go se desvía hasta 20 niveles. GIF animados compuestos según el método de disposición; un pool de workers de `NumCPU`. Sólo `golang.org/x/image`.
- **[vidsquash](https://github.com/agustinyarrus/vidsquash)** <sub>en curso</sub> — hace entrar un video bajo un límite de tamaño estricto (Discord, WhatsApp, Gmail…): un presupuesto de bitrate <i>R</i> = 8(<i>B</i> − <i>O</i>)/<i>d</i> con un modelo del overhead de MP4, una escalera de bits por píxel que elige la resolución y los cuadros por segundo, codificación en dos pasadas corregida con el método de la secante, tone mapping de HDR → SDR y una verificación con VMAF/SSIM. ffmpeg abajo, sin dependencias de Go.

## Cero dependencias, en números

| Proyecto | Líneas de código mío | Código de terceros | Lo que escribí a mano en su lugar |
|:--|--:|:--|:--|
| killport | 28,3 k de Go | **ninguno** — sólo la biblioteca estándar | 79 enlaces a Win32/NT, cliente HTTP/1.1, `net.Conn` sobre named pipes, parser de flags, interfaz de terminal |
| pdf-merge | 6,9 k de Go | **ninguno** | lexer, parser y escritor de PDF, descifrado, deduplicación de Merkle |
| clip2qr | 3,8 k de Go | **ninguno** | codificador QR, aritmética en GF(2⁸), Reed–Solomon, BCH |
| vidsquash | 3,9 k de Go | **ninguno** (ffmpeg en tiempo de ejecución) | planificador del control de bitrate, parseo de ffprobe, verificación de calidad |
| Capcom | 12,6 k de C# | **ninguno** — el .NET Framework que ya trae Windows | renderizador de Markdown, resaltador, escritor de JSON, cliente SSE, interfaz GDI |
| Carrona | 21,5 k de JS | three.js, para el render | motor XPBD, IK, campos de flujo, sintetizador, escritores de ZIP/PNG/ICO, cliente CDP |
| Prisma | 14,7 k de C | libdeflate | 13 decodificadores, codificador PNG/APNG, parser ISOBMFF, gestión de color, cuantizador |
| Lux | 6,1 k de C++ | stb_image, nanosvg, qoi, tinyexr | renderizador de mipmaps en mosaicos, decodificadores BCn/XCF/retro/científicos, SIMD |
| img | 3,8 k de Go | `golang.org/x/image` | color exacto al de libwebp, compositor de GIF, globbing |

<sub>Líneas no vacías, sin contar las pruebas ni el código vendorizado. Las cuatro herramientas de consola en Go comparten una capa de terminal de ~2,6 mil líneas.</sub>

## Cómo verifico

No miro a ojo: mido contra algo que ya sabe la respuesta.

| Proyecto | Oráculo |
|:--|:--|
| [Chainmate](https://github.com/agustinyarrus/chainmate) | el `.exe` original, respondiendo más de 20 sondas desde adentro del motor real — 258 pruebas |
| clip2qr | zxing-cpp, decodificando todas las versiones de la 1 a la 40 |
| img | libwebp, bit a bit — 18 de 18 casos de estrés |
| pdf-merge | la verificación estricta de qpdf, el orden del texto de pypdf y un diff de píxeles con PDFium |
| killport | salidas reales de Windows grabadas, `CommandLineToArgvW`, un simulador con reloj virtual — 613 pruebas |
| Carrona | mediciones físicas: patinaje del pie, estiramiento de los huesos, límites articulares — 1.207 verificaciones |
| Prisma | Pillow, OpenCV y un escritor de PNG de referencia, AddressSanitizer, fuzzing por mutación — 236 casos |
| Lux | exhaustivo donde se puede: los 65.536 pares de la premultiplicación, 400 disposiciones de mosaicos al azar |

## Stack

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/stack-dark.svg">
  <img alt="Mi stack como una tabla periódica de 64 elementos. Lenguajes: Go, C, C++, C#, JavaScript, TypeScript, Python, Java. Más lenguajes: PowerShell, GLSL, WebAssembly, SQL, POSIX sh, GDScript, HTML, CSS. Gráficos: Direct2D, DirectWrite, WIC, WebGL2, three.js, FreeType, HarfBuzz, SIMD. Windows: Win32, API nativa de NT, COM, DWM, WebView2, GDI/GDI+, Service Control Manager, named pipes. Sistemas: Docker Engine API, WSL, tablas TCP/UDP, http.sys, HTTP/1.1, Server-Sent Events, Job Objects, UAC. Web y móvil: Node.js, Vite, Web Audio, AudioWorklet, Web Workers, PWA, Chrome DevTools Protocol, Android. Formatos: PNG/APNG, WebP, AVIF/HEIF, PDF, QR, GIF, DEFLATE, EXR/HDR. Herramientas e IA: Git, GitHub Actions, MSVC, clang/LLD, Zig cc, AddressSanitizer, ffmpeg, llama.cpp. Veinte de los símbolos también son elementos químicos de verdad." src="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/stack-light.svg" width="100%">
</picture>

## Cómo construyo

- **Lo chico es una virtud.** El tiempo de arranque y el tamaño del binario se miden, no se adivinan.
- **Las dependencias se ganan su lugar.** Si lo puedo escribir bien — un codificador QR, un parser de PDF, un cliente HTTP/1.1 —, lo escribo.
- **Exacto le gana a parecido.** Colores exactos al bit, zoom exacto al píxel, audio exacto a la muestra, texto exacto al glifo.
- **Medir y después decidir.** Los timeouts, los umbrales y los tamaños de caché salen de mediciones, no de la costumbre.
- **Interfaces silenciosas.** Oscuras, sin marco, sin ruido — el contenido es la interfaz.

## Ahora

- Trabajando en servicios de backend y pipelines de CI/CD.
- Terminando **vidsquash** y agrandando la familia de herramientas nativas para Windows.

---

<sub>[LinkedIn](https://www.linkedin.com/in/ayarrus/) · Este README tampoco tiene dependencias: ni servicios de insignias ni rastreadores — cada imagen es un SVG hecho a mano en este repo, el código QR sale del codificador de clip2qr y la tela del encabezado está simulada con XPBD a 7 subpasos por cuadro, como Carrona.</sub>

<!-- i18n source=README.md sha256=17b8df7b98da -->
