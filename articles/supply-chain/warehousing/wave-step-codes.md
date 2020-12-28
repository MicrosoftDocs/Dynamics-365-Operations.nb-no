---
title: Bølgetrinnkoder
description: Dette emnet inneholder en oversikt over bølgetrinnkoder og hvordan de brukes.
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9332e45f7213ed815e4417969b617256778598db
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434817"
---
# <a name="wave-step-codes"></a>Bølgetrinnkoder

[!include [banner](../includes/banner.md)]

Bølgetrinnkoder er koder som brukere kan definere og bruke til å koble bestemte forekomster av bølgemetoder til en tilsvarende mal. Malene omfatter maler for etterfylling, containerbruk, etikettutskrift, lastplanlegging og sortering.

Når bølgetrinnkoder ikke brukes, må brukerne angi en fritekst for å referere til en bestemt mal fra den bølgemetodeforekomsten. Fritekst er utsatt for feil fordi brukerne må passe på at bølgestrinnteksten de legger til en bølgemal for en bestemt bølgetrinnmetode, samsvarer nøyaktig med bølgetrinnteksten i målmalen.

Bølgetrinnkoder for en bestemt bølgetrinntype konfigureres på en egen side. For alle bølgetrinnforekomster i en bølgemal som krever en bølgetrinnkode, må du velge bølgetrinnkoden i en rullegardinliste. Valg i en rullegardinliste erstatter fritekstoppføring og reduserer risikoen og innvirkningen av menneskelig feil. Oppsettkoder brukes til å koble en bølgetrinnmetode i en bølgemal til en målmal for metoden.

> [!NOTE]
> Bruk av bølgetrinnkoder-funksjonen er valgfritt. Den er aktivert i hele organisasjonen for alle juridiske enheter.

## <a name="setup-demo"></a>Installere demonstrasjon 

For denne demonstrasjonen må demonstrasjons være installert, og du må bruke demonstrasjonsdataene for firmaet **USMF**.

### <a name="enable-wave-step-codes"></a>Aktiver bølgetrinnkoder

Følg disse trinnene for å aktivere funksjonen for bølgetrinnkoder.

1. Gå til **Funksjonsbehandling**.
2. Velg dette for å aktivere funksjonen kalt **Organisasjonsomfattende bølgetrinnkode**.

Alle eksisterende bølgetrinn i fritekst i alle juridiske enheter oppgraderes til den nye strukturen. Når denne oppgraderingen er fullført for alle juridiske enheter, er funksjonen aktivert. Hvis funksjonen ikke kan aktiveres for én eller flere juridiske enheter, er ikke funksjonen aktivert for noen juridiske enheter.

Under aktivering utføres valideringer under dataoppgraderingen. Hvis oppgraderingen mislykkes, får du en feilmelding. En oppgradering kan mislykkes på grunn av følgende konflikter:

- Det finnes duplisert bølgetrinn i fritekst.
- Det finnes tilpasninger.
- Et bølgetrinn i fritekst som er knyttet til en bølgetrinnmetodeforekomst, samsvarer ikke med den forventede maltypen.

Når du har løst eventuelle konflikter som identifiseres i løpet av valideringene, kan du prøve å aktivere funksjonen på nytt.

Når funksjonen er aktivert, blir siden **Bølgetrinnkoder** (**Lagerstyring \> Oppsett \> Bølger \> Bølgetrinnkoder**) tilgjengelig. Denne siden viser en liste over bølgetrinnkodene som ble oppgradert da funksjonen Organisasjonsomfattende bølgetrinnkode ble aktivert.

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

Du utfører disse trinnene for hver juridiske enhet.
