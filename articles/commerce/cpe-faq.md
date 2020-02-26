---
title: Vanlige spørsmål om miljø for forhåndsvisning av Dynamics 365 Commerce
description: Dette emnet gir svar på vanlige spørsmål om Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljøet.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 061a160380e500ea52afbc35f0a95fe84d971bcf
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024758"
---
# <a name="dynamics-365-commerce-preview-environment-faq"></a>Vanlige spørsmål om miljø for forhåndsvisning av Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Dette emnet gir svar på vanlige spørsmål om Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljøet.

**Kan jeg overføre invitasjonen for forhåndsvisningsmiljøet i Commerce til en annen leier?**

Ja. For invitasjonsoverføringer kan du bruke [skjemaet for overføring av Commerce-forhåndsvisning](https://aka.ms/Dynamics365CommercePreviewTransferForm).

**Hvor lang tid tar invitasjonsoverføringen?**

Overføringen tar i gjennomsnitt omtrent tre til fem virkedager. Unntak kan imidlertid gjelde.

**Fungerer forhåndsvisningsmiljøet for Commerce med Dynamics 365 Finance eller Dynamics 365 Supply Chain-prosjekter**

Nr. Forhåndsvisningsmiljøet for Commerce fungerer bare med Dynamics 365 Retail-prosjekter.

**Kan vi bruke Commerce-forhåndsvisningsmiljøet som en e-handel-butikkfasade for kunder som for tiden implementerer Retail?**

Nr. Forhåndsvisningsmiljøet for Commerce er bare evalueringsmiljøet. Hvis du trenger et miljø for en kunde som implementerer Retail, kan du kontakte Microsoft.

**Kan forhåndsvisningsmiljøet for Commerce brukes til å klargjøre e-handelsfunksjonene oppå et eksisterende program/miljø som implementerer Retail?**

Nr. Forhåndsvisningsmiljøet for Commerce er for øyeblikket bare tilgjengelig i nye miljøer som ble distribuert på Retail-lagerenheter for SKU-prosjekter som har demonstrasjonsdata fra versjon 10.0.6.

**Hvilke kostnader er involvert i distribusjon av forhåndsvisningsmiljøet for Commerce på Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**

Retail er den eneste komponenten som driftes i abonnementet. Andre komponenter, for eksempel Retail Cloud Scale Unit (RCSU) og e-handel, blir driftet i Microsoft-abonnementer. Du kan bruke [Azure prising-kalkulatoren](https://azure.microsoft.com/pricing/calculator/) til å estimere denne kostnaden.

**Hvilke Azure-områder støttes for øyeblikket for forhåndsvisningsmiljøet i Commerce?**

Forhåndsvisningsmiljøet for Commerce kan bare distribueres i Nord-Amerika-området.

**Finnes det en nedlastbar virtuell harddisk (VHD) som har det komplette alternativet for OneBox virtuell maskin (VM)?**

Dynamics 365 Retail Cloud Scale Unit (RCSU) og e-handel er fullstendig programvare som en tjeneste (SaaS) og må være skybasert.

**Hvor lenge kan forhåndsvisningsmiljøet for Commerce brukes?**

Forhåndsvisningsmiljøet for Commerce har en 30-dagers tidsbegrensning fra datoen for klargjøring av e-handel.

**Kan jeg forlenge tidsbegrensningen for forhåndsvisningsmiljøet i Commerce?**

Ja. Du kan kontakte kundestøtteteamet ved hjelp av [skjemaet for utvidelse av Commerce-forhåndsvisning](https://aka.ms/Dynamics365CommercePreviewExtensionForm).

**Kan vi foreta flere forespørsler om et forhåndsvisningsmiljø for Commerce?**

Vi gir en kvote på ett miljø for Commerce-forhåndsvisning for hver forespørsel som godtas. Hvis du trenger mer enn ett forhåndsvisningsmiljø, kontakter du Microsoft. Se neste del for kontaktinformasjon.

## <a name="dynamics-365-commerce-preview-environment-contact-information"></a>Kontaktinformasjon for Dynamics 365 Commerce-forhåndsvisningsmiljø

Hvis du vil kontakte Microsoft med spørsmål eller forespørsler som er relatert til forhåndsvisningsmiljøet i Commerce, kan du gå til [Microsoft Dynamics 365 Commerce Yammer-gruppen for forhåndsvisning](https://aka.ms/Dynamics365CommercePreviewYammer) for å få hjelp.

Hvis du får problemer når du prøver å få tilgang til Yammer-gruppen, kan du kontakte Microsoft via e-post på <Dynamics365Commerce@microsoft.com>. Denne e-postadressen overvåkes ikke aktivt. Forvent derfor en forsinkelse i svaret.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over miljø for forhåndsvisning av Dynamics 365 Commerce](cpe-overview.md)

[Klargjøre et miljø for forhåndsvisning av Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurere et miljø for forhåndsvisning av Dynamics 365 Commerce](cpe-post-provisioning.md)

[Konfigurere valgfrie funksjoner for et miljø for forhåndsvisning av Dynamics 365 Commerce](cpe-optional-features.md)
