---
title: "Innkjøpskataloger"
description: "Denne artikkelen beskriver, på et høyt nivå, hvordan innkjøpere kan opprette og vedlikeholde innkjøpskataloger. Innkjøpskataloger definerer varene og tjenestene som de ansatte i firmaet kan bestille for intern bruk."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b94ecf3e173a2a7ce649170b6eff1e16f2626074
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---

# <a name="procurement-catalogs"></a>Innkjøpskataloger

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver, på et høyt nivå, hvordan innkjøpere kan opprette og vedlikeholde innkjøpskataloger. Innkjøpskataloger definerer varene og tjenestene som de ansatte i firmaet kan bestille for intern bruk.

Innkjøpsansvarlige kan opprette og vedlikeholde kataloger for varene og tjenestene som kan kjøpes for intern bruk i organisasjonen. Når kataloger er satt opp, kan de ansatte i firmaet opprette innkjøpsrekvisisjoner for å bestille fra dem. Katalogene kan brukes til å fremtvinge innkjøpspolicyer, slik at ansatte bare kan bestille varene og tjenestene som er tillatt for den juridiske enheten for innkjøp. Når du oppretter en innkjøpskatalog, bør du vurdere følgende oppgaver:

-   Konfigurer innkjøpskategorihierarkiet før du oppretter katalogen.
-   Bestem hvilke varer du vil at de ansatte skal kunne bestille. Du kan vise eller skjule bestemte produkter i en katalognode, eller du kan vise eller skjule alle produkter i en node.
-   Bestem hvor mange innkjøpskataloger du trenger. Tilgang til en innkjøpskatalog bestemmes av katalogpolicyregelen som du konfigurerer for den juridiske enheten og driftsenheten som en ansatt er tilordnet.

Flere faktorer bestemmer produktene som ansatte kan bestille og innkjøpskategoriene som de kan bruke når de oppretter innkjøpsrekvisisjoner:

-   Policyregelen for kategoritilgang i innkjøpspolicyen bestemmer hvilke innkjøpskategorier som er tilgjengelige i innkjøpsrekvisisjonen. Hvis ingen regler er definert, vil alle innkjøpskategorier være tilgjengelige.
-   Ansatte kan bare bestille et produkt hvis det er i den aktive innkjøpskatalogen for organisasjonen, og hvis det er i en node som er aktivert og ikke skjult. Produktet må også være i en kategori som en bestemt ansatt har tilgang til i henhold til policyregelen for kategoritilgang.
-   Policyregelen for katalog angir katalogen som brukes. Hvis ingen katalogpolicyregel er definert, bestemmer regelen for kategoritilgang produktene som en ansatt kan bestille på rekvisisjonen.

## <a name="prerequisites"></a>Nødvendig programvare
Tabellen nedenfor beskriver oppgavene som må fullføres før en innkjøper kan opprette en innkjøpskatalog.

| Oppgave                                                | Rolle               | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Definer et innkjøpskategorihierarki.            | Innkjøpssjef | Innkjøpskategorihierarkier brukes til å klassifisere varer eller transaksjoner for rapportering og analyse. Når du bruker et innkjøpskategorihierarki, kan firmaer strategisk administrere kategorier, produkter, leverandører og andre innkjøpsfaktorer fra et sentralt sted. Ett innkjøpskategorihierarki defineres for en hel organisasjon. Katalogen er basert på innkjøpskategorihierarkiet: kategoriene i hierarkiet blir noder i katalogen. Leverandører og produkter er inkludert i katalogen. |
| Legg til leverandører og produkter i innkjøpskategorier. | Innkjøpssjef | Når innkjøpskategorihierarkiet er opprettet for organisasjonen, kan hver innkjøpskategori knyttes til bestemte leverandører, produkter og så videre. Disse tilordningene kopieres automatisk til katalogen.                                                                                                                                                                                                                                                                                           |

## <a name="setting-up-a-catalog"></a>Definere en katalog.
Når forutsetningene er oppfylt, kan du opprette en kataloger. Du kan opprette enten en katalog som brukes i hele organisasjonen, eller flere kataloger som brukes av de forskjellige avdelingene i organisasjonen. Hvis du oppretter en katalog for hele organisasjonen, kontrolleres tilgangen til katalogen av policyregler for innkjøp.  

Katalogen definerer hvilke varer som er tilgjengelig når innkjøpsrekvisisjoner opprettes, men du kan bruke policyregler for tilgang til innkjøpskatalog for å bruke flere begrensninger. Siden nodene i en katalog er innkjøpskategorier, kan de deaktiveres av en policyregel for kategoritilgang. I dette tilfellet er produktene i denne kategorien ikke tilgjengelige for ansatte til bruk på innkjøpsrekvisisjoner. Du definerer tilgang til innkjøpskatalog på siden **Innkjøpspolicyer**. Tabellen nedenfor beskriver oppgavene som må fullføres hvis du vil definere en katalog.

| Oppgave                                                   | Rolle             | Beskrivelse                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opprett en ny katalog.                                  | Innkjøpsagent | Når du oppretter en katalog, kan du angi et navn og beskrivelse for katalogen. Du kan også definere om katalogen skal oppdateres manuelt eller automatisk, og angi eieren av katalogen.                                                                                                                                      |
| Kontroller om produkter er tilgjengelige i katalogen. | Innkjøpsagent | Siden produktene arves fra innkjøpskategoriene, vises alle i de aktuelle katalognodene. Du kan kontrollere om alle produkter i en node er skjult eller vises når katalogen brukes i en innkjøpsrekvisisjon. Du kan også kontrollere om enkeltprodukter i en node er skjult eller vises. |
| Publiser katalogen.                                   | Innkjøpsagent | Før en katalog er tilgjengelig for ansatte i en rekvisisjon, må du definere en katalogpolicyregel for katalogen, angi katalogens status til **Aktiv** og publisere katalogen. Du kan deaktivere kataloger du ikke lenger vil skal være tilgjengelige for brukerne.                                              |

Oppdateringer publiseres enten automatisk eller manuelt, avhengig av hvilket alternativ du velger for katalogen i feltet **Standard oppdateringstype** på **Kataloger**-siden. Følgende standard oppdateringstyper er tilgjengelige for kataloger:

-   **Dynamisk** – katalogen blir automatisk oppdatert når den endres.
-   **Statisk** – katalogene må oppdateres manuelt.
-   **Begge** – Hvis katalogen inneholder produktkategorier som har standard oppdateringstype **Statisk**, må den oppdateres manuelt når disse kategoriene oppdateres. Hvis katalogen inneholder produktkategorier som har standard oppdateringstype **Dynamisk**, oppdateres den automatisk når den endres.


<a name="see-also"></a>Se også
--------

[Definere et innkjøpskategorihierarki (oppgaveveiledning)](/dynamics365/unified-operations/supply-chain/procurement/tasks/set-up-procurement-category-hierarchy)




