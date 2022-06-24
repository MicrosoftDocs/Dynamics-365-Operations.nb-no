---
title: Tom avgiftsfunksjonsliste i parametere for avgiftsberegning
description: Denne artikkelen forklarer hvordan du feilsøker et problem der listen over avgiftsfunksjoner på siden Parametere for avgiftsberegning er tom.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 0d9286ec313a270da86181ff80ddfd690a757c9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869959"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Tom avgiftsfunksjonsliste i parametere for avgiftsberegning

[!include [banner](../includes/banner.md)]


## <a name="symptom"></a>Symptom

Du har publisert en funksjon i Regulatory Configuration Service (RCS), slik at du kan bruke den i Microsoft Dynamics 365 Finance. Når du åpner Finance, går til **Avgift** \> **Oppsett** \> **Avgiftskonfigurasjon** \> **Parametere for avgiftsberegning** og prøver å velge en verdi i feltet **Navn på funksjonsoppsett**, er imidlertid listen over verdier tom.

## <a name="reason"></a>Årsak

Dette problemet oppstår vanligvis fordi Finance-miljøet og RCS-miljøet ikke er i samme leier.

### <a name="rcs-tenant"></a>RCS-leier

Følg denne fremgangsmåten for å finne ID-en til RCS-leieren.

1. Kopier hele nettadressen til RCS. URL-adressen kan for eksempel være `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. Åpne et InPrivate-vindu i nettleseren, lim inn RCS-nettadressen på adresselinjen, og velg deretter **Angi**. Du kommer til påloggingssiden, der du finner ID-en for RCS-leieren. Hvis nettadressen til påloggingssiden for eksempel er `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d`, er leier-ID-en informasjonen som vises etter `https://login.microsoftonline.com/`, eller **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>Leier-ID for Finance-miljøet

Du kan finne leier-ID-en for Finance-miljøet ved å følge samme fremgangsmåte som du fulgte for å finne RCS-leieren. Husk å kopiere og lime inn hele nettadressen til Finance-miljøet i stedet for hele nettadressen til RCS.

## <a name="resolution"></a>Løsning

Hvis de to leier-ID-ene er ulike, har du fått problemet som er beskrevet i denne artikkelen. Hvis de er like, har du fått et urelatert problem. I dette tilfellet anbefaler vi at du kontakter Microsoft Kundestøtte.

### <a name="solution-1"></a>Løsning 1

Logg RCS-miljøet på samme leier som Finance-miljøet er logget på. Opprett og publiser deretter avgiftsfunksjonen.

### <a name="solution-2"></a>Løsning 2

Del avgiftsfunksjonen med Finance-leieren i RCS.

1. I RCS går du til **Globaliseringsfunksjoner** \> **Avgiftsberegning**.
2. Velg funksjonen du vil dele, og velg deretter **Del med** i **Organisasjoner**-fanen.
3. I feltet **Domenenavn for organisasjon** angir du et navn. Du kan for eksempel angi **contoso.onmicrosoft.com**.
4. Velg **Del**.

![Del med rullegardinboksen for ekstern organisasjon.](media/ShareTaxFeature.png)
