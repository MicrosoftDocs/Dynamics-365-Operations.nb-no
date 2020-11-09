---
title: Definere transportører
description: Dette emnet viser hvordan du konfigurerer en transportør og definere operasjoner, for eksempel service, forsendelsesmåte, transportbetalingsmiddel, transportbegrensninger og forsendelsessats.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a71ea3983018b136d4fe3b22eadc0c332d2a698
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016453"
---
# <a name="set-up-shipping-carriers"></a>Definere transportører

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du konfigurerer en transportør og definere operasjoner, for eksempel service, forsendelsesmåte, transportbetalingsmiddel, transportbegrensninger og forsendelsessats. En transportkoordinator kan deretter tilordne en transportør til en innkommende eller utgående last.


## <a name="create-a-new-shipping-carrier"></a>Opprett en ny transportør
1. Gå til **Navigasjonsrute > Moduler > Transportstyring > Oppsett > Transportører > Transportører**.
2. Velg **Ny** i handlingsruten.
3. Skriv inn en verdi i **Transportør** -feltet.
4. Skriv inn en verdi i **Navn** -feltet.
5. I **Modus** -feltet velger du et alternativ fra rullegardinmenyen.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Fyll ut generell informasjon om transportøren
1. Aktiver/deaktiver utvidelsen av delen **Oversikt**.
2. Merk eller fjern merket for **Aktiver transportør**.
3. I **Leverandørnummer** -feltet velger du et alternativ fra rullegardinmenyen. Velg leverandørkontoen som transportøren skal tilordnes til.  
4. Velg et alternativ i feltet **Transportbetalingsmiddel**. Velg **Manuell** for å bruke siden Transportbetalingsmiddel, eller velg **EDI** for å oppdatere betalingsmiddelet ved hjelp av utveksling av elektroniske data (EDI – Electronic Data Interchange).  
5. Merk eller fjern merket for **Aktiver transportørrangering**.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Opprett de nødvendige tjenestene for transportøren
1. Aktiver/deaktiver utvidelsen av delen **Tjenester**.
2. Velg **Ny**.
3. Skriv inn en verdi i **Transportørtjeneste** -feltet.
4. Skriv inn en verdi i **Navn** -feltet.
5. I **Transportmetode** -feltet velger du et alternativ fra rullegardinmenyen.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Definer adressen for transportør (valgfritt)
1. Aktiver/deaktiver utvidelsen av delen **Adresser**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Navn eller beskrivelse**.
4. I **Land/område** -feltet velger du et alternativ fra rullegardinmenyen.
5. I **Postnummer** -feltet velger du et alternativ fra rullegardinmenyen.
6. Skriv inn en verdi i **Gate** -feltet.
7. Velg **OK**.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Definer vurderingsprofilen for transportøren
1. Aktiver/deaktiver utvidelsen av delen **Vurderingsprofiler**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Vurderingsprofil**.
4. Skriv inn en verdi i **Navn** -feltet.
5. I **Område** -feltet velger du et alternativ fra rullegardinmenyen.
6. I **Lager** -feltet velger du et alternativ fra rullegardinmenyen.
7. I **Ratemotor** -feltet velger du et alternativ fra rullegardinmenyen. Velg ratemotoren som er i samsvar med kontrakten du har med transportøren.  
8. I **Vurderingsstandard** -feltet velger du et alternativ fra rullegardinmenyen.
9. I **Transittidmotor** -feltet velger du et alternativ fra rullegardinmenyen.
10. Velg **Lagre**.

