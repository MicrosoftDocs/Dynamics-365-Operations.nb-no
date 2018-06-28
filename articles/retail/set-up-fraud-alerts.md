---
title: Definere svindelvarsler
description: "Dette emnet forklarer hvordan du definerer regler for å varsle kundeservicerepresentanter om potensiell falsk informasjon når ordrer behandles. Du kan definere spesifikke koder som brukes til å sette mistenkelige ordrer på vent automatisk eller manuelt."
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e4f89d86b64e0c8c76c15d3c2c1c00af353e9ca
ms.openlocfilehash: 2534e687623ab750f349287a762a354bc0fcf12b
ms.contentlocale: nb-no
ms.lasthandoff: 05/17/2018

---

# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>Definere og arbeide med telefonsentersvindelvarsler

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du definerer kriterier og regler for å sette potensielle svindelordrer på vent for videre gjennomgang. Svindelkontrollfunksjonen brukes til å fastslå gyldigheten av informasjonen i en salgsordre. Hvis informasjonen i salgsordren ser mistenkelig ut basert på organisasjonens svindelvilkår og -regler, kan ordren settes på vent for videre gjennomgang. I så fall frigis ikke ordren til lageret for videre behandling før sperringen er fjernet.

> [!NOTE]
> Denne funksjonen kan bare brukes med salgsordrebehandling for Retail-telefonsenterkanalen.

## <a name="turning-on-the-fraud-check-feature"></a>Aktivere svindelkontrollfunksjonen

Hvis du vil bruke funksjonen for svindel, må du sette **Aktiver ordrefullføring**-alternativet på kanalen til **Ja** når telefonsenterkanalen er [definert](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/set-up-order-processing-options). Når ordrefullføring er aktivert, må telefonsenterbrukere velge **Fullført** på siden for salgsordrer for alle salgsordrer som opprettes. Fullføringshandlingen fører til at **Salgsordresammendrag**-siden åpnes. Når brukere angir de påkrevde betalingsdataene på siden **Salgsordresammendrag**, velger de **Send** for å fullføre bestillingen. Når bestillingen er sendt, utløses funksjonen for svindelkontroll, og eventuelle regler som er aktive i systemet, godkjennes automatisk.

Telefonsenterbrukere kan også manuelt sette salgsordrer på vent for svindelgjennomgang før de velger **Send**. Velg **Sperre** \> **Manuell sperre for svindel** for å sette en salgsordre på vent manuelt på siden for **Salgsordresammendrag**. Du blir deretter bedt om å angi en kommentar som forklarer hvorfor du setter ordren på vent. Denne kommentaren vises i [ordresperrer](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds) arbeidsområdet for å gi kontekst til brukeren som gjennomgår ordrer som er satt på vent, for å finne ut om ordren skal frigis.

I tillegg til å konfigurere **Aktiver ordrefullføring**-alternativet på kanalen må du konfigurere svindelkontrollfunksjonen i telefonsenterparameterne. Gå til **Retail** \> **Kanaloppsett** \> **Telefonsenteroppsett** \> **Telefonsenterparametere**. På siden **Telefonsenterparametere** i kategorien **Sperrer** sett alternativet **Svindelkontroll** til **Ja**.

I kategorien **Sperrer** bør du også definere [sperrekoder](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds) som skal brukes på en ordre som er enten settes på vent for svindelgjennomgang manuelt eller automatisk. Angi sperrekoder i feltene **Manuell sperrekode for svindel** og **Sperrekode for svindel**. Det kan være nyttig å opprette to unike sperrekoder, slik at brukere som jobber i sperrearbeidsområdet, enkelt kan filtrere og skille automatiske sperrer fra manuelle sperrer.

For at svindelkontrollfunksjonen skal fungere effektivt, må du også angi **Minste poengsum**-feltet. Alle svindelkriterier og -regler som er definert i systemet, har en poengsum. Når en salgsordre kontrolleres for svindeltreff, legges resultatene sammen for å gi rekkefølgen en total svindelpoengsum hvis ett eller flere treff blir funnet. Hvis den totale svindelpoengsummen for en ordre overskrider verdien av **Minste poengsum**-feltet, settes ordren automatisk på vent. Du kan eventuelt bruke de andre poengsumrelaterte feltene i kategorien **Sperrer** for å definere poengsum for e-post, telefonpoengsum, poengsum for postnummer/postkode og poengsum for utvidet postnummer/postkode. Hvis du ikke angir en poengsum for noen av disse statistiske svindelkriteriene når du definerer dem på siden **Statiske svindeldata**, vil systemet gi dem en poengsum ved å bruke standard poengsum du angav i kategorien **Sperrer** på siden **Telefonsenterparametere**.

Til slutt bruk feltet **Kommentartype for svindel** for å angi dokumenttypen som skal brukes når brukere skriver inn kommentarer når de plasserer en ordre på vent for svindelgjennomgang manuelt. Som regel settes dette feltet til **Merk**.

## <a name="defining-fraud-criteria-and-rules"></a>Definere kriterier og regler for svindel

Systemet refererer til to typer svindelkriterier for å fastsette om en ordre skal settes på vent for svindelgjennomgang:

- **Statiske svindeldata** bruker en bestemt verdi, for eksempel et telefonnummer som er plassert på en liste over blokkerte numre eller en e-postadresse som er flagget fordi det er kjent for bli brukt for falske transaksjoner tidligere. Hvis du vil definere statiske svindeldata, kan du gå til **Retail** \> **Kanaloppsett** \> **Telefonsenteroppsett** \> **Svindel** \> **Statiske svindeldata**. På siden **Statiske svindeldata** kan du legge til kriterier for svindel manuelt eller gjennom dataimport. Resultatene er knyttet til dem svindelinformasjonen. Hvis svindelkontrollfunksjonen er aktivert, vil alle salgsordrer som legges inn, sammenlignes med de statiske dataene. Hvis dataene finnes i kundens faktureringsadresse eller leveringsadressen som er knyttet til ordrehodet, eller hvis dataene finnes i leveringsadressene som er koblet til noen av linjene i salgsordren, legges resultatene for alle unike treff sammen og sammenlignes med **Minste poengsum**-verdien for å fastslå om ordren skal settes på vent.
- **Regler for svindel** består av brukerdefinerte variabler og betingelsene som er definert for disse variablene. Hvis du vil opprette regler, kan du gå til **Retail** \> **Kanaloppsett** \> **Telefonsenteroppsett** \> **Svindel** \> **Regler**. Regler for svindel lar et firma konfigurere et mer sammensatt regelsett som kan inneholde **AND** eller **OR** -setninger for å vurdere flere betingelser. En bruker vil for eksempel at alle ordrer for kunder som tilhører en bestemt kundegruppe, og som har bestilt et bestemt produkt, skal settes på vent for svindelgjennomgang. I så fall defineres betingelser for å validere kunden og produkter på **Regler**-siden, og en AND-betingelse brukes. En ordre blir deretter satt på vent bare hvis begge betingelser er oppfylt, og hvis poengsumverdien som er tilordnet til denne regelen, i tillegg til poengsumverdien for andre regler som samsvarer med orden, fører til at den totale svindelpoengsummen for ordren overskrider **Minimum poengsum**-verdi som er definert på siden **Telefonsenterparametere**.

> [!NOTE]
> Flere regler eller svært komplekse regler vil påvirke systemytelsen når salgsordrer sendes. Funksjonen for svindelkontroll er ikke optimalisert for å håndtere store mengder statiske svindeldataoppføringer og mange aktive regler. Husk at hver regel evalueres når telefonsenterbrukere velger **Send** ved salgsordreregistrering. Reglene evalueres mot salgsordrehodet og alle ordrelinjer. Jo flere regler som finnes, og jo mer kompliserte regelsetningene er, jo lenger tid tar behandlingen. Hvis det finnes mange linjeelementer på en ordre og et stort antall aktive regler og statiske dataoppføringer, kan den automatiske prosessen for gjennomgang og validering av alle dataene og beregning av svindelpoengsum ha en alvorlige innvirkning på ytelsen. Organisasjoner som bruker denne funksjonen, bør alltid teste og bekrefte at behandlingstiden for ordrensending er akseptabel før de utfører endringer av regler eller statiske svindelkriterier i produksjonsmiljøet.

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>Identifisere ordrer som er på vent for svindelgjennomgang

Når telefonsenterbrukere sender en salgsordre, og hvis ordren samsvarer med kriteriene eller reglene for svindel, og poengsummen er større enn minimum, får brukerne en advarsel som sier at ordren er satt på vent. Brukere kan lukke denne meldingen, fordi den bare er til informasjonsformål. Brukere kan også kommunisere denne informasjonen til kunden. Bedriften må finne ut hvilken protokoll som brukere følger i denne situasjonen.

Ordren er lagret, men **Ikke behandle**-flagget er angitt på den. Dette flagget garanterer at ordren ikke kan frigis til lageret. Når som helst kan brukere vise innstillingen for **Ikke behandle**-flagget for salgsordrer på siden **Detaljert status**. Denne siden kan åpnes fra sidene **Alle salgsordrer** og **Kundestøtte**. Systemet oppdaterer også verdien for **Detaljert status**-feltet for ordren til **Svindelsperre**.

Hvis du vil vise og behandle ordrene som er på vent for svindelgjennomgang, kan du gå til **Retail** \> **Kunder** \> **Ordresperrer**. På siden **Ordresperrer** velger du en oppføring i listen, og deretter klikker du på **Ordresperre** for å se en mer detaljert visning som inneholder informasjon om årsaken til at sperringen. I hurtigkategorien **Svindeldetaljer** kan du vise de systematiske svindelkriteriene som var et treff for bestillingen, og resultatene som ble brukt. Hvis ordren ble satt på vent manuelt, kan du gå gjennom eventuelle kommentarer som ble angitt av brukeren som satte ordren på vent, ved å se på **Svindelmerknader**-delen på **Notater**-hurtigkategorien.

Du finner mer informasjon om hvordan du arbeider med sperreordrer, ved å se [Ordresperrer](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds).

