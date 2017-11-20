---
title: "Registrering for produksjonsutførelse"
description: "Dette emnet beskriver viktige begreper og termer du må forstå for å kunne konfigurere og bruke produksjonsutførelse."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 939cb219a63a27ee9cb05036041d2722df3b0abc
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="registration-for-manufacturing-execution"></a>Registrering for produksjonsutførelse

[!include[banner](../includes/banner.md)]


Dette emnet beskriver viktige begreper og termer du må forstå for å kunne konfigurere og bruke produksjonsutførelse. 

Produksjonsutførelse er tiltenkt brukt hovedsakelig av produksjonsselskaper. Arbeidere kan registrere tids- og vareforbruk for produksjonsjobber ved hjelp av **Jobbregistrering**-siden. Alle registreringer godkjennes og overføres senere til de relevante modulene. Fortløpende godkjenning og overføring av registreringer lar ledere enkelt spore faktiske kostnader på produksjonsordrer.

## <a name="manufacturing-execution-and-registration-terminology"></a>Terminologi for produksjonsutførelse og registrering
Tabellen nedenfor viser begrepene som er knyttet til produksjonsutførelse og beslektede aktiviteter for registrering.

| Semester                          | beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Produksjonsutførelse       | En funksjon som brukes til å registrere tid, materialforbruk, kostnader for produksjonsjobber, prosjekter og indirekte aktiviteter. Registrering utføres i en registreringsklient for produksjonsutførelse.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Jobbliste                      | På siden **Jobbregistrering** ser arbeiderne listen over jobbene de må utføre på en bestemt ressurs, for eksempel en maskin. En arbeider kan registrere tids- og vareforbruk på hver jobb eller oppgave i jobblisten.                                                                                                                                                                                                                                                                                                                                                                           |
| Bunting av jobber                  | Hvis en arbeider starter flere jobber samtidig på siden **Jobbregistrering**, kalles dette bunting av jobber. Tiden som brukes på grupperte jobber, kan tilordnes til de enkelte jobbene på forskjellige måter ved hjelp av tildelingsnøkler.                                                                                                                                                                                                                                                                                                                                                         |
| Registreringer av leder/assistent | En arbeider kan registrere seg som assistent til en ressurs, og kan opprette et lite team der flere arbeidere arbeider på de samme produksjonsjobbene. Ressurser som arbeidere er knyttet til som hjelpere, kalles ledere. Bare lederressursen kan utføre registreringer. Alle assistenter får automatisk samme registreringer. Hvis en maskin for eksempel fungerer som lederen, kan arbeidere som er registrert som assistenter for denne maskinen, foreta registreringer på siden **Jobbregistrering**, og både maskinen og arbeiderne som er tilkoblet som assistenter, får de samme registreringene. |
| Indirekte aktivitet             | En aktivitet eller oppgave som ikke er direkte relatert til en produksjonsjobb eller et prosjekt, for eksempel et avdelingsmøte, en rengjøringsjobb eller en vedlikeholdsjobb i Shop Floor. Arbeidere kan foreta registreringer på indirekte aktiviteter slik de foretar registrering på produksjonsjobber og prosjekter.                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>Registreringer i produksjonsutførelse
Arbeidere kan utføre ulike typer registreringer i produksjonsutførelse for arbeid som utføres i produksjonsjobber. Avhengig av systemkonfigurasjon, kan det også være mulig for arbeidere å foreta registreringer på prosjektaktiviteter og ikke-produktive oppgaver, for eksempel pauser, fravær og indirekte aktiviteter. Her er registreringstypene:

-   **Innstempling/utstempling** (tilgjengelig med tid og fremmøte) – Arbeidere stempler inn når de kommer på jobb og stempler ut når de forlater og går hjem.
-   **Registrere på produksjonsjobber** – Arbeidere kan foreta registreringer, for eksempel oppstart av en jobb og tilbakemelding om en jobb, på produksjonsjobbene som vises i jobblisten. Arbeidere kan starte flere jobber samtidig. Dette kalles bunting av jobber.
-   **Registrere på lager** – Arbeidere kan foreta registreringer om materialer som brukes i produksjonen, men som ikke er direkte relatert til produksjonsjobber. Eksempler er fett, smøremidler eller annet materiale som brukes til å holde maskiner i gang. Registrering utføres i en lagerjournal.
-   **Registrere på prosjekter** (tilgjengelig med tid og fremmøte) – Arbeidere kan foreta registreringer, for eksempel oppstart og avslutning av arbeid på prosjektene eller prosjektaktivitetene som vises i jobblisten.
-   **Registrere prosjektgebyrer og prosjektvarer** (tilgjengelig med tid og fremmøte) – Arbeidere kan registrere gebyrer (utgifter) som er tilknyttet et prosjekt, i en prosjektgebyrjournal, for eksempel kilometergodtgjørelse og bompenger. Arbeidere kan også registrere vareforbruk i prosjekter. Dette gjøres i en prosjektvarejournal.
-   **Registrere som assistent for en annen arbeider** – Hvis to eller flere arbeidere skal arbeide sammen på en produksjonsjobb eller et prosjekt, kan en arbeider registrere seg som assistent for en maskin eller en annen arbeider, som i sin tur fungerer som leder. Om nødvendig kan lederen velge en annen arbeider som leder.
-   **Registrere fravær** (tilgjengelig med tid og fremmøte) – Arbeidere kan registrere tid på forskjellige fraværskoder som er definert. Det er mulig å vise fravær hvis arbeider kommer sent, krever fravær i løpet av arbeidsdagen eller går tidligere enn forventet i henhold til standard arbeidstid i profilen.
-   **Registrere pauser** (tilgjengelig med tid og fremmøte) – I løpet av arbeidsdagen kan arbeidere registrere at de forlater arbeidsstasjonen for å ta en pause. Flere pausetyper kan defineres. Når en arbeider kommer tilbake og logger på på nytt, registrerer systemet at arbeideren er tilbake, og pauseregistreringen stopper.
-   **Registrere indirekte aktiviteter** (tilgjengelig med tid og fremmøte) – Indirekte aktiviteter er ikke-produktive aktiviteter som arbeidere kan delta på i løpet av en arbeidsdag, for eksempel et avdelingsmøte, et teammøte eller en vedlikeholdsjobb i produksjonen. Arbeidere kan foreta registreringer på indirekte aktiviteter som er definert.
-   **Registrere overtid** (tilgjengelig med tid og fremmøte) – Arbeidere som har blitt bedt om å arbeide utover vanlig arbeidstid, kan velge om de ekstra timene skal registreres som fleksitid eller overtid.





