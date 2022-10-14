
![Architecture](../Kapitel%206:%20Enterprise%20Nutzung/platform-high-level-picture-automation.drawio.png)

## Einführung
Auf einer neuen Platform wollen wir Automation nutzen, um es teams zu ermöglichen Znetral verwlatete Terraform Repositories und andere Funktionalität zu nutzem. Es ist jedoch wichtig nicht alles Zentral zu verwalten, sondern den Teams so vie Freiraum wie möglich zu geben. In diesem Beispiel giebt es Tamplates für die folgenden Dinge:

 - Terraform repositories
   - Grundlegende Infrastruktur, die zentrale Terraform module nutzt
   - Erweiterbarkeit von Terraform für spezielle anforderungen
 - Zugriffskontrolle
   - Github Actions Erlauben und verwalten Zugriff basierend auf Gruppen
 - Key Value Store für Konfiguration
   - Hier wird Konfiguration gespeichert, die alle Repositories nutzen
 - Deployment location for code
   - Möglichkeit Repositories zu Erstellen, die mit der Cloud Infrastruktur verbunden sind, um einfaches CI/CD zu ermöglichen
 - API  
