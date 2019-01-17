---
title: Informasjonskoder og informasjonskodegrupper
description: Denne artikkelen gir en oversikt om informasjonskoder, informasjonskodegrupper og hvordan de brukes.
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: c9cd9197f395b69f65137a59392a4d83d692f6fa
ms.contentlocale: nb-no
ms.lasthandoff: 01/04/2019

---

# <a name="info-codes-and-info-code-groups"></a>Informasjonskoder og informasjonskodegrupper

[!include [banner](includes/banner.md)]

Denne artikkelen gir en oversikt om informasjonskoder, informasjonskodegrupper og hvordan de brukes.

Informasjonskoder gjør det mulig å hente data på i en salgsstedskasse (POS). Du kan bruke infokoder til å spørre kassereren om å angi informasjon i forskjellige handlinger på salgsstedet, for eksempel varesalg, retur av varer eller valg av kunder. Kasserere kan velge inndata fra en liste eller angi dem som en kode, et nummer, en dato eller tekst. Du kan tilordne informasjonskoder til forhåndsdefinerte butikkhandlinger, detaljvarer, betalingsmåter, kunder eller bestemte salgsstedsaktiviteter. Du kan bruke informasjonskoder til å gjøre følgende:

- Hente tilleggsinformasjon på transaksjonstidspunktet, for eksempel et flightnummer eller årsaken til en retur.
- Be kassereren om å velge fra en prisliste for bestemte produkter.
- Koble en delkode til en informasjonskode som gjør at kassereren blir bedt om å angi inndata mens vedkommende utfører en bestemt aktivitet. Når en kunde returnerer et produkt, kan du for eksempel be kassereren om å spørre hvorfor produktet returneres. Du kan deretter bruke delkoder til å vise en liste over årsaker som kassereren kan velge blant.
- Selg et produkt som en vanlig salg, rabattert salg eller gratisprodukt.
- Be kasserere om å angi en verdi eller velge fra en liste over delkoder når de åpner kasseskuffen uten å utføre en salgsoperasjon.

## <a name="info-codes-group"></a>Informasjonskodegruppe

I Dynamics 365 for Retail kan du opprette grupper av infokoder. Informasjonskodegrupper legger til fleksibilitet ved å la deg definere færre informasjonskoder og deretter bruke dem på mer fleksible måter. Du kan bruke informasjonskodegrupper på følgende måter:

- Definere færre infokoder, og enkelt bruke dem på nytt. Informasjonskoder som er inkludert i informasjonskodegrupper, har ingen forhåndsdefinerte avhengigheter om andre informasjonskoder. Du kan ta med den samme informasjonskoden i flere informasjonskodegrupper og deretter bruke prioritering til å vise de samme informasjonskodene i rekkefølgen som er mest aktuell i en gitt situasjon.
- Koble informasjonskoder til andre koder eller informasjonskodegrupper for å samle inn informasjon om et produkt eller en transaksjon, uten å definere en egen informasjonskode eller koblede informasjonskoden for hvert scenario.

## <a name="info-code-examples"></a>Informasjonskodeeksempler

**Eksempel 1: Bruke infokoder på nytt**

Du kan koble informasjonskoder slik at når én informasjonskode blir utløst, utløses en annen informasjonskode like etter. Når du selger enkelte produkter, kan du eksempel be kassereren om å spørre kunden om de vil kjøpe batterier og en produktgaranti. Når det gjelder andre produkter, kan du be kassereren om å spørre kunden om de vil kjøpe batterier, og også be om postnummeret deres. Hvis du oppretter koblede informasjonskoder for disse scenariene, må du definere alle variantene av informasjonskoden, slik at kassereren blir bedt om å be om riktig informasjon. Hvis du bruker informasjonskodegrupper, kan du definere vanlige informasjonskoder, for eksempel forespørsel om batterier, én gang og deretter bruke dem på nytt i flere informasjonskodegrupper. Du kan også bruke prioritering i informasjonskodegruppene til å identifisere rekkefølgen spørsmålene vises i.

**Eksempel 2: Koble infokoder til infokodegrupper**

Når du selger visse produkter, for eksempel mobilenheter, er det alltid aktuelt å samle inn et spesifikt sett med informasjon, for eksempel telefonnummer, MEID-nummer (Mobile Equipment Identifier) og serienummer. Du vil imidlertid også samle inn annen informasjon for et nettbrett enn for en mobiltelefon. Du kan definere en informasjonskodegruppe som inkluderer spørsmål om telefonnummeret, MEID-nummeret og serienummeret, og deretter koble informasjonskodegruppen til en individuell informasjonskode. Når den produktspesifikke informasjonskoden utløses, kan informasjonskodegruppen utløses i neste omgang, slik at du kan samle inn fellesdataene uten å måtte definere flere sett med koblede informasjonskoder for hver enhet.

