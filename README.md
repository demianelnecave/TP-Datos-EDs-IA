El siguiente proyecto fue realizado en el marco de la materia Datos, Ecuaciones Diferenciales e Inteligencia Artificial dictada durante el 1° bimestre de 2026 por Facundo Sapienza. Aquí se encuentra el notebook donde se puede reproducir los experimentos realizados.

A continuación se tiene una descripción del proyecto en cuestión:

## Título del proyecto
Trayectorias del espacio latente de frames de videos de sistemas dinámicos a partir de una NODE
## Integrantes del grupo

- Demián Elnecavé (@demianelnecave)
- Agustín Rabinowicz (@Agusraba)

## Descripción

Buscamos, partiendo de una VAE entrenada sobre frames de videos sintéticos de algún sistema dinámico simple (resorte con damping, péndulo simple, pelota rebotando), calcular la trayectoria del espacio latente de los frames. 
‎
‎Con esto, intentamos usar esa trayectoria para:

- Comparar los frames generados por la VAE con sus correspondientes de la trayectoria y debatir si pueden mejorar la performance del modelo
‎
- Aumentar la fluidez del video y predecir frames faltantes
‎
‎- Averiguar si la NODE aprende la dinámica que subyace en el video, esto es si hay algún tipo de semejanza entre el espacio latente de trayectorias de embeddings y las trayectorias del sistema

## Dataset o problema a abordar

Utilizaremos datasets sintéticos de videos de resolución fija y fondo negro de los sistemas dinámicos, sampleando de una distribución las condiciones iniciales. 

## Método propuesto 

Un video representado en la computadora lleva a pensar muy naturalmente en una serie temporal, mientras que también se puede pensar como algo que en la vida real varía de forma contonua. Esto hace que creamos que el pase al "continuo" que da una NODE pueda ser una buena idea. Como los videos "esconden" una dinámica modelada por una ecuación diferencial, creemos interesante saber si la NODE puede llegar a aprenderla,  a pesar de estar recibiendo datos de mayor dimensionalidad como son los embeddings de los frames.


