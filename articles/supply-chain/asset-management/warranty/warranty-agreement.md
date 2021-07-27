---
title: Garantiavtaler
description: Dette emnet beskriver garantiavtaler i Aktivastyring.
author: johanhoffmann
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1f5c8ca5acab8f62637be8f6a04d982a3181ffc2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354234"
---
# <a name="warranty-agreements"></a>Garantiavtaler

[!include [banner](../../includes/banner.md)]

 


I Aktivastyring kan du definere garantibetingelser som kan knyttes til et anleggsmiddel eller en anleggsmiddeltype. Garantibetingelser opprettes for en bestemt periode. Garanti kan defineres for å gi fullstendig dekning eller delvis dekning, og du kan definere betingelser som er knyttet til timer, utgifter og varer.

Det første trinnet er å opprette eventuelle leverandørgarantiavtaler du har for utstyret ditt. Deretter knytter du garantiavtaler til anleggsmidler eller anleggsmiddeltyper. Leverandørgarantiavtaler brukes bare til informasjonsformål. Hvis det er definert en leverandørgaranti for et anleggsmiddel, kan du se garantidekningsperioden for anleggsmidlet.

## <a name="create-a-warranty-agreement"></a>Opprette en garantiavtale

En garantiavtale kan inkludere flere avtalelinjer for å dekke garantien for arbeidstimer, utgifter og varer.

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Garanti**.
2. Velg **Ny** for å opprette et produkt.
3. Angi en garanti-ID i **Garanti**-feltet. 
4. Angi en beskrivelse i **Navn**-feltet.

    I hurtigfanen **Detaljer** viser **Aktiva**-feltet antall aktive anleggsmidler som bruker garantiavtalen.

5. På hurtigfanen **Garantilinjer** følger du denne fremgangsmåten for å legge til linjer som skal tas med i en garantiavtale:

    1. Velg **Legg til linje** for å legge til en ny betingelse i garantien. Et sekvensielt linjenummer angis automatisk i feltet **Linje**.
    2. Velg type garantiperiode i **Periode**-feltet.
    3. Angi et tall i **Intervall**-feltet. Dette feltet definerer antall perioder som garantien skal være gyldig for.
    4. I **Prosent**-feltet angir du dekningsprosenten for garantilinjen. Prosentsatsen viser hvor mye som dekkes av firmaet.

![Garantiside.](media/01-warranty.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]