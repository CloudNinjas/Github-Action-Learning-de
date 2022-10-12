# Infrastructure Factory

In großen Unternehmen giebt es nicht ein Team, das alles alleine verwaltet. Vielmehr giebt es viele kleine Teams, die gemeinsam am gleichen Ziel arbeiten. Daher iste es einfacher Infrastruktur Komponenten einmal zu definieren und int verschiedenen Szenarien wieder zu verwenden.

Hier ein Beispiel:
Angenommen wier wollen eine einfache Datenbank. Für eine Datenbank in der Cloud giebt es immer ähnliche Ansprüche. Die Datenbank muss auf eine Weise sicher sein (z.b. encryption on rest), sie muss erreichbar sein von einer backend Anwendung, und sie muss firmen in- und externen Standards genügen.

Eine solche Infrastruktur Komponente will und muss man nicht mehrfach definieren.

## Setting it up

Wie bereits erwähnt iste es möglich ein DevOps Mindset mit Infrastrukturdeployment zu verbinden.
Das bedeutet, wir nutzen Pipelines um Komponenten auf eine standartisierte Weise zu deployen.

### Idea

![Architecture](../Kapitel%206:%20Enterprise%20Nutzung/InfrastructureScenario2.drawio.png)
