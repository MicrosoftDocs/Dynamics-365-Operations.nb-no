---
title: Iframe-modul
description: Denne artikkelen dekker iframe-modulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e9f1804cde1010c585d53d63bc0a487bc5407552
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858943"
---
# <a name="iframe-module"></a>Iframe-modul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker iframe-modulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.

En iFrame-modul gir en iFrame (innebygd ramme) som er vert for eksternt innhold på et område. Den kan for eksempel brukes til å være vert for en YouTube-video eller PDF-filvisning på en områdeside. 

En iFrame-modul krever en mål-URL-adresse. Deretter er den vert for innholdet på målsiden i et HTML **iFrame**-element. Eksterne URL-adresser må være på tillatelseslisten i henhold til områdets sikkerhetspolicy for innhold (CSP). For iFrame-innhold bør URL-adresser tillates ved å bruke direktivet **frame-ancestor**. Hvis du vil ha mer informasjon, se [Behandle policy for innholdssikkerhet (CSP)](manage-csp.md).

> [!NOTE]
> iFrame-modulen er tilgjengelig i Dynamics 365 Commerce 10.0.13-versjonen.

Det følgende bildet viser eksempler på iFrame-moduler som viser eksterne videoer på områdesider.

![Eksempel på iFrame-moduler som viser eksterne videoer.](./media/ecommerce-iframe.PNG)

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
1. I dialogboksen **Opprett ny side**, under **Sidenavn**, angir du en **Markedsføringsside**, og velger deretter **Neste**.
1. Velg **Markedsføringsmal**-malen du opprettet, under **Velg en mal**, og velg deretter **Neste**.
1. Under **Velg et oppsett** velger du et sideoppsett (for eksempel **Fleksibelt oppsett**), og deretter velger du **Neste**.
1. Gå gjennom sidekonfigurasjonen under **Gjennomgang og fullfør**. Hvis du har behov for å redigere sideinformasjonen, velger du **Tilbake**. Hvis sideinformasjonen er riktig, velger du **Opprett side**. 
1. På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **iframe**-modulen, og deretter velger du **OK**.
1. I modulens egenskapsrute angir du verdien for **Mål-URL-adresse** til en ekstern URL-adresse for en video.
1. Angi andre egenskaper, for eksempel **Overskrift** og **Høyde** etter behov.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.
1. Gå til markedsføringssiden på området. Du skal se at videoen gjengis i iFrame-modulen.

> [!NOTE]
> Siden iFrame-modulen er vert for eksternt innhold, må forfattere på området kontrollere at innhold som er vert for en iFrame-modul, ikke bryter policyene for innholdsbegrensning i det aktuelle markedet. Hvis det er et innholdsbrudd på en side som bruker iFrame-modulen, kan forfatter av området fjerne iFrame-modulen ved å åpne siden i områdekonfiguratoren, velge **Fjern modul** i iFrame-modulsporet og deretter lagre og publisere siden på nytt.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Behandle policy for innholdssikkerhet (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
