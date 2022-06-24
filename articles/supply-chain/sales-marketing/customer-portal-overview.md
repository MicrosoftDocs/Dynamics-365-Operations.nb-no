---
title: Oversikt over kundeportal for Dynamics 365 Supply Chain Management (inneholder video)
description: Denne artikkelen introduserer kundeportalen og forklarer hvem som bør bruke den, samt hvordan den fungerer.
author: Henrikan
ms.date: 06/16/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ff074e62489fe74f0c2de6dae0e02d1da7e7f6ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901915"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Kundeportal for Dynamics 365 Supply Chain Management – oversikt

[!include [banner](../includes/banner.md)]


## <a name="what-is-the-customer-portal"></a>Hva er kundeportalen?

Moderne forsyningskjedesystemer trenger integreringsfunksjoner. De krever at beholdning, kundeetterspørsel og salgsavdelinger kan integreres i stedet for å eksistere i separate siloer. Kundeportalen hjelper organisasjoner som kjører Microsoft Dynamics 365 Supply Chain Management, å forbedre denne integreringen og holde kundene oppdatert på en mer effektiv måte.

Kundeportalen er en [Power Apps-portaler](/powerapps/maker/portals/overview)-mal som lar firmaer opprette et eksternt B2B-nettsted for scenarier som er relatert til behandling av salgsordrer. Malen bruker [dobbeltskriving](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md), Supply Chain Management og Power Apps-portaler for å gjøre det mulig for eksterne bedriftskunder å se og opprette data fra firmaets Dynamics 365-miljø.

Kundeportalmalen har alle tilpasningsmulighetene som portalfunksjonen i Power Apps tilbyr. Malen kan enkelt tilpasses for å representere firmaets merkevare, legge til ekstra funksjonalitet og endre brukeropplevelsen. Alle funksjonene som malen tilbyr som standard, kan endres etter behov.

> [!IMPORTANT]
> Det kan ikke forventes at malen er helt funksjonell i seg selv. Den fungerer bare som en mulighet for kunder som vil opprette et eksternt-rettet nettsted slik at bedriftskunder kan bruke data fra Supply Chain Management.

> [!NOTE]
> Dokumentasjonen for kundeportalen er rettet mot administratorer, tilpassere og systemintegratorer som vil konfigurere kundeportalen for en Supply Chain Management-installasjon. Den bruker begrepene _kunde_ og _bruker_ for å beskrive personer som er kunder av organisasjonen som kjører Supply Chain Management, og som kommer til å bruke den endelige portalen.

## <a name="video"></a>Video

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

Videoen [Oversikt over kundeportalmalen i Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) (vist over) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.

## <a name="who-should-use-it"></a>Hvem bør bruke den?

Kundeportalen er utviklet for firmaer som bruker Supply Chain Management og har følgende karakteristikker:

- De bør bygge et eksternt-rettet nettsted som kommuniserer informasjon om ordrebehandling (for eksempel ordrestatus eller kontoinformasjon) direkte fra Supply Chain Management-systemet til bedriftens kunder.
- De går over fra Dynamics AX 2012 til Supply Chain Management, og har tidligere brukt [portalen AX 2012 Customer Self-Service](/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

Følgende typer organisasjoner er **ikke** gode kandidater for å implementere kundeportalen:

- Firmaer som vil bygge et nettsted for kunder som ikke er virksomheter. Disse firmaene bør vurdere å opprette et [Dynamics 365 Commerce-nettsted for e-handel](../../commerce/create-ecommerce-site.md).
- Firmaer som allerede bruker et eksisterende Power Apps-portalnettsted til et lignende formål. Disse firmaene vil ikke få tilleggsfordeler ved å bruke kundeportalen. Kundeportalen leveres som en mal som fungerer som en veileder og et utgangspunkt for kunder som vil opprette en forbindelse mellom dobbeltskriving, Supply Chain Management og Power Apps-portaler. Hvis du allerede har konfigurert et nettsted som tjener dette formålet, er det ikke sikkert du får særlig mye igjen for å bruke kundeportalmalen til å klargjøre nettstedet på nytt.

## <a name="how-does-it-work"></a>Hvordan fungerer det?

Kundeportalen leveres som en mal for Power Apps-portaler. Den er avhengig av Power Apps-portaler og dobbeltskriving.

[Power Apps-portaler](/powerapps/maker/portals/overview) er en funksjon som lar brukere opprette et eksternt nettsted som personer fra utenfor organisasjonen kan logge på. Det kreves lite eller ingen koding for å opprette portaler. Kundeportalen er én av mange [Maler for Dynamics 365-portaler](/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) som er tilgjengelige fra Microsoft.

[Dobbel skriving](/powerapps/maker/portals/overview) er et bruksklart infrastrukturprodukt som gir interaksjon med minimal forsinkelse mellom Customer Engagement-apper og Finance and Operations-apper. Dobbel skriving gir toveisintegrering mellom Finance and Operations-apper og Microsoft Dataverse. Derfor gir den en integrert brukeropplevelse på tvers av appene. Kundeportalen er avhengig av tabeller som er synkronisert med dobbel skriving. Før data fra Supply Chain Management kan vises i kundeportalen, må dobbel skriving aktiveres for alle de aktuelle tabellene.

![Avhengigheter for kundeportal.](media/customer-portal-elements.png "Avhengigheter for kundeportal")

Kundeportalen fungerer som et utgangspunkt for organisasjoner som vil bruke Power Apps-portaler til å bygge et eksternt-rettet nettsted som bruker data fra organisasjonens Supply Chain Management-installasjon. Den hjelper organisasjoner med å koble sammen dobbeltskriving, Supply Chain Management og Power Apps-portaler.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]