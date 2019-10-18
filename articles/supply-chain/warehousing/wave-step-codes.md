---
title: Bølgetrinnkoder
description: Dette emnet inneholder en oversikt over bølgetrinnkoder og hvordan de brukes.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992363"
---
# <a name="wave-step-codes"></a>Bølgetrinnkoder

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a>Om bølgetrinnkoder

Bølgetrinnkoder er koder som brukere kan definere og bruke til å koble bestemte forekomster av bølgemetoder til en tilsvarende mal. Malene omfatter maler for etterfylling, containerbruk, etikettutskrift, lastplanlegging og sortering.

Når bølgetrinnkoder ikke brukes, må brukerne angi en fritekst for å referere til en bestemt mal fra den bølgemetodeforekomsten. Fritekst er utsatt for feil fordi brukerne må passe på at bølgestrinnteksten de legger til en bølgemal for en bestemt bølgetrinnmetode, samsvarer nøyaktig med bølgetrinnteksten i målmalen.

Bølgetrinnkoder for en bestemt bølgetrinntype konfigureres på en egen side. For alle bølgetrinnforekomster i en bølgemal som krever en bølgetrinnkode, må du velge bølgetrinnkoden i en rullegardinliste. Valg i en rullegardinliste erstatter fritekstoppføring og reduserer risikoen og innvirkningen av menneskelig feil. Oppsettkoder brukes til å koble en bølgetrinnmetode i en bølgemal til en målmal for metoden.

> [!NOTE]
> Bruk av funksjonen for bølgetrinnkoder er valgfri, og implementering er per juridisk enhet. Hvis en bestemt juridisk enhet bruker funksjonen, oppgraderes derfor alle eksisterende bølgetrinnkoder i den juridiske enheten til den nye strukturen.

## <a name="setup-demo"></a>Installere demonstrasjon 

For denne demonstrasjonen må demonstrasjons være installert, og du må bruke demonstrasjonsdataene for firmaet **USMF**.

### <a name="enable-wave-step-codes"></a>Aktiver bølgetrinnkoder

Følg disse trinnene for å aktivere funksjonen for bølgetrinnkoder.

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
2. I kategorien **Generelt** i hurtigfanen **Bølgebehandling** setter du alternativet **Aktiver bølgetrinnkoder** til **Ja**.

Alle eksisterende bølgetrinn i fritekst oppgraderes til den nye strukturen. Når denne oppgraderingen er fullført for en juridisk enhet, er ikke alternativet **Aktiver bølgetrinnkoder** tilgjengelig på siden **Lagerstyringsparametere**.

Valideringer utføres under oppgraderingen, og hvis oppgraderingen mislykkes, får du en feil melding. En oppgradering kan mislykkes på grunn av følgende konflikter:

- Det finnes duplisert bølgetrinn i fritekst.
- Det finnes tilpasninger.
- Et bølgetrinn i fritekst som er knyttet til en bølgetrinnmetodeforekomst, samsvarer ikke med den forventede maltypen.

Når du har løst eventuelle konflikter som identifiseres i løpet av valideringene, kan du kjøre oppgraderingsprosessen på nytt.

Når oppgraderingen er fullført, blir siden **Bølgetrinnkoder** (**Lagerstyring \> Oppsett \> Bølger \> Bølgetrinnkoder**) tilgjengelig. Denne siden viser en liste over bølgetrinnkodene som ble oppgradert da funksjonen for bølgetrinnkoder ble aktivert.

### <a name="create-new-wave-step-codes"></a>Opprette nye bølgetrinnkoder

Du kan bruke siden **Bølgetrinnkoder** til å opprette og slette bølgetrinnkoder.

Alle nye bølgetrinnkoder og den tilknyttede ID-en, må være unike på tvers av alle bølgetrinntyper, og de må defineres for en bestemt bølgetrinntype.

### <a name="apply-wave-step-codes"></a>Bruke bølgetrinnkoder

Når du har definert de aktuelle bølgetrinnkodene, kan de brukes på bølgeprosessmetodene.

Hvis du vil bruke bølgetrinnkoder, går du til den aktuelle målmalen. Her er målmalene som bølgetrinnkodene peker på:

- **Etterfyllingsmaler**: Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler
- **Maler for lastplanlegging**: Lagerstyring \> Oppsett \> Last \> Maler for lastplanlegging
- **Sorter maler** : Lagerstyring \> Oppsett \> Emballasje \> Utgående sorteringsmaler
- **Maler for containerbruk**: Lagerstyring \> Oppsett \> Containere \> Maler for containerbygging
- **Maler for etikettutskrift**: Lagerstyring \> Oppsett \> Dokumentruting \> Maler for bølgeetiketter

Malene i denne listen brukes når de refereres fra en bølgeprosessmetode som er valgt i en bølgemal. Når bølgetrinnkoden for bølgeprosessmetode i en bølgemal samsvarer med bølgetrinnkoden i én av maltypene, brukes malen.

### <a name="sample-scenario"></a>Eksempelscenario

Fremgangsmåten nedenfor hjelper deg med å garantere at etterfyllings malen du opprettet, brukes for bølgemalen.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgetrinnkoder**, og opprett en bølgetrinnkode for typen **Etterfylling**.
2. Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler**, og opprett en etterfyllingsmal.
3. I etterfyllingsmalen velger du bølgetrinnkoden du opprettet for typen **Etterfylling**.
4. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**, og velg bølgemalen du vil bruke.
5. I hurtigfanen **Metoder** i malen, velger du metoden **Etterfylling**.
6. I feltet **Bølgetrinnkode** velger du bølgetrinnkoden du valgte i etterfyllingsmalen.
