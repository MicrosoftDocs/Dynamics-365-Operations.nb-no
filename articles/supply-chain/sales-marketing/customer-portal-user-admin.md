---
title: Opprette og administrere brukere av kundeportalen
description: Dette emnet beskriver hvordan du oppretter brukerkontoer i kundeportalen og angir tillatelser for dem.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
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
ms.openlocfilehash: c56e41b8ea5039531205083b5b42aff05e05cf66
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413995"
---
# <a name="create-and-manage-customer-portal-users"></a>Opprette og administrere brukere av kundeportalen

I standardimplementeringen kan ikke brukerne selv registrere seg på nettsteder som opprettes ved hjelp av kundeportalen. For å logge på og bruke et nettsted må brukerne inviteres av administratoren. Microsoft har med vilje blokkert muligheten for at brukere kan registrere seg selv.

Før en bruker kan bruke en nettside, må det opprettes en kontaktoppføring for denne brukeren. Denne oppføringen angir hvilken kundekonto og juridisk enhet brukeren tilhører. Denne informasjonen er viktig for å sikre at brukeren kan opprette og vise salgsordrer.

Når brukere registrerer seg selv, opprettes det automatisk kontaktoppføringer for dem. Derfor kan du ikke sikre at en bruker velger riktig kundekonto og juridisk enhet. På den annen side gjør invitasjonsprosessen at en administrator kan tilordne den riktige kundekontoen og juridiske enheten til kontaktposten før det sendes en invitasjon. Hvis du tenker på å tilpasse løsningen slik at brukerne kan registrere seg selv, må du vurdere mulige konsekvenser.

## <a name="prerequisite-setup"></a>Forutsetninger for konfigurasjon

Kontakter i Power Apps-portaler lagres som poster i **Kontakter**-enheten i Common Data Service. Med dobbeltskrivetilgang synkroniseres disse postene til Microsoft Dynamics 365 Supply Chain Management etter behov.

![![Systemdiagram for kontakter i kundeportalen](media/customer-portal-contacts.png "Systemdiagram for kontakter i kundeportalen")](media/customer-portal-contacts.png "System diagram for Customer portal contacts")

Før du begynner å invitere nye kunder, må du kontrollere at du har aktivert **Kontakt**-enhetstilordningen i dobbeltskriving.

## <a name="the-invitation-process"></a>Invitasjonsprosessen

Hvis du vil invitere en eksisterende kontakt til kunde portalen, følger du fremgangsmåten i [Invitere kontakter til portalene dine](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) i dokumentasjonen for Power Apps-portaler.

Før du inviterer en kunde til å bli med på kundeportalen, må du kontrollere at kundens [kontaktoppføring](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) er tilgjengelig og konfigurert på følgende måte:

1. I **Firma**-feltet angir du den juridiske enheten du vil at kunden skal tilhøre i Supply Chain Management.
2. I **Kontonummer**-feltet angir du kontonummeret du vil at kunden skal ha i Supply Chain Management.

Når en kontakt er opprettet, skal du kunne se den i Supply Chain Management.

Hvis du vil ha mer informasjon, kan du se [Konfigurere en kontakt for bruk i en portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) i dokumentasjonen for Power Apps-portaler.

## <a name="out-of-box-web-roles-and-entity-permissions"></a>Standard nettroller og enhetstillatelser

Brukerroller i Power Apps-portaler defineres av [nettroller](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) og [enhetstillatelser](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions). Noen få roller er definert som standard i kundeportalen. Du kan opprette nye roller, og du kan endre eller fjerne eksisterende roller.

### <a name="out-of-box-web-roles"></a>Standard nettroller

Denne delen beskriver nettrollene som leveres med kundeportalen.

Hvis du vil ha mer informasjon om hvordan du endrer standardbrukerrollene, kan du se [Opprette nettroller for portaler](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles)og [Legge til postbasert sikkerhet ved hjelp av enhetstillatelser for portaler](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) i dokumentasjonen for Power Apps-portaler.

#### <a name="administrator"></a>Administrator

Administratoren overser og vedlikeholder nettstedet. Denne personen klargjør og konfigurerer kundeportalen. Administratoren vedlikeholder IT- og sikkerhetsaspektene ved portalen, og sørger for at alt kjører problemfritt. Administratoren kan også tilpasse og/eller endre portalen ved å legge til nye funksjoner, opprette nye roller og mer.

#### <a name="customer-representative"></a>Kunderepresentant

En kunderepresentant jobber for et kundeselskap og er ansvarlig for å administrere ordrene som firmaet legger inn. Kunderepresentanten kan se alle ordrene som er lagt inn for firmaet, samt hvilke brukere som la inn ordrene. Kunderepresentanten kan også se generell informasjon om kontoen og hvilke kontakter som kan legge inn bestillinger på vegne av denne kontoen.

#### <a name="authorized-users"></a>Autoriserte brukere

Autoriserte brukere kan legge inn ordrer og se statusen til ordrene de har lagt inn. De kan imidlertid ikke se statusen for ordrer som andre brukere i firmaet har lagt inn.

#### <a name="unauthorized-users"></a>Uautoriserte brukere

Uautoriserte brukere kan ikke se noen data. De kan bare se offentlig informasjon som for eksempel betingelser og vilkår samt detaljer om firmaet som kjører kundeportalen.

#### <a name="example"></a>Eksempel

Tabellen nedenfor viser hvilke salgsordrer brukerne har i hver enkelt nettrolle kan se i systemet.

| Salgsordre | Administrator | Kunderepresentant for kunde&nbsp;X | Autorisert bruker: Janne | Autorisert bruker: Stig | Uautorisert bruker: Mari |
|---|---|---|---|---|---|
| Kunde&nbsp;X bestiller:&nbsp;Janne | Ja | Ja | Ja | Nr. | Nr. |
| Kunde&nbsp;X bestiller:&nbsp;Stig | Ja | Ja | Nr. | Ja | Nr. |
| Kunde&nbsp;Y bestiller&nbsp;Mari | Ja | Nr. | Nr. | Nr. | Nr. |

> [!NOTE]
> Selv om både Stig og Janne er kontakter som arbeider for kunde X, kan de bare se de ordrene de selv har plassert, og ingen andre. Selv om Mari har en ordre i systemet, kan hun ikke se denne ordren i kundeportalen, fordi hun er en uautorisert bruker. (I tillegg må hun ha lagt inn ordren via en annen kanal enn kundeportalen.)
