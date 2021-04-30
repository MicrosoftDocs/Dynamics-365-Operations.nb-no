---
title: Brukergrensesnitt i Microsoft Office-stil i Forretningsdokumentbehandling
description: Dette emnet forklarer hvordan du bruker det nye brukergrensesnittet i funksjonen for administrasjon av forretningsdokument i ER-rammeverket (elektronisk rapportering).
author: v-anamir
ms.date: 04/12/2021
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
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881042"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Brukergrensesnitt i Microsoft Office-stil i Forretningsdokumentbehandling

[!include [banner](../includes/banner.md)]

Med forretningsdokumentadministrering kan forretningsbrukere redigere forretningsdokumentmaler ved å bruke en Microsoft 365-tjeneste eller den aktuelle Microsoft Office-skrivebordsapplikasjonen. Redigeringer kan inneholde utformingsendringer eller nye distribusjoner, eller brukere kan legge til plassholdere for å inkludere ytterligere data uten å måtte endre kildekoden. Hvis du vil ha mer informasjon om hvordan du arbeider med administrering av forretningsdokumenter, kan du se [Oversikt over administrering av forretningsdokumenter](er-business-document-management.md).

Det nye brukergrensesnittet (UI) er tydeligere og mer behagelig å bruke. **Forretningsdokument**-området viser bare malene som er tilgjengelige for gjeldende leverandør. I det forrige grensesnittet oppførte kategorien **Mal** alle malene som var tilgjengelige for alle leverandører. Den viste også alle malene som var opprettet og redigert av alle brukere som hadde samme rolle.

Du kan bruke **Nytt dokument**-knappen til å opprette og redigere en mal i en formatkonfigurasjon for elektronisk rapportering (ER) som leveres av en annen leverandør. I eksemplet i dette emnet er leverandøren Microsoft. Du kan også opprette en mal ved å laste opp din egen mal i Excel-format.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

Videoen om hvordan du [oppretter et nytt forretningsdokument ved å bruke Forretningsdokumentbehandling](https://youtu.be/gAIYl-mM_pw) (vist ovenfor) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), som er tilgjengelig på YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Gjøre det nye dokumentbrukergrensesnittet i forretningsdokumentadministrering tilgjengelig

Hvis du vil begynne å bruke det nye dokumentbrukergrensesnittet i forretningsdokumentadministrering, må du aktivere **Office-lignende brukergrensesnittopplevelse for forretningsdokumentadministrering**-funksjonen i **Funksjonsadministrering**-arbeidsområdet.

Følg disse trinnene for å aktivere denne funksjonen for alle juridiske enheter.

1. I **Funksjonsadministrering**-arbeidsområdet, i **Alle**-fanen velger du **Office-lignende brukergrensesnittopplevelse for forretningsdokumentadministrering**-funksjonen i listen.
2. Velg **Aktiver nå** for å aktivere den valgte funksjonen.
3. Oppdater siden for å få tilgang til den nye funksjonen.

## <a name="edit-templates-that-are-owned-by-other-providers"></a>Redigere maler som eies av andre leverandører

1. I **Forretningsdokumentadministrering**-arbeidsområdet velger du **Nytt dokument**.

    ![Arbeidsområdet Administrasjon av forretningsdokument](./media/BDM_overview_new_template1.png)

2. På **Velg**-fanen velger du dokumentet som skal brukes som mal, og velger deretter **Opprett dokument**.

    ![Forretningsdokumenter-dialogboksen](./media/BDM_overview_new_template2.png)

3. I den nye dialogboksen, i **Tittel**-feltet endrer du tittelen etter behov. Tittelteksten brukes til å navngi den nye ER-formatkonfigurasjonen som opprettes automatisk. Utkastversjonen av denne konfigurasjonen (**Kopi av FTI-kunderapport (GER)**) vil inneholde den redigerte malen og vil bli brukt til å kjøre dette ER-formatet for den gjeldende brukeren. Den opprinnelige malen fra den grunnleggende ER-formatkonfigurasjonen vil bli brukt til å kjøre dette ER-formatet for alle andre brukere.
4. I **Navn** -feltet endrer du navnet på den første revisjonen av den redigerbare malen som skal opprettes automatisk.
5. I **Kommentar**-feltet oppdater du merknadene for revisjonen av den redigerbare malen som opprettes automatisk.
6. Velg **OK** for å bekrefte starten på redigeringsprosessen.

    ![Dokumentopprettelse-dialogboksen](./media/BDM_overview_new_template3.png)

**Nytt dokument**-knappen brukes til å opprette og redigere en mal i en ER-formatkonfigurasjon som leveres av en annen leverandør. I dette eksemplet er leverandøren Microsoft. Når du velger **Nytt dokument**, kan du vise alle malene som eies av gjeldende leverandør og andre leverandører. Når du har valgt malen, åpnes den for redigering. Den redigerte malen blir deretter lagret i en ny ER-formatkonfigurasjon som genereres automatisk.

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>Last opp en mal som bruker et eksisterende Excel-format
Følg denne fremgangsmåten for å oppgi nødvendig informasjon før du laster opp en mal.

1. I **Forretningsdokumentadministrering**-arbeidsområdet velger du **Nytt dokument**.

    ![Arbeidsområdet Administrasjon av forretningsdokument](./media/BDM_overview_new_template1.png)
    
2. Gå til siden **Opprett en ny mal**, **Last opp**-fanen og deretter **Mal**-fanen, og velg **Bla gjennom** for å søke etter og velge Excel-filen du vil bruke som en mal. I **Mal**-delen er feltene **Tittel** og **Beskrivelse** fylt ut automatisk. De angir navnet på og beskrivelsen av den nye ER-formatkonfigurasjonen som opprettes automatisk. Du kan redigere disse feltene etter behov.
3. I **Dokumenttype**-delen i **Navn**-feltet angir du typen forretningsdokument. Denne verdien brukes til å søke i den riktige datakilden (det vil si ER-modellkonfigurasjonen).

    ![Mal-fanen](./media/BDM_overview_new_UI_import_21.jpg)

4. På **Datakilde**-fanen, på hurtigfanen **Filter**, velger du **Bruk filter**. I **Datakilde**-delen fylles **Navn**-feltet ut automatisk, men du kan også velge en verdi manuelt. Du kan bruke filteret til å søke etter riktig datakildenavn etter navn, beskrivelse, kode for land/område og forretningsdokumenttype.

    ![Datakilde-fanen](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > **Filter**-hurtigfanen brukes til å søke i den riktige datakilden (det vil si ER-modellkonfigurasjonen). Du kan redigere alle filterfelt for å finne den mest relevante datakilden for dokumentet du laster opp.
    > 
    > Betingelsene på **Filter**-hurtigkategorien brukes som **ELLER**-betingelser.
    
5. Velg **Registrer automatisk** i **Tilordning**-fanen. **Rotdefinisjon**-feltet fylles ut automatisk, men du kan også velge en verdi manuelt. Denne fanen viser slutttilordningen for elementene fra malen og modellen.

    ![Tilordning-fanen](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > Tilordningen i **Malstruktur**-delen bruker hele samsvaret mellom etikettene eller beskrivelsene i datakilden på brukerens språk, og i cellenavnet i malen.

6. Velg **Opprett dokument** for å bekrefte at du vil opprette en mal og starte redigeringsprosessen.

Hvis du vil ha mer informasjon, kan du se [Oversikt over forretningsdokumentadministrering](er-business-document-management.md).

Hvis det ikke finnes leverandør i Elektronisk rapportering, kan du opprette en. Hvis det ikke finnes en aktiv leverandør, kan du velge å aktivere en.

- Hvis du vil opprette en leverandør, endrer du navnet på leverandøren i **Navn**-feltet, oppdaterer Internett-adressen til den nye leverandøren i feltet **Internett-adresse** og velger **OK** for å bekrefte.

    ![Opprette ny leverandør i BDM](./media/bdm_create_provider.png)
    
- Hvis du vil aktivere eksisterende leverandør, velger du navnet på leverandøren i **Konfigurasjonsleverandør**-feltet, og velger **OK** for å angi leverandøren som aktiv.

    ![Aktivere leverandør i BDM](./media/bdm_choose_provider.png)

> [!NOTE]
> Hver BDM-mal refererer til leverandøren som forfatteren av konfigurasjonen. Dette er årsaken til hvorfor en aktiv leverandør er nødvendig for malen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
