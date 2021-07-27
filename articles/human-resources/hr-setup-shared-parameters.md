---
title: Konfigurere delte parametere
description: Du må definerte delte parametere for poster som deles på tvers av firmaer, for eksempel stillingsposter. Denne artikkelen forklarer hvordan du definerer personalparametere på tvers av juridiske enheter.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7aff01bee8cadcf852ae32fd60447c68e2174a2a
ms.sourcegitcommit: 43962e6fedaf55aab2f28f53bc38a69d2ff58403
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/01/2021
ms.locfileid: "6333002"
---
# <a name="configure-shared-parameters"></a>Konfigurere delte parametere

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du må definerte delte parametere for poster som deles på tvers av firmaer, for eksempel stillingsposter. Denne artikkelen forklarer hvordan du definerer personalparametere på tvers av juridiske enheter.

Noen typer poster, for eksempel stillingsposter, deles på tvers av firmaer. Du må sette opp delte parametere for disse postene. Du bruker for eksempel siden **Delte parametere for personaladministrasjon** til å definere parametere for personale på tvers av juridiske enheter. 

På siden **Delte parametere for personaladministrasjon** grupperes parameterne i områder, basert på deres funksjonalitet. 

### <a name="settings"></a>Innstillinger
I kategorien **Identifikasjon** må du velge identifikasjonstypene som representerer identifikasjonsnumrene som er oppført på siden. Du må definere identifikasjonstyper før du kan angi identifikasjonsopplysninger for arbeidere. Informasjonen om personnummer, nasjonale ID-nummer, fremmed ID-nummer og personlig ID-kode vedlikeholdes på siden **Identifikasjonstype**. Hvis du vil definere en ny ID-type eller gå gjennom listen over eksisterende typer, klikker du **Personaladministrasjon** &gt; **Koblinger** &gt; **Oppsett** &gt; **Identifikasjonstyper**. Du kan angi en enkelt kode og beskrivelse. 

I kategorien **Nummerserier** kan du velge nummerseriene som brukes for følgende poster: personalnummer, stilling, brukerforespørsels-ID, I-9-dokument, søker, diskusjon, fordel-ID og personalhandling (hvis denne posttypen er aktivert). Hvis du vil vedlikeholde nummerseriereferanser og -koder, kan du bruke listesiden **Nummerserier**. Hvis du vil finne denne siden, kan du bruke søkefunksjonen for sider. 

I kategorien **Stillinger** angi om nye stillinger er tilgjengelige for tilordning som standard:

- **Alltid** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes. Når det opprettes stillinger, blir dato og klokkeslett for **Tilgjengelig for tilordning** på i kategorien **Generelt** på **Stilling**-siden, automatisk satt til opprettelsesdato og -klokkeslett.
- **Aldri** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes. Hvis du velger dette alternativet, må du åpne **Stilling**-siden for hver nye stilling når den blir tilgjengelig. I kategorien **Generelt** angir du deretter **Tilgjengelig for tilordning**-datoen for å aktivere arbeidertilordning.

I kategorien **Avansert tilgang** kan du begrense tilgang til noe informasjon eller koblinger:

- **Begrense tilgang til arbeiderinformasjon** – Slå på denne funksjonen hvis brukerne bare skal kunne vise ansattinformasjon for de juridiske enhetene de har tilgang til, og for ansatte som har ansettelse i disse juridiske enhetene.

    Når denne funksjonen er aktivert, må du følge denne fremgangsmåten for å angi de riktige tillatelsene for hver bruker du vil begrense visningen for:

    1. Velg en bruker på **Brukere**-siden.
    1. Velg en rolle for brukeren. Alternativet **Tilordne organisasjoner** blir tilgjengelig.
    1. Velg **Tilordne organisasjoner**.
    1. På den nye siden velger du **Gi tilgang til bestemte organisasjoner individuelt**, og deretter velger du organisasjonene brukeren skal ha tilgang til.
    1. Gjenta trinn 2 til og med 4 for alle andre roller som brukeren har, inkludert systembrukerrollen.

    > [!NOTE]
    > Firmaene en bruker har tilgang til, må samsvare på tvers av alle brukerens roller.

- **Aktiver kompensasjonsvisning på tvers av firmaer** – Kompensasjon for ansatte tilordnes per ansatt. Noen ganger kan en ansatt være ansatt i flere juridiske enheter samtidig. Når denne funksjonen er aktivert, vises kompensasjon for hver juridiske enhet i Ansattselvbetjening og Lederselvbetjening uten at det krever at du endrer juridiske enheter. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
