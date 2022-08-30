---
title: Opprett en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner
description: Denne artikkelen beskriver hvordan du oppretter en Excel-arbeidsbok, slik at du kan redigere detaljhandelstransaksjoner i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: 93e0053c38c9595cab59947e4b65b0b4aa966380
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270216"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>Opprett en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter en Excel-arbeidsbok, slik at du kan redigere detaljhandelstransaksjoner i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Det finnes en forhåndsdefinert Excel-mal som kunder kan få tilgang til fra forskjellige deler av systemet, og bruke den til å redigere og kontrollere detaljhandelstransaksjoner. Kunder kan imidlertid også opprette en egendefinert Excel-arbeidsbok for dette formålet.

## <a name="create-and-configure-an-excel-workbook"></a>Opprette og konfigurere en Excel-arbeidsbok

Hvis du vil opprette og konfigurere en Excel-arbeidsbok slik at du kan redigere detaljhandelstransaksjoner, følger du disse trinnene.

1. Åpne Excel og opprett en tom arbeidsbok.
1. Velg **Mine tillegg** i fanen **Sett inn**.
1. I ruten til høyre velger du koblingen **Legg til serverinformasjon**.
1. Angi serverens URL-adresse, og velg deretter **OK**.
1. Hvis du får feil meldingen "Fant ingen appletregistreringer", kan du følge denne fremgangsmåten for å løse problemet:

    1. I Commerce kan du gå til **Systemadministrasjon \> Oppsett \> Parametere til Office-app**.
    1. Velg **Initialiser app-parametere** i hurtigfanen **App-parametere**.
    1. I bekreftelsesboksen velger du **OK**.
    1. I hurtigfanen **Registrerte appleter** velger du **Initialiser appletregistrering**.
    1. Gjenta de tre forrige trinnene etter behov.

1. Velg **Utforming**, og velg deretter **Legg til tabell**.
1. Basert på dataene som skal endres, velger du enhetene som må legges til i Excel-arbeidsboken for redigering. Bruk tabellen nedenfor som referanse.

    | Transaksjonstype | Dataenheter som skal brukes |
    |------------------|----------------------|
    | Hentesalgstransaksjoner, elektroniske ordrer, asynkrone kundeordrer, asynkrone kundetilbud | Transaksjon (kan overvåkes), salgstransaksjon (kan overvåkes), betalingstransaksjoner (kan overvåkes), mva-transaksjoner (kan overvåkes), rabattransaksjoner (kan overvåkes), gebyrtransaksjoner (kan overvåkes) |
    | Deponering til bank | Transaksjon (kan overvåkes), betalingsmiddeltransaksjoner til bank (kan overvåkes) |
    | Deponering til safe | Transaksjon (kan overvåkes), betalingsmiddeltransaksjoner til safe (kan overvåkes) |
    | Kasseoppgjør | Transaksjon (kan overvåkes), kasseoppgjørtransaksjoner (kan overvåkes) |
    | Inntekt, utgift | Transaksjon (kan overvåkes), inntekts-/utgiftstransaksjoner (kan overvåkes), betalingstransaksjoner (kan overvåkes) |
    | Deklarer startbeløp, fjerning av betalingsmiddel, flytpost, endre betalingsmiddel, fakturabetaling, kundeinnskudd | Transaksjon (kan overvåkes), betalingstransaksjoner (kan overvåkes) |

    > [!NOTE]
    > Det er viktig at du bare legger til én dataenhet i hver Excel-arbeidsbok. I tillegg må alle felt som er merket med et nøkkelsymbol, legges til i den aktuelle arbeidsboken.

1. Når arbeidsboken er konfigurert, bruker du de nødvendige filtrene. Sørg for at du bruker de samme filtrene i alle regnearkene i filen. Unngå å laste inn svært store mengder data i Excel-filen. Ellers kan ytelsen bli påvirket, og Excel og systemet mister kanskje noe av hastigheten. Det anbefales at du alltid bruker "Firma" og "Utdragsnummer" eller "Transaksjonsnummer" som filtre for filen.
1. Når filtrene er konfigurert, velger du **Oppdater** for å laste dataene.
1. Rediger de nødvendige dataene, og publiser dem deretter. Hvis knappen **Publiser** ikke er tilgjengelig, er det sannsynlig at enkelte nøkkelfelt ikke ble lagt til i Excel-arbeidsboken.

## <a name="additional-resources"></a>Tilleggsressurser

[Redigere og overvåke hentesalgs- og kassastyringstransaksjoner](edit-cash-trans.md)

[Rediger og overvåk nettordretransaksjoner og asynkrone kundeordretransaksjoner](edit-order-trans.md)

[Redigere finansdimensjoner for detaljhandelstransaksjoner](edit-financial-dim.md)

[Legge til felt i en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
