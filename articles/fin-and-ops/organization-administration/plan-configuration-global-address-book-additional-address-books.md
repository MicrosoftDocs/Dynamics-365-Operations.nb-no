---
title: "Planlegg hvordan du konfigurerer den globale adresseboken og flere adressebøker"
description: "Denne artikkelen beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du definerer og konfigurerer den globale adresseboken og eventuelle tilleggsadressebøker i Microsoft Dynamics 365 for Finance and Operations. Noen av avgjørelsene krever at du bekrefter beslutningene som er gjort for andre deler av produktet, for eksempel organisasjonshierarkiet."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 12bd0a02899c04b0511e2a50bc4a724d5074d13e
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a>Planlegg hvordan du konfigurerer den globale adresseboken og flere adressebøker

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du definerer og konfigurerer den globale adresseboken og eventuelle tilleggsadressebøker i Microsoft Dynamics 365 for Finance and Operations. Noen av avgjørelsene krever at du bekrefter beslutningene som er gjort for andre deler av produktet, for eksempel organisasjonshierarkiet.

<a name="global-address-book"></a>Global adressebok
-------------------

Før du begynner å arbeide med den globale adresseboken, må du bestemme standardverdiene for den. Disse standardverdiene brukes deretter til flere adressebøker du oppretter. 

**Beslutninger:**

-   Hvilken rekkefølge skal navn vises i for partsposter av typen **Person**? For eksempel er én rekkefølge etternavn, mellomnavn og fornavn.
-   Skal partsposter slettes fra adresseboken når rolleposten slettes? Hvis for eksempel en kundepost slettes, skal partsposten også slettes?
-   Når en ny post opprettes, skal brukere varsles hvis det finnes en lik post i den globale adresseboken?
-   Skal DUNS-nummeret (Data Universal Numbering System) inkluderes i informasjonen til en partspost?
-   Hvis DUNS-nummeret er inkludert i en partspost, skal unikheten til nummeret kontrolleres?
-   Når det opprettes en partspost i den globale adresseboken, vil du ha en standard partstype, person eller organisasjon?
-   Hvilke brukerroller skal ha tilgang til de private adressene og kontaktinformasjonen til partsposter?

## <a name="additional-address-books"></a>Flere adressebøker
Når du oppretter den globale adresseboken, kan du opprette flere adressebøker i henhold til behovet ditt, for eksempel en egen adressebok for hvert firma i organisasjonen din eller for hver bransje. Fabrikam er for eksempel en internasjonal organisasjon som har flere firmaer og flere bransjer. Fabrikam planlegger å opprette en adressebok for hver bransje. For bransjer som forekommer mer enn ett sted, for eksempel bransjen for pneumatiske verktøy, planlegger Fabrikam å opprette en adressebok for hver lokasjon. Chris, som er IT-ansvarlig hos Fabrikam, har opprettet listen nedenfor over adressebøker som kreves. Denne listen beskriver også partipostene som hver adressebok må inneholde.

-   **Kontrakter med offentlig sektor (PubSC)** – Partsposter for alle parter som er involvert i kontrakter med offentlig sektor som Fabrikam har inngått.
-   **Kontrakter med privat sektor (PriSC)** – Partsposter for alle parter som er involvert i kontrakter med privat sektor som Fabrikam har inngått.
-   **Elektroniske verktøy (ET)** – Partsposter for alle parter som er involvert i innkjøp eller salg av elektroniske verktøy, eller som ellers bruker elektroniske verktøy som leveres av eller kjøpes for Fabrikam i firmaet Fabrikam-Japan.
-   **Pneumatiske verktøy (PTJPN)** – Partsposter for alle parter som er involvert i innkjøp eller salg av pneumatiske verktøy, eller som ellers bruker pneumatiske verktøy som leveres av eller kjøpes for Fabrikam i firmaet Fabrikam-Japan.
-   **Pneumatiske verktøy (PTUSA)** – Partsposter for alle parter som er involvert i innkjøp eller salg av pneumatiske verktøy, eller som ellers bruker pneumatiske verktøy som leveres av eller kjøpes for Fabrikam i firmaet Fabrikam-USA.

**Beslutning:**

-   Hvor mange flere adressebøker vil du opprette?

### <a name="address-book-security"></a>Adresseboksikkerhet

Du kan opprette adressebøker når som helst, og du kan også angi sikkerhetsparametere for adressebøkene når som helst. Du trenger ikke angi tilgangsrettigheter for en adressebok, men hvis du ikke gjør det, kan alle ansatte i organisasjonen se alle partsposter i denne adresseboken. Du kan definere tilgangsrettigheter til partsposter via adressebøker. Sikkerhetsrettigheter er basert på team. Denne tilnærmingen sikrer at bare arbeidere som er tilordnet et team som har tilgang til en adressebok, kan vise partipostene i denne adresseboken. Du må velge teamene som har tilgang til hver adressebok. For hver adressebok kan du angi tilgangsrettigheter som kan gi eller nekte tilgang for bestemte team. Hvis du gir et team rettigheter til en adressebok, kan alle medlemmer av teamet vise postene i adresseboken. Hvis du ikke gir et team tilgang til en adressebok, kan medlemmer av teamet ikke vise adresseboken eller innholdet. 

**Beslutning:**

-   Hvilke team skal ha tilgang til hver nye adressebok du vil opprette?





