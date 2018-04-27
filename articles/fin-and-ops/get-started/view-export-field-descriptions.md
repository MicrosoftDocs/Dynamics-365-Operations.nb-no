---
title: Vise og eksportere feltbeskrivelser
description: "Denne artikkelen beskriver hvordan du viser beskrivelser og hvordan du bruker siden Feltbeskrivelser til å eksportere beskrivelser."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0164d64b8c37c19a3b8b13970dbda5927073eca8
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="view-and-export-field-descriptions"></a>Vise og eksportere feltbeskrivelser

[!INCLUDE [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du viser beskrivelser og hvordan du bruker siden Feltbeskrivelser til å eksportere beskrivelser.

Microsoft Dynamics 365 for Finance and Operations har beskrivelsene for noen av de mer kompliserte feltene. Disse beskrivelsene vises når du holder pekeren over et felt. Du kan også vise og eksportere beskrivelser på siden **Feltbeskrivelser**. 

Ikke alle sider har feltbeskrivelser. Vi vil bare gi beskrivelser for de mer komplekse feltene, og ikke der bruken av feltet er åpenbart. Derfor ha noen sider ikke noen feltbeskrivelser, noen sider har noen få beskrivelser og noen av de mer komplekse sidene, for eksempel mange av parametersidene, har mange beskrivelser. 

Hvis du har tilgang til utviklingsmiljøet i Finance and Operations, kan du legge til nye feltbeskrivelser og tilpasse eksisterende beskrivelser. Du kan for eksempel legge til firmaspesifikk informasjon i en feltbeskrivelse. Hvis du vil ha mer informasjon, kan du se [hjelpen for å tilpasse felt](../../dev-itpro/user-interface/customize-field-help.md).

## <a name="see-field-descriptions-in-the-user-interface"></a>Se feltbeskrivelsene i brukergrensesnittet.
Du kan vise feltbeskrivelser ved å holde pekeren over et felt. Hvis ingen beskrivelse er tilgjengelig, kan du se navnet på feltet når du holder pekeren over feltet. (Obs! I Dynamics AX 7.0 (februar 2016) kan feltbeskrivelser bare vises på siden **Feltbeskrivelser**.) Illustrasjon nedenfor viser feltbeskrivelsen som vises når du holder pekeren over feltet **Lås varer under opptelling**. 

[![Eksempel på en feltbeskrivelse](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Bruk siden Feltbeskrivelser til å vise og eksportere felthjelp
Siden **Feltbeskrivelser** lar deg vise og eksportere feltbeskrivelser. Du kan se feltbeskrivelsene som er tilgjengelige for én side om gangen.

### <a name="view-the-descriptions-for-a-page"></a>Vise beskrivelsene for en side

Følg fremgangsmåten nedenfor for å vise beskrivelsene for en side.

-   Skriv inn navn på siden i feltet **Velg en side**. Klikk eventuelt pilen for å åpne en liste over alle sidene, og bla deretter gjennom eller filtrer listen.

Du kan bruke navnet på siden som vises i brukergrensesnittet (for eksempel **Kunder**), eller kodenavnet (navn på applikasjonsobjekttre) som er tilgjengelig når du høyreklikker på en side (for eksempel **CustTable**). 

Hvis du vil ha informasjon om de forskjellige måtene å filtrere listen over sider, kan du se delen Søke etter en side senere i denne artikkelen. 

Hvis du setter alternativet **Inkluder felt uten beskrivelse** til **Ja**, vises alle feltene på siden selv om de ikke har en feltbeskrivelse.

### <a name="export-the-descriptions-for-a-page"></a>Eksportere beskrivelsene for en side

Følg fremgangsmåten nedenfor for å eksportere beskrivelsene for en side.

1.  Velg en siden i feltet **Velg en side**.
2.  Klikk **Åpne i Microsoft Office** i øvre høyre hjørne, og klikk deretter **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Søke etter en side

Det finnes flere måter å søke etter en side på i feltet **Velg en side**. I mange tilfeller må du klikke pilen i feltet **Velg en side** for å åpne rullegardinlisten og deretter velge fra en filtrert liste over sider.

-   Skriv inn deler av navnet, og åpne deretter rullegardinlisten for å velge fra en filtrert liste over sider.
-   Åpne rullegardinlisten, og klikk deretter **Sidenavn**-toppteksten øverst i listen, eller toppteksten **Navn på applikasjonsobjekttre for side**. Det vises en dialogboks der du kan bruke alternativer for avansert filtrering, for eksempel **Sidenavn begynner med**.
-   Skriv inn det fullstendige navnet på siden. Når du bruker dette alternativet, er det best å åpne rullegardinlisten og se hva som ellers er i den, selv om feltbeskrivelser vises.
    -   Hvis det er ett nøyaktig treff på navnet, vises feltbeskrivelsene for denne siden.
    -   Hvis det finnes mer enn ett treff, vises ingen beskrivelser. Du må åpne rullegardinlisten, og velg siden du vil bruke.
    -   Hvis navnet du skrev inn er en del av navnet på en annen side, vises beskrivelsene for siden. Hvis du imidlertid åpner rullegardinlisten, vises flere sider som inneholder dette navnet.

Ingen beskrivelser vises for eksempel når du skriver inn <strong>Opptelling</strong> i feltet *<strong><em>Velg en side</em></strong>*. Du åpner rullegardinlisten og ser at det er to sider med navnet <strong>Opptelling</strong>, i tillegg til flere sider som inneholder ordet Opptelling i navnet. Hvis du velger siden som har <strong>InventJournalCount</strong> som navn på applikasjonsobjekttre, vises feltbeskrivelsene for denne siden. Hvis du imidlertid åpner rullegardinlisten på nytt, ser du at listen nå inneholder alle sider som har "InventJournalCount"» som en del av navnet på applikasjonsobjekttreet.

## <a name="troubleshooting"></a>Feilsøking
Dette avsnittet inneholder informasjon om hvordan du feilsøker problemer som kan oppstå når du bruker feltbeskrivelser.

### <a name="i-cant-find-a-field-description"></a>Det er en feltbeskrivelse jeg ikke finner

Vi holder på med å legge til beskrivelser for de mer komplekse feltene. Hvis du trenger hjelp med et bestemt felt, må du gjerne gi oss tilbakemelding ved å legge til en kommentar for dette emnet.

### <a name="the-field-description-isnt-helpful"></a>Feltbeskrivelsen er ikke nyttig

Gi oss tilbakemelding ved å legge til en kommentar for dette emnet. Hvis du kan, beskriver du den ekstra informasjonen du trenger.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Jeg finner ikke et felt på siden Feltbeskrivelser

Hvis du vil vise alle feltene på en side, kan du angi **Ja** for alternativet **Inkluder felt uten beskrivelse**. Klikk feltet **Velg en side** for å kontrollere at du har valgt den riktige siden. Hvis navnet du skrev inn er en del av et annet feltnavn, har du kanskje valgt siden som har det lengste navnet.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Jeg finner ikke en side på siden Feltbeskrivelser

Hvis du vil ha informasjon om de forskjellige måtene å finne sider, kan du se avsnittet Søke etter sider tidligere i denne artikkelen. Hvis du har skrevet inn det nøyaktige navnet på siden, kan det hende at feltbeskrivelsene ikke vises hvis det finnes flere sider med samme navn. Klikk pilen i feltet **Velg en side** for å åpne en filtrert liste over sidene som er tilgjengelige.

<a name="see-also"></a>Se også
--------

[Hjelp for å tilpasse felt](../../dev-itpro/user-interface/customize-field-help.md)





