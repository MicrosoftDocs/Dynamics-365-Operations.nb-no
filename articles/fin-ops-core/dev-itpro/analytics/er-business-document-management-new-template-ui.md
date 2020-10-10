---
title: Nytt dokumentbrukergrensesnitt i forretningsdokumentbehandling
description: Dette emnet inneholder informasjon om hvordan du bruker det nye dokumentbrukergrensesnittet i funksjonen for forretningsdokumentadministrering i rammeverket for elektronisk rapportering (ER).
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 015b595f85397fc1cf2c0368814ddc0369176f82
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893201"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Nytt dokumentbrukergrensesnitt i forretningsdokumentbehandling

[!include [banner](../includes/banner.md)]

Med forretningsdokumentadministrering kan forretningsbrukere redigere forretningsdokumentmaler ved å bruke en Microsoft 365-tjeneste eller den aktuelle Microsoft Office-skrivebordsapplikasjonen. Redigeringer kan inneholde utformingsendringer eller nye distribusjoner, eller brukere kan legge til plassholdere for å inkludere ytterligere data uten å måtte endre kildekoden. Hvis du vil ha mer informasjon om hvordan du arbeider med administrering av forretningsdokumenter, kan du se [Oversikt over administrering av forretningsdokumenter](er-business-document-management.md).

Det nye dokumentbrukergrensesnittet (UI) er tydeligere og mer behagelig å bruke. **Forretningsdokument**-området viser bare malene som er tilgjengelige for gjeldende leverandør.

Med **Nytt dokument**-knappen kan brukere opprette og redigere en mal i en formatkonfigurasjon for elektronisk rapportering (ER) som leveres av en annen leverandør. I eksemplet i dette emnet er leverandøren Microsoft.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Gjøre det nye dokumentbrukergrensesnittet i forretningsdokumentadministrering tilgjengelig

Hvis du vil begynne å bruke det nye dokumentbrukergrensesnittet i forretningsdokumentadministrering, må du aktivere **Office-lignende brukergrensesnittopplevelse for forretningsdokumentadministrering**-funksjonen i **Funksjonsadministrering**-arbeidsområdet.

Følg disse trinnene for å aktivere denne funksjonen for alle juridiske enheter.

1. I **Funksjonsadministrering**-arbeidsområdet, i **Ny**-fanen velger du **Office-lignende brukergrensesnittopplevelse for forretningsdokumentadministrering**-funksjonen i listen.
2. Velg **Aktiver nå** for å aktivere den valgte funksjonen.
3. Oppdater siden for å få tilgang til den nye funksjonen.

### <a name="edit-templates-that-are-owned-by-other-providers"></a>Redigere maler som eies av andre leverandører

1. I **Forretningsdokumentadministrering**-arbeidsområdet velger du **Nytt dokument**.

    ![Arbeidsområdet Administrasjon av forretningsdokument](./media/BDM_overview_new_template1.png)

2. I dialogboksen velger du dokumentet som skal brukes som mal, og velger deretter **Opprett dokument**.

    ![Forretningsdokumenter-dialogboksen](./media/BDM_overview_new_template2.png)

3. I den nye dialogboksen, i **Tittel**-feltet endrer du tittelen etter behov. Tittelteksten brukes til å navngi den nye ER-formatkonfigurasjonen som opprettes automatisk. Utkastversjonen av denne konfigurasjonen (**Kopi av FTI-kunderapport (GER)**) vil inneholde den redigerte malen og vil bli brukt til å kjøre dette ER-formatet for den gjeldende brukeren. Den opprinnelige malen fra den grunnleggende ER-formatkonfigurasjonen vil bli brukt til å kjøre dette ER-formatet for alle andre brukere.
4. I **Navn** -feltet endrer du navnet på den første revisjonen av den redigerbare malen som skal opprettes automatisk.
5. I **Kommentar**-feltet oppdater du merknadene for revisjonen av den redigerbare malen som opprettes automatisk.
6. Velg **OK** for å bekrefte starten på redigeringsprosessen.

    ![Dokumentopprettelse-dialogboksen](./media/BDM_overview_new_template3.png)

**Nytt dokument**-knappen brukes til å opprette og redigere en mal i en ER-formatkonfigurasjon som leveres av en annen leverandør. I dette eksemplet er leverandøren Microsoft. Når du velger **Nytt dokument**, kan du vise alle malene som eies av gjeldende leverandør og andre leverandører. Når du har valgt malen, åpnes den for redigering. Den redigerte malen blir deretter lagret i en ny ER-formatkonfigurasjon som genereres automatisk.

Hvis du vil ha mer informasjon, kan du se [Oversikt over forretningsdokumentadministrering](er-business-document-management.md).
