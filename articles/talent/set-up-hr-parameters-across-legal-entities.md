---
title: Definere parametere for Personale (HR) på tvers av juridiske enheter
description: Du må definerte delte parametere for poster som deles på tvers av firmaer, for eksempel stillingsposter. Denne artikkelen forklarer hvordan du definerer personalparametere på tvers av juridiske enheter.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: cc5acf7ba1b350ee2c91923c7de3b4780385f3ef
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "305559"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a>Definere parametere for Personale (HR) på tvers av juridiske enheter

[!include [banner](includes/banner.md)]

Du må definerte delte parametere for poster som deles på tvers av firmaer, for eksempel stillingsposter. Denne artikkelen forklarer hvordan du definerer personalparametere på tvers av juridiske enheter.

Noen typer poster, for eksempel stillingsposter, deles på tvers av firmaer. Du må sette opp delte parametere for disse postene. Du bruker for eksempel siden **Delte parametere for personaladministrasjon** til å definere parametere for personale på tvers av juridiske enheter. 

På siden **Delte parametere for personaladministrasjon** grupperes parameterne i områder, basert på deres funksjonalitet. 

### <a name="previously-released-functionality"></a>Tidligere utgitt funksjonalitet
I kategorien **Identifikasjon** må du velge identifikasjonstypene som representerer identifikasjonsnumrene som er oppført på siden. Du må definere identifikasjonstyper før du kan angi identifikasjonsopplysninger for arbeidere. Informasjonen om personnummer, nasjonale ID-nummer, fremmed ID-nummer og personlig ID-kode vedlikeholdes på siden **Identifikasjonstype**. Hvis du vil definere en ny ID-type eller gå gjennom listen over eksisterende typer, klikker du **Personaladministrasjon** &gt; **Koblinger** &gt; **Oppsett** &gt; **Identifikasjonstyper**. Du kan angi en enkelt kode og beskrivelse. 

### <a name="if-youre-using-dynamics-365-for-talent"></a>Hvis du bruker Dynamics 365 for Talent
I kategorien **Identifikasjon** må du velge identifikasjonstypene som representerer identifikasjonsnumrene som er oppført på siden. Du må definere identifikasjonstyper før du kan angi identifikasjonsopplysninger for arbeidere. Informasjonen om personnummer, nasjonale ID-nummer, fremmed ID-nummer og personlig ID-kode vedlikeholdes på siden **Identifikasjonstype**. Hvis du vil definere en ny ID-type eller gå gjennom listen over eksisterende typer, klikker du **Personale** &gt; **Oppsett** &gt; **Identifikasjonstyper**. Du kan angi en enkelt kode og beskrivelse. 

I kategorien **Nummerserier** kan du velge nummerseriene som brukes for følgende poster: personalnummer, stilling, brukerforespørsels-ID, I-9-dokument, søker, diskusjon, fordel-ID og personalhandling (hvis denne posttypen er aktivert). Hvis du vil vedlikeholde nummerseriereferanser og -koder, kan du bruke listesiden **Nummerserier**. Hvis du vil finne denne siden, kan du bruke søkefunksjonen for sider. 

I kategorien **Stillinger** angi om nye stillinger er tilgjengelige for tilordning som standard:

-   **Alltid** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes. Når det opprettes stillinger, blir dato og klokkeslett for **Tilgjengelig for tilordning** på i kategorien **Generelt** på **Stilling**-siden, automatisk satt til opprettelsesdato og -klokkeslett.
-   **Aldri** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes. Hvis du velger dette alternativet, må du åpne siden **Stilling** for hver nye stilling etter hvert som de blir tilgjengelig, og deretter angi datoen for **Tilgjengelig for tilordning** i kategorien **Generelt** for å aktivere arbeidertilordning.


<a name="additional-resources"></a>Tilleggsressurser
--------

[Definere firmaspesifikke parametere for Personale](set-up-company-specific-hr-parameters.md)



