---
title: Installere, konfigurere og oppdatere kundeportalen
description: Denne artikkelen inneholder lisensdetaljer og konfigurasjonsinstruksjoner for kundeportalen.
author: Henrikan
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8344212e66cb57ea8c9d4e8c2cdfbf022bc199c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850590"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Installere, konfigurere og oppdatere kundeportalen

[!include [banner](../includes/banner.md)]


## <a name="licensing-requirements"></a>Lisenskrav

For å implementere kundeportalen må du ha følgende lisenser:

- **Power Apps-portaler** – denne lisensen kreves for å være vert for kundeportalen. Portaler lisensieres basert på bruk. Du finner mer informasjon i [Lisenskrav for Power Apps-portaler](/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Dobbel skriving** – Du må ha de nødvendige lisensene for å kunne bruke to dobbel skriving for Supply Chain Management-tabeller. Hvis du vil ha mer informasjon, kan du se [systemkravene for dobbeltskriving](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Avhengigheter for dobbeltskriving og Power Apps-portaler

Kundeportalen er avhengig av Power Apps-portaler og dobbeltskriving, som vist i følgende illustrasjon.

![Avhengigheter for kundeportal.](media/customer-portal-elements.png "Avhengigheter for kundeportal")

Til forskjell fra andre funksjoner fra Supply Chain Management, ligger kundeportalmalen i Power Apps-portaler. Kundeportalen er derfor begrenset av funksjonaliteten og mulighetene som leveres av Power Apps-portaler og tabellene i dobbeltskriving.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Nødvendig konfigurasjon for å aktivere kundeportalen

Når du er sikker på at du har de nødvendige lisensene, kan du konfigurere dobbeltskriving som beskrevet i [instruksjoner for innledende synkronisering med dobbeltskriving](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-entity-map.md).

Pass på at du aktiverer følgende tabelltilordninger i dobbel skriving:

- Overskrift for salgsordre
- Salgsordredetaljer
- kontakter
- Kontakter
- Produkter

Når denne installasjonen er fullført, kan du klargjøre kundeportalmalen.

## <a name="provision-the-customer-portal"></a>Klargjøre kundeportalen

Før du begynner, må du kontrollere at du allerede har fullført [den nødvendige konfigurasjonen](#required-setup). Deretter følger du disse trinnene for å klargjøre kundeportalen.

1. Gå til [make.powerapps.com](https://make.powerapps.com/).
2. Kontroller at du bruker miljøet der du har aktivert dobbeltskriving.
3. I **Opprett**-fanen ruller du ned til **Start fra mal**-delen og velger malen som heter **Kundeportal**.
4. Følg instruksjonene på skjermen.

Når klargjøringen er fullført, får du tilgang til kundeportalen i **Dine apper**-delen av **Hjem**-siden.

> [!NOTE]
> Hvis du ikke har installert dobbeltskriveløsningen i miljøet du arbeider i, vil du få en feilmelding, og kundeportalen blir ikke klargjort.

## <a name="update-the-customer-portal"></a>Oppdatere kundeportalen

Du kan legge til flere funksjoner i kundeportalen senere. Alle endringer som Microsoft gjør i de underliggende løsningskomponentene, vises automatisk i miljøet ditt. Nettstedet som er klargjort i miljøet ditt, vil imidlertid ikke automatisk gjenspeile endringer som gjøres i konfigurasjonsdataene. Du må ta i bruk disse endringene manuelt ved å hente koden fra den nye malen og flette den sammen med det klargjorte nettstedet.

## <a name="additional-resources"></a>Tilleggsressurser

Hvis du vil lære hvordan du kan definere og tilpasse kundeportalen, bør du starte med å se gjennom følgende dokumentasjon for den underliggende teknologien:

- [Dokumentasjon for Power Apps-portaler](/powerapps/maker/portals/overview)
- [Dokumentasjon for dobbel skriving](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

For å administrere portalene effektivt må du forstå Power Apps-portalene og Microsoft Dataverse-livssyklusen. Hvis du vil ha mer informasjon, kan du se følgende ressurser:

- [Om portalens livssyklus](/powerapps/maker/portals/admin/portal-lifecycle)
- [Oppgradere en portal](/powerapps/maker/portals/admin/upgrade-portal)
- [Overføre en portalkonfigurasjon](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Administrasjon livssyklus for løsning: Dynamics 365 for Customer Engagement-apper](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]