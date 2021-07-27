---
title: Stillinger
description: Dette emnet beskriver de konseptuelle elementene som en stilling kan inkludere. Det gir også eksempler som viser hvordan du kan bruke disse elementene i organisasjonen.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b44cfaedc4e1286d033bba49b54a12b7e096bf99
ms.sourcegitcommit: 43962e6fedaf55aab2f28f53bc38a69d2ff58403
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/01/2021
ms.locfileid: "6333139"
---
# <a name="positions"></a>Stillinger

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver de konseptuelle elementene som en stilling kan inkludere. Det gir også eksempler som viser hvordan du kan bruke disse elementene i organisasjonen.

Før du kan opprette en stilling, må du definere en jobb. Enkelte stillingsdetaljer, for eksempel kompensasjonsområdet, arbeidsoppgaven, stillingsvarigheten og rapporteringsrelasjonen, er datoeffektive.

## <a name="general-information"></a>Generell informasjon

Når du oppretter en stilling, må du velge en jobb. Følgende informasjon fylles automatisk ut fra jobben du velger:

- beskrivelse
- Stillingstittel
- Fulltidsekvivalent
- Jobbserie

Stillingstittelen brukes til å referere til tittelen til en ansatt. (Tittelen som er oppført på den ansatte, brukes ikke.) Derfor bør stillingstitlene standardiseres så mye som mulig.

> [!NOTE]
> En arbeider kan ikke tilordnes til en stilling på en dato som er før tilgjengelig tilordningsdato.
>
> En parameter i kategorien **Stillinger** på siden **Delte parametere for Human Resources** styrer virkemåten til tilordning av arbeider. Velg én av følgende verdier:
>
> - **Alltid** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes. Når det opprettes stillinger, blir dato og klokkeslett for **Tilgjengelig for tilordning** på i kategorien **Generelt** på **Stilling**-siden, automatisk satt til opprettelsesdato og -klokkeslett.
> - **Aldri** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes. Hvis du velger dette alternativet, må du åpne **Stilling**-siden for hver nye stilling når den blir tilgjengelig. I kategorien **Generelt** angir du deretter **Tilgjengelig for tilordning**-datoen for å aktivere arbeidertilordning. Hvis du velger dette alternativet, blir tilordningsdatoen for arbeideren satt til **Aldri** som standard når du prøver å tilordne arbeideren.

## <a name="position-duration"></a>Stillingsvarighet

Hver stilling har gyldighet i en bestemt tidsperiode som kalles varighet. Sommerstillinger kan for eksempel ha varighet fra 1. mai 2021 til 31. august 2021. Aktiveringsdatoen er datoen stillingen er aktiv i systemet. Avgangsdatoen er datoen når stillingen ikke lenger er aktiv i systemet.

Legg merke til at verken tilgjengelig tilordningsdato eller tilordningsdato for arbeider kan være før aktiveringsdatoen. En stilling vurderes ikke som aktiv før aktiveringsdatoen er nådd. Dessuten kan ikke en arbeidertilordning gå utover avgangsdatoen til stillingen.

## <a name="reports-to-position"></a>Rapporterer til stilling

Stillinger er viktige elementer i det nederste nivået i et organisasjonshierarki. Du kan angi stillingen en stilling rapporterer til, på **Stilling**-siden. Når du tilordner en arbeider til en stilling som rapporterer til en annen stilling, oppretter du en rapporteringsrelasjon mellom arbeidere som er tilordnet de to stillingene. Stilling 000220 rapporter for eksempel til stilling 000300. Kim Akers tilordnes stillingen 000220, og Sanjay Patel tilordnes stillingen 000300. Derfor rapporterer Kim Akers til Sanjay Patel.

> [!TIP]
> Rapporterer til stillingen brukes i hele systemet for å bestemme hvem en ansatts overordnede er. I det forrige eksemplet, hvis lederrollen er tilordnet Sanjay Patel i systemet, vil han se Kim Akers som en direkterapport i Lederselvbetjening. Rapporteringsrelasjonen kan også brukes når du oppretter arbeidsflytrutingsregler og kontrollisteoppgaver.

## <a name="relationships"></a>Relasjoner

Hvis organisasjonen bruker et matrisehierarki eller et annet egendefinert hierarki, kan du definere stillingshierarkityper. Du kan deretter legge til rapporteringsrelasjoner i stillinger for hver hierarkitype du definerer. Lori Penor er for eksempel en daglig leder hos Adventure Works, og tilordnes stillingen **Leder**. Lori administrerer utviklingen av et produkt som brukes til å rengjøre noe. Hun trenger en regnskapsfører for å hjelpe henne med økonomien. Hun har derfor rekruttert Kim Akers som hennes regnskapsfører. Kim rapporterer direkte til Sanjay Patel, men arbeider også sammen med Lori Penor på arbeid som er knyttet til Økonomi for å utvikle ryddeverktøyet.

For det forrige eksemplet måtte du fullført følgende oppgaver for å definere relasjonen mellom Kim Akers og Lori Penor:

1. Opprett en egendefinert stillingshierarkitype kalt **Gjenstand** for å opprette et hierarki som inkluderer stillinger som er ansvarlig for å arbeide med oppryddingsproduktet.
2. Angi **Leder**-stillingen til stillingen som stillingen Kims stilling rapporterer til i **Gjenstand**-hierarkiet.
3. Bruk stillingshierarkiet til å vise rapporteringsstrukturen til stillinger. Hvis du har flere stillingshierarkier, kan du vise hierarkiet for hver hierarkitype i stillingshierarkiet. Du kan også søke etter en stilling etter stillings-ID eller etter navnet på arbeideren som er tilordnet til stillingen. Stillingshierarkiet er et organisasjonshierarki.

## <a name="labor-union"></a>Fagforening

Du kan registrere om det kreves en fagforeningsavtale for stillingen, og hvilken arbeidsorganisasjon som brukes. Du kan også knytte avtalen til en juridisk enhet.

## <a name="financial-dimensions"></a>Finansdimensjoner

Når du oppretter finansdimensjonen for en stilling, må du angi en juridisk enhet. Du kan velge standarddimensjonene for hver dimensjon individuelt. Du kan også velge en distribusjonsmal for å fylle ut standarddimensjoner automatisk. En distribusjonsmal gir også muligheten til å fordele beløp på tvers av flere dimensjonsverdier.
