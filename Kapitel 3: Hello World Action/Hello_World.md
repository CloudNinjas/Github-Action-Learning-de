# Kapitel 3: Hello World Action

## Action Code

Alle Actions sind in einfacher yml Sprache, die beschreibt was die Action tun soll und wann sie ausgeführt werden soll,  geschrieben. In diesem "Hello World" Beispiel werden wir die einzelnen Teile einer solchen yml Datei betrachten und erklären, wie diese eine Action beschreiben.

Zunächst ein Screenshot des UIs der Standard Hello World Action von github.com:

![Hello World YML](../Kapitel%203:%20Hello%20World%20Action/Hello_World_yml_start.png?raw=true "Hello World YML")

Es sit außerdem möglich kleine Icons, welche sen Status der letzten Ausführung der Action anzeigen zum Repository hinzuzufügen (definable from which branch or event/trigger)

![Hello World](https://github.com/CloudNinjas/Github-Action-Learning-de/actions/workflows/hellow_world.yml/badge.svg)

## Der ON Block

Dieser Block defieniert, wann die Action ausgeführt werden soll. Die Optionen reichen von Ereignissen in Git (z.B. pull, push auf einen bestimmten Branch) bis hin zur manuellen Ausführung.(Actions können nur via dem Actions-Tab manuell ausgeführt werden, falls ein weiterer Trigger auf dem selben Branch existiert.)

## Der JOBS Block
In diesem Block wird festgelegt, was die Action machen soll. Zu Beginn wird bestimmt welcher Runner die Action ausführen soll, beispielsweise ein self-hosted Runner oder eine spezielles Image der von github.com gehosteten Runner. Eine Action kann aus eienm oder mehreren Jobs bestehen, die parallel ausgeführt werden.

Zu jedem Job gehört ein steps-Block, der festlegt, welche Workflow-Schritte wir ausführen wollen. Es ist möglich alles von Grund auf selbst zu definieren, oder vordefinierte  Workflow-Schritte aus dem [Actions Repository](https://github.com/actions). In Github Enterprise kann man öffentliche Workflow-Schritte whitelisten.In unserem Beispiel wird zunächst die [Checkout Action](https://github.com/actions/checkout) verwendet, um das aktuelle Repository für den Rest der des Scripts verfügbar zu machen. Danach nutzen wir den run Befehl um erst eien einzeilges und dann ein mehrzeilige Shellscript auszuführen.

Was alles möglich ist mit Actions hängt ganz davon ab, was man braucht. Von simplen Begrüßungen für neue Contributors bis hin zu komplexen Setups, die viele externe Systeme nutzen ist alles im Bereichj des Möglichen. Alles in allem ist Github Actions ein einfaches aber mächtiges CI/CD tool, das leicht zu nutzen ist. 

