# Kaiptel 2: Grundlagen

## Was sind Github Actions?

Github Actions sind eine Schnittstelle zum Ausführen von beliebigem code in eienem Repository. Häufige Anwendungsfälle sind Building, Testing, Release mangagement, deployment.

## Wie funktionieren Github Actions?
Grundsätzlich tut github actions nichts anderes als eine Shell auszuführen mit den Scritten, die man defieniert hat. Dieses simple Konzept ermöglicht es jede beliebige Programmier- oder Scriptingsprache zu verwenden . Die Installation von Tools kann entweder durch einen Schritt der Action (in jeder Ausführung der Action), oder durch die Intsallation auf einem self-hosted Runner.

## What do I need to start?
Als Startpunkt dient das Repository selbst. Github.com stellt Runner mit einer vielfalt an vorab installierten Tools zur Verfügung, also kann man seine erste Action sofort nach erstellen eines Repos definieren.

## Wichtige Details:
- Secrets
  - Secrets können direkt einem Repository oder einer Organisation hinzugefügt werden
  - Externe secret stores sind nicht zu empfehlen, da sie nur schlecht unterstützt werden.
- Nutzung
  - Die Kosten einer Action werden nach der Ausführung berechent, lange Actions können also teuer sein. 
  - Keep it stupid simple
  - Kleine wiederverwendbare Actions sind besser als eine große
  - Actions können verkettet werden
- Reporting
  - Erfolgreiche ausführungen können verfolgt werden und Banner 
- Ecosystem
  - Es giebt ein großes Repository mit vielen Actions von verifizierten Quellen, dei man sofort nutzen kann.
  

  
# STARTING IS THE FIRST STEP
