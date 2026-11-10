# MADRIDPATINA · Hockey línea

Web del Club MadridPatina para sus equipos, jugadores y familias: la semana y los próximos partidos, el calendario, los equipos (senior y cantera), las ligas, los partidos con su acta y su previa, los jugadores, el legado del club desde 2016/17 y el directo de nuestros partidos.

- **Web:** https://raphasilvafran.github.io/madridpatina-web/
- **Quién está detrás:** el Club MadridPatina, de forma voluntaria y sin ánimo de lucro.
- **Contacto:** liga.hockey@madridpatina.com

## De dónde salen los datos

De las actas y fichas públicas de la Federación Madrileña de Patinaje (FMP) y, para las ligas nacionales, de la Real Federación Española de Patinaje. La web lo cita siempre como fuente. Cómo se calcula cada número está en la propia web, en [Cómo lo calculamos](https://raphasilvafran.github.io/madridpatina-web/#/metodo).

## Privacidad

Las reglas completas están en la página [Privacidad](https://raphasilvafran.github.io/madridpatina-web/#/privacidad) de la web. En resumen:

- **Menores de edad** (y quien no sabemos si es mayor de edad): solo el nombre de pila, la inicial de cada apellido y el dorsal (por ejemplo, «Hugo G. A. · #17»). Nunca su foto, su edad, su fecha de nacimiento ni su nacionalidad.
- **Mayores de edad:** nombre y apellidos, dorsal, equipo y sus números; a veces, la foto de su ficha y el año de nacimiento.
- **Si no quieres salir con tu nombre**, escribe a liga.hockey@madridpatina.com con tu nombre, equipo y dorsal. Desde la siguiente actualización sales como «Anónimo», solo con tu dorsal. Lo pueden pedir los propios jugadores y, en el caso de los menores, sus padres, madres o tutores.
- Antes de publicar, un control comprueba que no se escapa el nombre completo, la foto ni la edad de ningún menor; si encuentra algo, no se publica.
- Las visitas se cuentan con GoatCounter, sin cookies ni datos personales.

## Qué hay en este repositorio

Solo la web ya generada. **No se edita a mano:** la genera y la publica el proceso de actualización del proyecto privado `fmp_better_scout_beta` (`scripts/reporte/actualizar_web.py`), que sustituye cada vez todo menos este README y `.nojekyll`.

| Ruta | Qué es |
|---|---|
| `index.html`, `manifest.webmanifest` | La página (una sola, con rutas `#/…`) y su instalación como app en el móvil |
| `assets/` | El código (`app.js`, `directo.js`), los estilos, las fuentes, los iconos y los sonidos |
| `data/app.json` | Lo principal: semanas, ligas, equipos, partidos y jugadores de la temporada |
| `data/historico.json` | El legado del club desde 2016/17 |
| `data/mapa.json`, `data/analisis.json` | Mapa de jugadores y arquetipos; pronósticos y cómo juega cada equipo |
| `data/agenda.json`, `data/festivos.json`, `cal/*.ics` | Calendario, pistas y calendarios para añadir al móvil |
| `data/clubes.json`, `data/otras_ligas.json` | Clubes rivales y sus jugadores en otras ligas |
| `data/nacional.json`, `data/nacional_historia.json` | Liga nacional (Federación Española) |
| `data/pronosticos.json`, `data/hitos.json`, `data/tiros.json`, `data/pista.json`, `data/videos.json`, `data/venues_geo.json`, `data/servicio.json` | Pronósticos, hitos del directo, tiros, vídeos sincronizados y pistas |
| `data/adultos.json` | Quién es mayor de edad (solo adultos), para que el directo ponga nombre completo solo a ellos |
| `escudos/badge/` | Escudos de los clubes |
| `fotos/` | Fotos de jugadores, **solo de mayores de edad** |

El directo, los avisos de Telegram y los apodos van aparte, en un servicio de Vercel (`madridpatina-directo`), que aplica las mismas reglas de privacidad.
