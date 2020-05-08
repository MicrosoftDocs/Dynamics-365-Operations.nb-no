---
title: Opprette avanserte kontrakter for fakturering basert på fremdriften
description: Dette emnet forklarer hvordan du oppretter prosjektkontrakter slik at du kan generere fakturaer for kunder, basert på en prosentdel av fullført arbeid.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282841"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Opprette avanserte kontrakter for fakturering basert på fremdriften
[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter prosjektkontrakter slik at du kan generere fakturaer for kunder, basert på en prosentdel av fullført arbeid. Fakturabeløpene beregnes automatisk for budsjettkategoriene av arbeid som du har definert for et prosjekt. Tidsmålingen av fakturaer defineres når du forhandler frem prosjektkontrakten med kunden.

Bruk disse prosedyrene for å definere en kontrakt, et tilknyttet prosjekt og faktureringsreglene som skal brukes for å beregne fakturabeløp for budsjettkategoriene av arbeid som du har definert for prosjektet.

Når du har opprettet kontrakten og prosjektet, kan du angi prosjektdetaljene. Du kan for eksempel angi aktivitetene og tilordne arbeidere til prosjektet.

## <a name="example"></a>Eksempel

Organisasjonen din er et firma som driver programvareutvikling. Du avtaler utvikling av en lønnsregnskapspakke for en kunde mot et totalgebyr på USD 20 000. Organisasjonen avtaler å sende en faktura til kunden etter hvert som du fullfører bestemte prosenter av prosjektet. Du definerer følgende prosjektkategorier for arbeidet, slik at du kan bruke dem i betalingsprosessen:

- Rådgivning
- Utforming
- Installasjon

Du definerer også faktureringsregler som automatisk beregner fakturabeløpene for prosenten av prosjektet som er fullført i hver kategori.

Budsjettlederen oppretter et budsjett for prosjektkategoriene. Beløpet for fullført arbeid beregnes automatisk som en prosent av faktisk arbeid, sammenlignet med budsjetterte beløp.

## <a name="prerequisites"></a>Forutsetninger

Før du oppretter et prosjekt som bruker faktureringsregler, må du definere nummerseriene for faktureringsregler og en gebyrjournal som brukes til å postere fremdriftsfaktureringer.

1. Gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Prosjektstyrings- og regnskapsparametere**.
2. Definer nummerserien du vil bruk når det opprettes faktureringsregler, på siden **Parametere for prosjektstyring og regnskap** i kategorien **Nummerserier**.
3. Gå til **Prosjektstyring og regnskap** \> **Journaler** \> **Gebyr**.
4. Velg **Ny** på **Gebyrjournal**-siden, og angi journalnavnet.

## <a name="create-a-contract-for-progress-billings"></a>Opprette kontrakt for fremdriftsfakturering

Bruk denne prosedyren til å opprette en prosjektkontrakt for et fastprisprosjekt. Du oppretter en prosjektfaktura når arbeidet som er fullført på prosjektet når en bestemt prosent.

1. Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Prosjektkontrakter**.
2. Velg **Ny** på siden **Prosjektkontrakter**.
3. I dialogboksen **Ny prosjektkontrakt** angir du følgende felt:

    - **Navn**
    - **Finansieringstype**
    - **Finansieringskilde**
    - **Salgsvaluta** – Dette er standardvalutaen som brukes til kundefakturaer som er tilknyttet prosjektkontrakten. Du kan imidlertid endre salgsvalutaen på en bestemt kundefaktura.

4. Velg **OK**. Informasjonen kopieres til hodet på **Prosjektkontrakter**-siden.
5. På **Prosjektkontrakter**-siden fyller du ut resten av den nødvendige informasjonen for prosjektet.

## <a name="create-a-project-for-progress-billings"></a>Opprette et prosjekt for fremdriftsfakturering

Bruk denne fremgangsmåten for å opprette et prosjekt og eventuelle underprosjekter som er tilknyttet en prosjektkontrakt.

1. Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Alle prosjekter**.
2. Velg **Ny** på siden **Alle prosjekter**.
3. I dialogboksen **Nytt prosjekt**, i feltet **Prosjekttype**, velger du **Tid og materialer**.
4. Velg en prosjektgruppe. En prosjektgruppe angir posteringsinformasjon for prosjekter som er tilordnet gruppen.
5. Velg **Opprett prosjekt**.
6. Når du har opprettet prosjektet, setter du prosjektstadiet til **Pågår**.

## <a name="create-a-budget-for-a-project"></a>Opprette et budsjett for et prosjekt

Budsjettkategoriene brukes til å automatisk beregne fakturabeløpene for arbeidsprosenten som er fullført for hver kategori. Følg disse trinnene for å opprette budsjettkategorier for de estimerte kostnadene.

1. Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Alle prosjekter**.
2. Velg og åpne prosjektet du vil bruke, på siden **Alle prosjekter**.
3. På **Prosjekter**-siden i handlingsruten, i kategorien **Plan** i **Budsjett**-gruppen klikker du **Prosjektbudsjett** for å opprette et nytt prosjekt.
4. Angi en estimert kost for hver kategori i prosjektet på siden **Prosjektbudjett**.

## <a name="create-billing-rules-for-progress-billings"></a>Opprette faktureringsregler for fremdriftsfakturering

1. Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Prosjektkontrakter**.
2. På **Prosjektkontrakter**-siden velger du og åpner en prosjektkontrakt.
3. Velg **Legg til** på hurtigfanen **Faktureringsregler** på prosjektkontrakt-siden.
4. Velg **Fremdrift** på **Faktureringsregel**-siden i **Linjetype**-feltet.
5. Angi totalverdien for kontrakten i feltet **Kontraktverdi** på hurtigfanen **Detaljer om faktureringsregellinje**.
6. Velg kategorien som gebyrtransaksjonen skal posteres til, i feltet **Kategori**.
7. Velg prosjektet som bruker denne faktureringsregelen, i feltet **Prosjekt**.
8. Valgfritt: Tilordne den samme faktureringsregelen til flere prosjekter. Velg et prosjekt i delen **Tilgjengelige prosjekter** på hurtigfanen **Prosjekt**, og velg deretter høyre pilknapp for å legge til prosjektet i delen **Valgte prosjekter**.
9. Valgfritt: Beregn prosentbeløpet som kunden holder tilbake fra betalinger på en faktura. I hurtigfanen **Betingelser for tilbakeholdelse av betaling** velger du finansieringskilden, og deretter angir du tilbakeholdelsesprosenten i **Bevaringsprosent**-feltet.
10. Gjenta denne prosedyren for å opprette ytterligere faktureringsregler for prosjektkontrakten.
