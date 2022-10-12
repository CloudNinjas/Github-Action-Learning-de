# Kapitel 5: Infrastructure deployments

Hier werden wir einige Szenarien vorstellen, in denen es sinnvoll ist Github Actions zu nutzen um Infrastrukturkomponenten zu deployen, zu updaten, oder zu löschen. 

## Warum?

Wenn es darum geht Infrastruktur zu deployen ist das wichtigste Einheitlichkeit. Wenn man mit den bekannten Cloud Anbietern arbeitet wird einem schnell klar, dass es nahezu unmöglich ist für jeden mit allen änderungen mitzuhalten. Um doch mithalten zu können benötigt man also ein Team aus vielen Personen mit unterschiedlichen Skills. Andrerseits ist es nötig, dass jedes Teammitglied das Produkt deployen kann und eventuell Fehler verstehen und beheben kann. Um das zu gewärleisten ist es wichtig eine einheitliche basis für deployments zu haben.

## Wie erreichen wir diese Einheitlichkeit?

Der erste Schritt in die richtige Richtung ist die Nutzung von Tools wie [Terraform](https://www.terraform.io/), [Packer](https://www.packer.io/), [Ansible](https://docs.ansible.com/), [Crossplane](https://crossplane.io/), [AWS Cloud Formation](https://aws.amazon.com/cloudformation/), [Azure Resource Manage](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview), or [Google Cloud Deployment Manager](https://cloud.google.com/deployment-manager/docs) und noch vielen mehr. Der Begriff "Infrastructure as code" fasst diese Tools zusammen.

In Terraform zum Beispiel ist der nächste Schritt Module zu erschaffen, welche die Kofigurtation der Infrastruktur beschreiben, die nötig ist um ihren service zu betreiben.

Der dritte schritt ist es die Aufrufe der module so neu zu erstellen, dass alle services auf die gleiche Weise deployed werden.

Die hier beschriebenen Schritte helfen eine konsistente Infrastruktur zu bauen und verhindern, dass man die selben einfache Probeleme immer wieder lösen muss.

## Neu Erstellen der Modulaufrufe

Mit "neu erstellen" meinen wir die Fähigkeit standard deployments so leich wie möglich, und ohne alle Komponenten von hand konfigurieren zu müssen, zu erstellen.
Um dies zu ermöglichen nutzen wir eine Kombination aus vordefinierten templates, versionierten Modulen, and GitHub Actions.

+ **Predefined templates:** Getestete Module, um Services zu erstellen
+ **Versioned modules:** Module haben versionen, um z.B. mit älteren Versionen arbeiten zu können 
+ **GitHub Actions:** Die Pipeline lösung unserer Wahl
