---
title: Organisere arbeidsstyrken ved hjelp av avdelinger, jobber og stillinger
description: Denne artikkelen beskriver konseptuell informasjon om avdelinger, jobber og stillinger, som er organisasjonselementer som vedlikeholdes i Personale.
author: twheeloc
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 0cb4e745eb6531d90a02778ba85e6caf790f2d46
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874282"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a>Organisere arbeidsstyrken ved hjelp av avdelinger, jobber og stillinger


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Avdelinger, jobber og stillinger er organisasjonselementer som vedlikeholdes i Personale. Denne artikkelen beskriver konseptuell informasjon om disse elementene. 

Eksemplet nedenfor brukes til å illustrere begreper som er beskrevet i denne artikkelen.

|**Avdeling**|**Posisjon**|**Jobb**|
|---|---|---|
|**Salg**|Salgssjef (øst)|Salgssjef|
|**Salg**|Salgssjef (vest)|Salgssjef|
|**Salg**|Salgssjef (sentralt)|Salgssjef|
|**Regnskap**|Regnskapsansvarlig|Regnskapssjef|
|**Regnskap**|Regnskap -A|Regnskapsfører|
|**Personale**|Personale (øst)|Personale|
|**Personale**|Personale (vest)|Personale|
|**Personale**|Personale (sentralt)|Personale|


##  <a name="departments"></a>Avdelinger

En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon som er ansvarlig for et bestemt område i organisasjonen, for eksempel salg eller regnskap. En avdeling som brukes til å rapportere om funksjonsområder og kan ha resultatansvar. En avdeling kan også inneholde en gruppe med kostsentre. Salg, regnskap og personale er noen eksempler på avdelinger i en organisasjon.

## <a name="jobs-and-positions"></a>Jobber og stillinger
En jobb er en samling oppgaver og ansvarsområder som kreves av en person som utfører en jobb. En stilling er én enkeltforekomst av en jobb. Ansvarsområder, jobboppgaver, jobbfunksjoner, ferdigheter, utdanningsinformasjon og sertifikater som kreves for en jobb, er også nødvendig for stillinger som er tilknyttet en jobb.

### <a name="job-tasks"></a>Jobboppgaver

Du kan opprette jobboppgaver som beskriver de grunnleggende oppgavene som må fullføres av en arbeider i en stilling for jobben. Den samme jobboppgaven kan legges til flere jobber, og stillinger for disse jobbene arver disse jobboppgavene. Eksempler på jobboppgaver er oppført i tabellen nedenfor.

| Jobb           | Jobboppgave                                                |
|---------------|-------------------------------------------------------------|
| Salgssjef | Ytelsesgjennomgang – Vurder jobbytelsen til hver enkelt selger.    |
| Regnskapsfører    | Fraværsgjennomgang – Godkjenn eller avvis fraværsforespørsler eller registreringer for hver selger. |


### <a name="job-functions"></a>Jobbfunksjoner

Jobbfunksjoner er som jobboppgaver. En jobbfunksjon beskriver en eller flere oppgaver, plikter eller ansvarsområder som er tilordnet til en jobb. Jobbtyper kan være knyttet til jobber og brukes til å definere og implementere rettighetsregler for kompensasjonsplaner. Eksempler på jobbfunksjoner er oppført i tabellen nedenfor.

| Jobb           | Jobbfunksjon                                                |
|---------------|-------------------------------------------------------------|
| Salgssjef | Adm. personer – Administrer personer som rapporterer til deg.               |
| Regnskapsfører    | Finansgjennomgang – Vedlikehold økonomiske data for et sett med kontoer. |

### <a name="job-types"></a>Jobbtyper

Bruk jobbtyper til å klassifisere lignende jobber i kategorier. Jobbtyper, på samme måte som jobbfunksjoner, kan være knyttet til jobber og brukes til å definere og implementere rettighetsregler for kompensasjonsplaner. Noen eksempler på jobbtyper er inkludert i følgende liste:
-   Heltid
-   Deltid
-   Lønn
-   Timelønn

### <a name="areas-of-responsibility"></a>Ansvarsområder

Bruk ansvarsområder for å angi arbeidsrollene, prosessene og produktene som en arbeider som er i en stilling for jobben, har ansvaret for. Et eksempel på et ansvarsområde for en jobb med navnet "Regnskap" kan være "Økonomisk rapportering for produkt A".

## <a name="positions"></a>Stillinger

Stillinger er et viktig element i det nederste nivået i et organisasjonshierarki. En stilling er én enkeltforekomst av en jobb. Stillingen "Salgssjef (øst)" er for eksempel bare én av stillingene som er knyttet til jobben "Salgssjef". Stillinger finnes i en avdeling, og tilordnes til arbeidere.
### <a name="position-creation-and-maintenance"></a>Opprettelse og vedlikehold av stilling

-   Du kan vise en logg over stillingsrelaterte systemendringer på en lett tilgjengelig listeside.
-   Du kan opprette årsakskoder som brukerne kan velge når de oppretter eller endrer stillinger.
-   Du kan opprette personalhandlingstyper og tilordne en nummerserie til personalhandlinger.
-   Du kan angi en arbeidsflyt slik stillingstillegg og -endringer kan kreve godkjenning.

### <a name="position-duration"></a>Stillingsvarighet
Hver stilling har et tidsrom som stillingen er gyldig i. Dette tidsrommet kalles varighet. Sommerstillinger kan for eksempel ha varighet fra 1. mai 2015 til 31. august 2015.

### <a name="worker-assignments"></a>Arbeidertilordninger
Når du tilordner en arbeider til en stilling, fyller du denne stillingen. Du kan tilordne arbeidere til flere stillinger, men bare én arbeider kan tilordnes til en stilling på samme tid.

### <a name="reporting-relationships"></a>Rapporteringsrelasjoner
Stillinger er viktige elementer i det nederste nivået i et organisasjonshierarki. Du kan angi stillingen en stilling rapporterer til, på **Stilling**-siden. Når du tilordner en arbeider til en stilling som rapporterer til en annen stilling, oppretter du en rapporteringsrelasjon mellom arbeidere som er tilordnet de to stillingene. Stillingen "Regnskapsfører-A" rapporterer for eksempel til stillingen "Regnskapsansvarlig". Ana Bowman tilordnes stillingen "Regnskapsansvarlig", og Felix Henderson tilordnes stillingen "Regnskapsfører-A". Det betyr at Felix Henderson rapporterer til Ana Bowman. 

Hvis organisasjonen bruker et matrisehierarki eller et annet egendefinert hierarki, kan du konfigurere stillingshierarkityper og deretter legge til rapporteringsrelasjoner i stillinger for hver hierarkitype som du definerer. Olivia Wilson er for eksempel en daglig leder hos Adventure Works, og tilordnes stillingen "Leder". Olivia administrerer utviklingen av et produkt som brukes til å rengjøre noe. Olivia trenger en regnskapsfører for å hjelpe til med økonomien for utvikling av produktet. Hun har derfor rekruttert Felix Henderson som regnskapsfører. Felix rapporterer direkte til Ana Bowman, men arbeider også sammen med Olivia Wilson på arbeidet sitt knyttet til Økonomi for å utvikle ryddeverktøyet. 

For det forrige eksemplet ville du fullført følgende oppgaver for å definere relasjonen mellom Felix Henderson og Ana Bowman:
1.  Opprett en egendefinert stillingshierarkitype kalt "Gjenstand" for å opprette et hierarki som inkluderer stillinger som er ansvarlig for å arbeide med oppryddingsproduktet.
2.  Tilordne lederstillingen til stillingen som regnskapsfører-A-stillingen rapporterer til i gjenstand-hierarkiet.

Bruk siden **Stillingshierarki** til å vise rapporteringsstrukturen til stillinger. Hvis du har flere stillingshierarkier, kan du vise hierarkiet for hver hierarkitype i **stillingshierarkiet**. Du kan også søke etter en stilling etter stillings-ID eller etter navnet på arbeideren som er tilordnet til stillingen. **Stillingshierarkiet** er et organisasjonshierarki.

## <a name="date-effective-records"></a>Poster med gyldighet fra dato
For noen poster kan du angi fremtidige endringer i posten. Følgende informasjon er gyldig dato.

<table>
<thead>
<tr class="header">
<th>Poster</th>
<th>Gyldig datoinformasjon</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Jobber</td>
<td><ul>
<li>Noe detaljert jobbinformasjon</li>
<li>Jobbklassifiseringsinformasjon</li>
<li>Kompensasjonsinformasjon</li>
</ul></td>
</tr>
<tr class="even">
<td>Posisjoner</td>
<td><ul>
<li>Noe detaljert stillingsinformasjon</li>
<li>Arbeidertilordninger</li>
<li>Stillingsvarigheter</li>
<li>Stillingshierarkier</li>
</ul></td>
</tr>
</tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
