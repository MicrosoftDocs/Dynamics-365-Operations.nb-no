---
title: Konfigurere alternativer for ordrebehandling
description: Dette emnet inneholder informasjon om hvordan du behandler ordrer for telefonsentre ved hjelp av Microsoft Dynamics 365 for operasjoner - handel.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eb62073fdfa50576d2c613594f3d85cbc0b322f6
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-order-processing-options"></a>Konfigurere alternativer for ordrebehandling

Dette emnet inneholder informasjon om hvordan du behandler ordrer for telefonsentre ved hjelp av Microsoft Dynamics 365 for operasjoner - handel. 

Støtter flere kanaler for detaljhandel, for eksempel nettbutikker, murstein og mørtel butikker og telefonsentre handel og handel i Dynamics 365 for operasjoner. I telefonsentre tar arbeidere imot kundeordrer over telefon og oppretter salgsordrer. Dette emnet beskriver hvordan du oppretter et telefonsenter og konfigurerer alternativer for samtalesenteret. Hvert telefonsenter kan ha sine egne brukere, betalingsmåter, prisgrupper, finansdimensjoner og leveringsmåter. Du kan konfigurere disse alternativene når du oppretter telefonsenteret. **Viktig:** Før telefonsenterarbeidsflyter kan brukes når den gjeldende Dynamics AX-brukeren oppretter salgsordrer, må brukeren tilordnes til telefonsenteret som en telefonsenterbruker. Du kan bruke siden **Telefonsenter** til å aktivere eller deaktivere funksjonsgrupper som er unike for telefonsentre. Følgende grupper funksjoner kan aktiveres:

-   **Ordrefullføring** – Denne gruppen inneholder funksjoner som er relatert til betalinger og ordrefullføring på siden **Salgsordre**.
-   **Styrt salg** – Denne gruppen inneholder funksjoner som er knyttet til kildekoder, skript og katalogforespørsler.

Når du aktiverer disse funksjonene i innstillingene for telefonsenter, blir de tilgjengelige på siden **Salgsordre** for brukere som er knyttet til telefonsenteret. De fleste av disse funksjonene krever ekstra oppsett før de kan brukes. Bilder og skript er aktivert som en del av innstillingen for styrt salg for det bestemte telefonsenteret. Hvis denne funksjonen er aktivert, vises skript og produktbilder i faktaboksruten på siden **Salgsordre**. Standardbildet som er angitt for et produkt, vises. Skript kan konfigureres for en vare, katalog, kunde eller vare i konteksten til en katalog. Telefonsenterordrer kan vise flere detaljer om hvordan prisen for en bestemt ordrelinje ble avledet. For eksempel kan ordrene vise hvilke rabatter som ble brukt. Du kan aktivere denne funksjonaliteten ved **kundereskontro**&gt;**Setup**&gt;**Kundeparametere**&gt;**priser**&gt;**pris detaljer**. Du kan få tilgang til siden **Prisdetaljer** fra rullegardinlisten **Salgsordrelinje**. Du kan bruke sporing av ordrehendelse for revisjonsformål, gå gjennom handlingene som utføres på en ordre i løpet av ordrens levetid, eller spore handlinger til en bestemt bruker. Du kan for eksempel registrere handlingen hver gang en bruker oppretter en salgsordre, setter en ordre på vent, overstyrer et tillegg eller oppdaterer en ordrelinje. Du kan definere ordrehendelser for å spore handlinger for bestemte brukere, brukergrupper eller alle brukere i en bestemt periode. Du kan vise hvilke handlinger som ble utført på et dokument ved å åpne siden **Ordrehendelser** fra handlingsruten på siden for dette dokumentet. Du kan konfigurere rekkefølgen hendelser på **salg og markedsføring**&gt;**Setup**&gt;**hendelser**&gt;**ordne hendelser**. Når en kundeordre ikke kan leveres til planlagt tid, kan et firma automatisk sende e-postvarsler til kunden for å forklare ordrestatusen og gi kunden en mulighet til å avbryte bestillingen. Hvis forsinkelsen overskrider en angitt terskel, kan ordren annulleres automatisk. Opptil tre e-postmeldinger kan sendes med angitte intervaller:

1.  **Første varsel om annullering** – Kunden kan annullere ordren.
2.  **Andre varsel om annullering** – Kunden kan annulere ordren.
3.  **Siste varsel om annullering** – Systemet annullerer bestillingen, og kunden blir informert om annulleringen.

Du kan la enkeltkunder og -produkter være fritatt fra den automatiske varslingen og annulleringen. Det utløses et marginvarsel når du legger til en vare i en ordre. Varselet inneholder viktig informasjon om varen, for eksempel prismargin og varens lønnsomhet. Du kan bruke denne informasjonen til å avgjøre om du skal bruke en prisoverstyring når du legger til en vare i salgsordren. Du kan for eksempel definere terskler for handelsmarginene for å angi at en terskel på 40 prosent eller mer over kostnaden er akseptabel for en vare, men at en terskel på 20 til 39 prosent over kostnaden er tvilsom. Dette betyr at alle varer med en terskel mellom 20 og 39 prosent vil utløse en advarsel. Alle varer med en terskel under 20 prosent over kostnaden kan ikke selges og vareprisen kan ikke justeres. Du kan konfigurere varsler for margen i **kunder**&gt;**Setup**&gt;**Kundeparametere**&gt;**margen varsler**. Når du definerer mva-tilordningen basert på standardregler, kan du finne en samsvarende prioritet for adresseelementer. Du kan for eksempel angi at kontroll av mva-grupper etter postnummer har høyere prioritet enn kontroll av mva-grupper etter delstat. Når du angir nye kundeadresseposter, blir mva-gruppen tilordnet automatisk basert på hvordan kundens adresse samsvarer med standardregler og prioritetssamsvar du har definert. Du kan konfigurere denne funksjonaliteten på siden **Økonomiparametere**.


