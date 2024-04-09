# Maven Artifact

Dieses Projekt ist ein einfaches Beispiel für die Verwendung von Maven zur Erstellung eines Java-Artefakts und dessen Verwendung.

## Aufbau des Artefakts

```java
package org.example;

public class HelloWorld {
    public static void sayHello() {
        System.out.println("Hello, World!");
    }
}

```
Die `HelloWorld`-Klasse ist eine einfache Java-Klasse, die eine statische Methode `sayHello()` enthält. Diese Methode gibt die Zeichenfolge "Hello, World!" auf der Konsole aus.

- **package org.example;**: Die Klasse ist im Paket `org.example` organisiert. Pakete dienen dazu, Klassen logisch zu gruppieren und Namenskonflikte zu vermeiden. (man könnte auch das von der bbw mit ch.bbw verwenden)

- **System.out.println("Hello, World!");**:
 Dies ist eigentlich schon das ganze artefakt, da es nicht mehr macht alls `Hello, World!` in die Konsole auszugeben. 

Die `HelloWorld`-Klasse kann verwendet werden, um eine einfache Nachricht (Wie sout einfach der String ist vorgegeben) auszugeben.

## Erstellen des Maven-Artefakts

Um das Maven-Artefakt zu erstellen, kann man folgende Schritte befolgen:

1. **Projekt klonen**: Das Git-Repository auf den lokalen Computer klonen:

```bash
git clone https://github.com/DaniDevOfficial/DevOpsMavenArtifactV3
```

2. **Navigieren zum Projekt**: 
Ins Verzeichnis des geklonten Projekts wechseln:

```bash
cd MavenArtifact
```

3. **Maven Artefakt Builden**: 
Den folgenden Maven-Befehl ausführen, um das Projekt zu builden und das Artefakt zu erstellen:

```bash
mvn clean install
```

## Verwendung des Maven-Artefakts

Nachdem das Maven-Artefakt erstellt wurde, kann man es in anderen Projekten verwenden. Hier ist, wie man es hinzufügen kann:

1. **Erstellen eines neuen Projekts**
 Ein neues Maven-Projekt erstellen oder ein vorhandenes Maven-Projekt öffnen, in dem man das erstellte Artefakt verwenden möchte.

2. **Bearbeiten der `pom.xml`**
 Das `pom.xml` des neu erstellten Projekts öffnen und die Abhängigkeit zum Maven-Artefakt hinzufügen. Dazu die `<dependency>`-Konfiguration mit der `groupId`, `artifactId` und `version` des Artefakts verwenden. 
 Bsp:

```xml
<dependency>
    <groupId>org.example</groupId>
    <artifactId>MavenArtifact</artifactId>
    <version>1.0-SNAPSHOT</version>
</dependency>
```

3. **Verwendung des Artefakts**
In meiner Verwendung des Artefakts hier wird ganz eifach die Dependecy `HelloWorld` aufgerufen und davon wird `sayHello` verwedend, wass `Hello, World!` in die Konsole printen sollte. 
```java
package org.example;

public class App 
{
    public static void main( String[] args )
    {
        HelloWorld.sayHello();
    }
}

```


