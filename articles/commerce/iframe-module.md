---
title: Iframe-modul
description: Dette emnet dekker iFrame-modulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 58446289c9a53af30d4d6d331a1a609ae0d2a0ad
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818204"
---
# <a name="iframe-module"></a>Iframe-modul

[!include [banner](includes/banner.md)]

Dette emnet dekker iFrame-modulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En iFrame-modul gir en iFrame (innebygd ramme) som er vert for eksternt innhold på et område. Den kan for eksempel brukes til å være vert for en YouTube-video eller PDF-filvisning på en områdeside. 

En iFrame-modul krever en mål-URL-adresse. Deretter er den vert for innholdet på målsiden i et HTML **iFrame**-element. Eksterne URL-adresser må være på tillatelseslisten (også kalt "hvitelisten") i henhold til områdets sikkerhetspolicy for innhold (CSP). For iFrame-innhold bør URL-adresser tillates ved å bruke direktivet **frame-ancestor**. Hvis du vil ha mer informasjon, se [Behandle policy for innholdssikkerhet (CSP)](manage-csp.md).

> [!NOTE]
> iFrame-modulen er tilgjengelig i Dynamics 365 Commerce 10.0.13-versjonen.

Det følgende bildet viser eksempler på iFrame-moduler som viser eksterne videoer på områdesider.

![Eksempel på iFrame-moduler som viser eksterne videoer](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>Egenskaper for iFrame-modul

| Egenskapsnavn             | Verdi                 | beskrivelse |
|---------------------------|-----------------------|-------------|
| Overskrift | Tekst | Overskriften for modulen. |
| Mål-URL-adresse | URL | URL-adressen som vertsmodulen ligger i. |
| Høyde | Tall eller prosent | Høyden på modulen, i piksler eller som en prosent. Verdien **100** vil for eksempel bli behandlet som antall piksler, og verdien **100 %** vil bli behandlet som en prosent. |
| Aria-etikett | Tekst | En ARIA-etikett (Accessible Rich Internet Applications) kan defineres for tilgjengelighetsformål. |

## <a name="add-an-iframe-module-to-a-page"></a>Legg til en iFrame-modul på en side

Følg denne fremgangsmåten for å legge til en iFrame-modul på en side for å vise en ekstern video.

1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du **Markedsføringsmal**, og velger deretter **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I **Velg en mal**-dialogboksen velger du malen **Markedsføringsmal**. Under **Sidenavn** angir du **Markedsføringsside**, og velger deretter **OK**.
1. På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **iFrame**-modulen, og deretter velger du **OK**.
1. I modulens egenskapsrute angir du verdien for **Mål-URL-adresse** til en ekstern URL-adresse for en video.
1. Angi andre egenskaper, for eksempel **Overskrift** og **Høyde** etter behov.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.
1. Gå til markedsføringssiden på området. Du skal se at videoen gjengis i iFrame-modulen.
 
## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Behandle policy for innholdssikkerhet (CSP)](manage-csp.md)
