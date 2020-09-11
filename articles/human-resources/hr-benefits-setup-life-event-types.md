---
title: Konfigurere hendelsestyper for levetid
description: Microsoft Dynamics 365 Human Resources bruker livshendelsestyper til å definere hendelser hvor det er gyldig å oppdatere ansattes fordelsregistrering.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5286bcd940f4068531bae624876c8a35e64db4c3
ms.sourcegitcommit: 9723b5ff40c84677316d71e185cf862556b32cf9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/31/2020
ms.locfileid: "3741492"
---
# <a name="configure-life-event-types"></a>Konfigurere hendelsestyper for levetid

Microsoft Dynamics 365 Human Resources bruker livshendelsestyper til å definere hendelser hvor det er gyldig å oppdatere ansattes fordelsregistrering. For eksempel bli gift eller få barn. Hver livshendelsestype-ID kan bare knyttes til én livshendelsestype. Hvis du for eksempel oppretter en ID for livslhendelse som kalles for "Adresseendring", som er knyttet til livshendelsetypen "Endring av ansattes adresse", kan du ikke opprette en annen ID som kalles fra "Endring av ansattes adresse" og knytte den til livshendelsestypen "Endring av ansattes adresse". 

Når du har opprettet livshendelsestyper, må du knytte dem til plantyper. Hvis du vil ha mer informasjon, se [Opprett plantyper](hr-benefits-setup-plan-types.md).

   > [!NOTE]
   > Når du har opprettet en livshendelse, må du knytte den til en plantype. Hvis du vil ha mer informasjon, se [Opprett plantyper](hr-benefits-setup-life-event-types.md).

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
| **Endring i ansettelsesstatus** | <ul><li>Arbeider > Ansettelse</li><li>Side med ansettelseslogg</li></ul> | Endring i ansettelsesstatus |
| **Adresseendring for ansatt** | <ul><li>Arbeider > Profil > Adresser </li><li>Arbeider > Personlige opplysninger > Personlige kontakter > Adresse</li></ul> Lagt til, redigert eller slettet adresse |
| **Endring for avhengig** | <ul><li>Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Legg til eller slett en avhengig</li><li>Ansattselvbetjening</li></ul> | Lagt til eller slettet avhengig. Relasjonen med den personlige kontakten må være underordnet, ektefelle, innenlands partner eller tidligere ektefelle. Oppdatering av **Gyldig fra**-datoen utløser livshendelsen. Hvis du ikke oppdaterer denne datoen, utløses ingen livshendelse. |
| **Fødsel eller adopsjon (avhengig)** | <ul><li>Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig</li><li>Ansattselvbetjening</li></ul> | Feltet **Adopsjonsdato** må være fylt ut. Fødselsdatoen for barnet er obligatorisk. |
| **Dekningstap (ektefelle/samboer)** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Dekningstap | **Dekningstap** valgt for en personlig kontakt, sammen med **Gjelder fra** |
| Endring i ansettelse for samboer | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Ansatt | <ul><li>Post med detaljer om avhengig opprettet og boksen **Personlig kontakt ansatt** = Ja</li><li>Boksen **Personlig kontakt ansatt** endret endret (Ja eller Nei)</li></ul> |
| **Permisjon (ektefelle/samboer)** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Permisjon | <ul><li>Post med detaljer om avhengig opprettet og **EhrLOAEffectiveDate** fylt ut</li><li>**personPrivateDetails.EhrIsLOA** er endret (Ja eller Nei)</li><li>**personPrivateDetails.EhrLOAEffectiveDate** er endret</li></ul> |
| **Endring i dekning (stilling)** | <ul><li>Arbeider > Stillingstilordning > Tilordninger for arbeiderstilling</li><li>Stillinger > Stillinger</li></ul> | <ul><li>Bytt til stillingen i tilordningspostene for arbeiderstilling</li><li>Bytte av arbeidertilordning i stillingen</li></ul> |
| **Helseforsikring (ansatt/avhengig)** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Helseforsikring gjelder fra | Blir ikke automatisk utløst når en personlig kontakt legger inn en effektiv dato. |
| **Støtte for rettskjennelse** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Avhengig > Støtte for rettskjennelse (QMSCO/QDRO) og effektive datoer | Utløser ingen automatiske oppdateringer. Den påvirker ikke rettighetene. Den registrerer en livshendelse. |
| **Død** | Arbeider > Profil > Personlige opplysninger > Dødsdato | En dødsdato er angitt |
| **Forsikringsbevis** | <ul><li>Arbeider > Arbeider > Versjoner > Ansettelseshistorikk > Dato for leder > Fordelsdetaljer</li><li> Arbeider > Ansettelse > Fordelsdetaljer > Bekreftelsesdato</li></ul> | <ul><li>En arbeider angir en bekreftelsesdato</li><li>En arbeider setter EvidenceOfInsurability-feltet til **Ja**</li></ul> |
| **Mottaker** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter | Det blir lagt til en personlig kontakt, og boksen **Mottaker** og **Gjelder fra** er fylt ut. Den personlige kontakten må være av typen **Child**, **Spouse**, **DomesticPartner**, **Sibling**, **FamilyContact**, **OtherContact**, **Parent**, **BeneficiaryEstate**, **BeneficiaryOrg** eller **BeneficiaryTrust**. |
| **Helseforsikring for ansatte** | Arbeider > Arbeider > Versjoner > Ansettelseshistorikk > Dato for leder > Fordelsdetaljer | <ul><li>**EhrMedicareEligibilityDate** er endret</li><li>**MedicareEligibile** er satt til **Ja**</li></ul> |
| **Fødselsdag** | Arbeider > Profil > Personlige opplysninger > Personlige kontakter > Detaljer om avhengig > Fødselsdato | En fødselsdato blir lagt til eller oppdatert (ikke etter Behandling av endring av levetidshendelse). Eksempel: Hvis **Alternativer for rettighet for personlig kontakt** for et barn er satt til Alder: 26 i Oppsett > Fordeler > Alternativer for rettighet for personlig kontakt, og hvis HR-personale kjører Behandling av endring av levetidshendelse en hvilken som helst dag etter at den avhengige har fylt 26 år, vises det en melding om at den avhengige ikke lenger har rett på dekning. |
| **Endring av arbeiderrettigheter (ikke spesifikk for USA)** | <ul><li>Arbeider > Ansettelse</li><li>Arbeider > Arbeider > Versjoner > Ansettelseshistorikk</li></ul> | <ul><li>Ansatttype, Ansettelseskategori eller brukerdefinerbare rettighetsfelt endres</li><li>**HcmEmploymentDetail.EhrEmploymentType**-endringer (behandles bare for *endrede* ansaettelsesdetaljposter, behandles ikke for *nye* ansettelsesposter, som ny ansettelse og avslutning)</li></ul> |
| **Ny rettighetsoverstyring (ikke spesifikk for USA)** | Human Resources Avansert > Fordeler > Planer > Fordeler > Overstyr rettighetsregler | Bruke Behandling av levetidshendelse | EhrBenefitEligibilityRuleOverride.ValidFrom |
| **Endring av Overstyr rettighetsregler (ikke spesifikk for USA)** | Human Resources Avansert > Fordeler > Planer > Fordeler > Overstyr rettighetsregler | Bruke Behandling av levetidshendelse (registrerer bare endringer i feltene **ValidFrom** og **ValidTo** under Overstyr rettighetsregler) |
| **Utløp av Overstyr rettighetsregler (ikke spesifikk for USA)** | Human Resources Avansert > Fordeler > Planer > Fordeler > Overstyr rettighetsregler | Bruke Behandling av endring av levetidshendelse. Hvis du for eksempel redigerer Overstyr utløpsdato for rettighetsregel i en plan til i dag klokken 17, et klokkeslett etter klokken 17 eller de følgende dagene, og deretter kjører Behandling av endring av levetidshendelse, vises en melding om at overstyring av rettighetsregel er utløpt. |
| **Ny fordelsplan (ikke spesifikk for USA)** | Human Resources Advansert > Fordeler > Planer > Ny | <ul><li>Rettighetsalternativer legges til i en gjeldende plan</li><li>En ny plan med tilknyttede rettighetsalternativer legges til</li></ul></br></br>HR-personale bør kjøre Behandling av rettighet for levetidshendelse i denne forekomsten. |
| **Endring av rettighetsregel (ikke spesifikk for USA)** | Human Resources Avansert > Fordeler > Regler/alternativer > Rettighetsregler | Bruke Behandling av rettighet for levetidshendelse. Logges når **EhrBenefitEligibilityRule**-poster har følgende verdier endret: **UseEmplCategory**, **UseEmplStatus** eller **UseEmplType**. Oppdaterer bare livshendelsestransaksjoner som allerede finnes for en endret regel eller et rettighetskriterium. |
