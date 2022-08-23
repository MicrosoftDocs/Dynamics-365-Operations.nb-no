---
title: Opprette et nytt produkthierarki
description: Denne artikkelen beskriver hvordan du oppretter et nytt produkthierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 54a29381bb9231766d76b653904339d4bd60c257
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270134"
---
# <a name="create-a-new-product-hierarchy"></a>Opprette et nytt produkthierarki


[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter et nytt produkthierarki i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Dynamics 365 Commerce støtter flere kanaler for detaljhandel. Disse detaljhandelskanalene omfatter nettbutikker, telefonsentre og detaljhandelsbutikker (også kalt fysiske butikker). Hver detaljhandelsbutikkanal kan ha sine egne betalingsmåter, prisgrupper, salgsstedskasser, inntekts- og utgiftskontoer og ansatte. Du må sette opp alle disse elementene før du kan opprette en detaljhandelsbutikkanal. 

Et handelsprodukthierarki brukes til å definere det overordnede hovedprodukthierarkiet for organisasjonen. Du kan bruke et handelsprodukthierarki for varehandel, prissetting og kampanjer, rapportering og planlegging av sortimentet. Bare ett handelsprodukthierarki kan tilordnes per organisasjon.

## <a name="create-and-configure-a-product-hierarchy"></a>Opprette og konfigurere et produkthierarki

Hvis du vil opprette og konfigurere et handelsprodukthierarki, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Handelsprodukthierarki**.
1. Hvis det ikke finnes noe hierarki enda, går du til **Handlingsrute** og velger **Nytt** for å opprette roten til hierarkiet.
1. Under **Generelt**:
    1. I **Navn**-boksen angir du et navn.
    1. I **Beskrivelse**-boksen angir du en beskrivelse.
    1. I **Brukervennlig navn**-boksen angir du et brukervennlig navn.
    1. Sett **Aktivt** til **Ja**.

## <a name="add-hierarchy-nodes"></a>Legge til hierarkinoder

Hvis du vil legge til hierarkinoder, følger du disse trinnene.

1. I handlingsruten velger du **Rediger kategorihierarki**.
1. Velg den overordnede noden du vil legge til en ny node for, og velg deretter **Ny kategorinode**.
1. I **Generelt**-delen oppgir du **Navn**, **Beskrivelse**, **Brukervennlig navn** og **Nøkkelord**.
1. Under **Generelt**:
    1. I **Navn**-boksen angir du et navn.
    1. I **Beskrivelse**-boksen angir du en beskrivelse.
    1. I **Brukervennlig navn**-boksen angir du et brukervennlig navn.
    1. I **Nøkkelord**-boksen angir du relevante nøkkelord.
    1. I **Visningsrekkefølge**-boksen angir du et nummer for visningsrekkefølgen (valgfritt).
1. Velg **Lagre** i handlingsruten.
1. Gjenta trinnene ovenfor for å legge til flere noder.

Bildet nedenfor viser opprettelsen av en ny produkthierarkinode.

![Opprett produkthierarki.](media/create-product-hierarchy.png)

## <a name="other-settings"></a>Andre innstillinger

Kategoriattributtgrupper kan også tilordnes til hver gruppe etter behov.  

## <a name="additional-resources"></a>Tilleggsressurser

[Commerce-hierarkier](retail-hierarchies.md)

[Administrere produktkategorier og produkter ](category-management-product-creation.md)

[Endre sorteringsrekkefølgen for varehandelsenheter](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
