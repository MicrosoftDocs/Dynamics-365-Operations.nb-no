---
title: Spore endringer i rekrutteringsdata
description: Med prosessovervåkingsfunksjonen kan du spore når kandidater, ledige stillinger eller stillingssøknader endres for rapporterings- eller overholdelseshensyn.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: c009f82e69bff0e4ea540514de8f9e60eca1e466
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462156"
---
# <a name="track-changes-in-recruiting-data"></a>Spore endringer i rekrutteringsdata

[!include [banner](includes/banner.md)]

Du kan spore endringer som gjøres i kandidater, ledige stillinger eller stillingssøknader ved hjelp av overvåkingsbehandling. Dette er nyttig for rapporterings- eller overholdelsesårsaker.

Du kan vise de sporede dataene i Power BI ved hjelp av OData-koblingen. Hvis du vil ha mer informasjon, se [Koble til OData-feeder i Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-connect-odata).

## <a name="track-changes"></a>Spor endringer
Følg denne fremgangsmåten for å konfigurere sporing av endringer i rekrutteringsdata:

1. I [Power Apps](https://web.powerapps.com) velger du det aktuelle miljøet.

2. Velg **Innstillinger** (tannhjulikonet), velg **Avanserte tilpassinger**, og velg deretter **Ressurser** under **Utviklerressurser**. 

3. På siden **Utviklerressurser** kopierer du verdien i feltet **Web-API-verdi for forekomst**. Verdien kan for eksempel se slik ut: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. Du kan deretter foreta en spørring mot dataene fra en av følgende enheter:
  - Logg for ledig stilling (msdyn_jobopeninghistories)
  - Logg for stillingssøknad (msdyn_jobapplicationhistories) 
  - Kandidatlogg (msdyn_candidatehistories)

## <a name="data-reported"></a>Data rapportert

Følgende data er tilgjengelige med prosessovervåking.

| Data rapportert | Beskrivelse |
| --- | --- |
| Endret av (msdyn_ChangedbyId) | Referanse til bruker |
| Opprettet den (createdon) |  Dato og klokkeslett i UTC da endringen skjedde |
| Endringstype (msdyn_changetype) | Hvilken endring skjedde |
| Vanlige verdier for kandidater, ledige stillinger <br></br>og stillingssøknader | Opprettet<br></br>Oppdatert |
| Logg for stillingssøknad | Artefakt lagt til <br></br>Artefakt fjernet |
| Logg for ledig stilling | GJØREMÅL: post lagt til <br></br>GJØREMÅL: post fjernet <br></br>GJØREMÅL: post oppdatert <br></br>GJØREMÅL: deltager lagt til <br></br>GJØREMÅL: deltaker fjernet |
| Kandidatlogg | Artefakt lagt til <br></br>Artefakt fjernet <br></br>Arbeidserfaring lagt til <br></br>Arbeidserfaring fjernet <br></br>Utdannelse lagt til <br></br>Utdannelse fjernet <br></br>Kompetanse lagt til <br></br>Kompetanse fjernet <br></br>Merke lagt til <br></br>Merke fjernet <br></br>Sosialt nettverk lagt til <br></br>Sosialt nettverk fjernet <br></br>Personopplysninger lagt til <br></br>Personopplysninger oppdatert<br></br> |
| Endrede felt (msdyn_changedfields) | JSON-objekt som viser endrede felt, kan kanskje ikke lagre verdier for alle felt.<br></br><br></br>For endringer av typen opprettet og oppdatert vises feltene i den opprettede eller endrede posten.<br></br><br></br>Når det gjelder endringstypen lagt til, vises feltene i den underordnede posten.<br></br><br></br>**Eksempel:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>} |
|Logg for stillingssøknad | Stillingssøknad (msdyn_JobapplicatonId)<br></br>Status (msdyn_status) <br></br>Statusårsak (msdyn_statusreason) <br></br>Avvisningsårsak (msdyn_rejectionreason) |
| Logg for ledig stilling | Ledig stilling (msdyn_JobopeningId) <br></br>Status (msdyn_jobopeningstatus) <br></br>Statusårsak (msdyn_jobopeningstatusreason) |
| Kandidatlogg | Kandidat (msdyn_CandidateId) |
