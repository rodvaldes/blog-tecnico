# Maven

## [Overview qué es Maven](https://maven.apache.org/what-is-maven.html)

### Objetivos de Maven

- Facilitar el proceso de build.
- Proveer un sistema uniforme de Build.
- Proveer información de calidad del proyecto.
- Proveer una guía de mejores prácticas de desarrollo.
- Permitir una migración transparente para lo snuevos features.

## Website Principal

[Proyecto Apache Maven](https://maven.apache.org/)


## Getting Started Maven en 5 minutos
### Generar una aplicación con Maven

El siguiente es el comando que permite generar una aplicación Java basada en un archetype.

```bash
mvn archetype:generate -DgroupId=com.cybersyn.app -DartifactId=maventest -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
cd maventest/
mvn package
$ java -cp target/maventest-1.0-SNAPSHOT.jar com.cybersyn.app.App
Hello World!
```

## [Getting Started](https://maven.apache.org/guides/getting-started/index.html)

```bash
mvn -B archetype:generate \
  -DarchetypeGroupId=org.apache.maven.archetypes \
  -DgroupId=com.mycompany.app \
  -DartifactId=my-app
```

### Compilar
mvn compile

### Test

mvn test

### Crear un JAR y almacenarlo en el repositorio local de maven

mvn package
mvn install
mvn site


### Para habilitar como proyecto Eclipse IDE

mvn eclipse:eclipse

### [Ciclo de vida de Build](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)





## [Project Object Model POM .xml](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html)
---



### Ejemplo pom.xml mínimo 
    <project>
      <modelVersion>4.0.0</modelVersion>
      <groupId>com.mycompany.app</groupId>
      <artifactId>my-app</artifactId>
      <version>1</version>
    </project>

### ejemplo pom.xml desarrollo de plugin para Jira Server.

[Introducción al POM](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html)



