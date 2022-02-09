# Introducción a la minería de datos. Fundamentos de PLN. Práctica 1.

Borja Navarro Colorado

## Objeto

El objetivo de esta práctica es crear un *script* que procese un texto más o menos amplio con las aplicaciones comunes del PLN:

- lematización,
- *PoS_tagger*,
- *parser* de dependencias y
- detección de entidades nombradas.

Para ello, se utilizará el *pipeline* básico de la herramienta de PLN [SpaCy](https://spacy.io/), herramieta esta de uso común en minería de textos por ser bastante óptima (si bien la calidad del análisis no es simpre el mejor). Con esta práctica aprenderás, así, los fundamentos de SpaCy como herramienta de PLN para preprocesar corpus para minería de textos.

## Herramientas

- Cuaderno COLAB para crear el código: [https://colab.research.google.com](https://colab.research.google.com) y cuenta gCloud.
- Python (ya instalado en COLAB)
- SpaCy: [https://spacy.io/](https://spacy.io/)

## Corpus

Para darle algo de interés a la práctica, vamos a utilizar el tipo de texto más complejo que exite: el texto literario. En concreto debéis analizar una novela del corpus [ELTeC](https://github.com/COST-ELTeC).

ELTeC es un corpus multilingüe de novelas publicada en Europa durante los siglos XIX y XX. Cada novela está anotada a tres niveles: básico, estándar y avanzado. __Debéis seleccionar una novela del nivel estándar.__ A este nivel, cada novela está marcada en XML siguiendo el estándar [TEI](https://tei-c.org/). Podéis utilizar el idioma que queráis (siempre que se encuentre en SpaCy, ver [modelos disponibles](https://spacy.io/models)). Por ejemplo:

- novelas en español: [https://github.com/COST-ELTeC/ELTeC-spa/tree/master/level1](https://github.com/COST-ELTeC/ELTeC-spa/tree/master/level1)
- novelas en inglés: [https://github.com/COST-ELTeC/ELTeC-eng/tree/master/level1](https://github.com/COST-ELTeC/ELTeC-eng/tree/master/level1)
- novelas en francés: [https://github.com/COST-ELTeC/ELTeC-fra/tree/master/level1](https://github.com/COST-ELTeC/ELTeC-fra/tree/master/level1)
- novelas en portugués: [https://github.com/COST-ELTeC/ELTeC-por/tree/master/level1](https://github.com/COST-ELTeC/ELTeC-por/tree/master/level1)
- etc...

Dado que el corpus está en GitHub, se puede descargar y procesar directamente desde COLAB.


## Documentación

- Documentación básica SpaCy. Aquí está explicado todo lo necesario sobre PLN para realizar esta páctica:
    [https://spacy.io/usage/spacy-101](https://spacy.io/usage/spacy-101)
- Más información sobre SpaCy:
    - Curso avanzado: [https://course.spacy.io/es/](https://course.spacy.io/es/)
    - Documentación oficial: [https://spacy.io/usage](https://spacy.io/usage)

### Por pasos:

1. Crear un cuaderno COLAB vacío.
2. Importar SpaCy (Esto es fácil :) )
3. Descargar los módulos SpaCy para el idioma elegido e importar.
4. Asignar a una variable y crear así el *pipeline* de análisis.
5. Descargar el corpus desde GitHub y abrir una única novela en la carpeta level1.
5. Procesar el XML y extraer los párrafos:
    - etiqueta "p"
    - para procesar XML en python, se recomienda por su sencillez [Beautiful Soup](https://beautiful-soup-4.readthedocs.io/en/latest/#)
6. Analizar el texto con el *pipeline* básico de SpaCy y extraer "palabra | lema | categoria_gramatical".
7. Extraer los grupos nominales según el análisis de dependencias y ordenar por frecuencias de aparición.
8. Extraer las entidades nombradas y ordenar por frecuencias de aparición.
9. Crear un gráfico en COLAB donde se muestren la cantidad de nombres, adjetivos, verbos y adverbios.
10. Entrega: enviar enlace del cuaderno COLAB al profesor.




