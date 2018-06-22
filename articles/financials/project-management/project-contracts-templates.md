---
title: Synkroniser prosjektkontrakter fra Project Service Automation direkte til prosjektkontrakter i Finance and Operations
description: "Dette emnet beskriver malen og underliggende oppgaver som brukes til å synkronisere prosjektkontrakter og prosjekter direkte fra Microsoft Dynamics 365 for Project Service Automation til Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 8d8e3268ae8c612bad87c3c6416f223219149ee6
ms.contentlocale: nb-no
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-contracts-and-projects-from-project-service-automation-directly-to-project-contracts-and-projects-in-finance-and-operations"></a>Synkroniser prosjektkontrakter fra prosjekter fra Project Service Automation direkte til prosjektkontrakter og prosjekter i Finance and Operations

Dette emnet beskriver malen og underliggende oppgaver som brukes til å synkronisere prosjektkontrakter og prosjekter direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE] 
> Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, må du installere KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Dataflyt for Project Service Automation til Finance and Operations

> [!NOTE]
> Før du kan bruke Project Service Automation til Finance and Operations-integrasjonsløsningen, bør du være kjent med Dynamics 365-dataintegrasjonsfunksjonen.

Project Service Automation til Finance and Operations-integrasjonsløsningen bruker dataintegrasjonsfunksjonen til å synkronisere data på tvers av Project Service Automation og Finance and Operations. Integrasjonsmalen som er tilgjengelig i dataintegreringsfunksjonen, muliggjør flyt av data om prosjektkontrakter, prosjekter, prosjektkontraktlinjer og milepæler på prosjektkontraktlinjer fra Project Service Automation til Finance and Operations.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance and Operations.

[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Maler og oppgaver

For å få tilgang til de tilgjengelige malene velg **Prosjekter** i administrasjonssenter for Microsoft PowerApps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.

Følgende mal og underliggende oppgaver brukes til å synkronisere prosjektkontrakter og prosjekter fra Project Service Automation til Finance and Operations:

- **Navnet på malen i Dataintegrering:** Prosjekter og kontrakter (PSA til Fin and Ops)
- **Navn på oppgavene i prosjektet:**

  - Prosjektkontrakter PSA til Fin and Ops
  - Prosjekter PSA til Fin and Ops
  - Prosjektkontraktlinjer PSA til Fin and Ops
  - Milepæler på prosjektkontraktlinje PSA til Fin and Ops

Før synkronisering av prosjektkontrakter og prosjekter kan skje må du synkronisere kontoer.

## <a name="entity-set"></a>Enhetssett

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| Ordre                           | Integreringsenhet for prosjektkontrakt.                |
| Prosjekter                         | Integreringsenhet for prosjekt.                         |
| Ordrelinjer                      | Integreringsenhet for prosjektkontraktlinje.          |
| Milepæler for prosjektkontraktlinje | Integreringsenhet for milepæl for prosjektkontraktlinje. |

## <a name="entity-flow"></a>Enhetsflyt

Prosjektkontrakter administreres i Project Service Automation, og de synkroniseres til Finance and Operations som prosjektkontrakter. Som en del av malen integrering kan du angi integrasjonskilden i Finance and Operations for prosjektkontrakten.

Etter regning- og fast pris-prosjekter administreres i Project Service Automation, og de synkroniseres til Finance and Operations som prosjekter. Som en del av malen integrering kan du angi integrasjonskilden i Finance and Operations for prosjektet.

Prosjektkontraktlinjer administreres i Project Service Automation, og de synkroniseres til Finance and Operations som faktureringsregler for prosjektkontrakt. Synkroniseringen vil oppdatere prosjekttypen for kontraktlinjeprosjektet for prosjektgruppen hvis metoden for fakturering er forskjellig fra standard prosjekttype.

Milepæler for prosjektkontraktlinjer administreres i Project Service Automation, og de synkroniseres til Finance and Operations som milepæler for prosjektkontraktfakturering.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Project Service Automation til Finance and Operations-integrasjonsløsning

**Prosjektkontrakt-ID**-feltet er tilgjengelig på **Prosjektkontrakter**-siden. Dette feltet er gjort til en naturlig og unik nøkkel for å støtte integreringen.

Når en ny prosjektkontrakt opprettes, og hvis en **Prosjektkontrakt-ID**-verdi ikke finnes fra før, genereres den automatisk ved hjelp av en nummerserie. Verdien består av **ORD**, etterfulgt av en stigende nummerserie og et suffiks på seks tegn. Her er et eksempel: **ORD-01022-Z4M9Q0**.

**Prosjektnummer**-feltet er bare tilgjengelig på **Prosjekter**-siden. Dette feltet er gjort til en naturlig og unik nøkkel for å støtte integreringen.

Når et nytt prosjekt opprettes, og hvis en **Prosjektnummer**-verdi ikke finnes fra før, genereres den automatisk ved hjelp av en nummerserie. Verdien består av **PRJ**, etterfulgt av en stigende nummerserie og et suffiks på seks tegn. Her er et eksempel: **PRJ-01049-CCNID0**.

Når Project Service Automation til Finance and Operations-integrasjonsløsningen brukes<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, angir et oppgraderingsskript **Prosjektkontrakt-ID**-feltet for eksisterende prosjektkontrakter og **Prosjektnummer**-feltet for eksisterende prosjekter i Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

- Før synkronisering av prosjektkontrakter og prosjekter kan skje må du synkronisere kontoer.
- I tilkoblingssettet, legg til et integreringsnøkkelfelttilordning for **msdyn\_organizationalunits** til **msdyn\_name \[Name\]**. Du må kanskje først legge til et prosjekt i tilkoblingssettet. Hvis du vil ha mer informasjon om integreringsnøkler, kan du se Dynamics 365-dataintegrasjon.
- I tilkoblingssettet, legg til et integreringsnøkkelfelttilordning for **msdyn\_projects** til **msdynce\_projectnumber \[Project Number\]**. Du må kanskje først legge til et prosjekt i tilkoblingssettet. Hvis du vil ha mer informasjon om integreringsnøkler, kan du se Dynamics 365-dataintegrasjon.
- **SourceDataID** for prosjektkontrakter og prosjekter kan oppdateres til en annen verdi eller fjernes fra tilordningen. Standardmalverdien er **Project Service Automation**.
- **PaymentTerms**-tilordningen må oppdateres, slik at den gjenspeiler gyldige betalingsbetingelser i Finance and Operations. Du kan også fjerne tilordningen fra prosjektoppgaven. Standard verditilordning har standardverdier for demonstrasjonsdata. Tabellen nedenfor viser verdiene i Project Service Automation.

    | Verdi | beskrivelse   |
    |-------|---------------|
    | 1     | Netto 30        |
    | 2     | 2%10, netto 30 |
    | 3     | Netto 45        |
    | 4     | Netto 60        |

## <a name="power-query"></a>Power Query
Du må bruke Microsoft Power Query til å filtrere data hvis følgende betingelser er oppfylt:

- Du har salgsordrer i Microsoft Dynamics 365 for Sales.
- Du har flere organisasjonsenheter i Project Service Automation, og disse organisasjonsenhetene skal tilordnes til flere juridiske enheter i Finance and Operations.

Hvis du må bruke Power Query, følger du disse retningslinjene:

- Prosjektkontraktmalene (PSA til Fin and Ops) har et standardfilter som inkluderer bare salgsordrer av typen **Arbeidselement (msdyn\_ordertype = 192350001)**. Dette filteret sikrer at prosjektkontrakter ikke opprettes for salgsordrer i Finance and Operations. Hvis du oppretter din egen mal, må du legge til dette filteret.
- Du må opprette et Power Query-filter som inkluderer bare kontraktorganisasjoner som skal synkroniseres med den juridiske enheten for integreringstilkoblingssettet. For eksempel prosjektkontrakter som du har med kontraktorganisasjonsenheten for Contoso US, må synkroniseres til den juridiske enheten USSI, men prosjektkontrakter som du har med kontraktorganisasjonsenheten for Contoso Global, må synkroniseres til den juridiske enheten USMF. Hvis du ikke legger til dette filteret i oppgavetilordningen, synkroniseres alle prosjektkontrakter til den juridiske enheten som er definert for tilkoblingssettet, uavhengig av kontraktsorganisasjonsenheten.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

> [!NOTE] 
> Feltene **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** og **AddressZipCode** er ikke inkludert i standardtilordningen for prosjektkontrakter. Du kan legge til tilordningen hvis du krever at disse dataene skal synkroniseres for prosjektkontrakter.
> Feltene **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** og **ProjectType** er ikke inkludert i standardtilordningen for prosjekter. Du kan legge til tilordningene hvis du krever at disse dataene skal synkroniseres for prosjekter.

Illustrasjonen nedenfor viser eksempler på maloppgavetilordningene i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.

[![Tilordning av mal](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Tilordning av mal](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Tilordning av mal](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Tilordning av mal](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

