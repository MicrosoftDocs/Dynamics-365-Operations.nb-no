---
title: Konfigurer hendelsestyper for levetid
description: Microsoft Dynamics 365 Human Resources bruker livshendelsestyper til å definere hendelser for å oppdatere ansattes fordelsregistrering.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df523dd4da11e24c7b601c8f34aef24ad6cb3b18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337016"
---
# <a name="configure-life-event-types"></a>Konfigurer hendelsestyper for levetid

Dynamics 365 Human Resources bruker **livshendelsestyper** til å definere hendelser hvor det er gyldig å oppdatere ansattes fordelsregistrering, som å gifte seg eller få barn. Hver livshendelsestype-ID kan bare knyttes til én livshendelsestype. Hvis du for eksempel oppretter en **ID for livshendelse** som kalles for **Adresseendring**, som er knyttet til livshendelsetypen **Endring av ansattes adresse**, kan du ikke opprette en annen ID som kalles **Endring av ansattes adresse** og knytte den til livshendelsestypen **Endring av ansattes adresse**. Hvis en livshendelsestype ikke er knyttet til en plantype, utløser ikke livshendelsestypen en livshendelse. Hvis du vil ha mer informasjon, se [Opprett plantyper](hr-benefits-setup-plan-types.md).

## <a name="create-a-life-event-type"></a>Opprette en livshendelsestype

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Livshendelsestyper**.

2. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **ID for levetidshendelsestype** | Den unike ID-en for levetidshendelsestypen. |
   | **Beskrivelse** | En beskrivelse av livshendelsestypen. |
   | **Levetidshendelsestype** | En katalysator for å oppdatere en ansatts fordelsregistrering. Du finner en liste over livshendelser under [Livshendelser](hr-benefits-setup-payment-frequencies.md?life-events) nedenfor. |

4. Velg **Lagre**.

## <a name="view-attached-plans"></a>Vise tilnyttede planer

Du kan se en liste over planer som er knyttet til den valgte **livshendelsestypen**. Livshendelser er knyttet til en plantype, og plantyper er knyttet til en plan.

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Livshendelsestyper**.

2. Velg **Handlinger**.

3. Velg **Tilknyttede planer**.

## <a name="life-events"></a>Levetidshendelser

Du kan velge mellom følgende livshendelser når du oppretter en livshendelsestype:

| Levetidshendelse | Lokasjon | Utløser |
| --- | --- | --- |
| **Endring i sivilstand** | **Arbeider > Profil > Personlige opplysninger > Sivil status**| Endring i sivil status |
| **Endring i ansettelsesstatus** |**Arbeider > Ansettelse> Side med ansettelseslogg** | Når det gjelder ansatte som har en eksisterende ansattdetalj, utløses en livshendelse hvis du oppretter en ny ansattdetalj med en annen ansettelsesstatus.  Hvis en eksisterende ansettelsesdetalj oppdateres med en annen ansettelsesstatus, utløses også en livshendelse.  |
| **Adresseendring for ansatt** |**Arbeider > Profil > Adresser**</li><li>**Arbeider > Personlige opplysninger > Personlige kontakter > Adresse**</li></ul> | Endring i adresse. Adressen må være **Primær** for å utløse en livshendelse. |
| **Endring for avhengig** |<br><ul><li>**Arbeider > Profil > Personlige opplysninger > Personlige kontakter**/li><li>**Ansattselvbetjening**</li></ul> | Legg til en personlig kontakt som angir dem som avhengige, og angi **Gyldig fra**. Oppdater en personlig kontakts avhengige **Gyldig til**-informasjon. Relasjonen med den personlige kontakten må være underordnet, ektefelle, innenlands partner eller tidligere ektefelle.  |
| **Fødsel eller adopsjon (avhengig)** |<br><ul><li>**Arbeider > Profil > Personlige opplysninger > Personlige kontakter**</li><li>**Ansattselvbetjening > Rediger personlige detaljer > Personlige kontakter**</li></ul>| **Fødselsdato** eller **Adopsjonsdato** legges til eller oppdateres. **Fødselsdato** for barnet er obligatorisk. |
| **Dekningstap (ektefelle/samboer)** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Dekningstap | **Dekningstap** valgt for en personlig kontakt, sammen med **Gjelder fra** |
| Endring i ansettelse for samboer | **Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Ansatt** | Opprette en personlig kontakt og angi **Ansatt** til **Ja**. Oppdater en personlig kontakt og endre **Ansatt**.  |
| **Permisjon (ektefelle/samboer)** | **Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Permisjon** | Personlig kontakt opprettet og **Gyldighetsdato for permisjon** defineres. **Permisjon** for personlig kontakt oppdateres. **Gyldig dato for permisjon** for personlig kontakt oppdateres.  |
| **Endring i dekning (stilling)** |<br><ul><li>**Arbeider > Stillingstilordning > Tilordninger for arbeiderstilling**</li><li>**Stillinger > Stillinger**</li></ul>| Bytt til stillingen i tilordningspostene for arbeiderstilling. Bytte av arbeidertilordning i stillingen. |
| **Endring i dekning (lønn)** |<br><ul><li>**Arbeider > Kompensasjon > Fast plan**</li><li>**Arbeider > Personlig informasjon > Årlig fordelslønn**</li></ul>| Hvis **Fordelsbehandling > Delte parametere for personaladministrasjon > Fordeler > Årlig fordelslønn** ikke er aktivert, vil oppdatering av **Arbeider > Kompensasjon > Fast plan** opprette en livshendelse. Hvis **Fordelsbehandling > Delte parametere for personaladministrasjon > Fordeler > Årlig fordelslønn** er aktivert, vil oppdatering av **Arbeider > Personlig informasjon > Årlig fordelslønn** opprette en livshendelse. |
| **Helseforsikring (ansatt/avhengig)** | **Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Helseforsikring gjelder fra** | Hvis du legger til eller oppdaterer datoen for **Helseforsikring gjelder fra** for en personlig kontakt, opprettes denne livshendelsen. |
| **Støtte for rettskjennelse** | **Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Avhengig > Støtte for rettskjennelse** (QMSCO/QDRO) og effektive datoer | Når du oppretter en personlig kontakt, opprettes det en livshendelse hvis **Støtte for rettskjennelse** er **Ja**. Hvis du oppdaterer **Støtte for rettskjennelse** eller **Utløpsdato for rettskjennelse**, utløses også en livshendelse. |
| **Død** | **Arbeider > Profil > Personlige opplysninger > Dødsdato** | En **dødsdato** angis eller oppdateres. |
| **Forsikringsbevis** | **Arbeider > Arbeider > Versjoner > Ansettelseshistorikk > Dato for leder > Fordelsdetaljer** | **Forsikringsbarhetsbevis** settes til **Ja**. **Kontrolldato for forsikringsbarhetsbevis** er angitt. |
| **Mottaker** | **Arbeider > Profil > Personlige opplysninger > Personlige kontakter** | Det blir lagt til en personlig kontakt, og feltene **Mottaker** og **Gjelder fra** er fylt ut. Den personlige kontakten må være av typen **Barn**, **Ektefelle**, **Samboer**, **Søsken**, **Familiekontakt**, **Annen kontakt** eller **Forelder**. |
| **Helseforsikring for ansatte** | **Arbeider > Arbeider > Versjoner > Ansettelseshistorikk > Dato for leder > Fordelsdetaljer** | **Berettiget til helseforsikring** settes til **Ja**. **Gyldighetsdato for helseforsikring** endres. |
| **Fødselsdag** | **Fordelsbehandling > Behandling av endring av levetidshendelse** | Disse livshendelsene opprettes fra **Behandling av endring av levetidshendelse**. Prosessen analyserer den valgte perioden og den juridiske enheten og finner tilknyttede arbeidere. Den beregner den siste fødselsdagen og oppretter en fødselsdagslivshendelse hvis det ikke allerede er opprettet en. |
| **Endring av arbeiderrettigheter (ikke spesifikk for USA)** |<br><ul><li>**Arbeider > Ansettelse**</li><li>**Arbeider > Arbeider > Versjoner > Ansettelseshistorikk**</li></ul>| Oppretter en livshendelsestype i følgende tilfeller:<br><ul><li>Ved oppretting av et nytt ansettelsesforhold, og det finnes et tidligere ansettelsesforhold, og arbeidertypen endres.</li><li>Ved oppretting av en ny ansettelsesdetalj, og det finnes en tidligere ansettelsesdetalj, og ansettelsestypen eller ansettelseskategorien endres.</li><li>Ved oppdatering av en ansettelsespost og en annen arbeidertype er definert.</li><li>Ved oppdatering av en ansettelsesdetaljpost og en annen ansettelsestype eller -kategori er angitt.</li></ul> |
| **Ny rettighetsoverstyring (ikke spesifikk for USA)** | **Human Resources Avansert > Fordeler > Planer > Fordeler > Overstyr rettighetsregler** | Bruke Behandling av levetidshendelse<br>Oppretting av en ny overstyring av en fordelsplanberettigelse for en arbeider utløser denne livshendelsen.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Endring av Overstyr rettighetsregler (ikke spesifikk for USA)** | **Human Resources Avansert > Fordeler > Planer > Fordeler > Overstyr rettighetsregler** | Oppdatering av **Gyldig fra** eller **Gyldig til** i en overstyring av en fordelsplanberettigelse utløser denne livshendelsen. |
| **Utløp av Overstyr rettighetsregler (ikke spesifikk for USA)** | Fordelsbehandling > Behandling av endring av levetidshendelse  | Disse livshendelsene opprettes fra **Behandling av endring av levetidshendelse**. Prosessen analyserer den valgte perioden og den juridiske enheten og finner tilknyttede overstyringer av fordelsplanberettigelse. Det oppretter livshendelser hvis overstyringene er utløpt. |
| **Ny fordelsplan (ikke spesifikk for USA)** | **Human Resources Advansert > Fordeler > Planer > Ny** | Rettighetsalternativer legges til i en gjeldende plan. En ny plan med tilknyttede rettighetsalternativer legges til.</br></br>HR-personale bør kjøre Behandling av rettighet for levetidshendelse i denne forekomsten. |
| **Endring av rettighetsregel (ikke spesifikk for USA)** | **Fordelsbehandling > Rettighetsregler** | Bruke Behandling av rettighet for levetidshendelse. Logges når **BenefitEligibilityRule**-poster har følgende verdier endret: **UseEmplCategory**, **UseEmplStatus** eller **UseEmplType**. Oppdaterer bare livshendelsestransaksjoner som allerede finnes for en endret regel eller et rettighetskriterium. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
