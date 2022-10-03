---
title: Tillat redigeringer i interne data for økonomimodulbilag
description: Denne artikkelen gir informasjon om hvordan du redigerer interne data i finansbilag.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 6e346c6ff881d3a33743196b45247493fd19ed1d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573258"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Tillat redigeringer i interne data for økonomimodulbilag

[!include[banner](../includes/banner.md)]


Når du posterer regnskapsoppføringer i økonomimodulen, brukes ofte **Beskrivelse**-feltet til å lagre interne merknader eller dokumentasjon. Hvis informasjonen er feil, kan den forårsake forvirring og gjøre det vanskeligere å lukke periodeslutt. Ved hjelp av denne funksjonen kan regnskapssjefen eller regnskapslederen rette feil ved å redigere **Beskrivelse**-feltet på posterte bilag i økonomimodulen.

Endringer i posterte bilag i økonomimodulen er begrenset til data som er interne av natur. Ved hjelp av denne funksjonen kan du aldri redigere data som beløp, posteringsdatoer, finanskontoer og transaksjonsvalutaen. Endringer i dataene vil påvirke den eksterne rapporteringen av regnskapsoppgjør og må bare gjøres gjennom nye finansbilag.

> [!NOTE]
> For Dynamics 365 Finance, versjon 10.0.29 er denne funksjonen begrenset til endringer i **Beskrivelse**-feltet.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Rediger interne data for økonomimodulbilag

Før interne data i finansbilag kan redigeres, må du aktivere funksjonen **Tillat redigeringer av interne data i finansbilag** i arbeidsområdet **Funksjonsstyring**.
Når funksjonen er aktivert, må brukeren som skal redigere posterte bilag, tildeles regnskapssjef- eller regnskapslederrollen. Du kan også legge til tillatelser for andre roller ved å tilpasse sikkerhetsrollene.

Redigeringsprosessen er bare tillatt fra Bilagstransaksjoner-siden.

1. Gå til **Økonomimodul** > **Forespørsler og rapporter** > **Bilagstransaksjoner**.
2. Angi søkekriterier for å velge bilag i dialogboksen **SysQuery**.
3. Velg linjene for bilagene du vil redigere, og velg deretter **Rediger bilagslinjer** > **Rediger interne bilagsdata**.

    [![Bilagstransaksjoner-side.](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
På siden **Rediger interne bilagsdata** vises følgende data for hver linje du har valgt:
  
  - Finanskonto
  - Kontonavn
  - Bilag
  - Nåværende beskrivelse
  - Ny beskrivelse

    [![Journalbilag.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Bare **Ny beskrivelse**-feltet kan redigeres. Som standard tilsvarer verdien i feltet **Gjeldende beskrivelse**, slik at du raskt kan rette små feil i beskrivelsen.

4. Endre **Ny beskrivelse**-feltet i hver rad, eller slett beskrivelsen fra hver rad.

   Hvis flere rader må oppdateres med samme verdi, kan du også følge denne fremgangsmåten:

      1. Velg radene du vil redigere, og velg deretter **Bulkoppdater valgte poster**.
      2. Velg feltet **Felt du vil redigere**, i feltet som skal redigeres. Oppslaget omfatter for øyeblikket bare feltet **Ny beskrivelse**.
      3. Angi en ny beskrivelse i feltet **Ny verdi**.
      4. Velg **Oppdater**. Alle de valgte postene blir oppdatert med den nye verdien.

      [![Bulkoppdater de valgte postene-dialogboks.](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. I feltet **Årsak til redigering** skriver du inn en merknad som forklarer hvorfor redigeringen ble gjort. Denne merknaden vises på siden **Revisjonssporet for bilagsredigeringer**.

   Det kan gjøres flere endringer i det samme bilaget, og hver redigering spores.

## <a name="audit-trail-of-voucher-edits"></a>Revisjonsspor for bilagsredigeringer

Et revisjonsspor vedlikeholdes spesielt for å spore endringene som gjøres ved hjelp av denne funksjonen. Du kan gå til revisjonssporet for bilagsredigering på to måter:

  - Gå til **Økonomimodul** > **Forespørsler og rapporter** > **Bilagstransaksjoner**. Velg **Rediger bilag** > **Revisjonsspor for bilagsredigeringer** på siden **Bilagsforespørsler**-siden. Revisjonssporet vises bare for den valgte bilagsposten. 
   
    Når du åpner forespørselen på denne måten, kan du fokusere på alle endringer som ble gjort i én enkelt bilagspost.
  
  - Gå til **Økonomimodul** > **Periodiske oppgaver** > **Revisjonsspor for bilagsredigeringer**. I dialogboksen angir du kriterier for å angi bilagene du vil vise revisjonssporet for redigeringer for. Hvis du vil vise revisjonssporet for alle bilag, lar du kriteriene stå tomme og velger **OK**. 
    
    Når du åpner forespørselen på denne måten, kan du filtrere etter endringer som ble gjort på en bestemt dato eller av en bestemt bruker.

**Revisjonsspor på redigeringer**-siden viser følgende informasjon:

- **Opprettet dato og klokkeslett** – Datoen og klokkeslettet for redigeringen.
- **Årsak til redigering** – Årsaken til at brukeren angav for redigeringen.
- **Opprettet av** – Brukeren som gjorde endringen.

Hvis du vil vise detaljene for hvert revisjonsspor, driller du ned på verdien **Opprettet dato og klokkeslett**. Siden **Vis redigerte bilagsegenskaper** viser samme informasjon som den opprinnelige redigeringssiden, inkludert den forrige beskrivelsen og den oppdaterte beskrivelsen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
