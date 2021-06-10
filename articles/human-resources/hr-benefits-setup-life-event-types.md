---
title: Konfigurere hendelsestyper for levetid
description: Microsoft Dynamics 365 Human Resources bruker livshendelsestyper til å definere hendelser hvor det er gyldig å oppdatere ansattes fordelsregistrering.
author: andreabichsel
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 821e11d6ee22cb560b3d23017c7c332f80d41c18
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057652"
---
# <a name="configure-life-event-types"></a>Konfigurere hendelsestyper for levetid

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources bruker livshendelsestyper til å definere hendelser hvor det er gyldig å oppdatere ansattes fordelsregistrering, som å gifte seg eller få barn. Hver livshendelsestype-ID kan bare knyttes til én livshendelsestype. Hvis du for eksempel oppretter en ID for livslhendelse som kalles for "Adresseendring", som er knyttet til livshendelsetypen "Endring av ansattes adresse", kan du ikke opprette en annen ID som kalles fra "Endring av ansattes adresse" og knytte den til livshendelsestypen "Endring av ansattes adresse". Hvis en livshendelsestype ikke er knyttet til en plantype, utløser ikke livshendelsestypen en livshendelse. Hvis du vil ha mer informasjon, se [Opprett plantyper](hr-benefits-setup-plan-types.md).

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

Du kan se en liste over planer som er knyttet til den valgte livshendelsestypen. Livshendelser er knyttet til en plantype, og plantyper er knyttet til en plan.

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Livshendelsestyper**.

2. Velg **Handlinger**.

3. Velg **Tilknyttede planer**.

## <a name="life-events"></a>Levetidshendelser

Du kan velge mellom følgende livshendelser når du oppretter en livshendelsestype:

| Levetidshendelse | Lokasjon | Utløser |
| --- | --- | --- |
| **Endring i sivilstand** | Arbeider > Profil > Personlige opplysninger > Sivil status| Endring i sivil status |
| **Endring i ansettelsesstatus** | Arbeider > Ansettelse<br>Side med ansettelseslogg | Når det gjelder ansatte som har en eksisterende ansattdetalj, utløses en livshendelse hvis du oppretter en ny ansattdetalj med en annen ansettelsesstatus.  Hvis en eksisterende ansettelsesdetalj oppdateres med en annen ansettelsesstatus, utløses også en livshendelse.  |
| **Adresseendring for ansatt** | Arbeider > Profil > Adresser<br>Arbeider > Personlige opplysninger > Personlige kontakter > Adresse | Endring i adresse. Adressen må være primær for å utløse en livshendelse. |
| **Endring for avhengig** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter<br>Ansattselvbetjening | Legg til en personlig kontakt som angir dem som avhengige, og angi **Gyldig fra**. Oppdater en personlig kontakts avhengige **Gyldig til**-informasjon. Relasjonen med den personlige kontakten må være underordnet, ektefelle, innenlands partner eller tidligere ektefelle.  |
| **Fødsel eller adopsjon (avhengig)** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter<br>Ansattselvbetjening > Rediger personlige detaljer > Personlige kontakter | **Fødselsdato** eller **Adopsjonsdato** legges til eller oppdateres. **Fødselsdato** for barnet er obligatorisk. |
| **Dekningstap (ektefelle/samboer)** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Dekningstap | **Dekningstap** valgt for en personlig kontakt, sammen med **Gjelder fra** |
| Endring i ansettelse for samboer | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Ansatt | Opprette en personlig kontakt og angi **Ansatt** til **Ja**. Oppdater en personlig kontakt og endre **Ansatt**.  |
| **Permisjon (ektefelle/samboer)** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Permisjon | Personlig kontakt opprettet og **Gyldighetsdato for permisjon** defineres. **Permisjon** for personlig kontakt oppdateres. **Gyldig dato for permisjon** for personlig kontakt oppdateres.  |
| **Endring i dekning (stilling)** | Arbeider > Stillingstilordning > Tilordninger for arbeiderstilling<br>Stillinger > Stillinger | Bytt til stillingen i tilordningspostene for arbeiderstilling. Bytte av arbeidertilordning i stillingen. |
| **Endring i dekning (lønn)** | Arbeider > Kompensasjon > Fast plan<br>Arbeider > Personlig informasjon > Årlig fordelslønn | Hvis Fordelsbehandling > Delte parametere for personaladministrasjon > Fordeler > Årlig fordelslønn er ikke aktivert, oppdaterer arbeider > Kompensasjon > Fast plan vil opprette en livshendelse. Hvis Fordelsbehandling > Delte parametere for personaladministrasjon > Fordeler > Årlig fordelslønn er aktivert, oppdaterer arbeider > Personlig informasjon > Årlig fordelslønn vil opprette en livshendelse. |
| **Helseforsikring (ansatt/avhengig)** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Helseforsikring gjelder fra | Hvis du legger til eller oppdaterer datoen for **Helseforsikring gjelder fra** for en personlig kontakt, opprettes denne livshendelsen. |
| **Støtte for rettskjennelse** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Avhengig > Støtte for rettskjennelse (QMSCO/QDRO) og effektive datoer | Når du oppretter en personlig kontakt, opprettes det en livshendelse hvis **Støtte for rettskjennelse** er **Ja**. Hvis du oppdaterer **Støtte for rettskjennelse** eller **Utløpsdato for rettskjennelse**, utløses også en livshendelse. |
| **Død** | Arbeider > Profil > Personlige opplysninger > Dødsdato | En dødsdato angis eller oppdateres. |
| **Forsikringsbevis** | Arbeider > Arbeider > Versjoner > Ansettelseshistorikk > Dato for leder > Fordelsdetaljer | **Forsikringsbarhetsbevis** settes til **Ja**. **Kontrolldato for forsikringsbarhetsbevis** er angitt. |
| **Mottaker** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter | Det blir lagt til en personlig kontakt, og boksen **Mottaker** og **Gjelder fra** er fylt ut. Den personlige kontakten må være av typen **Barn**, **Ektefelle**, **Samboer**, **Søsken**, **Familiekontakt**, **Annen kontakt** eller **Forelder**. |
| **Helseforsikring for ansatte** | Arbeider > Arbeider > Versjoner > Ansettelseshistorikk > Dato for leder > Fordelsdetaljer | **Berettiget til helseforsikring** settes til **Ja**. **Gyldighetsdato for helseforsikring** endres. |
| **Fødselsdag** | Fordelsbehandling > Behandling av endring av levetidshendelse | Disse livshendelsene opprettes fra **Behandling av endring av levetidshendelse**. Prosessen analyserer den valgte perioden og den juridiske enheten og finner tilknyttede arbeidere. Den beregner den siste fødselsdagen og oppretter en fødselsdagslivshendelse hvis det ikke allerede er opprettet en. |
| **Endring av arbeiderrettigheter (ikke spesifikk for USA)** | Arbeider > Ansettelse<br>Arbeider > Arbeider > Versjoner > Ansettelseshistorikk | Oppretter en livshendelsestype i følgende tilfeller:<br><ul><li>Ved oppretting av et nytt ansettelsesforhold, og det finnes et tidligere ansettelsesforhold, og arbeidertypen endres.</li><li>Ved oppretting av en ny ansettelsesdetalj, og det finnes en tidligere ansettelsesdetalj, og ansettelsestypen eller ansettelseskategorien endres.</li><li>Ved oppdatering av en ansettelsespost og en annen arbeidertype er definert.</li><li>Ved oppdatering av en ansettelsesdetaljpost og en annen ansettelsestype eller -kategori er angitt.</li></ul> |
| **Ny rettighetsoverstyring (ikke spesifikk for USA)** | Human Resources Avansert > Fordeler > Planer > Fordeler > Overstyr rettighetsregler | Bruke Behandling av levetidshendelse<br>Oppretting av en ny overstyring av en fordelsplanberettigelse for en arbeider utløser denne livshendelsen.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Endring av Overstyr rettighetsregler (ikke spesifikk for USA)** | Human Resources Avansert > Fordeler > Planer > Fordeler > Overstyr rettighetsregler | Oppdatering av **Gyldig fra** eller **Gyldig til** i en overstyring av en fordelsplanberettigelse utløser denne livshendelsen. |
| **Utløp av Overstyr rettighetsregler (ikke spesifikk for USA)** | Fordelsbehandling > Behandling av endring av levetidshendelse  | Disse livshendelsene opprettes fra **Behandling av endring av levetidshendelse**. Prosessen analyserer den valgte perioden og den juridiske enheten og finner tilknyttede overstyringer av fordelsplanberettigelse. Det oppretter livshendelser hvis overstyringene er utløpt. |
| **Ny fordelsplan (ikke spesifikk for USA)** | Human Resources Advansert > Fordeler > Planer > Ny | Rettighetsalternativer legges til i en gjeldende plan. En ny plan med tilknyttede rettighetsalternativer legges til.</br></br>HR-personale bør kjøre Behandling av rettighet for levetidshendelse i denne forekomsten. |
| **Endring av rettighetsregel (ikke spesifikk for USA)** | Fordelsbehandling > Rettighetsregler | Bruke Behandling av rettighet for levetidshendelse. Logges når **BenefitEligibilityRule**-poster har følgende verdier endret: **UseEmplCategory**, **UseEmplStatus** eller **UseEmplType**. Oppdaterer bare livshendelsestransaksjoner som allerede finnes for en endret regel eller et rettighetskriterium. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]