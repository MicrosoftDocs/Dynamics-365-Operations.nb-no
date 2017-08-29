--- 
title: Opprette Kanban-regel ved hjelp av en hendelse for Kanban-linje
description: "Denne fremgangsmåten oppretter en Kanban-regel ved å bruke hendelsesinnstillingen for Kanban-linjen for å utløse trekk fra en prosessaktivitet."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: cc8c3ff5e98ccce56a7a19b16c1aceac650cdf5a
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>Opprette Kanban-regel ved hjelp av en hendelse for Kanban-linje

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten oppretter en Kanban-regel ved å bruke hendelsesinnstillingen for Kanban-linjen for å utløse trekk fra en prosessaktivitet. Kanban-regelen blir utløst av en kanban-prosessaktivitet, med et antall like eller større enn 25 hver. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven. Denne oppgaven er ment for prosessingeniøren eller verdistrømlederen, når de klargjør produksjon av et nytt eller endret produkt i et lean-miljø.


## <a name="create-a-kanban-rule"></a>Opprette en Kanban-regel
1. Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.
2. Klikk Ny.
3. Velg Hendelse i feltet Etterfyllingsstrategi.
    * Dette genererer Kanbaner direkte fra behovet. Den brukes til å definere regler som definerer et bestillingsproduktscenario.  
4. Angi eller velg en verdi i feltet Første planaktivitet.
    * Angi eller velg SpeakerAssemblyAndPolish. Den første aktiviteten i en Kanban-regel er en prosessaktivitet i produksjonsflyten. Når du velger aktiviteten, blir gyldighetsdatoene for aktiviteten kopiert til gyldighetsdatoene for Kanban-regelen.  
5. Vis delen Detaljer.
6. Skriv L0001 i Produkt-feltet.
7. Utvid delen Hendelser.
8. Velg Automatisk i hendelsesfeltet Kanban-linje.
    * Dette genererer hendelses-Kanbaner ved behov.  Dette feltet brukes for å konfigurere Kanban-regler som etterfyller materiale som kreves for en etterfølgende prosessaktivitet. Når du velger Automatisk, opprettes hendelses-Kanbaner med behovet. Denne innstillingen anbefales hvis du har tenkt å utføre produksjon på samme dag.  
9. Sett Minimumsantall for hendelse til 25.
    * Hendelses-Kanbaner genereres når behovsantallet er lik eller større enn dette feltet. Dette er nyttig hvis du vil produsere et ordreantall som er mindre enn dette feltet på en maskin og flere enn dette feltet på en annen maskin.  
10. Klikk Lagre.

## <a name="create-sales-order-and-trigger-kanban-chain"></a>Opprette salgsordre og utløse Kanban-kjede
1. Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.
2. Klikk Ny.
3. Angi eller velg en verdi i Kundekonto-feltet.
    * Velg kundekontoen USA-003, Forest Wholesales.  
4. Klikk OK.
5. Skriv inn L0001 i feltet Varenummer.
    * L0001 er varen du opprettet Kanban-regelen for.  
6. Sett verdien for Antall til 27.
    * Siden 27 er høyere enn minimumsantallet 25 i Kanban-regelen, utløser dette en hendelses-Kanban.  
7. Skriv inn 1 i feltet Område.
8. Angi eller velg en verdi i feltet Lager.
    * Velg lager 13.  
9. Klikk Lagre.

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>Vise Kanban som er generert av Kanban-regelen
1. Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.
2. Finn og velg ønsket post i listen.
3. Vis delen Kanbaner.
    * Legg merke til at en Kanban for 27 ble opprettet for å behandle aktiviteten basert på den opprettede Kanban-regelen.  
    * Dette er det siste trinnet.  


