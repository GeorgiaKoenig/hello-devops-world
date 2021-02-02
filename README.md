# hello-devops-world
A hotchpotch of DevOps recipes

DevOps recipes are about to pop up here --> 

[1.1. Erweiterung der Definition of Done]
- Ein simples, aber folgenreiches DevOps-Rezept ist die Erweiterung der ggfs. verwendeten Definition of Done um den folgenden Zusatz:
Ein Softwareartefakt ist erst Done wenn es fertig ist UND (&&) in einer produktionsähnlichen Umgebung fehlerfrei funktioniert. Damit wäre die Entwicklungsabteilung gezwungen, betriebs-spezifische Aspekte beim Entwickeln präsent zu halten und einen (engeren) Austausch mit dem IT-Betrieb zu praktizieren.
Ein sehr aussagekräftiges Zitat von Gene Kim (bekannt durch The DevOps Handbook und The Phoenix Project) hierzu:
If I had a magic wand, I’d change the Agile sprints and definition of „done“: „At the end of each sprint, we must have working and shippable code …demonstrated in an environment that resembles production.“

[1.2. Continuous Integration, Delivery & Deployment]
- Continuous Integration (C. Int.) ist eine Entwicklungspraxis, bei der Entwickler in die Lage versetzt werden, mehrmals täglich Code in ein gemeinsames Repository zu integrieren. Jeder Check-in wird dann durch einen automatisierten Build verifiziert, so dass Teams auftretende Probleme frühzeitig erkennen können. Dabei handelt sich kontrekt um eine Praktik, die es ermöglicht, eine generierte Binärdatei automatisiert nach Fertigstellung unter verschiedenen Aspekten zu testen. Dazu können Tests wie System-, Integrations-, Regressions-, Benutzerakzeptanz-, Leistungs- und Sicherheitstests genutzt werden. Ist die zuvor vereinbarte Anzahl an Tests erfolgreich durchlaufen, gilt die Binärdatei als qualitativ hochwertig und in der Produktivumgebung einsetzbar. Die Qualifikation einer getesteten Binärdatei wird als Continuous Delivery (C. Delv.) bezeichnet. Continuous Delivery ist damit, aufbauend auf C. Int., eine Reihe von Prozessen und Praktiken, die darauf abzielen, Verschwendung aus dem Softwareproduktionsprozess radikal zu entfernen und eine schnellere Bereitstellung von Features zu ermöglichen. Zudem wird eine schnellere und effektivere Feedbackschleife zwischen Unternehmen und Benutzern angestrebt. Idealerweise wird ein Team befähigt eigene Deployments „on demand“ durchzuführen. Neben (C. Delv.) ist noch das Konzept des Continuous Deployment (C. Depl.) beachtenswert. Continuous Deployment geht einen Schritt über C. Delv. hinaus: Bei Continuous Delivery basiert die Bereitstellung in die Produktivumgebung auf einem manuellen Auslöser, d.h. die Entscheidung muss von Fall zu Fall neu getroffen werden. Im Unterschied dazu erfolgt die Bereitstellung in die Produktivumgebung in einem Continuous Deployment Prozess automatisch. Die Sequenz der Automatisierung für Aktivitäten, beginnend mit dem Continuous Integration Prozess bis zur Produktionsumgebung, wird in diesem Fall als Pipeline oder Delivery Pipeline bezeichnet.
Darin laufen alle Schritte, die auf die herkömmliche Art manuell abgearbeitet werden müssten, automatisiert ab.

[1.3. Shared Services]
- Dieses Konzept ist dem The DevOps handbook antnommen und sei hier Bereitstellung von Shared Services genannt. Es beinhaltet die Erstellung und Verwaltung von Self-Service-Funktionen durch das OPS-Team, d.h. zentralisierte Plattformen und Tooling-Services, die jedes SCRUM Team nutzen kann, um produktiver zu werden. Die Funktion dieser bereitgestellten Services kann beispielsweise das Aufsetzen von produktionsähnlichen Environments, Deployment Pipelines, automatisierten Testing-Werkzeugen oder Produktionstelemetrie-Dashboards sein. Dabei sind diese Plattformen und Dienste idealerweise automatisiert und auf Abruf verfügbar.

[1.4. Ops-Liaison-Modell]
- Das Ops-Liaison-Modell kann genutzt werden, um die Zusammenarbeit zwischen Teams aus der Softwareentwicklung (Dev) und des IT-Betriebs (Ops) zu stärken. Jedem der involvierten Entwicklungsteams wird eine sogenannte Ops-Liasion aus dem Ops-Team zugewiesen. Diese Liaison begleitet das Dev-Team, bringt dessen Bedürfnisse in die Operations-Roadmap ein und führt alle erforderlichen Aufgaben aus. Im Idealfall wird mittels des Ops-Liaison-Modells Ressourcen‑, Priorisierungs- und Zeit-Konflikte frühzeitig identifiziert und verringert.
Zudem wird das von der Ops-Liaison in die Dev-Teams eingebrachte IT-Betriebs-Wissen in automatisierten Code umgewandelt, der zuverlässiger und umfassender wiederverwendet werden kann. Dabei handelt es sich um den sogenannten Infrastructure-as-Code-Ansatz.

[1.5. Reduzierung technischer Schulden]
- Das Konzept der technischen Schulden (engl. technical debt) wird prominent in The DevOps Handbook beschrieben. Damit ist gemeint, dass technische Schulden (Workarounds, ineffiziente Fixes, prozessuale Umwege etc.) analog zu finanziellen Schulden auf Dauer, wenn ignoriert, zu einer deutlich eingeschränkten Handlungsfähigkeit führt. Es wird danach gestrebt, technische Schulden stetig zu mindern und bestenfalls zu vermeiden. Die hinter diesem Konzept stehende Ansicht ist die, dass die Verbesserung täglicher Arbeit wichtiger ist als die tägliche Arbeit selbst, und dass alle Teams über eigene Kapazitäten verfügen müssen. Hand in Hand zu diesem Konzept findet sich zudem in der Literatur die Forderung 20 % der täglichen Arbeit beider Abteilungen für die Tilgung sog. technischer Schulden (technical debts) zu reservieren. Dies entspräche einem Tag in der Woche bzw. einer Woche im Monat. Die Prämisse ist also zusammenfassend, dass die Ansammlung technischer Schulden (analog zu finanziellen Schulden) zunehmend handlungsunfähig machen, besonders wenn sie langfristig ignoriert werden. Ohne diese Maßnahmen läuft ein Team Gefahr, dass die eigene Produktivität unter dem stetig wachsenden Druck der eigenen technischen Schulden zum Stillstand kommen wird.

[1.6. Gemeinsame Rituale]
- Eine weitere Möglichkeit zur Verbesserung der Kommunikation ist die der Integration von IT-Betriebsmitarbeitern in etablierte Entwickler-Rituale. Das bedeutet, dass Personen aus dem OPS Team an den jeweiligen Ritualen des Dev-Teams teilnehmen. Dabei liegt der Fokus besonders auf den Standardritualen nach SCRUM, namentlich Sprint Planning, Daily Stand-ups und Retrospektiven. Das Feedback aus dem operativen Bereich hilft dem Product Owner, die Auswirkungen von Entscheidungen besser zu verstehen. Die zusätzlichen Arbeiten, die bei der Retrospektive des Projektteams identifiziert werden, fallen in die breite Kategorie der Verbesserungsarbeit, wie z. B. Fehlerbehebung, Refactoring und Automatisierung der manuellen Arbeit. Die Product Owner können die Verbesserungen zugunsten von Kundenmerkmalen verschieben oder entpriorisieren.

[1.7. Developers on Support]

[1.8. Generative Culture nach Ron Westrum]

[1.9. System thinking]

[1.10.Infrastructure-as-Code Ansatz]

[1.11. Value Stream Mapping]

[1.12. Job Shadowing]

[1.13. A/B Testing]

[1.14. Canary Release]

[1.15. Blameless Postmortem]

[1.16. Shift security to the left Ansatz]

[1.17. Embeded Ops Modell]

[1.18. Virtualization]

[1.19. Version everything]

[1.20. Single source of truth Repository]

[1.21. T-shaped people]

[1.22. Fail fast / fail safe Ansatz]

[1.23. Chaos engineering (http://principlesofchaos.org/)]

[1.24. Aktive Beteiligung der Stakeholder]
- Dies ist das grundlegende Leitprinzip von DevOps. DevOps kann nur dann erfolgreich sein, wenn sowohl die Entwickler als auch die Betriebs- und Supportmitarbeiter wirklich engagiert zusammenarbeiten und einen integrierten Ansatz zur Erreichung der Ziele verwenden.

[1.25. Automatisiertes Testen]
- Automatisierte Regressionstests werden von agilen Teams sehr häufig eingesetzt, um zu helfen, Probleme sofort zu beheben und eine höhere Codequalität zu liefern. Dies funktioniert auch bei DevOps gut, da es ein dringendes Bedürfnis des Betriebspersonals ist, dass der ausgelieferte Code einem bestimmten Qualitätsstandard entspricht.

[1.26. Integriertes Konfigurationsmanagement]
- In einer DevOps-Umgebung bezieht sich das Konfigurationsmanagement nicht nur auf die aktuelle Lösung, an der gearbeitet wird, sondern auch auf die Konfigurationsprobleme zwischen der Lösung und der restlichen Infrastruktur der Organisation. Das integrierte Konfigurationsmanagement hilft den Betriebsteams, die potenziellen Auswirkungen eines neuen Releases klarer zu sehen, was wiederum dabei hilft, bessere Entscheidungen darüber zu treffen, wann das Release durchgeführt werden sollte.

[1.27. Integriertes Änderungsmanagement]
- Beim integrierten Änderungsmanagement arbeiten Betriebs- und Entwicklungsteams zusammen, um zu verstehen, wie sich der Einsatz verschiedener Technologien auf das Unternehmen als Ganzes auswirkt, und arbeiten dann daran, dies zu bewältigen.

[1.28. Integrated Deployment Planning]
- Ein DevOps-Ansatz bedeutet, dass die Betriebsingenieure eng mit den Entwicklern zusammenarbeiten, wenn es um die Planung der Bereitstellung von Produkten gemäß einem organisatorischen Bereitstellungsplan geht.

[1.29. Produktionsunterstützung]
- Eine DevOps-Implementierung kann vorsehen, dass die Entwickler nicht nur an neuen Releases arbeiten, sondern auch an der Behebung kritischer Probleme mit einer Lösung, die bereits in Produktion ist. Obwohl sie als drittes und letztes Team in die Lösung von Produktionsproblemen involviert sind, ist dies ein ziemlich häufiges Vorkommnis und gibt ihnen Einblicke in Produktionsprobleme, die ihnen helfen, bessere Lösungen zu entwerfen.

[1.30. Anwendungsüberwachung]
- Dies bezieht sich auf die Praxis der Überwachung und Protokollierung von Lösungen in Echtzeit, sobald sie in Produktion sind. Dadurch erhalten wir Leistungsmetriken, die die Zuverlässigkeit der Lösung verbessern und Ausfälle verhindern.

[1.31. Magic (automatisierte) Dashboards]
- Der DevOps-Ansatz kann unterstützt werden, indem (automatisierte) Dashboards für verschiedene wichtige Metriken erstellt und geteilt werden. Dies begünstigt im besten Fall den Informationsfluss zwischen Teams, erhöht das Bewusstsein für die gemeinsame Wertgenerierung (Collective Ownership) und motiviert durch das Teilen von Erfolgen und positiven Trends. Natürlich können nicht alle Metriken automatisiert werden, aber einige Schlüsselmetriken können mit automatisierten Dashboards in Echtzeit eingesehen werden und sie liefern wichtige Geschäftsinformationen.


