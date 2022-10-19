# Kapitel 1: Setup

## Vorraussetzungen

 - Github.com oder Github Enterprise Repository
 - Grundkentnisse in BASH/CMD/SHELL
 - Alles andere :)

## Ausgangspunkt

Github Actions und Workflows sind ein einfacher Weg, um Inhalte eines Git-Repository automatisch zu builden und deployen. Das bedeutet, dass Actions auf einem existeirenden Repository operieren. Github.com stellt standard Runner zum Ausführen dieser Actions zu Verfügung. Jede Organisation/Repository erhält eine begrenzte Menge an Build-Zeit umsonst, ist diese erschöpft, so kann sie kostenpflichtig erweitert weden. Mehr Information zu Preisen gibt es hier: 
[Official Github Action Billing Documentation](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions)


## Runners

### Github-hosted runners

Github.com stellt Standard Runner für fast alle Anwendungen, die keine speziellen Tools benötigen und nicht in einem komerziellen Kontext mit eröhten Sicherheitsanforderungen sind, zur Verfügung.  (nur verfügbar auf github.com).

 - OS: ubuntu, windows and macos (immer neueste Version)
 - Hardware: 2core, 7GB RAM, 14 GB SSD
 - Intallierte Tools: [Lange Liste von Tools](https://github.com/actions/runner-images#software-and-image-support)


### Self-hosted runners

Self-hosted Runner werden von Ihnen selbst verwaltet. Um self-hosted Runner nutzen zu können, müssen diese explizit zu ihrem Repository oder ihrer Organisation hinzugefügt werden. Mehr dazu hier: [Adding self-hosted runners](https://docs.github.com/en/actions/hosting-your-own-runners/adding-self-hosted-runners). Mann kann diesen Prozess natürlich auch automatisieren, zum Beispiel so: [Docker Image](https://hub.docker.com/repository/docker/vexx662/github-action-runner-proxy). Diese Art von Runner ist die einzige Möglichkeit Actions in  Github Enterprise zu nutzen. Für fast alle Nutzungsszenarien ist eine einfache VM mit den vorinstallierten tools völlig ausreichend, nur in Szenarien mit vielen parallelen Ausführungen mit langer Laufzeit ist es sinnvoll größer zu skalieren.

 - OS: Alle (Linux highly advised!)
 - Hardware: abhängig von der Anwendung (so klein wie möglich) (2 core, 4GB RAM)
 - Tools: Alle (wir empfehlen python auf jedem runner)

Anmerkungen:
 - Runner führen alle ausstehenden Actions aus, also ist hohe Verfügbarkeit kein muss
 - Probleme auf VM Level werden nicht in GitHub Action geloggt
 - Zugriff auf Firmeninterne Netzwerkressourcen kann eine Herausforderung sein
 - um Updates und Sicherheit muss man sich selbst kümmern!

[Official Github Self Hosted Runner Documentation](https://docs.github.com/en/actions/hosting-your-own-runners/about-self-hosted-runners)

