---
title: Sikkerhetskopiere ER-maler
description: Dette emnet beskriver hvordan du bruker sikkerhetskopier for elektronisk rapportering (ER) for gjenoppretting av maler.
author: NickSelin
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 932ba44b4223bf9c9d93ffb19e17f6e57bb303b5
ms.sourcegitcommit: bbb64b3475eef155b3f9d1bdc440545da8a7182f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553097"
---
# <a name="backup-storage-of-er-templates"></a>Sikkerhetskopiere ER-maler

[!include [banner](../includes/banner.md)]

[Rammeverket for elektronisk rapportering (ER)](general-electronic-reporting.md) lar bedriftsbrukere konfigurere formater for utgående dokumenter i overensstemmelse med de juridiske kravene i ulike land. Konfigurerte ER-formater kan bruke forhåndsdefinerte maler til å generere utgående dokumenter i forskjellige formater, for eksempel Microsoft Excel-regneark, Microsoft Word-dokumenter eller PDF-dokumenter. Malene er fylt ut med data som kreves av den konfigurerte dataflyten for genererte dokumenter.

Hvert konfigurerte format kan publiseres som en del av en ER-løsning. Hver enkelt ER-løsning kan eksporteres fra en forekomst av Finance and Operations og importeres til en annen forekomst.

ER-rammeverket bruker [dokumentbehandlingsrammeverket](../../fin-ops/organization-administration/configure-document-management.md) til å beholde de nødvendige malene for gjeldende Finance and Operations-forekomsten. Avhengig av innstillingene for ER-rammeverket kan Microsoft Azure Blob Storage eller en Microsoft SharePoint-mappe velges som fysisk primær lagringsplassering for maler. (Hvis du vil ha mer informasjon, kan du se [Konfigurere ER-rammeverket](electronic-reporting-er-configure-parameters.md).) DocuValue-tabellen inneholder en enkeltpost for hver mal. I hver post lagrer feltet **AccessInformation** banen til en malfil som er plassert på den konfigurerte lagringsplasseringen.

Når du administrerer dine Finance and Operations-forekomster, kan det hende du vil overføre gjeldende forekomst til en annen plassering. Du kan for eksempel overføre produksjonsforekomsten til et nytt sandkassemiljø. Hvis du har konfigurert ER-rammeverket til å lagre maler i Blob Storage, refererer DocuValue-tabellen i det nye sandkassemiljøet til forekomsten av Blob Storage i produksjonsmiljøet. Denne forekomsten er imidlertid ikke tilgjengelig fra sandkassemiljøet, fordi overføringsprosessen ikke støtter overføring av artefakter i Blob Storage. Hvis du prøver å kjøre et ER-format som bruker en mal til å generere forretningsdokumenter, oppstår det derfor et unntak, og du blir varslet om den manglende malen. Du blir også veiledet til å bruke ER-oppryddingsverktøyet til å slette og deretter importere på nytt ER-formatkonfigurasjonen som inneholder malen. Fordi du kan ha flere ER-formatkonfigurasjoner kan denne prosessen være tidkrevende.

Funksjonen for sikkerhetskopiering av ER-maler kan hjelpe deg med å sørge for at malene dine alltid er tilgjengelige for generering av forretningsdokumenter.

> [!NOTE]
> Denne funksjonen kan bare brukes når Blob Storage er valgt som fysisk lagringsplassering for ER-maler.

For denne funksjonen blir alle maler i en ny ER-formatkonfigurasjon i gjeldende miljø, automatisk lagret til lagringsplasseringen for sikkerhetskopier av maler (databasetabellen ERDocuDatabaseStorage) når følgende hendelser oppstår:

- Du importerer en ny ER-formatkonfigurasjon som inneholder en mal.
- Du fullfører utkastversjonen av en ER-formatkonfigurasjon som inneholder en mal.

Sikkerhetskopier av maler overføres til en ny forekomst av Finance and Operations som en del av programdatabasen.

Hvis en mal med et ER-format er nødvendig for generering av utgående dokumenter, for eksempel for å behandle leverandørbetalinger inkludert generering av betalingsmelding og kontrollrapporter, men den nødvendige malen ikke finnes på den primære lagringsplassen, oppstår følgende hendelser:

- Hvis malen er tilgjengelig på lagringsplasseringen for sikkerhetskopier, hentes den automatisk fra lagringsplasseringen for sikkerhetskopien, gjenopprettes til den primære lagringsplasseringen og brukes for gjeldende kjøring.
- Alle brukere som er tilordnet til rollen **Utvikler av elektronisk rapportering** eller **Systemansvarlig**, varsles om problemet med den manglende malen via Handlingssenter. Meldingen som vises, avhenger av verdien for den parameteren **Kjør automatisk prosedyren for å gjenopprette de ødelagte malene satsvis**:

    - Hvis denne parameteren er satt til **Av**, anbefaler meldingen at du starter den satsvise prosessen for automatisk å løse lignende problemer for andre maler for ER-formatkonfigurasjon. Meldingen inneholder en kobling som du kan bruke til å starte den satsvise prosessen.
    - Hvis denne parameteren er satt til **På**, varsler meldingen deg om at det har blitt oppdaget et problem med manglende maler og at en ny satsvis prosess, **Gjenopprett skadede maler fra sikkerhetskopi i intern database**, er planlagt automatisk. Denne satsvise prosessen løser automatisk lignende problemer for andre maler.

Hvis du vil konfigurere parameteren **Kjør automatisk prosedyren for å gjenopprette de ødelagte malene satsvis**, gjør du følgende:

1. I Finance and Operations åpner du **Organisasjonsstyring \> Elektronisk rapportering \> siden Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. I dialogboksen **Brukerparametere** angir du den nødvendige verdien for parameteren **Kjør automatisk prosedyren for å gjenopprette de ødelagte malene satsvis**.

> [!NOTE]
> Denne parameteren er definert som programbruker og loggføres firmaspesifikk.

![Siden ER-konfigurasjoner](./media/GER-BackupTemplates-1.png)

Illustrasjonen nedenfor viser et eksempel på meldingen som vises når parameteren **Kjør automatisk prosedyren for å gjenopprette de ødelagte malene satsvis** er satt til **På**.

![Siden Leverandørbetalingsjournal](./media/GER-BackupTemplates-2.png)

Illustrasjonen nedenfor viser den satsvise prosessen **Gjenopprett skadede maler fra sikkerhetskopi i intern database** på siden **Satsvis jobb**.

![Siden Satsvis jobb](./media/GER-BackupTemplates-3.png)

Utførelsesloggen for den fullførte satsvise prosessen **Gjenopprett skadede maler fra sikkerhetskopi i intern database** inneholder informasjon om malene som er gjenopprettet fra lagringsplasseringen for sikkerhetskopier til den primære lagringsplasseringen.

![Siden Logg for satsvis jobb](./media/GER-BackupTemplates-4.png)

Prosessen for å automatisk opprette sikkerhetskopier av maler som finnes i ER-formatkonfigurasjoner, er aktivert som standard. Hvis du vil stoppe sikkerhetskopiering av maler, setter du alternativet **Stopp sikkerhetskopiering av maler** til **Ja** i kategorien **Vedlegg** på siden **Parametere for elektronisk rapportering**. Du kan åpne denne siden fra arbeidsområdet **Elektronisk rapportering**.

Hvis du setter alternativet **Stopp sikkerhetskopiering av maler** til **Ja** og ikke vil beholde sikkerhetskopiene som tidligere ble laget av maler, velger du **Rydd opp på plassering for sikkerhetskopier** på siden **Parametere for elektronisk rapportering**.

Hvis du oppgraderte miljøet til Finance and Operations versjon 10.0.5 (oktober 2019) og vil overføre til et nytt miljø som omfatter ER-formatkonfigurasjoner som kan kjøres, velger du **Fyll ut plassering for sikkerhetskopi** på siden **Parametere for elektronisk rapportering** før overføringen utføres. Denne knappen starter prosessen for å ta sikkerhetskopier av alle tilgjengelige maler, slik at de kan lagres på lagringsplasseringen for sikkerhetskopier for ER-maler.

![Siden Parametere for elektronisk rapportering](./media/GER-BackupTemplates-5.png)

## <a name="supported-deployments"></a>Støttede distribusjoner

I Finance and Operations versjon 10.0.5 er funksjonen for sikkerhetskopiering av ER-maler bare tilgjengelig i skydistribusjoner.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Konfigurere rammeverket for elektronisk rapportering](electronic-reporting-er-configure-parameters.md)
