---
title: Opprette og administrere brukere av kundeportalen
description: Dette emnet beskriver hvordan du oppretter brukerkontoer i kundeportalen og angir tillatelser for dem.
author: dasani-madipalli
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 453c6f18c689bb8bf2f6208d9181b23a2792f41a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907771"
---
# <a name="create-and-manage-customer-portal-users"></a>Opprette og administrere brukere av kundeportalen

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I standardimplementeringen kan ikke brukerne selv registrere seg på nettsteder som opprettes ved hjelp av kundeportalen. For å logge på og bruke et nettsted må brukerne inviteres av administratoren. Microsoft har med vilje blokkert muligheten for at brukere kan registrere seg selv.

Før en bruker kan bruke en nettside, må det opprettes en kontaktoppføring for denne brukeren. Denne oppføringen angir hvilken kundekonto og juridisk enhet brukeren tilhører. Denne informasjonen er viktig for å sikre at brukeren kan opprette og vise salgsordrer.

Når brukere registrerer seg selv, opprettes det automatisk kontaktoppføringer for dem. Derfor kan du ikke sikre at en bruker velger riktig kundekonto og juridisk enhet. På den annen side gjør invitasjonsprosessen at en administrator kan tilordne den riktige kundekontoen og juridiske enheten til kontaktposten før det sendes en invitasjon. Hvis du tenker på å tilpasse løsningen slik at brukerne kan registrere seg selv, må du vurdere mulige konsekvenser.

## <a name="video"></a>Video
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

Videoen [Inviter kunder til å registrere seg og bruke kundeportalen din](https://youtu.be/drGUYHX9QIQ) (vist ovenfor) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), tilgjengelig på YouTube.

## <a name="prerequisite-setup"></a>Forutsetninger for konfigurasjon

Kontakter i Power Apps-portaler lagres som poster i **Kontakter**-tabellen i Microsoft Dataverse. Med dobbeltskrivetilgang synkroniseres disse postene til Microsoft Dynamics 365 Supply Chain Management etter behov.

![Systemdiagram for kontakter i kundeportalen](media/customer-portal-contacts.png "Systemdiagram for kontakter i kundeportalen")

Før du begynner å invitere nye kunder, må du kontrollere at du har aktivert **Kontakt**-tabelltilordningen i dobbel skriving.

## <a name="the-invitation-process"></a>Invitasjonsprosessen

Hvis du vil invitere en eksisterende kontakt til kunde portalen, følger du fremgangsmåten i [Invitere kontakter til portalene dine](/powerapps/maker/portals/configure/invite-contacts) i dokumentasjonen for Power Apps-portaler.

Før du inviterer en kunde til å bli med på kundeportalen, må du kontrollere at kundens [kontaktoppføring](/powerapps/maker/portals/configure/configure-contacts) er tilgjengelig og konfigurert på følgende måte:

1. I **Firma**-feltet angir du den juridiske enheten du vil at kunden skal tilhøre i Supply Chain Management.
2. I **Kontonummer**-feltet angir du kontonummeret du vil at kunden skal ha i Supply Chain Management.

Når en kontakt er opprettet, skal du kunne se den i Supply Chain Management.

Hvis du vil ha mer informasjon, kan du se [Konfigurere en kontakt for bruk i en portal](/powerapps/maker/portals/configure/configure-contacts) i dokumentasjonen for Power Apps-portaler.

## <a name="out-of-box-web-roles-and-table-permissions"></a>Standard nettroller og tabelltillatelser

Brukerroller i Power Apps-portaler defineres av [nettroller](/powerapps/maker/portals/configure/create-web-roles) og [tabelltillatelser](/powerapps/maker/portals/configure/assign-entity-permissions). Noen få roller er definert som standard i kundeportalen. Du kan opprette nye roller, og du kan endre eller fjerne eksisterende roller.

### <a name="out-of-box-web-roles"></a>Standard nettroller

Denne delen beskriver nettrollene som leveres med kundeportalen.

Hvis du vil ha mer informasjon om hvordan du endrer de bruksklare brukerrollene, kan du se [Opprette nettroller for portaler](/powerapps/maker/portals/configure/create-web-roles) og [Legge til postbasert sikkerhet ved hjelp av tabelltillatelser for portaler](/powerapps/maker/portals/configure/assign-entity-permissions) i dokumentasjonen for Power Apps-portaler.

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
| Kunde&nbsp;X bestiller:&nbsp;Janne | Ja | Ja | Ja | Nei | Nei |
| Kunde&nbsp;X bestiller:&nbsp;Stig | Ja | Ja | Nei | Ja | Nei |
| Kunde&nbsp;Y bestiller&nbsp;Mari | Ja | Nei | Nei | Nei | Nei |

> [!NOTE]
> Selv om både Stig og Janne er kontakter som arbeider for kunde X, kan de bare se de ordrene de selv har plassert, og ingen andre. Selv om Mari har en ordre i systemet, kan hun ikke se denne ordren i kundeportalen, fordi hun er en uautorisert bruker. (I tillegg må hun ha lagt inn ordren via en annen kanal enn kundeportalen.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]