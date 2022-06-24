---
title: Oversikt over posteringsprofiler
description: Denne artikkelen beskriver hvordan posteringsprofiler brukes for Microsoft Dynamics 365-apper.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7ef3be13e82ff3722fc81247b5cd581b0b571b0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876131"
---
# <a name="posting-profiles-overview"></a>Oversikt over posteringsprofiler

I Finance and Operations-apper brukes begrepet *posteringsprofiler* til å beskrive konfigurasjonene som styrer hvordan underfinanskontoer konverteres til hovedkontoer, slik at de kan brukes i transaksjoner som posteres til økonomimodulen. De kontrollerer for eksempel hvordan kunden konverteres til en hovedkonto for kunder når en faktura posteres.

Noen moduler og funksjoner har en side som inneholder ordene "posteringsprofil" i navnet (for eksempel **kundeposteringsprofil** eller **leverandørposteringsprofil**). I tillegg har noen moduler flere alternativer for konfigurasjon av hovedbokpostering for transaksjoner som genereres fra underregnskapet. I **Produksjonskontroll**-modulen kan du for eksempel definere postering etter produksjonsgruppe, ressurs eller ressursgruppe.

Legg merke til at for mange typer transaksjoner finnes det et alternativ til posteringsprofiler: posteringsdefinisjoner. For støttede dokumenter kan du bruke posteringsdefinisjoner i stedet for posteringsprofiler til å klassifisere hovedkontoer og finansdimensjoner for regnskapsoppføringer. Hvis du planlegger å bruke disposisjoner eller forhåndsdisposisjoner, kreves det en posteringsdefinisjon for å definere kontoene for regnskapsoppføringene.

Før du kan konfigurere posteringsprofilene, posteringsdefinisjonene eller siden **Kontoer for automatiske transaksjoner**, må du konfigurere kontoplanen på **Hovedbok**-siden i den juridiske enheten du vil konfigurere.

## <a name="posting-types"></a>Posteringstyper

I Finance and Operations-apper brukes en posteringstype til å definere en generell kategori for et debet- eller et kreditbeløp. Denne kategorien er uavhengig av hovedkontoen i økonomimodulen. Det finnes posteringstyper for hvert debet- eller kreditbeløp i økonomimodulen.

Ett enkelt bilag kan ha en eller flere posteringstyper. En transaksjon som for eksempel posteres via en generell journal der kontoen og motkontoen er satt til **Hovedbok**, vil ha posteringstypen **Finansjournal** for både debet- og kreditbeløpet. I kontrast til dette vil en leverandørfaktura ha flere posteringstyper. Disse posteringstypene inkluderer én linje for leverandørsaldoen og flere linjer for motposteringen, for eksempel **Finansjournal**.

Du kan vise posteringstypen i **Posteringstype**-feltet på **Generelt**-fanen på siden **Bilagstransaksjoner**.

> [!TIP]
> Du kan bruke verktøylinjen **Tilpassing** til å legge til **Posteringstype**-feltet i rutenettet på **Oversikt**-fanen eller til å flytte det. På denne måten kan du gjøre det enklere å få tilgang til eller vise dette feltet når du viser bilag.

## <a name="detail-settings-for-a-posting-profile"></a>Detaljerte innstillinger for en posteringsprofil 

Når du konfigurerer posteringsprofiler, definerer feltet **Kontokode** nivået til innstillingen. Følgende alternativer er tilgjengelige: **Tabell**, **Gruppe** og **Alle**. Samsvaret stopper etter det første treffet, og rekkefølgen er fra det mest spesifikke nivået til det minst spesifikke nivået. Selv om **Kontokode**-feltet kan ha et litt annerledes navn i noen tilfeller, vil virkemåten og funksjonen i feltet forbli den samme. Lagerposteringsprofilen inneholder for eksempel et **Varekode**-felt og et **Kontokode**-felt. Begge feltene har verdier for **Tabell**, **Gruppe** og **Alle**.

Hvis **Hovedkonto**-feltet står tomt for en posteringsprofil, og du ikke har konfigurert en hovedkonto på siden **Kontoer for automatiske transaksjoner** eller en modulspesifikk eller funksjonsspesifikk side, får du en feilmelding når du posterer en transaksjon som bruker den posteringstypen. Vanligvis vil meldingen være «Finner ikke kontoen for \[posteringstype\]».

### <a name="table-value"></a>Tabellverdi

Verdien for **Tabel** refererer til hovedposten som er knyttet til posteringsprofilen. Hver tabellpost er spesifikk for én verdi. Du angir verdien i feltet som skal vises etter **Kontokode**-feltet. Dette feltet kalles vanligvis **Konto** eller **Konto/gruppenummer**. Det nøyaktige navnet varierer, avhengig av hvilken side det vises på.

Hvis du for eksempel arbeider med en kundeposteringsprofil, representerer **Tabell**-verdien en bestemt kunde. Hvis du velger **Tabell** i feltet **Kontokode**, må du derfor velge kundenummeret i feltet **Konto-/gruppenummer**.

**Tabell**-verdien representerer den mest spesifikke posttypen. Systemet bruker alltid denne verdien, selv om du har konfigurert en annen post der verdien for **Gruppe** eller **Alle** er valgt. Denne verdien overstyrer også verdiene du har opprettet som standardverdier på siden **Kontoer for automatiske transaksjoner**.

Vi anbefaler ikke at du bruker **Tabell**-verdien som primærmekanisme for administrasjon av posteringsprofilene, fordi det kan oppstå problemer med datakvaliteten hvis det vedlikeholdes en egen posteringsprofil for hver hoveddatapost. Det er også vanskelig å vedlikeholde og avstemme en egen posteringsprofil for hver hoveddatapost. I stedet bør denne verdien brukes til å administrere unntak i posteringsprofilene.

### <a name="group-value"></a>Gruppeverdi

**Gruppe**-verdien refererer til grupperingsposten som støttes av hovedposten som er knyttet til posteringsprofilen. Hver gruppepost er spesifikk for én verdi. Du angir verdien i feltet som skal vises etter **Kontokode**-feltet. Dette feltet kalles vanligvis **Konto** eller **Konto/gruppenummer**. Det nøyaktige navnet varierer, avhengig av hvilken side det vises på.

**Gruppe**-verdien krever at du først konfigurerer en gruppe og kobler den til én eller flere poster for kontoen. **Gruppe**-verdien er mindre spesifikk enn **Tabell**-verdien, men mer spesifikk enn **Alle**-verdien. Hvis ingen poster er konfigurert for en tabell, prøver systemet å finne en post for gruppen som posten tilhører.

Hvis du for eksempel jobber med en kundeposteringsprofil, og du velger **Gruppe** i **Kontokode**-feltet, må du velge en kundegruppe i feltet **Konto-/gruppenummer**. Du må forhåndsdefinere kundegruppene på **Kundegruppe**-siden, og du må angi en kundegruppe når du oppretter en kunde.

Hvis du må spore flere hovedkontoer for en angitt posteringstype, anbefaler vi at du bruker **Gruppe**-verdien. Du har for eksempel tre hovedkontoer for handel med kunder: én for vanlige kunder, én for ansatte og én for konserninternt salg. I dette tilfellet anbefaler vi at du oppretter tre kundegrupper for å segmentere kundene. Tilordne deretter hver kundegruppe til den riktige hovedkontoen i kundeposteringsprofilen. Følgende tabell viser de tre kundegruppene for dette eksemplet.

| Kundegruppe | Navn | Beskrivelse |
|----------------|------|-------------|
| EXT | Ekstern kunde | Denne gruppen brukes for alle standard eksterne kunder. |
| EMP | Ansatte | Denne gruppen brukes for alle ansatte som foretar innkjøp fra organisasjonen. |
| INT | Konserninternt salg | Denne gruppen brukes for alle konserninterne kundekontoer som brukes sammen med integrering av salgsordrer og bestillinger. |

I posteringsprofilen definerer du deretter tre linjer. På hver linje velger du **Gruppe**-verdien og den tilknyttede hovedkontoen.

### <a name="all-value"></a>Alle-verdi

**Alle**-verdien angir at innstillingene gjelder for alle poster. Hvis du velger **Alle**-verdien i **Kontokode**-feltet, er ikke feltet **Konto-/gruppenummer** tilgjengelig, og du kan ikke velge en bestemt post som konfigurasjonen skal brukes på.

**Alle**-verdien er den minst spesifikke verdien. Den brukes bare hvis systemet ikke finner et treff for **Tabell**- eller **Gruppe**-verdien. Du bør velge **Alle**-verdien når du bare har én hovedkonto for en bestemt posteringstype.

Når du for eksempel jobber med en kundeposteringsprofil, gjelder hovedkontoene du angir, for alle andre kunder og kundegrupper som ikke har noen post for en bestemt tabell (kunde) eller gruppe (kundegruppe).

### <a name="category"></a>Kategori

Lagerposteringsprofiler har en tilleggsverdi som gjelder salgskategorien eller innkjøpskategorien. Denne verdien ligner på **Tabell**-verdien, og gjelder bare for en bestemt salgs- eller innkjøpskategori.

### <a name="default-value"></a>Standardverdi

Hvis du ikke oppretter en post for en posteringstype i en posteringsprofil der **Kontokode**-feltet er satt til **Alle**, og systemet ikke finner en samsvarende posteringsprofilpost for **Gruppe**- eller **Tabell**-verdien, tilbakestilles systemet til standardverdien som kan angis på siden **Kontoer for automatiske transaksjoner**. Hvis du vil ha mer informasjon, kan du se [Kontoer for automatiske transaksjoner](accounts-for-auto-transactions.md).

## <a name="clearing-accounts"></a>Avregningskontoer

Begrepet *avregningskonto* brukes ofte i regnskap. Enkelte posteringstyper i Microsoft Dynamics 365-apper er avregningskontoer. Med andre ord tømmes saldoen i kontoen eller tilbakeføres når en annen transaksjon posteres. Når du for eksempel posterer et produktmottak for en bestilling, posteres summen av de estimerte kostnadene for produktene, pluss mva og eventuelle gebyrer på bestillingslinjene, til posteringstypen for innkjøps avsetning som gjeld. Når du fakturerer bestillingen, tilbakeføres saldoen fra posteringstypen for innkjøps avsetning og flyttes til handelskontoen i leverandørreskonto.

## <a name="additional-resources"></a>Tilleggsressurser

Mange moduler i Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Project Operations har en posteringsprofil eller flere konfigurasjoner som styrer hvordan postering i økonomimodulen fungerer. Bruk følgende emner til å finne ut mer om posteringsprofilene og posteringsoppsettene i hver modul:

- [Kontoer for automatiske transaksjoner](accounts-for-auto-transactions.md)
- [Leverandører-postering](accts-payble-posting.md)
- [Kunder-postering](accts-recvble-posting.md)
- [Postering av aktivaleie](../asset-leasing/set-up-lease-posting-accts.md)
- Postering i ressursbehandling (kommer snart)
- Kontant- og bankbehandling (kommer snart)
- Posteringskontoer for valutarevaluering (kommer snart)
- Postering av reiseregning (kommer snart)
- [Posteringsprofil for anleggsmidler](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Postering for konserninternt regnskap (kommer snart)
- Lagerposteringsprofil (kommer snart)
- [Posering av netto innkjøpspris](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Oversikt over posteringsdefinisjoner](posting-definitions.md)
- Postering i produksjonskontroll (kommer snart)
- Postering i prosjektstyring og regnskap (kommer snart)
- Postering i tjenestebehandling (kommer snart)
- Avgiftspostering (kommer snart)
- Tids- og fremmøtepostering (kommer snart)
- Postering i transportstyring (kommer snart)
- Posteringsprofiler for rabattstyring (kommer snart)
