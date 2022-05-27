---
title: Konfigurere delte parametere
description: Dette emnet forklarer hvordan du definerer personalparametere på tvers av juridiske enheter.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e59745e01905be50e6908fb9587b8afc17604382
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692121"
---
# <a name="configure-shared-parameters"></a>Konfigurere delte parametere

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du må definerte delte parametere for poster som deles på tvers av firmaer, for eksempel **Stilling**-poster. Dette emnet forklarer hvordan du definerer personalparametere på tvers av juridiske enheter.

Noen typer poster, for eksempel **Stilling**-poster, deles på tvers av firmaer. Du må sette opp delte parametere for disse postene. Siden **Delte parametere for personaladministrasjon** brukes for eksempel til å definere parametere for personale på tvers av juridiske enheter. 

På siden **Delte parametere for personaladministrasjon** grupperes parameterne i områder, basert på deres funksjonalitet. 

### <a name="settings"></a>Innstillinger
I kategorien **Identifikasjon** må du velge identifikasjonstypene som representerer identifikasjonsnumrene som er oppført på siden. Du må definere identifikasjonstyper før du kan angi identifikasjonsopplysninger for arbeidere. Informasjonen om personnummer, nasjonale ID-nummer, fremmed ID-nummer og personlig ID-kode vedlikeholdes på siden **Identifikasjonstype**. Hvis du vil definere en ny ID-type eller gå gjennom listen over eksisterende typer, går du til **Personaladministrasjon** &gt; **Koblinger** &gt; **Oppsett** &gt; **Identifikasjonstyper**. Du kan angi en enkelt kode og beskrivelse. 

I kategorien **Nummerserier** kan du velge nummerseriene som brukes for følgende poster: **personalnummer**, **stilling**, **brukerforespørsels-ID**, **I-9-dokument**, **søker**, **diskusjon**, **fordel-ID** og **personalhandling** (hvis denne posttypen er aktivert). Hvis du vil vedlikeholde nummerseriereferanser og -koder, kan du bruke listesiden **Nummerserier**. Hvis du vil finne denne siden, kan du bruke søkefunksjonen for sider. 

I kategorien **Stillinger** angi om nye stillinger er tilgjengelige for tilordning som standard:

- **Alltid** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes. Når det opprettes stillinger, blir dato og klokkeslett for **Tilgjengelig for tilordning** på i kategorien **Generelt** på **Stilling**-siden, automatisk satt til opprettelsesdato og -klokkeslett.
- **Aldri** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes. Hvis du velger dette alternativet, må du åpne **Stilling**-siden for hver nye stilling når den blir tilgjengelig. I kategorien **Generelt** angir du deretter **Tilgjengelig for tilordning**-datoen for å aktivere arbeidertilordning.

I kategorien **Avansert tilgang** kan du begrense tilgang til noe informasjon eller koblinger:

- **Begrense tilgang til arbeiderinformasjon** – Velg denne funksjonen hvis brukerne bare skal kunne vise ansattinformasjon for de juridiske enhetene de har tilgang til, og for ansatte som har ansettelse i disse juridiske enhetene.

    Når denne funksjonen er valgt, må du følge denne fremgangsmåten for å angi de riktige tillatelsene for hver bruker du vil begrense visningen for:

    1. Velg en bruker på **Brukere**-siden.
    1. Velg en rolle for brukeren. Alternativet **Tilordne organisasjoner** blir tilgjengelig.
    1. Velg **Tilordne organisasjoner**.
    1. På den nye siden velger du **Gi tilgang til bestemte organisasjoner individuelt**, og deretter velger du organisasjonene brukeren skal ha tilgang til.
    1. Gjenta trinn 2 til og med 4 for alle andre roller som brukeren har, inkludert systembrukerrollen.

    > [!NOTE]
    > Firmaene en bruker har tilgang til, må samsvare på tvers av alle brukerens roller.

- **Aktiver kompensasjonsvisning på tvers av firmaer** – Kompensasjon for ansatte tilordnes per ansatt. Noen ganger kan en ansatt være ansatt i flere juridiske enheter samtidig. Når denne funksjonen er valgt, vises kompensasjon for hver juridiske enhet i **Ansattselvbetjening** og **Lederselvbetjening** uten at det krever at du endrer juridiske enheter. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
