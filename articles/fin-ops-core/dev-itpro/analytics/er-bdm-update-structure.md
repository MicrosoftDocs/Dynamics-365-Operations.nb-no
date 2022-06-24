---
title: Oppdatere strukturen til en forretningsdokumentmal
description: Denne artikkelen forklarer hvordan du oppdaterer strukturen til en forretningsdokumentmal ved hjelp av funksjonen for administrasjon av forretningsdokument.
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 2adecba4e988bfe04de2c181501b6c3ef8491dcf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880290"
---
# <a name="update-the-structure-of-a-business-document-template"></a>Oppdatere strukturen til en forretningsdokumentmal 

[!include[banner](../includes/banner.md)]

I **Malstruktur**-ruten i malredigeringsprogrammet [Administrasjon av forretningsdokument](er-business-document-management.md) kan du endre en forretningsdokumentmal ved å [legge til nye felter](er-bdm-add-field-to-excel-template.md) i en mal i Microsoft Excel. Strukturen til malen oppdateres deretter automatisk i Dynamics 365 Finance, slik at den gjenspeiler endringene du har gjort i **Malstruktur**-ruten.

Du kan også endre en mal ved hjelp av nettbasert funksjonalitet i Office 365. Du kan for eksempel legge til et nytt navngitt element, for eksempel et bilde eller en figur, i det redigerbare regnearket. I dette tilfellet oppdateres ikke strukturen til malen i Finance automatisk, og elementet du la til, vises ikke i **Malstruktur**-ruten. Oppdatere malstrukturen manuelt i Finance ved å velge **Oppdater struktur** på siden for malredigering.

Hvis du vil ha mer informasjon om denne funksjonen, kan du fullføre eksemplet nedenfor.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Eksempel: oppdatere strukturen til en forretningsdokumentmal

Dette eksemplet viser hvordan en systemadministrator kan oppdatere strukturen til en forretningsdokumentmal i Finance etter at malen er endret i Office Online. Delene nedenfor forklarer hvilke trinn som er involvert.

### <a name="prepare-a-business-document-template-for-editing"></a>Klargjøre en forretningsdokumentmal for redigering

Fullfør følgende prosedyrer i [Oversikt over administrasjon av forretningsdokument](er-business-document-management.md).

1. [Konfigurere ER-parametere](er-business-document-management.md#configure-er-parameters)
2. [Importere ER-løsninger](er-business-document-management.md#import-er-solutions)
3. [Aktivere administrasjon av forretningsdokument](er-business-document-management.md#enable-business-document-management)
4. [Konfigurere parametere](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>Redigere en forretningsdokumentmal

1. I **Forretningsdokumentadministrering**-arbeidsområdet velger du **Nytt dokument**.
2. På siden **Opprett en ny mal** velger du malen **Fritekstfaktura (ER-eksempel) (Excel)**.
3. Velg **Opprett dokument**.
4. I **Tittel**-feltet skriver du inn **Eksempel på fritekstfaktura for Litware**.
5. Velg **OK** for å opprette den nye malen.

    > [!NOTE]
    > Hvis du ennå ikke har logget på Office Online, blir du [ledet til påloggingssiden for Office 365](er-business-document-management.md#frequently-asked-questions). Du kan gå tilbake til Finance-miljøet ved å velge **Tilbake**-knappen i nettleseren.

    Den nye malen åpnes for redigering i den innebygde kontrollen for Excel Online på siden for malredigering.

[![Bruke arbeidsområdet for administrasjon av forretningsdokument til å begynne å redigere en forretningsdokumentmal.](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>Se gjennom gjeldende struktur for den redigerbare malen

1. Velg **Støttelinjer** i **Vis**-gruppen i **Visning**-fanen på båndet i Excel Online.
2. I den redigerbare malen velger du rektanglet ovenfor maltittelen. Dette rektanglet er et bilde kalt **rptHeaderCompLogo**.
3. Hvis **Malstruktur**-ruten er skjult, velger du **Vis struktur**.
4. Utvid **Rapport \> Faktura \> rptHeader \> rptHeaderPart1** i **Malstruktur**-ruten.
5. Legg merke til at elementet **rptHeaderCompLogo** vises som et underordnet element for **Rapport \> Faktura \> rptHeader \> rptHeaderPart1** i malstrukturen i Finance.

[![Bruke arbeidsområdet for administrasjon av forretningsdokument til å se gjennom gjeldende struktur for en redigerbar mal.](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>Oppdatere strukturen til en forretningsdokumentmal ved å slette et bilde

1. Velg bildet **rptHeaderCompLogo** i den redigerbare malen i Excel Online.
2. Følg ett av disse trinnene for å slette det valgte bildet fra den redigerbare malen:

    - Trykk på **Delete** på tastaturet.
    - Velg og hold (eller høyreklikk på) bildet, og velg deretter **Klipp ut**.

    > [!NOTE]
    > Elementet **rptHeaderCompLogo** er fortsatt i malstrukturen i Finance, selv om bildet ikke lenger er inkludert i Excel-malen.

3. Velg **Oppdater struktur** for å synkronisere strukturen til den redigerbare malen i Excel og Finance.
4. Utvid **Rapport \> Faktura \> rptHeader \> rptHeaderPart1** i **Malstruktur**-ruten.
5. Legg merke til at elementet **rptHeaderCompLogo** ikke lenger er inkludert i malstrukturen i Finance.

[![Bruke arbeidsområdet for administrasjon av forretningsdokument til å slette et bilde fra en forretningsdokumentmal.](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>Oppdatere strukturen til en forretningsdokumentmal ved å legge til et bilde

1. Velg **Bilde** i **Illustrasjoner**-gruppen i **Sett inn**-fanen på båndet i Excel Online.
2. Velg **Velg fil**, bla frem til bildet du vil legge til, velg det, og velg deretter **OK**.
3. Velg **Sett inn**.
4. Flytt det nye bildet til det er på riktig sted. Bildet får som standard et navn i Excel. Bildet kan for eksempel få navnet **Bilde 2**.
5. Velg **Oppdater struktur** for å synkronisere strukturen til den redigerbare malen i Excel og Finance.
6. Utvid **Rapport \> Faktura \> rptHeader \> rptHeaderPart1** i **Malstruktur**-ruten.
7. Legg merke til at det nye bildet nå er inkludert som et element i malstrukturen i Finance.

[![Bruke arbeidsområdet for administrasjon av forretningsdokument til å legge til et bilde i en forretningsdokumentmal.](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>Relaterte koblinger

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Oversikt over administrasjon av forretningsdokument](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]