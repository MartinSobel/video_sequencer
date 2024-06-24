# Video Sequencer

## Introduccion
¿Qué se evidencia al desmontar una obra audiovisual? En el transcurso del desarrollo de la humanidad, la necesidad de generar relatos fue algo que estuvo presente en todo momento. El uso de cortes en el cine ha evolucionado significativamente desde los primeros días del medio, pasando de simples trucos visuales a complejas técnicas narrativas y estilísticas que muchas veces retoman los elementos de las primeras rupturas de las vanguardias. Cada etapa en la historia del cine ha aportado nuevas ideas y enfoques al arte del montaje, haciendo del corte una herramienta fundamental para la narración cinematográfica.

Si analizamos el lenguaje audiovisual de hoy en día, podemos observar que hay una fuerte presencia en la utilización de cortes de una forma cada vez más excesiva en los procesos de montaje y edición. Los tiempos se aceleran, y la información llega en la menor cantidad de tiempo posible, generando una vertiginosa experiencia basada en una sucesión de imágenes dinámica y precisa. Los relatos cambian drásticamente.

La exploración desarrollada consiste en un patch de Pure Data que permite recorrer el tiempo de manera no lineal a través de saltos a frames previos. El mismo permite la posibilidad de generar efectos estroboscópicos y una sincronización por BPM generando así una pieza que podría ser también así utilizada en sincronía con algún elemento sonoro.

## Antecedentes
En la década de 1960, los efectos estroboscópicos se popularizaron en la música y el cine. "2001: A Space Odyssey" (1968), dirigida por Stanley Kubrick, es un ejemplo clásico del uso de efectos estroboscópicos. En la famosa secuencia de "Stargate", los efectos de luz y los patrones estroboscópicos crean una experiencia visualmente abrumadora que refleja el viaje interdimensional del protagonista. Las luces estroboscópicas se convirtieron en un elemento común en los conciertos, creando efectos visuales impactantes que se sincronizaban con la música.

En relación al proceso de manipulación de montaje, podemos referenciar a los siguientes artistas como fuente de inspiración para la exploración de saltos temporales dentro de un mismo archivo:
- Passage À L'Acte (1993), Martin Arnold | 11’ 29” | [Link](https://vimeo.com/398345542)
- Instructions for a Light & Sound Machine (2005), Peter Tscherkassky | 17’ | [Link](https://www.dailymotion.com/video/x2rbcyx)
- Kepko (2022), Sega Bodega | 3’ | [Link](https://youtu.be/CW5HeFHuJig)
Pensando en la cuestión de imágenes para generar un efecto estroboscópico, podemos pensar en estas referencias:
- Outer space (1999), Peter Tscherkassky | 10’ 26” | [Link](https://vimeo.com/314251447)
- Mothlight (1963), Stan Brakhage | 3’ | [Link](https://youtu.be/S5P5vkegmvU)

## El algoritmo
El patch está basado en un sistema que utiliza Gem para visualizar un video MP4 utilizando el componente `pix_movie`, que a través de un metrónomo controlado por BPM va generando saltos de frames previos (está seteado en -20 por default)

## Proximas etapas
Este proyecto es una simple prueba, pero a futuro sería ideal agregarle nuevos features que permitan crear piezas visuales de forma mas comoda y rapida, entre ellos:
- Posibilidad de cargar múltiples videos e iterar entre ellos de forma euclidiana
- Opción para obtener un render del output del procesamiento en un archivo nuevo  [research](https://forum.pdpatchrepo.info/topic/9836/gem-how-to-save-video)
- Carga y procesamiento de audio del video [research](https://forum.pdpatchrepo.info/topic/8940/manipulate-video-with-sound)

## Changelog
### V7
- UI intuitiva que permite elegir el archivo y la manipulación de parámetros a través de sliders
- Adaptacion a resolucion automatica 
- Sincronización vía OSC

## Instalacion
La versión de Pure Data en la que fue esto testeado es la `0.52.2`, pero debería funcionar en versiones futuras que soporten `Gem` sin problema.

## [Video DEMO](https://youtu.be/BZhYhMdDeig)
