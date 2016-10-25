#Estrategia de Branching Atlassian Bamboo

#Overview

Esta es la traducción del documento de branching de https://confluence.atlassian.com/bamboo/bamboo-best-practice-branching-and-dvcs-398393354.html.

# Introducción 
## Enfoque de buenas prácticas
#Overview General

Bamboo Best Practice - Branching and DVCS

No importa cuan terrorifico pueda parecer, hacer branch del código es inevitable- y también una poderosa manera de permitirle al desarrollador trabajar
de manera aislada de diferentes aspectos del proyecto.

EL modelo de branching más simple es el que consta de un branch maestro y un branch ade desarrollo. El master o branch (mainline) contiene las versiones
de producción para release. De manera paralela al master corre el branch de desarrollo, donde los desarrolladores trabajan en features que serán mergeadas
de vuelta al master.

Cuando features sificientes han sido desarrolladas, estas serán integradas de vuelta al master para conformar el próximo release de producción.
Este simple método puede ser extendido con otras branches para hacer el trabajo de desarrollo más flexible, estis incluyen:

* Feature Branches.
* Release branches.
* Hotfix branches.

Pero debido a que el desarrollador no está constantemente integrando los cambios desde el master a su branch de desarrollo, puede existir incertidumbre
respecto a si el código va a funcionar eventualmente cuando sea integrado devuelta al master.

Lo ultimo que queremos hacer es contaminar el master con código no funcional desde el branch.
Bamboo ofrece algunas herramientas útiles para enfrentar el tema de los branches. Esta guía de mejores prácticas explora algunas de las formas 
que Bamboo maneja el beanching para la mejora de las practicas de desarrollo de software.

### Feature branching con planes de branches de Bamboo.


