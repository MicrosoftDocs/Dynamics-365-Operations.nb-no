---
title: Kundeportal for Dynamics 365 Supply Chain Management – oversikt
description: Dette emnet introduserer kundeportalen og forklarer hvem som bør bruke den, samt hvordan den fungerer.
author: dasani-madipalli
manager: tfehr
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 86d9a40d991e915d3529e0c330f7559d8e7ce9ea
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529584"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Kundeportal for Dynamics 365 Supply Chain Management – oversikt

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="what-is-the-customer-portal"></a>Hva er kundeportalen?

Moderne forsyningskjedesystemer trenger integreringsfunksjoner. De krever at beholdning, kundeetterspørsel og salgsavdelinger kan integreres i stedet for å eksistere i separate siloer. Kundeportalen hjelper organisasjoner som kjører Microsoft Dynamics 365 Supply Chain Management, å forbedre denne integreringen og holde kundene oppdatert på en mer effektiv måte.

Kundeportalen er en [Power Apps-portaler](https://docs.microsoft.com/powerapps/maker/portals/overview)-mal som lar firmaer opprette et eksternt B2B-nettsted for scenarier som er relatert til behandling av salgsordrer. Malen bruker [dobbeltskriving](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), Supply Chain Management og Power Apps-portaler for å gjøre det mulig for eksterne bedriftskunder å se og opprette data fra firmaets Dynamics 365-miljø.

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
- De går over fra Dynamics AX 2012 til Supply Chain Management, og har tidligere brukt [portalen AX 2012 Customer Self-Service](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

Følgende typer organisasjoner er **ikke** gode kandidater for å implementere kundeportalen:

- Firmaer som vil bygge et nettsted for kunder som ikke er virksomheter. Disse firmaene bør vurdere å opprette et [Dynamics 365 Commerce-nettsted for e-handel](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site).
- Firmaer som allerede bruker et eksisterende Power Apps-portalnettsted til et lignende formål. Disse firmaene vil ikke få tilleggsfordeler ved å bruke kundeportalen. Kundeportalen leveres som en mal som fungerer som en veileder og et utgangspunkt for kunder som vil opprette en forbindelse mellom dobbeltskriving, Supply Chain Management og Power Apps-portaler. Hvis du allerede har konfigurert et nettsted som tjener dette formålet, er det ikke sikkert du får særlig mye igjen for å bruke kundeportalmalen til å klargjøre nettstedet på nytt.

## <a name="how-does-it-work"></a>Hvordan fungerer det?

Kundeportalen leveres som en mal for Power Apps-portaler. Den er avhengig av Power Apps-portaler og dobbeltskriving.

[Power Apps-portaler](https://docs.microsoft.com/powerapps/maker/portals/overview) er en funksjon som lar brukere opprette et eksternt nettsted som personer fra utenfor organisasjonen kan logge på. Det kreves lite eller ingen koding for å opprette portaler. Kundeportalen er én av mange [Maler for Dynamics 365-portaler](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) som er tilgjengelige fra Microsoft.

[Dobbeltskriving](https://docs.microsoft.com/powerapps/maker/portals/overview) er et integrert infrastrukturprodukt som gir nær sanntidsinteraksjon mellom modelldrevne apper i Dynamics 365 og Finance and Operations-apper. Dobbeltskriving gir toveisintegrering mellom Finance and Operations-apper og Common Data Service. Derfor gir den en integrert brukeropplevelse på tvers av appene. Kundeportalen er avhengig av enheter som er synkronisert med dobbeltskriving. Før data fra Supply Chain Management kan vises i kundeportalen, må dobbeltskriving aktiveres for alle de aktuelle enhetene.

![Avhengigheter for kundeportal](media/customer-portal-elements.png "Avhengigheter for kundeportal")

Kundeportalen fungerer som et utgangspunkt for organisasjoner som vil bruke Power Apps-portaler til å bygge et eksternt-rettet nettsted som bruker data fra organisasjonens Supply Chain Management-installasjon. Den hjelper organisasjoner med å koble sammen dobbeltskriving, Supply Chain Management og Power Apps-portaler.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]