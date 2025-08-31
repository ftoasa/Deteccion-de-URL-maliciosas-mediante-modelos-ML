# Detección de URL maliciosas mediante modelos de aprendizaje automático

## Contexto
    Las URL maliciosas o sitios web maliciosos representan una grave amenaza para la ciberseguridad. Albergan contenido no solicitado (spam, phishing, descargas no autorizadas, etc.) y atraen a usuarios desprevenidos a ser víctimas de estafas (pérdidas económicas, robo de información privada e instalación de malware), causando pérdidas de miles de millones de dólares cada año. Hemos recopilado este conjunto de datos para incluir un gran número de ejemplos de URL maliciosas, con el fin de desarrollar un modelo basado en aprendizaje automático que las identifique y nos permita detenerlas antes de que infecten sistemas informáticos o se propaguen por internet.

## Contenido
    Hemos recopilado un enorme conjunto de datos de 651 191 URL, de las cuales 428 103 son benignas o seguras, 96 457 son desfiguradas, 94 111 son de phishing y 32 520 son de malware. La Figura 2 muestra su distribución porcentual. Como sabemos, una de las tareas más cruciales es la selección del conjunto de datos para un proyecto de aprendizaje automático. Hemos seleccionado este conjunto de datos de cinco fuentes diferentes.

    Para recopilar URL benignas, de phishing, malware y desfiguración, utilizamos el conjunto de datos de URL (ISCX-URL-2016). Para aumentar las URL de phishing y malware, utilizamos el conjunto de datos de la lista negra de dominios de malware. Aumentamos las URL benignas utilizando el repositorio Git de Faizan. Finalmente, aumentamos el número de URL de phishing utilizando los conjuntos de datos Phishtank y PhishStorm. Como ya hemos mencionado, estos conjuntos de datos se recopilan de diferentes fuentes. Primero, recopilamos las URL de diferentes fuentes en un marco de datos independiente y, finalmente, las fusionamos para conservar únicamente las URL y su tipo de clase.

## Conclusiones

    ### Tamaño y diversidad
    El dataset contiene 651.191 URLs, recopiladas de cinco fuentes distintas, incluyendo ISCX-URL-2016, Phishtank, PhishStorm, listas negras de malware y repositorios de URLs benignas. Esta diversidad garantiza que los modelos entrenados sobre él puedan generalizar mejor a diferentes tipos de amenazas.

    ### Distribución de clases

    Benignas: 428.103 (~65,7%)

    Desfiguración: 96.457 (~14,8%)

    Phishing: 94.111 (~14,4%)

    Malware: 32.520 (~5%)

    Se evidencia un desbalance importante, con predominio de URLs benignas y una proporción reducida de malware, lo que sugiere la necesidad de técnicas de balanceo para entrenar modelos robustos.

    ### Preparación del dataset
    Cada tipo de URL se recopiló por separado y luego se fusionó en un marco de datos final, conservando solo la URL y su clase. Esto facilita un procesamiento limpio y reproducible.

    ### Aplicabilidad para aprendizaje automático

    Las etiquetas claras permiten entrenar modelos supervisados multiclase.

    La combinación de fuentes especializadas para phishing y malware asegura que las clases minoritarias sean relevantes y realistas.

# Bibliografía

    ISCX. (2016). ISCX URL Dataset 2016. Canadian Institute for Cybersecurity. Recuperado de https://www.unb.ca/cic/datasets/url-2016.html

    Phishtank. (s.f.). Phishing URL Dataset. OpenPhish. Recuperado de https://www.phishtank.com/

    PhishStorm. (s.f.). PhishStorm Dataset. Recuperado de https://www.phishstorm.com/

    Malware Blacklist. (s.f.). Malware Domain List. Recuperado de https://www.malwaredomainlist.com/

    Faizan, M. (s.f.). Repositorio de URLs benignas. GitHub. Recuperado de https://github.com/faizan-url-repo