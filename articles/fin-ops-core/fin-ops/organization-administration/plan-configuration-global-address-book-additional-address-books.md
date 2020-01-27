---
title: Plan for den globale adresseboken og andre adressebøker
description: Dette emnet beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du definerer og konfigurerer den globale adresseboken og eventuelle tilleggsadressebøker.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c6e71e5f537f0f9309eca1025c8e74cdce6716
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2883417"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>Planlegge den globale adresseboken og andre adressebøker

[!include [banner](../includes/banner.md)]

Dette emnet beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du definerer og konfigurerer den globale adresseboken og eventuelle tilleggsadressebøker. Noen av avgjørelsene krever at du bekrefter beslutningene som er gjort for andre deler av produktet, for eksempel organisasjonshierarkiet.

## <a name="global-address-book"></a>Global adressebok

Før du begynner å arbeide med den globale adresseboken, må du bestemme standardverdiene for den. Disse standardverdiene brukes deretter til flere adressebøker du oppretter.

**Beslutninger**

- Hvilken rekkefølge skal navn vises i for partsposter av typen **Person**? For eksempel er én rekkefølge etternavn, mellomnavn og fornavn.
- Skal partsposter slettes fra adresseboken når rolleposten slettes? Hvis for eksempel en kundepost slettes, skal partsposten også slettes?
- Når en ny post opprettes, skal brukere varsles hvis det finnes en lik post i den globale adresseboken?
- Skal DUNS-nummeret (Data Universal Numbering System) inkluderes i informasjonen til en partspost?
- Hvis DUNS-nummeret er inkludert i en partspost, skal unikheten til nummeret kontrolleres?
- Når det opprettes en partspost i den globale adresseboken, vil du ha en standard partstype, person eller organisasjon?
- Hvilke brukerroller skal ha tilgang til de private adressene og kontaktinformasjonen til partsposter?

## <a name="additional-address-books"></a>Flere adressebøker

Når du oppretter den globale adresseboken, kan du opprette flere adressebøker i henhold til behovet ditt, for eksempel en egen adressebok for hvert firma i organisasjonen din eller for hver bransje. Fabrikam er for eksempel en internasjonal organisasjon som har flere firmaer og flere bransjer. Fabrikam planlegger å opprette en adressebok for hver bransje. For bransjer som forekommer mer enn ett sted, for eksempel bransjen for pneumatiske verktøy, planlegger Fabrikam å opprette en adressebok for hver lokasjon. Chris, som er IT-ansvarlig hos Fabrikam, har opprettet listen nedenfor over adressebøker som kreves. Denne listen beskriver også partipostene som hver adressebok må inneholde.

- **Kontrakter med offentlig sektor (PubSC)** – Partsposter for alle parter som er involvert i kontrakter med offentlig sektor som Fabrikam har inngått.
- **Kontrakter med privat sektor (PriSC)** – Partsposter for alle parter som er involvert i kontrakter med privat sektor som Fabrikam har inngått.
- **Elektroniske verktøy (ET)** – Partsposter for alle parter som er involvert i innkjøp eller salg av elektroniske verktøy, eller som ellers bruker elektroniske verktøy som leveres av eller kjøpes for Fabrikam i firmaet Fabrikam-Japan.
- **Pneumatiske verktøy (PTJPN)** – Partsposter for alle parter som er involvert i innkjøp eller salg av pneumatiske verktøy, eller som ellers bruker pneumatiske verktøy som leveres av eller kjøpes for Fabrikam i firmaet Fabrikam-Japan.
- **Pneumatiske verktøy (PTUSA)** – Partsposter for alle parter som er involvert i innkjøp eller salg av pneumatiske verktøy, eller som ellers bruker pneumatiske verktøy som leveres av eller kjøpes for Fabrikam i firmaet Fabrikam-USA.

**Beslutning:**

- Hvor mange flere adressebøker vil du opprette?
