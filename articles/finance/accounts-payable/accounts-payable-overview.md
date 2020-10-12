---
title: Oversikt over å konfigurere leverandør
description: Denne artikkelen beskriver sidene du bruker til å definer grunnleggende og valgfrie funksjoner for leverandører. Den beskriver også trinnene i oppsettet som du må fullføre før du begynner å definere leverandører.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eed11cbe73ede71cabf83655fc1d37b1a979a4c
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830289"
---
# <a name="configure-accounts-payable-overview"></a>Oversikt over å konfigurere leverandør

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver sidene du bruker til å definer grunnleggende og valgfrie funksjoner for leverandører. Den beskriver også trinnene i oppsettet som du må fullføre før du begynner å definere leverandører.

<a name="prerequisites-for-accounts-payable-setup"></a>Forutsetninger for oppsett av Leverandører
----------------------------------------

Før du kan konfigurere Leverandører må du fullføre følgende konfigurasjon:

-   I Økonomimodul:
    -   Hvis du planlegger bruk av betalingsjournaler, må du konfigurere betalingsjournaler.
    -   Hvis du planlegger å kjøre kursjusteringer, må du konfigurere valutakoder på siden Valutaer, konfigurere valutakurstyper på siden Valutakurstyper og konfigurere valutakurser på siden Valutakurser.
-   I Kontant- og bankbetaling definerer du bankkontoer som skal brukes med betalingsmåter.

## <a name="setup-pages-for-accounts-payable"></a>Konfigurasjonssider for Leverandører

Bruk de følgende sidene til å sette opp den grunnleggende funksjonaliteten i Leverandører for hver juridiske enhet. Sidene vises i rekkefølgen som anbefales for oppsett. Du kan gjøre oppsettet enklere ved å opprette maler fra de første postene som opprettes. I en mal angis verdiene vanligvis i mange felt for å reflektere funksjonene som organisasjonen ønsker å implementere for en bestemt type leverandør.
1.  På siden Betalingsbetingelser definerer du betalingsbetingelsene du tilordner til salgsordrer, bestillinger, kunder og leverandører, og som bestemmer forfallsdatoer for fakturaers. Hvis du vil ha mer informasjon, kan du se [Definere leverandørbetalingsgebyrer](tasks/define-vendor-payment-fees.md).
2.  På siden Betalingsmåter - leverandører oppretter og vedlikeholder du informasjon om hvordan organisasjonen betaler sine leverandører.
3.  På siden Leverandørgrupper oppretter og vedlikeholder du grupper av leverandører som deler viktige parametere for postering, utligning og betaling, rapportering og prognoser.
4.  På siden Leverandørposteringsprofiler angir du hvordan leverandørtransaksjoner posteres til økonomimodulen.
5.  På siden Leverandørparametere angir du standardinnstillinger som brukes hvis ingen bestemt innstilling er angitt, parametere for forskjellige typer funksjonalitet og de ulike nummerseriene for Leverandører.
6.  På siden Skjemaoppsett definerer du formatet for forskjellige dokumenter som er knyttet til leverandører, og som firmaet bruker til å holde oversikt over mottak fra leverandører og til å registrere årsaker til betalingsflyten til leverandører.
7.  På siden leverandører oppretter og vedlikeholder du leverandørkontoer, og skattemyndighetene som organisasjonen din rapporterer merverdiavgift til.

## <a name="optional-setup-pages-for-accounts-payable"></a>Valgfrie sider for leverandøroppsett
I tillegg til den grunnleggende funksjonaliteten har Leverandører andre funksjoner som du kan definere.

De ekstra oppsettssidene organiseres etter funksjonalitet.

**Policyer**
-   På siden Leverandørfakturapolicy angir du leverandørfakturapolicyer.

**Fakturakontroll**

-   På siden Toleranse for fakturatotaler definerer du toleranser for fakturatotaler.
-   Angi toveis og treveis kontrollpolicyer på Kontrollpolicy-siden.
-   På siden Pristoleranser definerer du toleranser for enhetspriser.
-   Angi toleransegrupper for varepriser på siden Pristoleransegrupper for vare.
-   Angi toleransegrupper for leverandørpriser på siden Pristoleransegrupper for leverandør.
-   På siden Toleranser for tillegg definerer du toleranser for tillegg.

**Arbeidsflyt**

-   På siden Arbeidsflyter for leverandørreskontro definerer du arbeidsflytkonfigurasjoner for journalgodkjenninger og innkjøpsrekvisisjoner.

**Årsaker**

-   På siden Leverandørårsaker definerer du årsakskoder.

**Tillegg**

-   På siden Tilleggskode definerer du koder for tilleggene som skal brukes i bestillinger.
-   På siden Leverandørtilleggsgruppe oppretter og vedlikeholder du tilleggsgrupper for leverandører.
-   På siden Varetilleggsgrupper  oppretter og vedlikeholder du tilleggsgrupper for varer.
-   På Automatiske gebyrer-siden definerer du gebyrene som tilordnes ordrer automatisk.

**Tilleggsvarer**

-   På Tilleggsvaregrupper - Leverandør -siden oppretter og vedlikeholder du tilleggsvaregrupper for leverandører.
-   På Tilleggsvaregrupper - Lager -siden oppretter og vedlikeholder du tilleggsvaregrupper for varer.

**Distribusjon**

-   På Leveringsbetingelser-siden oppretter og vedlikeholder du betingelsene for en vares overføring fra selger til kjøper.
-   På Leveringsmåter-siden oppretter og vedlikeholder du transportmåtene som brukes ved levering av en ordre fra selgeren til kjøperen.
-   På Fraktsone-siden oppretter og vedlikeholder du identifikatorer og beskrivelser av mottaksadresser.

**Skjemaer**

-   På Skjemamerknader-siden oppretter du standardteksten som skal vises på forskjellige sider.
-   På Skjemasorteringsparametere-siden definerer du sorteringsrekkefølgen for rekvisisjoner, mottakslister, følgesedler og fakturaer.
-   På Oppsett for utskriftsbehandling-siden definerer du utskriftsbehandlingsinformasjon for originaler og kopier av sider.

**Betalinger**

-   På Kontantrabatt-siden definerer og administrer du betingelsene for å oppnå kontantrabatter. Kontantrabattkodene er knyttet til leverandører, og brukes på bestillinger.
-   På Betalingsplaner-siden definerer du betalingsplaner som brukes til å administrere avdragsbetalinger til leverandører.
-   På Betalingsdager-siden definerer du betalingsdagene som skal brukes til beregning av forfallsdager, og angir betalingsdager for en bestemt dag i uken eller måneden.
-   På Betalingsgebyr-siden oppretter og vedlikeholder du betalingsgebyrer som er knyttet til leverandører.
-   På Betalingsinstruksjon-siden oppretter og vedlikeholder du betalingsinstruksjoner.

**Statistikk**

-   På Definisjoner av aldersfordelingsperiode-siden setter du opp brukerdefinerte intervaller som brukes til å analysere modenhetsdistribusjon for leverandørkontoer.
-   På Bransje-siden oppretter du bransjekoder (LOB) som er tilordnet til leverandører.

**1099-avgift**

-   På **1099-felt**-siden kontrollerer og oppdaterer du minimumsbeløpene som må rapporteres til det amerikanske skattevesenet, Internal Revenue Service (IRS), basert på de nyeste IRS-kravene.

## <a name="optional-setup-for-other-modules"></a>**Valgfritt oppsett for andre moduler**
**Organisasjonsstyring**

-   På Nummerserier-siden definerer du nummerseriegrupper for fakturanumre.
-   På de følgende sidene definerer du adresseinformasjon:
    -   Adresseoppsett
    -   NAF-koder
    -   Import av postnumre

**Økonomi**

-   På Finansdimensjoner-siden definerer du finansdimensjoner.
-   På de følgende sidene definerer du avgiftsinformasjon:
    -   Mva-koder
    -   Mva-grupper
    -   Vare, mva-grupper
    -   Kontogruppe
    -   Mva-fritakskoder
    -   Mva-jurisdiksjoner
    -   Skattemyndigheter
    -   Mva-utligningsperioder

**Kontant- og bankbehandling**

-   På siden Koder for betalingsformål definerer du sentralbankens formålskode.





