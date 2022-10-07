# Kapitel 5: Infrastructure deployments

Hier werden wir einige Szenarien vorstellen, in denen es sinnvoll ist Github Actions zu nutzen um Infrastrukturkomponenten zu deployen, zu updaten, oder zu löschen. 

## Warum?

Wenn es darum geht Infrastruktur zu deployen ist das wichtigste Einheitlichkeit. Wenn man mit den bekannten Cloud Anbietern arbeitet wird einem schnell klar, dass es nahezu unmöglich ist für jeden mit allen änderungen mitzuhalten. Um doch mithalten zu können benötigt man also ein Team aus vielen Personen mit unterschiedlichen Skills. Andrerseits ist es nötig, dass jedes Teammitglied das Produkt deployen kann und eventuell Fehler verstehen und beheben kann. Um das zu gewärleisten ist es wichtig eine einheitliche basis für deployments zu haben.

## How to achieve the key consistency

Der erste Schritt in die richtige Richtung ist die Nutzung von Tools wie [Terraform](https://www.terraform.io/), [Packer](https://www.packer.io/), [Ansible](https://docs.ansible.com/), [Crossplane](https://crossplane.io/), [AWS Cloud Formation](https://aws.amazon.com/cloudformation/), [Azure Resource Manage](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview), or [Google Cloud Deployment Manager](https://cloud.google.com/deployment-manager/docs) und noch vielen mehr. Der Begriff "Infrastructure as code" fasst diese Tools zusammen.

The second step is to create, in the case of terraform, modules to have your configuration, that is necessary for your service to work, defined in your modules.

The third step is to recreate the calls to your modules in such a way that you deploy every service in the same way.

All of the steps above are helping to build consistent infrastructure deployments and to avoid facing simple issues over and over again.

## Recreating the calls to your modules

With "recreating" we mean to be able to create default deployments easy as possible and without having to setup every component individually.
To achieve this we combine predefined templates, versioned modules, and GitHub Actions.

### Predefined templates

This are tested module calls to create the service you want to create. 
