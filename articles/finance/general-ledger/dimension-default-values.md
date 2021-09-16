---
title: Standard finansdimensjoner i finansjournaler
description: Dette emnet beskriver reglene som definerer hvordan finansdimensjonsverdier angis for transaksjoner som registreres via finansjournaler. Det inneholder også detaljer om scenarioer der det brukes faste dimensjoner.
author: kweekley
ms.date: 09/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransDaily, LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 327bc27f068e1f9eefacc6b5defa27044cb1a77e
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472538"
---
# <a name="default-financial-dimensions-on-financial-journals"></a>Standard finansdimensjoner i finansjournaler

[!include [banner](../includes/banner.md)]

Dette emnet beskriver reglene som definerer hvordan finansdimensjonsverdier angis for transaksjoner som registreres via finansjournaler (men ikke via lagerjournaler eller prosjektjournaler). Det inneholder også detaljer om scenarioer der det brukes faste dimensjoner.

## <a name="symptom"></a>Symptom

Finansdimensjonsverdiene er ikke angitt som forventet for kontoen eller motkontoen i en finansjournal. Følgende scenarioer er to eksempler:

Et bilag registreres i en journal i en generell journal. Kontoen er en leverandørkonto, og motkontoen er en bankkonto. Leverandørens finansdimensjoner angis som standard i kontoen, men bankens finansdimensjoner blir ikke angitt som standard i motkontoen. I stedet blir dimensjonsverdiene fra kontoen angitt som standard i motkontoen.

En kunde har tilordnet standard finansdimensjonsverdier, og en hovedkonto for omsetning har en fast dimensjonsverdi tilordnet for avdelingsregnskapsdimensjonen. Et bilag registreres i en generell journal.  Kontoen er kunden, og motkontoen er en finanskonto, spesielt inntektskontoen med den faste dimensjonsverdien. Fast dimensjon som ikke er definert i motkontoen for hovedkontoen for omsetning. I stedet blir den satt til avdelingsdimensjonsverdien fra kontoen, som kom fra kunden.  Etter posteringen av bilaget brukes den faste dimensjonsverdien på den posterte regnskapsoppføringen, men bilaget viser fremdeles kundens avdelingsverdi på inntektskontoen. 

Hvilke regler følges for finansdimensjonsverdier definert på bilag i en journal?

## <a name="resolution"></a>Oppløsning

Følgende regler følges for å registrere finansdimensjonsverdier som standard på linjene til et bilag i finansjournaler, for eksempel økonomijournalen eller leverandørfakturajournalen. 

1. **Journalhode**

   - Journalhodedimensjoner registreres som standard fra journalnavndimensjoner.

2. **Journallinjekonto**

   - Dimensjoner for journallinjekonto registreres som standard fra journalhodedimensjoner.
   - Hvis noen finansdimensjoner er tomme, angis deres verdier som standard fra kunde-, leverandør-, bank-, anleggsmiddel-, prosjekt- eller finansdimensjoner.

     - Hvis kontotypen er **Finans**, behandles en fast dimensjon i en finanskonto som en standarddimensjon under transaksjonsoppføring.
     - Hvis kontotypen er **Kunde**, **Leverandør**, **Bank**, **Anleggsmidler** eller **Prosjekt**, kan hovedkontoen ennå ikke fastslås. Derfor blir det aldri angitt en fast dimensjon for kontoen.

3. **Journallinjemotkonto**

 - Først hentes dimensjoner for journallinjemotkonto som standard fra dimensjoner for journallinjekonto.

 - Hvis noen finansdimensjoner er tomme, kommer den neste standardoppføringen fra standarddimensjonene fra Kunde, Leverandør, Bank, Anleggsmidler, Prosjekt eller Finans.
   1. Hvis motkontotypen er **Finans**, behandles en fast dimensjon i en finanskonto som en standarddimensjon under transaksjonsoppføring. Hvis en dimensjonsverdi allerede er angitt som standard fra kontoen, vil hovedkontoens standardverdi eller faste dimensjonsverdi ikke overstyre den eksisterende verdien.
   2. Hvis motkontotypen er **Kunde**, **Leverandør**, **Bank**, **Anleggsmidler** eller **Prosjekt**, er hovedkontoen som ennå ikke er kjent, slik at en fast dimensjon aldri vil bruke motkontoen som standard.

4. **Postering**

    1. Under postering blir hovedkontoen for hver linje i regnskapsoppføringen (for både kontoen og motkontoen) evaluert for å fastslå om det er en fast dimensjonsverdi. Hvis det er definert en fast dimensjon, erstattes eventuelle eksisterende eller tomme verdier med den faste dimensjonsverdien.

        Den faste dimensjonsverdien vises **ikke** på journallinjene etter postering. I stedet vises den i regnskapsoppføringen når du viser bilaget etter at den er postert.

    2. Ingen andre dimensjonsverdier angis som standard under postering, inkludert ekstra finanskontoer som kan legges til under postering, for eksempel øreavrundingskontoer og konserninterne kontoer som forfaller til eller forfaller fra kontoer. Standard dimensjonsoppføringer for tilleggs finanskontoer tas fra kontoene eller motkontoene.

Når det gjelder å angi dimensjonsverdier som standard, kan ikke journalstandardprosessen fastslå om en tom dimensjonsverdi med hensikt var tom, eller om standardoppføringen ikke er utført. Hvis en dimensjonsverdi med hensikt er tom, kan det fremdeles angis en verdi som standard ved å bruke standardrekkefølgen som er beskrevet tidligere. Hvis du krever at en dimensjon har en tom verdi, må du kanskje opprette en dimensjon som har verdien **0** (null) eller **Tom**, slik at den kan brukes i stedet for en tom dimensjon.

Gå gjennom følgende scenarioer hvis du vil ha eksempler på standardrekkefølgen for finansdimensjonen.

### <a name="scenario-1"></a>Scenario 1

Gå til **Økonomimodul \> Journaloppsett \> Journalnavn** og velg journalnavnet for **GenJrn**. I hurtigfanen **Finansdimensjoner** definerer du deretter følgende verdier for standard finansdimensjonene:

- **BUSINESSUNIT:** 001
- **DEPARTMENT:** 024

[![Journalnavnside](./media/financial-dimension-defaulting-jrnl-names-01.png)](./media/financial-dimension-defaulting-jrnl-names-01.png)

Gå til **Økonomimodul \> Journaloppføringer \> Økonomimodul**, og opprett en ny generell journal som bruker journalnavnet **GenJrn**. Dimensjonene registreres som standard fra journalnavnet (tabellen LedgerJournalName) til journalhodet (tabellen LedgerJournalTable), som vist i fanen **Finansdimensjoner**.

[![Fanen Finansdimensjoner på siden Økonomijournaler](./media/financial-dimension-defaulting-genrl-jrnl-02.png)](./media/financial-dimension-defaulting-genrl-jrnl-02.png)

Gå til **Linjer**. I feltet **Kontotype** velger du **Finans**, og deretter angir du **170150** i feltet **Konto**. Deretter velger du **TAB**-tasten for å flytte ut av feltet. Dimensjonene registreres som standard fra journalhodet. Derfor vises verdien for **Konto** som **170150-001-024**.

[![Journallinjer for en generell journal på siden Journalbilag](./media/financial-dimension-defaulting-jrnl-vchr-03.png)](./media/financial-dimension-defaulting-jrnl-vchr-03.png)

Endre verdien for **Konto** til **170150-001-023**. Angi enten et debetbeløp eller et kreditbeløp. I feltet **Motkontotype** velger du **Finans**, og deretter angir du **600150** i feltet **Motkonto**. Dimensjonsverdiene registreres som standard fra kontoen. Derfor vises verdien for **Motkonto** som **600150-001-023**.

### <a name="scenario-2"></a>Scenario 2

Bruk de samme finansdimensjonene som du definerte for journalnavnet i scenario 1. Deretter går du til **Kunder \> Kunder \> Alle kunder**, og definerer standard finansdimensjonsverdier for kunde US-001. Velg kunden for å åpne kundedetaljene. I fanen **Finansdimensjoner** beholder du standardverdien for dimensjonen **BUSINESSUNIT** (**001**). Legg til dimensjonen **COSTCENTER**, og angi **007** som verdien.

Opprett en ny økonomijournal som bruker journalnavnet **GenJrn**. I fanen **Finansdimensjoner** endrer du standardverdien for **BUSINESSUNIT** fra **001** til **002**.

Gå til **Linjer**. I feltet **Kontotype** velger du **Kunde**, og deretter angir du **US-001** i feltet **Konto**. Hvis du vil vise finansdimensjoner for ikke-finanskontotyper, velger du **Finansdimensjoner \> Konto**. Følgende standardoppføringer for finansdimensjonsverdiene angis:

- **BUSINESSUNIT:** 002 – Standardoppføringen tas fra journalhodet. Verdien **001** er ikke angitt som standard fra kunde US-001, fordi det allerede er angitt en standardverdi.
- **COSTCENTER:** 007 – Standardoppføringen tas fra oppsettet for kunde US-001.
- **DEPARTMENT:** 024 – Standardoppføringen tas fra journalhodet.

I feltet **Motkontotype** velger du **Finans** når du er tilbake på linjen, og deretter angir du **600150** i feltet **Motkonto**. Følgende standard finansdimensjonsverdier angis på linjen:

- **BUSINESSUNIT:** 002 – Standardoppføringen hentes fra kontoens finansdimensjoner. (Den ble opprinnelig registrert som standard fra journalhodet.)
- **DEPARTMENT:** 024 – Standardoppføringen hentes fra kontoens finansdimensjoner. (Den ble opprinnelig registrert som standard fra journalhodet.)
- **COSTCENTER:** 007 – Standardoppføringen hentes fra kontoens finansdimensjoner. (Den ble opprinnelig registrert som standard kunden.)

### <a name="scenario-3"></a>Scenario 3

I den samme journalen du brukte for scenario 2, legger du til en ny linje. I feltet **Kontotype** velger du **Finans**, og deretter angir du **170150** i feltet **Konto**. Fjern standarddimensjonsverdiene, slik at bare 170150 beholdes. I feltet **Motkontotype** velger du **Kunde**, og deretter angir du **US-001** i feltet **Motkonto**. Følgende standardoppføringer for finansdimensjonsverdiene angis:

- **BUSINESSUNIT:** 002 – Standardoppføringen hentes fra journalhodet, fordi kontodimensjonsverdien er tom. Verdien **001** er ikke angitt som standard fra kunde US-001, fordi en standardverdi allerede var hentet fra journalhodet. Hvis verdien for **BUSINESSUNIT** med hensikt var tom, må du også fjerne finansdimensjonen i motkontoen.
- **COSTCENTER:** 007 – Standardoppføringen hentes fra kunden US-001, fordi kontodimensjonsverdien og journalhodedimensjonsverdien er tom. Hvis verdien for **COSTCENTER** med hensikt var tom, må du også fjerne finansdimensjonen i motkontoen.
- **DEPARTMENT:** 024 – Standardoppføringen hentes fra journalhodet, fordi kontodimensjonsverdien er tom. Hvis verdien for **DEPARTMENT** med hensikt var tom, må du også fjerne finansdimensjonen i motkontoen.

### <a name="scenario-4"></a>Scenario 4

Bruk de samme standard finansdimensjonsverdiene som du definerte for journalnavnet og kunden i scenarioene 1 og 2. Deretter definerer du en fast dimensjonsverdi for dimensjonen **BUSINESSUNIT** for hovedkontoen 170150. Gå til **Økonomimodul \> Kontoplan \> Kontoer \> Hovedkontoer**. I feltet **Hovedkonto** velger du **170150**, og deretter velger du **Legg til** i fanen **Overstyringer for juridisk enhet**. Velg **USMF** som den juridiske enheten, og velg deretter **Legg til**. Velg den posten, og velg deretter **Standarddimensjoner**. Endre verdien for dimensjonen **BUSINESSUNIT** til **Fast verdi** og angi **003** som verdien.

Opprett en ny økonomijournal som bruker journalnavnet **GenJrn**. Fjern alle standarddimensjonsverdiene i fanen **Finansdimensjoner**.

Gå til **Linjer**. I feltet **Kontotype** velger du **Finans**, og deretter angir du **170150** i feltet **Konto**. Deretter velger du **TAB**-tasten for å flytte ut av feltet. Dimensjonsverdiene blir angitt som standard fra hovedkontooppsettet for kontoen 170150. Derfor vises verdien for **Konto** som **170150-003-**.

Endre verdien for **Konto** til **170150-004-**. **Journalfunksjonaliteten hindrer ikke at en fast dimensjonsverdi blir endret.** Angi enten et debetbeløp eller et kreditbeløp. I feltet **Motkontotype** velger du **Finans**, og deretter angir du **170250** i feltet **Motkonto**. Finansdimensjonsverdien 004 registreres som en standard fra kontoen. Poster deretter dokumentet. Velg **Bilag** i journalen. Legg merke til at verdien for **BUSINESSUNIT** tilbakestilles til den faste dimensjonsverdien, **003**, under postering.

Når du returnerer til bilaget i journalen, gjenspeiler **ikke** dimensjonen **BUSINESSUNIT** den faste dimensjonsverdien. Den har alltid verdien som ble vist på skjermen før postering. Posteringsprosessen endrer ikke noe som er angitt på bilaget. Bare regnskapsoppføringen endres under postering.

## <a name="developer-notes"></a>Utviklermerknader

Hvis du er utvikler og vil se på kode for standardprosessen, kan du gå gjennom følgende metoder:

- **LedgerJournalEngine.accountModified()** – Denne metoden er hovedoppføringspunktet for den primære kontodimensjonen som er standard for alle journaler (og overstyres av noen journaltyper).
- **LedgerJournalEngine.offsetAccountModified()** – Denne metoden er hovedoppføringspunktet for standardprosessen for motkontodimensjon.
