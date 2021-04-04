---
title: Nytt dokumentbrukergrensesnitt i forretningsdokumentbehandling
description: Dette emnet inneholder informasjon om hvordan du bruker det nye dokumentbrukergrensesnittet i funksjonen for administrasjon av forretningsdokument for elektronisk rapportering.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f8099f2f6872c34c30de918a6fc5fd27bcde958
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565716"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Nytt dokumentbrukergrensesnitt i Forretningsdokumentbehandling

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]