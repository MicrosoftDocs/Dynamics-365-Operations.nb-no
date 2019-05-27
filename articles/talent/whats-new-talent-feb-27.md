---
title: Hva er nytt eller endret i Dynamics 365 for Talent (27. februar 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d8e6a02b43ad60e3a0c4382f98cb808066587da7
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518732"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-27-2019"></a>Hva er nytt eller endret i Dynamics 365 for Talent (27. februar 2019)?

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2163

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>Legge til en Egendefinerte felt-meny i systemadministrasjon

Navigasjon til **Egendefinerte felt**-menyen er lagt til i **Systemadministrasjon**-arbeidsområdet.

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>Skjule import- og opprettalternativene for nye mobilapper

For øyeblikket kan ikke nye mobilapper opprettes i Talent. Alternativet for å opprette nye mobilopplevelser er fjernet fra **Mobilapp**-menyen.

### <a name="variable-compensation-award-dmf-entity"></a>Variabel kompensasjonsbelønning (DMF-enhet)

I denne versjonen er en **Variabel kompensasjonsbelønning** for DMF-enhet (Data Management Framework) nå tilgjengelig for eksport.

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>UK-adresser vises på siden for analyse av personaladministrasjon som sveitsiske adresser

I denne versjonen vises adresser etter poststed. Denne versjonen løser problemer der visualiseringer viste feil ansattlokasjon.

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>Workforce Power BI-rapporten viser en feil når en arbeiders ansiennitetsdato er på skuddårsdag.

En løsning er gjort i Microsoft Power BI for å ta hensyn til ansiennitetsdatoer som faller på 29. februar.

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>Fast kompensasjon for ansatt, variable belønninger for ansatte, variable planer for ansatte (registreringer) tillater egendefinerte felt

Egendefinerte felt kan nå legges til for fast kompensasjon for ansatt, variable belønninger for ansatte og variable planer for ansatte (registreringer). Nå kan du spore mer informasjon om faste og variable kompensasjonsplaner for ansatte, i tillegg til informasjonen som er tilgjengelig som standard. Egendefinerte felt kan angis og oppdateres via enten brukergrensesnittet eller enhetene som angis.

### <a name="other-miscellaneous-bug-fixes"></a>Andre feilrettinger

Denne versjonen inneholder andre mindre feilrettinger.

## <a name="coming-soon"></a>Kommer snart

### <a name="advanced-compensation-security-fixed-and-variable"></a>Avansert kompensasjonssikkerhet (fast og variabel)

I mange organisasjoner kan kompensasjons- og fordelsansvarlige bare ha tilgang til bestemte kompensasjonsposter. Disse oppføringene kan være for ledere eller regionale ansatte. Med denne endringen kan HR-personale administrere og vedlikeholde kompensasjonsplanene for ulike ansattgrupper i organisasjonen. Sikkerhetsroller som kan tilordnes til faste og variable planer, bestemmer tilgangen til disse planene og ansattdataene som er knyttet til dem (for eksempel lønnsinformasjon og bonusposter). Bare rollene som har den angitte tilgangen, vil kunne behandle kompensasjon for disse ansatte.

### <a name="platform-update-24"></a>Plattform update 24

Hvis du vil ha mer informasjon om Microsoft Dynamics 365 for Finance and Operations Plattformoppdatering 24 (mars 2019), kan du se [forhåndsvisningsfunksjonene i Finance and Operations Plattformoppdatering 24 (mars 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>Gjør fast kompensasjon for ansatte tilgjengelig for fremtidige stillingstilordninger

Det er vanlig at ansatte som deltar i en organisasjon, har en fremtidig startdato. Med denne endringen kan fast kompensasjon defineres for ansatte som har fremtidige stillingstilordninger.

## <a name="known-issues"></a>Kjente problemer

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-to-finance-and-operations"></a>Endringer i Core HR-integrasjonsmalen (Talent Common Data Service til Finance and Operations)
Malen for Core HR er oppdatert til en "avansert spørringsmal". Som standard vil derfor den avanserte spørringen være tilgjengelig for prosjekter som opprettes ved hjelp av denne malen. I tillegg vil eventuelle standardfunksjoner bare være synlige i redigeringsprogrammet for avansert spørring. (Standard tilordningsfunksjoner vises som "FN" i tilordningene.)

Hvis du vil ha mer informasjon om tilordningsfeil, kan du se [Hva er nytt eller endret i Dynamics 365 for Talent Core HR (14. desember 2018)](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14).

For å bruke den nye malen oppretter du et nytt prosjekt og velger den nye Talent-integrasjonsmalen.

Bruk følgende fremgangsmåte for å oppdatere den eksisterende malen.

1. Oppdater følgende tilordninger:

    - **Jobbstillinger til stillinger:** Fjern denne tilordningen.
    - **Den overordnede jobbtilordningsoppgaven for jobbstillinger til stillinger:** Fjern denne tilordningen.
    - **Jobbstillinger til basisstilling:** Legg til en ny tilordning fra **Jobbstillinger** Common Data Service-enheten til **Basisstilling** Finance and Operations-enheten. Flytt den til plassering 7 i sekvensen.

        [![Jobbstillinger til basisstilling-tilordning](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **Jobbstillinger til stillingsdetaljer:** Legg til en ny tilordning fra **Jobbstillinger** Common Data Service-enheten til **Stillingsdetaljer** Finance and Operations-enheten. Flytt den til plassering 8 i sekvensen.

        [![Jobbstillinger til stillingsdetaljer-tilordning](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **Jobbstillinger til stillingsvarigheter:** Legg til en ny tilordning fra **Jobbstillinger** Common Data Service-enheten til **Stillingsvarigheter** Finance and Operations-enheten.

        [![Jobbstillinger til stillingsvarigheter-tilordning](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **Jobbstillinger til stillingshierarkier:** Legg til en ny tilordning fra **Jobbstillinger** Common Data Service-enheten til **Stillingshierarkier** Finance and Operations-enheten. Velg **Avansert spørring** for å gjøre den avanserte spørringen tilgjengelig for prosjektet.

       [![Avansert spørring-knapp](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. Legg til følgende tilordninger.
    
    [![Tildeling](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom = VALIDFROM cdm_validto cdm_validto = VALIDTO
       
    2. Velg **Avansert spørring og filtrering**-koblingen ved siden av **Søk**-feltet.  

    3. Finn **cdm_parentjobpositionid.cdm_jobpositionnumber**-kolonnen, og velg nedpil-knappen til høyre for den.

    4. I dialogboksen som vises, velger du **Fjern tomme**.

    5. Velg **Legg til kolonne \> Legg til betinget kolonne** for å legge til en standardverditransformering for HIERARCHYTYPENAME.

        [![Legg til betinget kolonne-kommando](./media/Add-column.png)](./media/Add-column.png)

    6. I dialogboksen **Legg til betinget kolonne** angir du **HIERARCHYTYPENAME** som navn på den nye kolonnen.
    7. I **Hvis**-delen av betingelsen velger du et felt, bruker **til** som relasjon og angir en hvilken som helst verdi. I ***Deretter**- og **Ellers**-delene av betingelsen angir du hva standardverdien skal være. I dette tilfellet angir du **Linje** i begge deler.

        [![Legg til betinget kolonne-dialogboks](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. Velg **OK** for å lukke dialogboksen **Avansert spørring og filtrering**.
    9. På siden for **Tilordningsoppgave** velger du den nye kolonnen som kilde for å opprette en annen tilordning for HIERARCHYTYPENAME.

        [![Tildeling](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)
