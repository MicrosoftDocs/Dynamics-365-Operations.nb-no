---
title: Opprydding av ER-overføring
description: Dette emnet beskriver hvordan du kan bruke funksjonen for ER-overføringsopprydding til å løse problemer med ER-maler.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: edb60f247b2bd6cc4ecd514e3e85bafbb681788d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686374"
---
# <a name="er-migration-cleanup"></a>Opprydding av ER-overføring 

[!include[banner](../includes/banner.md)]

Når du administrerer dine Finance-forekomster, kan det hende du vil overføre gjeldende forekomst til en annen plassering. Du kan for eksempel overføre produksjonsforekomsten til et nytt sandkassemiljø. Hvis du har konfigurert ER-rammeverket (elektronisk rapportering) til å lagre maler i Microsoft Azure Blob Storage, refererer **DocuValue**-tabellen i det nye sandkassemiljøet til forekomsten av Blob Storage i produksjonsmiljøet. Denne forekomsten er imidlertid ikke tilgjengelig fra sandkassemiljøet, fordi overføringsprosessen ikke støtter overføring av artefakter i Blob Storage. Det forventes imidlertid at du i det nye sandkassemiljøet refererer til forekomsten av BLOB Storage i sandkassemiljøet som ennå ikke henter ER-malene.

Hvis du prøver å kjøre et ER-format som bruker en mal til å generere forretningsdokumenter, oppstår det et unntak, og du blir varslet om den manglende malen. Du blir også veiledet til å bruke alternativet for opprydding av ER-overføring til å slette og deretter importere ER-formatkonfigurasjonen som inneholder malen.

[![Kjøre et ER-format](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

Du får en lignende feil hvis du går til **Konfigurasjoner**-siden (**Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**) og i konfigurasjonstreet prøver å slette en ER-formatkonfigurasjon som bruker en mal.

[![Slette et ER-format](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

Fullfør følgende fremgangsmåte for å løse problemer med ER-maler du ikke har tilgang til.

1.  Gå til siden **Organisasjonsstyring** \> **Periodisk** \> **Overføringsopprydding**-siden.
2.  Velg en ER-formatkonfigurasjon som ikke kan utføres eller slettes.
3.  Velg **Slett**.
4.  Bekreft slettingen av valgt ER-formatkonfigurasjon.
5.  [Importer](download-electronic-reporting-configuration-lcs.md) den slettede ER-formatkonfigurasjonen til gjeldende Finance-forekomst.

## <a name="applicability"></a>Relevans

> [Viktig] **Overføringsopprydding** er bare målrettet for ER-formatkonfigurasjoner som inneholder ER-maler som ikke er tilgjengelige. Når du sletter en ER-formatkonfigurasjon ved å bruke alternativet **Overføringsopprydding**, sletter ER maler som er relatert til konfigurasjonsartefaktene i den eneste programdatabasen. Eksistensen av de nødvendige fysiske filene i Blob Storage blir ikke validert. I stedet antas det at det ikke finnes noen. Du må derfor ikke bruke alternativet for **Overføringsopprydding** som et alternativ til ER-konfigurasjonssletting på **Konfigurasjoner**-siden. Bruk alternativet for **Overføringsopprydding** bare når ER-konfigurasjonssletting på **Konfigurasjoner**-siden mislykkes.
>
> Hvis du bruker alternativet for **Overføringsopprydding** for å slette en ER-formatkonfigurasjon når den refererte malen er tilgjengelig i Blob Storage, sletter du bare relaterte konfigurasjonsartefakter i programdatabasen. Den fysiske filen for malen i Blob-lageret blir værende. Filoverskriving i Blob Storage er ikke lenger tillatt. Hvis du vil ha mer informasjon, kan du se [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217). I tillegg vil du ikke lenger kunne importere konfigurasjonene som er slettet, på nytt ved hjelp av overføringsopprydding i dette miljøet. Hvis du vil løse dette problemet, må du finne den tilsvarende filen i Blob Storage og slette den manuelt.

[![Importere et ER-format](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

Det kan oppstå et lignende problem hvis du overfører programforekomsten til en annen plassering som er brukt som et overføringsmål mer enn én gang, og der BLOB Storage allerede inneholder ER-malfiler.

Fordi du kan ha flere ER-formatkonfigurasjoner kan denne prosessen være tidkrevende. Derfor er bruk av funksjonen [Sikkerhetskopiere ER-maler](er-backup-storage-templates.md) til å gjenopprette maler med brutte referanser automatisk, foretrukket.
