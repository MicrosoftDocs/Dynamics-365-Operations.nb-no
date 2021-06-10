---
title: Konfigurere delte parametere
description: Du må definerte delte parametere for poster som deles på tvers av firmaer, for eksempel stillingsposter. Denne artikkelen forklarer hvordan du definerer personalparametere på tvers av juridiske enheter.
author: andreabichsel
ms.date: 02/03/2020
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
ms.openlocfilehash: 888caa19a9befd32ce27b27e499cdfe88a1bbf01
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054530"
---
# <a name="configure-shared-parameters"></a>Konfigurere delte parametere

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du må definerte delte parametere for poster som deles på tvers av firmaer, for eksempel stillingsposter. Denne artikkelen forklarer hvordan du definerer personalparametere på tvers av juridiske enheter.

Noen typer poster, for eksempel stillingsposter, deles på tvers av firmaer. Du må sette opp delte parametere for disse postene. Du bruker for eksempel siden **Delte parametere for personaladministrasjon** til å definere parametere for personale på tvers av juridiske enheter. 

På siden **Delte parametere for personaladministrasjon** grupperes parameterne i områder, basert på deres funksjonalitet. 

### <a name="previously-released-functionality"></a>Tidligere utgitt funksjonalitet
I kategorien **Identifikasjon** må du velge identifikasjonstypene som representerer identifikasjonsnumrene som er oppført på siden. Du må definere identifikasjonstyper før du kan angi identifikasjonsopplysninger for arbeidere. Informasjonen om personnummer, nasjonale ID-nummer, fremmed ID-nummer og personlig ID-kode vedlikeholdes på siden **Identifikasjonstype**. Hvis du vil definere en ny ID-type eller gå gjennom listen over eksisterende typer, klikker du **Personaladministrasjon** &gt; **Koblinger** &gt; **Oppsett** &gt; **Identifikasjonstyper**. Du kan angi en enkelt kode og beskrivelse. 

### <a name="if-youre-using-dynamics-365-human-resources"></a>Hvis du bruker Dynamics 365 Human Resources
I kategorien **Identifikasjon** må du velge identifikasjonstypene som representerer identifikasjonsnumrene som er oppført på siden. Du må definere identifikasjonstyper før du kan angi identifikasjonsopplysninger for arbeidere. Informasjonen om personnummer, nasjonale ID-nummer, fremmed ID-nummer og personlig ID-kode vedlikeholdes på siden **Identifikasjonstype**. Hvis du vil definere en ny ID-type eller gå gjennom listen over eksisterende typer, klikker du **Personale** &gt; **Oppsett** &gt; **Identifikasjonstyper**. Du kan angi en enkelt kode og beskrivelse. 

I kategorien **Nummerserier** kan du velge nummerseriene som brukes for følgende poster: personalnummer, stilling, brukerforespørsels-ID, I-9-dokument, søker, diskusjon, fordel-ID og personalhandling (hvis denne posttypen er aktivert). Hvis du vil vedlikeholde nummerseriereferanser og -koder, kan du bruke listesiden **Nummerserier**. Hvis du vil finne denne siden, kan du bruke søkefunksjonen for sider. 

I kategorien **Stillinger** angi om nye stillinger er tilgjengelige for tilordning som standard:

-   **Alltid** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes. Når det opprettes stillinger, blir dato og klokkeslett for **Tilgjengelig for tilordning** på i kategorien **Generelt** på **Stilling**-siden, automatisk satt til opprettelsesdato og -klokkeslett.
-   **Aldri** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes. Hvis du velger dette alternativet, må du åpne siden **Stilling** for hver nye stilling etter hvert som de blir tilgjengelig, og deretter angi datoen for **Tilgjengelig for tilordning** i kategorien **Generelt** for å aktivere arbeidertilordning.


[!INCLUDE[footer-include](../includes/footer-banner.md)]