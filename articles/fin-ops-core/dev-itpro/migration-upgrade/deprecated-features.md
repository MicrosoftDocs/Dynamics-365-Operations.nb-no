---
title: Fjernede eller avskrevne funksjoner i tidligere versjoner
description: Denne artikkelen beskriver funksjoner som er fjernet, eller som ble planlagt for fjerning fra Dynamics 365 for Finance and Operations og tidligere versjoner.
author: sericks007
ms.date: 02/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea9355b040c6431f5ddcccc4aaa0de73e21ad299
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124566"
---
# <a name="removed-or-deprecated-features-in-previous-releases"></a>Fjernede eller avskrevne funksjoner i tidligere versjoner

[!include [banner](../includes/banner.md)]



> [!IMPORTANT]
> Denne artikkelen oppdateres ikke lenger. Hvis du vil se en oppdatert liste over funksjoner som er fjernet eller avskrevet fra økonomi- og driftsapper, kan du søke etter **"Funksjoner som er fjernet eller avskrevet"**-innhold som er knyttet til appen du bruker.

Denne artikkelen beskriver funksjoner som er fjernet eller avskrevet fra Dynamics 365 for Finance and Operations og tidligere versjoner av dette produktet.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging. 

Detaljert informasjon om objekter i økonomi- og driftsapper finnes i [Tekniske referanserapporter](/dynamics/s-e/global/axtechrefrep_61). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av økonomi- og driftsapper.

## <a name="finance-1007-with-platform-update-31"></a>Finance 10.0.7 med Platform update 31

### <a name="chinese-voucher-types-without-account-groups-selection"></a>Kinesiske bilagstyper uten valg av kontogrupper
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Endret til funksjonen med kontogruppevalg. |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Etter 1. desember 2020 planlegger vi å ikke lenger støtte kinesiske bilagstyper uten kontogruppevalg. Finne flere detaljer om ny funksjonsutforming i Hva er nytt i 10.0.7 |

## <a name="finance-and-operations-1006-with-platform-update-30"></a>Finance and Operations 10.0.6 med Platform update 30


### <a name="dimensionhashgethashstr-_message"></a>DimensionHash.getHash(str _message)

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Windows avskriver bruken av SHA1, som dokumentert i [Windows-håndhevelse av SHA1-sertifikater](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx).  |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Etter 1. april 2020 må utviklere bruke plattform-API-ene som finnes i klassen **HasFunction**. |

### <a name="hashcomputesha1hashstring-message"></a>Hash.ComputeSHA1Hash(string message)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Windows avskriver bruken av SHA1, som dokumentert i [Windows-håndhevelse av SHA1-sertifikater](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx).  |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Plattform |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Etter 1. april 2020 må utviklere bruke plattform-API-ene som finnes i klassen **HasFunction**. |


### <a name="formdatetimecontrolsetutcstring"></a>FormDateTimeControl.setUtcString()

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Vi trekker tilbake metoden **setUtcString()** fordi en bedre erstatningsmetode er tilgjengelig. |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Plattform |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Utgått: Innen 1. oktober 2020 planlegger vi å ikke lenger støtte **setUtcString()**-metoden. Utviklere bør i stedet bruke **setUtcDateTime()**-metoden. |

### <a name="blocklist-report-it--feature-reference-it-00001"></a>Blokkeringslisterapport (IT) – funksjonsreferanse IT-00001

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Ikke lovpålagt. |
| **Erstattet med en annen funksjon?**   | Nei |
| **Berørte produktområder**         | Italiensk lokalisering |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Vi planlegger å slutte å støtte denne rapporten innen 1. oktober 2020. |

### <a name="domestic-tax-report--feature-reference-it-00003"></a>Lokal avgiftsrapport – funksjonsreferanse IT-00003

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Ikke lovpålagt. |
| **Erstattet med en annen funksjon?**   | Nei |
| **Berørte produktområder**         | Italiensk lokalisering |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Utgått: Innen 1. oktober 2020 planlegger vi å ikke lenger støtte **Lokal avgiftsrapport – funksjonsreferanse IT-00003**. |

## <a name="october-2019-deprecation-announcement"></a>Avskrivningskunngjøring for oktober 2019

### <a name="flowchart-diagrams-in-business-process-modeler"></a>Flytskjemadiagrammer for Forretningsprosessmodelerer

<table>
<tbody>
<tr>
<td><strong>Årsak til avskrivning/fjerning</strong></td>
<td>Vi avskriver flytskjemakomponenten i BPM (Forretningsprosessmodelerer), fordi eldre utforming forårsaket lav bruk.</td>
</tr>
<tr>
<td><strong>Erstattet med en annen funksjon?</strong></td>
<td>Nei</td>
</tr>
<tr>
<td><strong>Berørte områder</strong></td>
<td>Forretningsprosessmodelerer</td>
</tr>
<tr>
<td><strong>Status</strong></td>
<td>Avskrevet: Komponenten flytdiagram i BPM forventes å bli fjernet i 2020. Følgende funksjonalitet vil være utilgjengelig:
<ul>
<li>Alle flytskjemaer vil være skrivebeskyttede og ikke tilgjengelige for redigering. Figuregenskapene som er knyttet til flytskjemaaktiviteter, vil heller ikke være tilgjengelige. Disse flytskjemaene inneholder både standard flytskjemaer som genereres automatisk og tilpassede flytskjemaer som endres basert på disse standard flytskjemaene.</li>
<li>Prosesstrinnene vil være skrivebeskyttede og ikke tilgjengelige for redigering.</li>     
<li>Den eldre funksjonen for tilpassings-/gapanalyse vil ikke være tilgjengelig. Derfor blir ingen gapliste automatisk opprettet eller tilgjengelig for eksport.
<p><strong>Merk:</strong> Denne funksjonen ble tidligere avskrevet og erstattet av Microsoft Azure DevOps-integrasjoner.</p>
</li>
<li>Versjonsloggen for flytskjemaet vil ikke være tilgjengelig.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="finance-and-operations-1005-with-platform-update-29"></a>Finance and Operations 10.0.5 med Platform update 29

### <a name="us-payroll-tax-updates"></a>Oppdateringer om arbeidsgiveravgift i USA

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Vi trekker tilbake skatteoppdateringer for den amerikanske lønnsfunksjonaliteten på grunn av lav bruk og forbedret funksjonalitet som nå tilbys via strategiske integrasjoner.  |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Payroll |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Utgått: Innen 31. juli 2024 planlegger vi å ikke lenger gi skatteoppdateringer til amerikanske lønnskunder. Funksjonaliteten vil forbli i produktet, men forbedringene vil ikke lenger holde funksjonaliteten oppdatert og eventuelle produktfeil vil bli evaluert på et sak-til-sak grunnlag. |

>[!NOTE]
> Dette representerer en endring fra den opprinnelige avslutningsdatoen 1. oktober 2021. Hvis du vil ha mer informasjon, se [Skatteoppdateringer avsluttes for lønnsfunksjonen i USA i Microsoft Dynamics 365 for Finance and Operations](https://aka.ms/financepayrollfaq).


### <a name="data-management-staging-clean-up"></a>Opprydding av oppsamling i Databehandling
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Oppfyller ikke kjernekravene som kreves for planlegging av periodisk opprydding. |
| **Erstattet med en annen funksjon?**   | Ja, oppryddingsfunksjonen for jobblogg legges til for å oppfylle scenarioene helhetlig. |
| **Berørte produktområder**         | Databehandling |
| **Distribusjonsalternativ**              | Alle  |
| **Status**                         | Avskrevet: Måltidsrammen for funksjonaliteten som skal fjernes, er desember 2020. |

## <a name="finance-and-operations-1004-with-platform-update-28"></a>Finance and Operations 10.0.4 med Platform update 28

### <a name="france-fec-accounting-data-export-in-xml"></a>Frankrike: dataeksport til FEC-regnskap i XML

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | **Fransk FEC-revisjonsfil** er tilgjengelig via **Økonomimodul** \> **Periodiske oppgaver** \> **Dataeksport** og erstatter txt-format.
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Økonomimodul |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet. Måltidsrammen for funksjonaliteten som skal fjernes, er juli 2020. |


### <a name="legacy-navigation-bar"></a>Eldre navigasjonsfelt

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Hodejustering med andre Dynamics- og Office-produkter. Hvis du vil ha mer informasjon, kan du se [Oppdatert navigasjonsfelt som justeres etter Office-hodet](/business-applications-release-notes/April19/dynamics365-finance-operations/updatednavbar).
| **Erstattet med en annen funksjon?**   | Fra og med plattformoppdatering 24 ble et navigasjonsfelt med ny design og søkefunksjon introdusert. |
| **Berørte produktområder**         | Webklient |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Fra og med april 2020 vil ikke det gamle navigasjonsfeltet lenger være tilgjengelig. Frem til dette tidspunktet kan kunder gå tilbake til det gamle navigasjonsfeltet via siden **Alternativer for klientytelse**. |


## <a name="finance-and-operations-1002-with-platform-update-26"></a>Finance and Operations 10.0.2 med Platform update 26


### <a name="legacy-default-action-behavior"></a>Eldre virkemåte for standardhandlinger

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Eldre virkemåte for standardhandlinger i rutenett fører til at en uventet kolonne har standardhandlingskobling etter at rutenettkolonner er omorganisert via tilpasning. Den nye funksjonen for treg standardhandling retter opp dette. Hvis du vil ha mer informasjon, se [Trege standardhandlinger i rutenett](/business-applications-release-notes/October18/dynamics365-finance-operations/sticky-default-action). |
| **Erstattet med en annen funksjon?**   | Fra Platform update 21 ble en funksjon for "trege standardhandlinger" innført. Denne funksjonen kan aktiveres på **Alternativer for klientytelse**-siden. |
| **Berørte produktområder**         | Rutenett i webklienten |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Fra april 2020 blir trege standardhandlinger bli standard virkemåte, uten en mekanisme for å gå tilbake til den gamle virkemåten. |

### <a name="legacy-is-one-of-filtering-experience"></a>Eldre "er en av"-filtreringsopplevelse

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | "Er en av"-filtreringsopplevelse gikk gjennom en ny utforming i Platform update 22, og planen er at dette skal være eneste "er en av"-filtreringsopplevelse. |
| **Erstattet med en annen funksjon?**   | Fra Platform update 22 ble en forbedret "er en av"-filtreringsopplevelse tilgjengelig på **Alternativer for klientytelse**-siden. Hvis du vil vite mer, kan du se [Optimalisert "er en av"-filtreringopplevelse](/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering). |
| **Berørte produktområder**         | Webklient |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Fra april 2020 blir den forbedrede "er en av"-opplevelsen standard virkemåte, uten en mekanisme for å gå tilbake til den gamle virkemåten. |

### <a name="parameter-to-enable-sales-orders-with-multiple-project-contract-funding-sources"></a>Parameteren for å aktivere salgsordrer med flere finansieringskilder for prosjektkontrakt
Støtte for opprettelse av prosjektbaserte salgsordrer der prosjektkontrakten har flere finansieringskilder, er aktivert med **Prosjektparametere management**-innstillingen **Tillat salgsordrer for prosjekt med flere finansieringskilder**. Denne parameteren er ikke aktivert som standard. 

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonen aktiveres alltid når parameteren er fjernet. |
| **Erstattet med en annen funksjon?**   | Nei. Funksjonen for å støtte prosjektbaserte salgsordrer som har flere finansieringskilder, vil alltid være aktivert.   |
| **Berørte produktområder**         |Parameteren **Tillat salgsordrer for prosjekter med flere finansieringskilder** blir fjernet. Fremgangsmåtene nedenfor endres når parameteren blir fjernet: **ctrlSalesOrderTable**-metoden i **ProjStatusType**-klassen, **valider**-metoden for **ProjId**-feltet og **kjør**-metoden i **SalescreateOrder**-skjemaet. De følgende metodene avskrives når parameteren blir fjernet: **IsSalesOrderAllowedForMultipleFundingSources** i **ProjTable**-tabellfilen, **IsAllowSalesOrdersForMultipleFundingSourcesParamEnabled**-metoden i **ProjTable**-tabellfilen, **AllowSalesOrdersForMultipleFundingSources**-datafeltet i **ProjParameters**-skjemaet og **ProjParameterEntity**-filer, **IsAssociatedToMultipleFundingSourcesContract** privat metode i **ProjTable**-tabellfilen. |
| **Distribusjonsalternativ**              | Alle  |
| **Status**                         | Avskrivingen planlegges for april 2020-frigivelsesbølgen. |

### <a name="legacy-workflow-reports-for-tracking-and-instance-status"></a>Eldre arbeidsflytrapporter for sporings- og forekomststatus

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Eldre arbeidsflytrapporter for sporings- og forekomststatus avskrives fordi de ikke lenger refereres til fra navigeringen. Rapportnavnene er WorkflowWorkflowInstanceByStatusReport og WorkflowWorkflowTrackingReport. |
| **Erstattet med en annen funksjon?**   | Arbeidsflytlogg-skjemaet kan brukes i stedet. |
| **Berørte produktområder**         | Webklient |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Måltidsrammen for funksjonaliteten som skal fjernes, er april 2020. |

## <a name="finance-and-operations-1001-with-platform-update-25"></a>Finance and Operations 10.0.1 med Platform update 25

### <a name="deprecated-apis-and-potential-breaking-changes"></a>Avskrevne APIer og potensielle oppdelingsendringer


#### <a name="deriving-from-internal-classes-is-deprecated"></a>Avleding fra interne klasser er avskrevet

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Før Platform update 25 var det mulig å opprette en klasse eller tabell som var avledet fra en intern klasse/tabell som er definert i en annen pakke/modul. Dette er ikke en sikker kodepraksis. Fra og med Platform update 25 viser kompilatoren en advarsel. |
| **Erstattet med en annen funksjon?**   | Kompilatoradvarselen vil bli erstattet av en feil i Platform update 26. Denne endringen er bakoverkompatibel ved kjøretid, som betyr at Platform update 25 eller nyere kan distribueres i et hvilket som helst sandkasse- eller produksjonsmiljø uten å måtte endre egendefinert kode. Denne endringen påvirker bare utviklings- og kompileringstid.|
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Advarselen vil bli en kompileringsfeil i Platform update 26. |

#### <a name="overriding-internal-methods-is-deprecated"></a>Overstyring av interne metoder er avskrevet

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Før Platform update 25 var det mulig å overstyre en intern metode i en avskrevet klasse som er definert i en annen pakke/modul. Dette er ikke en sikker kodepraksis. Fra og med Platform update 25 viser kompilatoren en advarsel. |
| **Erstattet med en annen funksjon?**   | Denne advarselen vil bli erstattet av en kompileringsfeil i Platform update 26. Denne endringen er bakoverkompatibel ved kjøretid, som betyr at Platform update 25 eller nyere kan distribueres i et hvilket som helst sandkasse- eller produksjonsmiljø uten å måtte endre egendefinert kode. Denne endringen påvirker bare utviklings- og kompileringstid. |
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Advarselen vil bli en kompileringsfeil i Platform update 26. |

## <a name="finance-and-operations-1000-with-platform-update-24"></a>Finance and Operations 10.0.0 med Platform update 24

### <a name="renaming-released-products"></a>Gi nytt navn til frigitte produkter 
| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Når du bruker funksjonen **Gi primærnøkkelen nytt navn** til å endre Itemid for et frigitt produkt, oppdateres bare direkte referanser til sekundærnøkkel. Alle andre referanser til det frigitte produktet, for eksempel fra produksjonsordrer, vil beholde det gamle ItemId. Det kan derfor være inkonsekvente data som til slutt vil blokkere forretningsprosesser. |
| **Erstattet med en annen funksjon?**   | Nei. |
| **Berørte produktområder**         | Behandling av produktinformasjon |
| **Distribusjonsalternativ**              | Alle  |
| **Status**                         | Fjernet fra og med Finance and Operations 10.0.0 med Platform update 24.|


## <a name="finance-and-operations-813-with-platform-update-23"></a>Finance and Operations 8.1.3 med Platform update 23

### <a name="sql-server-reporting-services-reportviewer-control"></a>Report Viewer-kontrollen i SQL Server Reporting Services
Kunder kan bruke **Eksport**-handlingen som er angitt av den innebygde Report Viewer-kontrollen i SQL Server Reporting Services (SSRS), til å laste ned dokumenter som er produsert av Finance and Operations-programmer. Denne HTML-baserte presentasjon av rapporten gir brukerne en ikke-paginert forhåndsvisning av dokumentet.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Den ikke-paginerte typen for den HTML-baserte forhåndsvisningsopplevelsen leverer **ikke** gjengivelse med de fysiske dokumentene som produseres av Finance and Operations til slutt. Ved fullt og helt ta i bruk PDF som standardformat for forretningsdokumenter skal brukerne kunne dra nytte av en moderne visningsopplevelse med forbedret ytelse ved produksjon av rapporter i programmet. |
| **Erstattet med en annen funksjon?**   | I fremtiden vil PDF-dokumenter være standardformat for rapporter som gjengis av Finance and Operations.   |
| **Berørte produktområder**         | Denne endringen påvirker **ikke** kundescenarier der rapporter distribueres elektronisk eller sendes direkte til skrivere.    |
| **Distribusjonsalternativ**              | Alle  |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. Funksjonen for automatisk forhåndsvisning av programrapporter som bruker et innebygd PDF-visningsprogrammet, er planlagt for mai 2019-plattformoppdateringen. |

### <a name="client-kpi-controls"></a>Klient-KPI-kontroller
Innebygde nøkkelytelsesindikatorer (KPIer) kan modelleres i Visual Studio av en utvikler og tilpasses ytterligere av sluttbrukeren.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | De opprinnelige klientkontrollene som brukes til å definere KPIer, har lavt kundeopptak og er avhengige av at en utvikler legger til sporbare mål. |
| **Erstattet med en annen funksjon?**   | PowerBI.com-tjenesten leverer fremragende verktøy for å definere og behandle KPIer basert på data fra eksterne kilder.  I en kommende utgivelse planlegger vi å gjøre det mulig for deg å bygge inn løsninger som er plassert på PowerBI.com i programarbeidsområder.   |
| **Berørte produktområder**         | Denne oppdateringen hindrer utviklere i å introdusere nye KPI-kontroller i Visual Studio-designeren.    |
| **Distribusjonsalternativ**              | Alle  |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="deprecated-apis-and-future-breaking-changes"></a>Avskrevne APIer og fremtidige oppdelingsendringer

#### <a name="field-groups-containing-invalid-field-references"></a>Feltgrupper med ugyldige feltreferanser

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Det er mulig for tabellmetadatadefinisjoner å ha feltgrupper som inneholder ugyldige feltreferanser. Hvis distribuert kan dette føre til kjøretidsfeil for kjøring i Finansrapportering og SQL Server Reporting Services (SSRS). Dette problemet kategoriseres for øyeblikket som en *kompilatoradvarsel* i stedet for en *feil*, noe som betyr at den distribuerbare pakkeopprettingen og -distribusjonen kan fortsette uten å rette problemet. Slik løser du dette problemet:<br><br>1. Fjern den ugyldige feltreferansen fra definisjonen for tabellfeltgruppen.<br><br>2. Kompiler på nytt.<br><br>3. Sørg for at advarsler eller feil håndteres. |
| **Erstattet med en annen funksjon?**   | Advarselen vil bli erstattet av en kompileringsfeil i fremtiden. |
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Advarselen er en kompilatorfeil i plattformoppdateringer for versjon 10.0.11 av økonomi- og driftsapper. |

#### <a name="complete-list"></a>Fullstendig liste
Hvis du vil ha tilgang til den fullstendige listen over APIer som kan avskrives, kan du se [Avskriving av metoder og metadataelementer](deprecation-deletion-apis.md).

## <a name="finance-and-operations-81-with-platform-update-20"></a>Finance and Operations 8.1 med Platform update 20

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Regler for partioverføringer for kontooppføringer i underfinansjournal
Den synkrone overføringsmodusen avskrives i Økonomimodulparametere.  Denne modusen erstattes bare av asynkron og planlagt parti, som allerede finnes som alternativer for overføring. Hvis du vil ha mer informasjon, se bloggen [Parametere for økonomimodul – Regler for partioverføring](https://community.dynamics.com/365/financeandoperations/b/financials/archive/2019/03/15/general-ledger-parameters-batch-transfer-rules).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Vi fjerner alternativet Synkron på grunn av innvirkning på ytelsen til systemet. |
| **Erstattet med en annen funksjon?**   | Asynkrone og planlagte partier er alternativer som skal brukes i stedet for synkron.   |
| **Berørte produktområder**         | Økonomimodul, Leverandører, Kunder, Innkjøp, Utgift    |
| **Distribusjonsalternativ**              | Alle  |
| **Status**                         | Avskrevet: Måltidsrammen for funksjonaliteten som skal fjernes, er versjon 10.0.|

### <a name="electronic-reporting-for-russia"></a>Elektronisk rapportering for Russland
Funksjonen for å konfigurere txt og xml-filformat med deklarasjoner. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet av Elektronisk rapportering, |
| **Erstattet med en annen funksjon?**   | Ja. |
| **Berørte produktområder**         | Økonomimodul |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Fjernet fra og med Finance and Operations 8.1 med Platform update 20. |

### <a name="financial-reports-generator-for-russia"></a>Generator for finansrapporter for Russland
Et verktøy for å konfigurere datainnsamling for regnskaps- og avgiftsrapporter og eksportere data til XLS- og DOC-rapportmaler. Funksjonelle deler: Eksportere data til XLS- og DOC-rapportmaler, spørringer, faste forutsetninger fjernes. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Fjernede deler er erstattet av Elektronisk rapportering. |
| **Erstattet med en annen funksjon?**   | Ja. Oppsettet av brukergrensesnittet for finansrapporter skal brukes til å definere datasamlingsregler etter finanskontoer eller mva-registre. Eksport av data til forskjellige filtyper, faste forutsetninger og spørringsaktive datainnsamlingsregler skal konfigureres i Elektronisk rapportering. |
| **Berørte produktområder**         | Økonomimodul. |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Fjernet fra og med Finance and Operations 8.1 med Platform update 20. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Integrasjon med eksterne leverandører for sending av elektronisk rapportering via kommunikasjonskanaler for Russland
Med eksport av genererte elektroniske filer med deklarasjoner til mappen for å sende ytterligere til offisielle leverandører av elektroniske rapportering som importerer tilbake tilstand.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med konfigurerbar funksjon for elektroniske meldinger. |
| **Erstattet med en annen funksjon?**   | Ja.  |
| **Berørte produktområder**         | Økonomimodul, mva |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Fjernet fra og med Finance and Operations 8.1 med Platform update 20. |


### <a name="profit-tax-register-wizard"></a>Veiviser for registre for fortjenesteavgift
Funksjon for å opprette maler for nye registre for fortjenesteavgift. Denne funksjonen oppretter X++-objekter for nye registre, som deretter opprettes som maler med den riktige beregningslogikken lagt til.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonen er ikke kompatibel med Finance and Operations-utvidelsesmodellen. |
| **Erstattet med en annen funksjon?**   | Nei |
| **Berørte produktområder**         | Mva |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Fjernet fra og med Finance and Operations 8.1 med Platform update 20. |

### <a name="payroll-and-human-resources-for-russia"></a>Lønn og personale for Russland
Landsspesifikk modul for Russland for behandling av informasjon om stabsadministrasjon, timeregistreringsdetaljer for ansatte, lønnsregnskap og oppretting av lønnsoppgaver. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Lønn er ikke inkludert i det globale strategiske fokuset i Dynamics 365-porteføljen. Partnere og ISV-er står best stilt til å tilby lønnsfunksjonalitet som samsvarer med lokale forskrifter og skatteoppdateringer.|
| **Erstattet med en annen funksjon?**   | Nei|
| **Berørte produktområder**         | Russisk administrasjon av lønn og personale |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Måltidsrammen for funksjonaliteten som skal fjernes, er en av de fremtidige oppdateringene for versjon 10.0. |

## <a name="finance-and-operations-80-with-platform-update-15"></a>Finance and Operations 8.0 med Platform update 15
Ingen funksjoner er fjernet eller avskrevet med denne versjonen. Plattformoppdatering 15 er kumulativ og inneholder nye eller endrede funksjoner fra plattformoppdatering 13, plattformoppdatering 14 og plattformoppdatering 15.

## <a name="finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Finance and Operations, Enterprise Edition 7.3 med Platform update 12

### <a name="personalized-product-recommendations"></a>Personlige produktanbefalinger 
Fra 15. februar 2018 vil forhandlere ikke lenger kunne vise personlige produktanbefalinger på en salgsstedsenhet. Hvis du vil ha mer informasjon, kan du se [Oversikt over produktanbefalinger](../../../commerce/product-recommendations.md).  

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Vi fjerner gjeldende versjon av produktanbefalingstjenesten fordi vi utformer denne funksjonen på nytt med en bedre algoritme og nyere detaljhandelsorienterte funksjoner.  |
| **Erstattet med en annen funksjon?**   | Nei. Etter våren 2018 planlegger vi imidlertid å få tilbake denne funksjonen for å dra nytte av en ny anbefalingstjeneste.   |
| **Berørte produktområder**         | Personlige produktanbefalinger i POS                                                    |
| **Distribusjonsalternativ**              | Alle                                                                                      |
| **Status**                         |Fjernet fra og med 15. februar 2018. Dette påvirker kunder som kjører Dynamics 365 for Operations 1611 og senere.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Utvidelse av listen over elektroniske rapporteringsfunksjoner (ER)
Muligheten til å introdusere egendefinerte funksjoner som skal brukes i ER-uttrykksverktøyet (hvis du vil ha mer informasjon, se [Utvide listen over funksjoner for elektronisk rapportering (ER)](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)), støttes ikke lenger. På grunn av endringer i ER-API-ene ble API-en for å kalle innebygde funksjoner fra ER-uttrykksverktøyet, interne, og kan ikke utvides lenger.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Kodeforseglingsinitiativ  |
| **Erstattet med en annen funksjon?**   | Ingen. Når det er behov for en ny innebygd funksjon, må en ny utvidelsesforespørsel adresseres til ER-rammeverksteamet.<br><br>Som en midlertidig løsning mens den forespurte funksjonen er under utvikling i ER-teamet, kan den nødvendige logikken programmeres som en metode for en egendefinert programklasse. Denne metoden kan være tilgjengelig i et ER-uttrykk som en egenskap i den tilføyde ER-datakilden for **Program\Klasse**-typen som refererer til denne egendefinerte programklassen.  |
| **Berørte produktområder**         | Rammeverk for elektronisk rapportering                                                      |
| **Distribusjonsalternativ**              | Alle                                                                                      |
| **Status**                         | Fjernet fra og med Finance and Operations, Enterprise Edition 7.3.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Lager per varegruppe- og Lager per lagerdimensjon-aldersfordelte saldolister

Disse to rapportene støttes ikke lenger i Finance and Operations. I stedet kan **Aldersfordeling for lager**-rapporten brukes til å forbedre brukeropplevelsen.

| &nbsp;  | &nbsp; |
|--------------|-----------------------|
| **Årsak til avskrivning**       | Duplikat funksjonalitet  |
| **Erstattet med en annen funksjon?** | Ja. De to rapportene er erstattet av **Aldersfordeling for lager**-rapporten.     |
| **Berørte produktområder**       | Lagerstyring, kostnadsstyring        |
| **Distribusjonsalternativ**        | Alle|
| **Status**                       | Avskrevet: Menyelementene for de to rapportene er fjernet i versjon 7.3. Koden for rapportene beholdes imidlertid i produktet. Planen er å fjerne koden i en fremtidig versjon. |

### <a name="power-bi-content-packs-available-on-appsource"></a>Power BI-innholdspakker som er tilgjengelige på AppSource
Innholdspakkene **Kostnadsstyring**, **Finansresultat** og **Retail Channel Performance**, tilgjengelig på [Microsoft AppSource](https://appsource.microsoft.com), er avskrevet som følge av produktoppdateringer i Microsoft Power BI. Systemadministrasjonsskjemaer som brukes til å distribuere disse innholdspakkene til PowerBI.com, avskrives også i Finance and Operations.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Produktoppdateringer i Microsoft Power BI. |
| **Erstattet med en annen funksjon?**   | Innholdspakkene **Kostnadsstyring**, **Finansresultat** og **Retail Channel Performance**, tilgjengelig på [AppSource](https://appsource.microsoft.com)-nettstedet, blir erstattet av analyseprogrammer som tillater integreringer av løsning på databasenivå. Hvis du vil ha mer informasjon om analyseprogrammer, se [Innebygd Power BI i arbeidsområder](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Berørte produktområder**         | Kostnadsstyring, økonomi og detaljhandel                                                                                               |
| **Distribusjonsalternativ**              | Bare sky (integrasjon med PowerBI.com støttes ikke i lokale distribusjoner.)                                                                                                            |
| **Status**                         | Avskrevet: Måltidsrammen for funksjonalitetsfjerningen er 2. kvartal 2018.    |

### <a name="standard-ui-in-data-management-workspace"></a>Standardgrensesnitt i arbeidsområdet for databehandling

Standardgrensesnittet i databehandling er det eldre brukergrensesnittet, som er standardgrensesnittet som vises for brukerne når de besøker arbeidsområdet for databehandling.

| &nbsp;  | &nbsp; |
|------------------|-------------------------|
| **Årsak til avskrivning/fjerning** | Vi investerer i å gi nye brukeropplevelser i det nye brukergrensesnittet.             |
| **Erstattet med en annen funksjon?**   | Det nye brukergrensesnittet kalles *forbedret visning* og erstatter det gamle brukergrensesnittet.            |
| **Berørte produktområder**         | Arbeidsområdet for databehandling                                                     |
| **Distribusjonsalternativ**              | Alle                                                                           |
| **Status**                         | Avskrevet: Måltidsrammen for funksjonaliteten som skal fjernes, er 2. kvartal 2018. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Forbrukeravgift, mva, tjenesteavgift for India

Disse avgiftene har blitt sammenfattet i indisk GST.

|  &nbsp;                                           |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsak til fjerning eller avskrivning**       | Disse avgiftene har blitt sammenfattet i indisk GST.                          |
| **Erstattet med en annen funksjon?**            | Indisk GST                                                              |
| **Berørte produktområder**                  | Mva                                                                     |
| **Distribusjonsalternativ**                       | Alle moduler                                                   |
| **Status**                                  | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |    

### <a name="file-validation-utility-fvu-for-india"></a>Filvalideringsverktøyet (FVU) for India

|              &nbsp;                               |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsak til fjerning eller avskrivning**       | Mangel på kundebruk                                                  |
| **Erstattet med en annen funksjon?**            | Nei                                                                      |
| **Berørte produktområder**                  | Indisk kildeskatt                                                  |
| **Distribusjonsalternativ**                       | Alle moduler                                                                    |
| **Status**                                  | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.   |        

### <a name="tdstcs-certificate-for-india"></a>TDS/TCS-sertifikat for India

Brukere kan laste ned dette fra den offentlige portalen.

|             &nbsp;                                |    &nbsp;                                                                     |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsak til fjerning eller avskrivning**       | Mangel på kundebruk                                                  |
| **Erstattet med en annen funksjon?**            | Nei                                                                      |
| **Berørte produktområder**                  | Indisk kildeskatt                                                  |
| **Distribusjonsalternativ**                       | Alle moduler                                                                   |
| **Status**                                  | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Insitamentsplan for eksport/import (EXIM) for India


|              &nbsp;                               |        &nbsp;                                                                 |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsak til fjerning eller avskrivning**       | Mangel på kundebruk                                                  |
| **Erstattet med en annen funksjon?**            | Nei                                                                      |
| **Berørte produktområder**                  | Importer og eksporter                                                       |
| **Distribusjonsalternativ**                       | Alle moduler                                                                    |
| **Status**                                  | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Personlige produktanbefalinger 
Fra 15. februar 2018 vil forhandlere ikke lenger kunne vise personlige produktanbefalinger på en salgsstedsenhet. Hvis du vil ha mer informasjon, kan du se [Oversikt over produktanbefalinger](../../../commerce/product-recommendations.md).  

|  &nbsp; |  &nbsp;|
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Vi fjerner gjeldende versjon av produktanbefalingstjenesten fordi vi utformer denne funksjonen på nytt med en bedre algoritme og nyere detaljhandelsorienterte funksjoner.  |
| **Erstattet med en annen funksjon?**   | Nei. Etter våren 2018 planlegger vi imidlertid å få tilbake denne funksjonen for å dra nytte av en ny anbefalingstjeneste.   |
| **Berørte produktområder**         | Personlige produktanbefalinger i POS                                                    |
| **Distribusjonsalternativ**              | Alle                                                                                      |
| **Status**                         |Fjernet fra og med 15. februar 2018. Dette påvirker kunder som kjører Dynamics 365 for Retail 7.2 og senere. |


## <a name="finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Finance and Operations, Enterprise Edition juli 2017 med Platform update 8

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Valutaomregning for regnskap og rapporteringsvalutaer

Valutaomregning for regnskap og rapporteringsvalutaer ble innført når det ble innført euro.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Begrenset bruk og tillegg av funksjonen Kopier juridisk enhet som en erstatning.      |
| **Erstattet med en annen funksjon?**   | Nei, men funksjonene Kopier juridisk enhet og Konfigurasjoner ble lagt til for å gjøre det enklere å flytte et selskap som har kjernekrav som endrer seg. |
| **Berørte produktområder**         | Økonomistyring     |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.   |


### <a name="warehouse-mobile-devices-portal"></a>Portal for lagermobilenheter

Portal for lagermobilenheter (WMDP) var en frittstående komponent som var beregnet for selvdrevet lokal distribusjon. Denne komponenten støttes ikke lenger i Finance and Operations. Et innebygd program som gir en bedre brukeropplevelse, erstatter funksjonaliteten til WMDP.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Duplikat funksjonalitet.       |
| **Erstattet med en annen funksjon?**   | Ja. Denne funksjonen er erstattet med Finance and Operations - Warehousing. Hvis du vil ha mer informasjon om oppsett og forutsetninger, kan du se [Oversikt over Installere og konfigurere lagerappen](../../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Berørte produktområder**         | Lagerstyring, transportstyring     |
| **Distribusjonsalternativ**              | Portal for lagermobilenheter (WMDP) var en frittstående komponent som var beregnet for selvdrevet lokal distribusjon.               |
| **Status**                         | Avskrevet: Måltidsrammen for funksjonaliteten som skal fjernes, er 4. kvartal 2019.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Avansert bankavstemming, samsvarsregel for manuelt samsvar

En samsvarsregele ble brukt til å velge og merke et bankdokument når dokumenter ble avstemt manuelt i avstemmingsregnearket.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Begrenset bruk.                                                                         |
| **Erstattet med en annen funksjon?**   | Nei. Kolonnefiltrering skal brukes til å finne dokumenter for avstemming. |
| **Berørte produktområder**         | Kontant- og bankbehandling                                                               |
| **Distribusjonsalternativ**              | Alle                                                                                    |
| **Status**                         | Fjernet fra og med juli 2017.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611 med Platform update 3

### <a name="aeb-payment-formats-for-spain"></a>AEB-betalingsformatene for Spania

Betalingsformatene Consejo Superior Bancario ble brukt til å sende remitteringsfiler til banken for kunde- og leverandørbetalinger. Innholdet i disse formatene ble bestemt av Asociación Española de Banca. Den dekker Cuaderno 19, 32, 58, 34.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                                  |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022-kredittoverføring og avtalegirobetalingsformater for Spania |
| **Berørte produktområder**         | Leverandør, kunde                                    |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Bankbetalingsoverføringer for Litauen

Bankbetalingsoverføringer ble generert og skrevet ut ved hjelp av eksportformatet for betalingsoverføring (LT) for Litauen. Det litauiske markedet begynte å bruke LITAS, det samordnede elektroniske banksystemet i 2005.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Litauen     |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS Direkte Remittering betalingsformatene for Norge

BBS Direkte Remittering betalingsformatene omfatter eksport av purring på kundebetaling (avtalegiro) og import av returmelding.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.  |
| **Erstattet med en annen funksjon?**   | Format for AvtaleGiro-kundebetaling for Norge kan brukes til å generere meldinger for AvtaleGiro. Importer av returmelding vil bli implementert i fremtidige versjoner. |
| **Berørte produktområder**         | Leverandør, kunde   |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Verktøy for kontoplan for Spania

Dette verktøyet brukes når en kontoplan i Spania krever store endringer. Brukere kan importere en ny kontoplan i Microsoft Excel- eller tekstformat, og kan også importere regnskapsoppgjør.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Begrenset bruk                                                  |
| **Erstattet med en annen funksjon?**   | Nei                                                             |
| **Berørte produktområder**         | Økonomimodul                                                 |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="dom80-payment-format-for-belgium"></a>Dom80-betalingsformat for Belgia

Eldre Belgisk betalingsformat for purring (avtalegiro).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                          |
| **Erstattet med en annen funksjon?**   | Ja, ISO 20022 Avtalegiroformat for Belgia         |
| **Berørte produktområder**         | Kunder                                            |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG-betalingsformatene for Sveits

DTA/EZAG-formatene er integrert i ESR-systemet fordi de kan inneholde referansenummeret. Referansenummeret er ikke obligatorisk, og derfor kan disse formatene brukes til å behandle alle leverandørbetalinger. Disse formatene brukes av firmaer som har en bankkonto på et annet sted enn "Postfinance".

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Sveits   |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB-betalingsformat for Østerrike

EDIFACT-DIRDEB-betalingsformat for purring (avtalegiro).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                          |
| **Erstattet med en annen funksjon?**   | Ja, ISO 20022 Avtalegiroformat for Østerrike         |
| **Berørte produktområder**         | Kunder                                            |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="edivat-for-belgium"></a>EDIVAT for Belgia

EDIVAT er en foreldet belgisk standard for elektronisk deklarering via sikker e-post. Dynamics AX 2012 beholder den skrivebeskyttede løsningen for å få tilgang til den historiske dataene.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonaliteten brukes ikke lenger.                           |
| **Erstattet med en annen funksjon?**   | Nei                                                             |
| **Berørte produktområder**         | Økonomimodul                                                 |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>eGiro EDIFACT CREMUL-betalingsimportformatet for Norge

eGiro er basert på den internasjonale UN EDIFACT CREMUL-standarden (Multiple Credit Advice Message) som brukes ved automatisk postering av kundebetalinger. eGiro er implementert som et importformat for kundebetaling i Dynamics AX.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                                                     |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Camt.054-varselimporten. |
| **Berørte produktområder**         | Kundereskontro                                                                       |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                            |

### <a name="external-inventory-for-poland"></a>Eksternt lager for Polen

Bevis for varer som er hentet fra en salgsleverandør uten innkjøp. Varer som håndteres i eksternt lager, påvirker ikke standardlager og kan selges og deretter kjøpes automatisk. Denne prosessen oppretter reelle lagerbevegelser.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med en annen funksjon                                    |
| **Erstattet med en annen funksjon?**   | Ja, kjernefunksjonaliteten Inngående forsendelse                |
| **Berørte produktområder**         | Leverandører, lagerstyring                         |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Generator for finansrapporter for Øst-Europa

Et verktøy brukes for å konfigurere datainnsamling for regnskaps- og avgiftsrapporter og eksportere data til XLS- og DOC-rapportmaler.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Begrenset bruk                                                                            |
| **Erstattet med en annen funksjon?**   | Nei. Verktøyet vil bli erstattet av elektroniske rapporteringskonfigurasjoner i fremtidige versjoner. |
| **Berørte produktområder**         | Økonomi                                                                           |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Import av kundebetalingstransaksjoner for Finland

Du kan velge et importformat for finske betalinger for å importere kundebetalingstransaksjoner fra en ekstern fil som banken leverer.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                                                     |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Camt.054-varselimporten. |
| **Berørte produktområder**         | Kundereskontro                                                                       |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Import av betalingstransaksjoner i en finansjournal for Finland

Et format som er spesifikk for Finland, som brukes for å importere regnskapstransaksjoner til økonomimodulen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                                                     |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Camt.053-bankkontoutdragsimporten ved hjelp av Avansert bankavstemming. |
| **Berørte produktområder**         | Kundereskontro                                                                       |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integrasjon med Isabel-synkronisert (CIS) for Belgia

Isabel er rammeverket for elektroniske banktjenester i Europa og de facto standard i Belgia.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Integrasjon med Isabel-klienten er avsluttet.   |
| **Erstattet med en annen funksjon?**   | Nei. Betalingsformatene som brukes ikke lenger brukes erstattes av ISO20022 Betalingsformat for kredittoverføring for Belgia. |
| **Berørte produktområder**         | Leverandører     |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Endringer i kontoplanen og regnskapsreglene for Spania

Denne funksjonen brukes til endringer i kontoplanen og regnskapsreglene i Spania. Den tilordner kontoer for å gjøre bidra til overføring av den gamle kontoplanen til den nye kontoplanen, og sammenligner det forrige regnskapsåret med det nye regnskapsåret, selv om de ble postert til ulike kontonumre.

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Begrenset bruk                                                  |
| **Erstattet med en annen funksjon?**   | Nei                                                             |
| **Berørte produktområder**         | Økonomimodul                                                 |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Pagamento Fornittori-betalingsformatet for leverandør

Eldre italiensk betalingsformat for kredittoverføringer.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                          |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Italia         |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="payment-export-formats-for-estonia"></a>Eksportformater for betaling for Estland.

Formatene Telehansa og Teleservice brukes for eksport for bankbetaling.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Estland       |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="payment-file-archive-for-norway"></a>Betalingsfilarkiv for Norge

Når betalingsfiler genereres, arkiverer filarkivet automatisk alle filene som opprettes, også filer som tidligere ble skrevet eller lest.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med en annen funksjon                                        |
| **Erstattet med en annen funksjon?**   | Ja, arkiverte jobber for elektronisk rapportering                            |
| **Berørte produktområder**         | Leverandører, kunder, organisasjonsstyring |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.     |

### <a name="payment-import-formats-for-estonia"></a>Importformater for betaling for Estland

Formatene Telehansa og TeleTeenus brukes for import for bankbetaling.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                                                    |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Camt.054-bankvarselimporten. |
| **Berørte produktområder**         | Kundereskontro                                                                        |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                             |

### <a name="payroll-information-in-human-resources"></a>Lønnsinformasjon i Personale

Lønnsinformasjon i Personale

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Denne funksjonaliteten er erstattet av kjernesider for Lønn og Personale.  |
| **Erstattet med en annen funksjon?**   | **Fordeler**, **Inntekter** og andre tilknyttede sider som tidligere var i US Payroll, er konfigurert på nytt og er nå en del av kjerneinstallasjonen av Personale for å støtte ekstern lønnsbehandling. Denne funksjonaliteten er tilgjengelig ved å bruke **Personale 1** \> **Lønn**-konfigurasjonsnøkkelen. |
| **Berørte produktområder**         | Personale, Lønn   |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611.    |

### <a name="performance-management-goal-workflow"></a>Arbeidsflyt for mål for ytelsesstyring

Ytelsesstyring omfatter målstyring og integrasjon med ytelsesvurderinger.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Ytelsesstyring ble endret, og antall målsider ble redusert for å forenkle prosessen.                 |
| **Erstattet med en annen funksjon?**   | Nei. Mål er synlige for lederselvbetjeningsportalen, og endres og vises av lederen. |
| **Berørte produktområder**         | Forvaltning av menneskelig kapital       |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Postgirot og Postgirot Utland-betalingsformatene for Sverige

Postgirot og Postgirot Utland-betalingsformatene for Sverige.

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Sverige        |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="radio-frequency-identifier"></a>Radiofrekvensidentifisering

Radiofrekvensidentifisering (RFID) er en datainnsamlingsteknikk som bruker elektroniske brikker til å lagre identifiseringsdata. Innhenting av data krever ikke at leseren må være der brikkene er.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Lav kundebruk og begrenset funksjonssett.   |
| **Erstattet med en annen funksjon?**   | Nei                                              |
| **Berørte produktområder**         | Lagerstyring                            |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations 1611. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Rapport om fakturanummerering for delstat for Latvia

Latvisk lovgivning angir bestemte regler for nummerering av salgsfakturaer. Funksjonen lar deg tilordne bestemte numre til salgsfakturaer, basert på brukeren eller brukergruppen. Deretter kan du generere en rapport eller en XML-fil. Du kan også skrive ut en rapport om fakturanumre som er brukt.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Fakturanummerering for delstat trenger ikke lenger å vedlikeholdes. Rapport om brukte fakturanumre er ikke lenger nødvendig. |
| **Erstattet med en annen funksjon?**   | Nei       |
| **Berørte produktområder**         | Kunder    |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Definer navnene på lederen og en generelle regnskapsføreren for et firma for Litauen

Navnet på lederen og den generell regnskapsføreren for et firma kan angis i firmainformasjonen og brukes i forskjellige utskrifter av lokale rapporter.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med en annen funksjon                                     |
| **Erstattet med en annen funksjon?**   | Ja, oppsettet av kontrollører kan brukes til det samme formålet.   |
| **Berørte produktområder**         | Leverandører, Kundereskontro, Kontant- og bankbehandling |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.  |

### <a name="shipping-carrier-interface"></a>Transportørgrensesnitt

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Duplikat funksjonalitet   |
| **Erstattet med en annen funksjon?**   | Delvis erstattet av transportstyring |
| **Berørte produktområder**         | Salg og markedsføring, Lagerstyring  |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611.  |

### <a name="telepay-payment-formats-for-norway"></a>TelePay-betalingsformatene for Norge

TelePay-betalingsformatene omfatter eksportformater for leverandør (kredittoverføring) og purring på kundebetaling (avtalegiro).

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                                                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 betalingsformat for kredittoverføring og AvtaleGiro-kundebetalingsformatet for Norge, i tillegg til pain.002 og camt.054 for import av bankvarselreturfiler. |
| **Berørte produktområder**         | Leverandør, kunde                                                          |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Eksportformater for leverandørbetaling for Finland

Det finnes to formater for eksport av betalinger for Finland. LM02 (FI) brukes for innenlandsbetalinger, og LUM2 (FI) brukes for utenlandsbetalinger.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Finland       |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="warehouse-management-ii"></a>Lagerstyring II

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Lagerstyring II-løsningen (WMS II) som var tilgjengelig i **Beholdningsstyring**-modulen, dupliserer funksjonaliteten i **Lagerstyring**-modulen som ble lansert i Dynamics AX 2012 R3.                                                                         |
| **Erstattet med en annen funksjon?**   | **Lagerstyring**-modulen som ble lansert i AX 2012 R3, Dynamics AX 2012 R3 CU8 og Dynamics AX 2012 R3 CU9, erstatter Lagerstyring II-funksjonene. Den nye modulen har mer avanserte funksjoner og mer fleksible lagerstyringsprosesser enn i Lagerstyring II. |
| **Berørte produktområder**         | Lagerstyring, salg og markedsføring, innkjøp og leverandører   |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611.    |

### <a name="worker-reminders-in-human-resources"></a>Arbeiderpåminnelser i Personale

Lønnsinformasjon i Personale

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Liten bruk                                                           |
| **Erstattet med en annen funksjon?**   | Nei                                                                  |
| **Berørte produktområder**         | Personale                                                     |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611 |

### <a name="workflow-for-creating-goals"></a>Arbeidsflyt for å opprette mål

En arbeidsflyt for behandling av opprettelsen av ansattes mål er en av flere arbeidsflyter som var tilgjengelige for å koordinere ytelsesstyringsprosessen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Ytelsesstyring er utformet på nytt i Finance and Operations.     |
| **Erstattet med en annen funksjon?**   | Den nyutformede funksjonen for ytelsesstyring gir større kontroll over innholdet i målene, målene som brukes til å spore fremdrift og vedlegg av støttedokumentasjon. Mål kan lagres som maler og deretter brukes på nytt. Denne funksjonen kan hjelpe deg med å konfigurere flere mål for ansatte raskere. |
| **Berørte produktområder**         | Forvaltning av menneskelig kapital                 |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Muligheten til å avbryte endringer i en leverandørfaktura

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Ytelsesforbedring        |
| **Erstattet med en annen funksjon?**   | Nei                             |
| **Berørte produktområder**         | Leverandørreskontro               |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0. |

### <a name="aif-axd-and-axbc-integrations"></a>AIF-, AxD- og AxBC-integreringer

I Application Integration Framework (AIF) kan data utveksles med eksterne systemer gjennom forretningslogikk som vises som tjenester. Dynamics AX inneholder tjenestene som er basert på dokumenter og .NET Business Connector (AxBC). Et dokument opprettes ved hjelp av XML. XML-en inneholder hodeinformasjon som legges til for å opprette en *melding* som kan overføres til eller fra Dynamics AX. Eksempler på dokumenter er salgsordrer og bestillinger. Nesten enhver enhet, for eksempel en kunde, kan imidlertid representeres av et dokument. Tjenester som er basert på dokumenter, bruker **Axd \<Document\>**-klassene.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Arkitekturen i AIF- og AxD-dokumenter kan ikke skaleres til en skytjeneste. Det oppstod ytelsesproblemer rundt masseimport.                                        |
| **Erstattet med en annen funksjon?**   | Denne funksjonen erstattes av rammeverket for dataimport/-eksport, som støtter regelmessig bulkimport/-eksport. For AxBC anbefaler vi at du bruker de faktiske tabellene. |
| **Berørte produktområder**         | AxD-er, AxBC-er og AIF   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.   |

### <a name="billing-code-rate-scripts"></a>Satsskript for faktureringskode

Satsskript ble brukt til å beregne faktureringssatser for betalingskoder. Dette skriptet krevde egendefinert utvikling i C Sharp- eller Visual Basic-programmeringsspråket. I den gjeldende versjonen av Dynamics AX støttes ikke **satsskript for faktureringskode**.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Støtte for de egendefinerte C Sharp- eller Visual Basic-skriptene ble ikke lagt til i Dynamics AX 7.0. |
| **Erstattet med en annen funksjon?**   | Nei                                                                                      |
| **Berørte produktområder**         | Offentlig sektor, kunder                                    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                                          |

### <a name="boms-without-bom-versions"></a>Stykklister uten stykklisteversjoner

Når konfigurasjonsnøkkelen **Stykklisteversjoner** ble deaktivert, ble stykklisteversjonene skjult i alle skjemaer, og systemet fremtvang en 1:1-relasjon mellom frigitte produkter og stykklister. I gjeldende versjon av Dynamics AX kan ikke **Stykklisteversjoner**-konfigurasjonsnøkkelen deaktiveres.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Bruk av en konfigurasjonsnøkkel for å styre stykklisteversjoner kan ikke skaleres i et skymiljø. |
| **Erstattet med en annen funksjon?**   | Nei                                                                                      |
| **Berørte produktområder**         | Behandling av produktinformasjon, Lagerstyring                                    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                                          |

### <a name="brazilian-bordero"></a>Brasiliansk Bordero

Spesifikk betalingsmåte for brasilianske firmaer

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Støtte for den brasilianske Bordero-metoden for betalingsmåte er fjernet fra brasiliansk lokalisering |
| **Erstattet med en annen funksjon?**   | Nei   |
| **Berørte produktområder**         | Leverandører   |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="brazilian-sintegra-statement"></a>Brasiliansk Sintegra-utdrag

Utdrag for føderal skatt for ICMS-avgift

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Dette utdraget gjelder ikke lenger i enkelte delstater i Brasil. |
| **Erstattet med en annen funksjon?**   | Nei. Brukere kan bruke det generelle elektroniske rapporteringsverktøyet for å konfigurere utdraget hvis det er nødvendig i bestemte situasjoner. |
| **Berørte produktområder**         | Regnskapsbøker    |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasiliansk SCAN-eventualitetsmodus for NF-e

(SCAN)-eventualitetsmiljø brukes til å generere, eksportere og importere statusen for en Nota Fiscal eletrônica (NF-e) når miljøet for Secretaria da Fazenda (SEFAZ) ikke er tilgjengelig.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Denne eventualitetsmetoden er ikke lenger tilgjengelig i alle delstater i Brasil |
| **Erstattet med en annen funksjon?**   | Nei                                                                          |
| **Berørte produktområder**         | Kunder                                                         |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.              |

### <a name="business-analyzer"></a>Business Analyzer

Denne mobilapplikasjonen lar brukere se gjennom viktige forretningsdata.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonen har blitt erstattet med en annen funksjon.   |
| **Erstattet med en annen funksjon?**   | Innholdspakken Overvåk økonomiske resultater for Microsoft Power BI inneholder nøkkelmetrikk for økonomi som tidligere var tilgjengelig i verktøyet Business Analyzer. |
| **Berørte produktområder**         | Økonomimodul      |
| **Status**                         | Avskrevet: Bruken av Business Analyzer er avskrevet.    |

### <a name="business-statistics"></a>Forretningsstatistikk

Oppsett av forretningsstatistikkforespørsler som kan hjelpe deg med å analysere ytelsen til organisasjonen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Foreldet tilnærming til forretningsanalyse (BI), lav kundebruk og begrenset funksjonssett |
| **Erstattet med en annen funksjon?**   | Nye BI-løsninger for den gjeldende versjonen av Dynamics AX                                      |
| **Berørte produktområder**         | Innkjøp og leverandører, Leverandører, Salg og markedsføring, Kunder         |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Endre datofunksjonen for dokumentet i fakturagodkjenningsjournalen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Liten bruk                                                               |
| **Erstattet med en annen funksjon?**   | Ja. Du kan endre dokumentdatoen på den posterte leverandørtransaksjonen. |
| **Berørte produktområder**         | Leverandørreskontro                                                        |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03-betalingsformat for Nederland

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Formatet er ikke lenger i bruk i Nederland fordi det er erstattet av SEPA-funksjonaliteten. |
| **Erstattet med en annen funksjon?**   | SEPA-betalingseksport  |
| **Berørte produktområder**         | Alle moduler     |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.   |

### <a name="compliance-center"></a>Overholdelsessenter

Overholdelsessenteret var et Enterprise Portal-område for administrasjon av kravene til dokumentasjon til samsvar som er knyttet til Sarbanes-Oxley-loven.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Mangel på kundebruk. Microsoft SharePoint inkluderer samme funksjon som var tilgjengelig i overholdelsessenteret. |
| **Erstattet med en annen funksjon?**   | Nei   |
| **Berørte produktområder**         | Samsvar og interne kontroller  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.    |

### <a name="connector-for-microsoft-dynamics"></a>Connector for Microsoft Dynamics

Dette verktøyet ble brukt til å integrere viktige data fra Microsoft Dynamics CRM til Dynamics ERP-programmer.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonen har blitt erstattet med en annen funksjon. |
| **Erstattet med en annen funksjon?**   | Dataverse                                      |
| **Berørte produktområder**         | Connector for Dynamics                         |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Containerenhet og fysisk beholdning av flere dimensjoner

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Duplikat funksjonalitet |
| **Erstattet med en annen funksjon?**   | Ja. Denne funksjonaliteten er erstattet med funksjonssettet for konsolidert partiordre etter AX 2012. Dette funksjonssettet inneholder den konsoliderte beholdningen. |
| **Berørte produktområder**         | Behandling av produktinformasjon, Produksjonskontroll, Lagerstyring, Salg og markedsføring  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0. |

### <a name="cue-group-metadata"></a>Bunkegruppemetadata

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Bunkegrupper ble brukt til å vise én eller flere bunker i faktaboksområdet. Det var begrenset opptak, og det var også ytelsesproblemer fordi en postendring i et overordnet skjema forårsaket én spørring per bunke i bunkegruppen. |
| **Erstattet med en annen funksjon?**   | Nei      |
| **Berørte produktområder**         | Alle moduler    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.  |

### <a name="cue-metadata"></a>Bunkemetadata

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Bunkemetadata er begrenset til antall- eller suminformasjon.    |
| **Erstattet med en annen funksjon?**   | Side-ved-side-metadataene ble innført for å gi mer fleksibilitet for modellering. Du kan for eksempel opprette gjeldende antall, navigasjon og nøkkelytelsesindikatorer (KPI-er). Side-ved-side-metadata er direkte erstatning av bunkemetadata. |
| **Berørte produktområder**         | Alle moduler           |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0      |

### <a name="danish-check-format"></a>Dansk sjekkformat

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Støtte for dansk sjekkformatoppsett er avsluttet, og rapporten har blitt fjernet fra DK-lokalisering. |
| **Erstattet med en annen funksjon?**   | Nei    |
| **Berørte produktområder**         | Alle moduler    |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.  |

### <a name="data-partitions"></a>Datapartisjoner

Datapartisjoner gir en logisk separasjon av data i Dynamics AX-databasen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Datapartisjoner ble introdusert i Dynamics AX 2012 R2 for å gjøre det mulig å isolere data. I et vanlig scenario har et firmaet datterselskaper, og data fra ett av datterselskapene skal ikke være synlig for et annet datterselskap, selv om begge datterselskaper håndteres av samme IT-avdelingen. Ekstra skript og administrasjon i hele programmet var imidlertid nødvendig for å opprette nye partisjoner og fylle dem med data, og for å sikkerhetskopiere partisjonsdata. I skyen, der vi har tilgang til databasetjenester for plattform som en tjeneste (PaaS) (Microsoft Azure SQL-Database), er det mye mer effektivt å bruke en database som isolasjonsbeholder enn å utføre isolasjon i programmet. Uavhengig av om partisjonering av data er nødvendig for datterselskaper, for flere leiere, eller bare for skala, mener vi at situasjonene kan håndteres bedre gjennom flere Finance and Operations-forekomster. |
| **Erstattet med en annen funksjon?**   | Kunder som bruker datapartisjoner, må bruke flere forekomster av Finance and Operations hvis databasenivåskillet er viktig.    |
| **Berørte produktområder**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Database og fildelingslagring for vedlegg

Dynamics AX 2012 tillot lagring av vedlegg i databasen og delte filer. Ingen av disse alternativene støttes lenger.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Lagring av delte filer støttes ikke lenger fordi skyvertmiljøer ikke kan kommunisere med lokale delte filer. Databaselagring er avviklet til fordel for Azure Blob-lagring. Azure Blob-lagring tilsvarer lagring i databasen, siden dokumenter kan bare åpnes med Finance and Operations-klientskjemaer. Dette gir fordelen med å gi lagring som ikke har en negativ innvirkning på ytelsen til databasen. Blob-lagring er standard lagringsmekanisme for dokumentbehandling og fungerer umiddelbart. |
| **Erstattet med en annen funksjon?**   | Databaselagring er avviklet til fordel for Azure Blob-lagring.   |
| **Berørte produktområder**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.   |

### <a name="delimitation"></a>Avgrensing

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Finner ingen bruk av funksjonen. |
| **Erstattet med en annen funksjon?**   | Nei                                     |
| **Berørte produktområder**         | Timeregistrering                    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.         |

### <a name="desktop-client"></a>Skrivebordsklient

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Dynamics AX-klientopplevelsen har fått ny utforming for å forbedre brukervennligheten på tvers av plattformer og enheter.                      |
| **Erstattet med en annen funksjon?**   | Den nye webklienten er basert på skrivebordskjemametadataene og programmeringsmodellen som har blitt endret for å gi en rik webplattform. |
| **Berørte produktområder**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.   |

### <a name="direct-database-connection"></a>Direkte databasetilkobling

I Dynamics AX 2012 R3 kan Retail Modern POS kobles direkte til kanaldatabasen på samme måte som Enterprise POS. Dette var i tillegg til standard kommunikasjonsmetode for Retail Modern POS-kommunikasjon via detaljhandelsserver.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Direkte databasetilkobling krevde protokoller med lavere sikkerhet, og ble hovedsakelig brukt til å oppnå den høyeste ytelsen. På grunn av ytelses- og sikkerhetsforbedringene som er utført i Finance and Operations, fører denne funksjonen nå til flere problemer enn den løser. |
| **Erstattet med en annen funksjon?**   | Nei. Nå støttes bare standard kommunikasjon for detaljhandelsserver.  |
| **Berørte produktområder**         | Kanaldatabase/Retail Modern POS   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.  |

### <a name="dutch-swift-mt940"></a>Nederlandsk SWIFT MT940

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Generisk funksjonalitet brukes nå i stedet for lokalisert funksjonalitet.                    |
| **Erstattet med en annen funksjon?**   | Ja, denne funksjonaliteten er erstattet av funksjonalitet for avanserte bankavstemming. |
| **Berørte produktområder**         | Alle moduler                                                                              |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL for Tyskland)

Denne funksjonaliteten leverte XBRL-utdata (eXtensible Business Reporting Language) som er beregnet spesifikt for den tyske eBilanz-taksonomien.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Mangel på kundebruk  |
| **Erstattet med en annen funksjon?**   | Denne funksjonen er ikke erstattet av en annen funksjon, men flere spesialiserte XBRL-pakker som gir rik XBRL-funksjonalitet, er tilgjengelige for det tyske markedet. |
| **Berørte produktområder**         | Management Reporter      |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.  |

### <a name="enterprise-portal-client"></a>Enterprise Portal-klient

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | En enkelt klient plattform er levert.  |
| **Erstattet med en annen funksjon?**   | Den nye webklienten er basert på skrivebordskjemametadataene og programmeringsmodellen som har blitt endret for å gi en rik webplattform. |
| **Berørte produktområder**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.   |

### <a name="environmental-sustainability"></a>Miljømessig bærekraft

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Lav kundebruk og begrenset funksjonssett  |
| **Erstattet med en annen funksjon?**   | Nei              |
| **Berørte produktområder**         | Samsvar og interne kontroller, leverandører  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0. |

### <a name="form-activex-and-managed-host-controls"></a>Lage ActiveX- og administrerte vertskontroller

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | ActiveX-kontrollene og de administrerte vertskontrollene er basert på den avskrevne skrivebordsklienten. |
| **Erstattet med en annen funksjon?**   | Det utvidbare kontrollrammeverket støtter bygging av nye kontroller som er basert på HTML, CSS og JavaScript, og er en førsteklasses kontroll i Microsoft Visual Studio-verktøymiljøet. |
| **Berørte produktområder**         | Alle moduler     |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Generer forhåndsmerknader ved hjelp av et parti

Generering av forhåndsmerknad kan ikke kan utføres ved hjelp av et parti, men kan fremdeles utføres av en bruker.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Det finnes ikke noe skjema for å beholde og vise den resulterende forhåndsmerknadsfilen når den blir generert ved hjelp av et parti. |
| **Erstattet med en annen funksjon?**   | Forhåndsmerknader kan fremdeles genereres, og brukeren har kontroll over plasseringen der filen skal lagres.   |
| **Berørte produktområder**         | Leverandører, Kundereskontro, Kontant- og bankbehandling  |
| **Status**                         | Fjernet fra og med AX 7.0.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Tysk DTAUS-betalingseksport og kontoutdragsimport (totaler og transaksjoner)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Formatet er ikke lenger i bruk i Tyskland fordi det er erstattet av SEPA-funksjonaliteten (felles eurobetalingsområde).                    |
| **Erstattet med en annen funksjon?**   | Ja, denne funksjonaliteten er erstattet av SEPA-betalingseksport og avanserte funksjoner for bankavstemming for import av kontoutdrag. |
| **Berørte produktområder**         | Alle moduler  |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="german-dtazv-payment-format-in-domestic-currency"></a>Tysk DTAZV-betalingsformat i innenlands valuta

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Formatet er ikke lenger i bruk i Tyskland fordi det er erstattet av SEPA-funksjonaliteten. |
| **Erstattet med en annen funksjon?**   | SEPA-betalingseksport    |
| **Berørte produktområder**         | Leverandørreskontro   |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.    |

### <a name="german-mt940-import"></a>Tysk MT940-import

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Generisk funksjonalitet brukes nå i stedet for lokalisert funksjonalitet.                    |
| **Erstattet med en annen funksjon?**   | Ja, denne funksjonaliteten er erstattet av funksjonalitet for avanserte bankavstemming. |
| **Berørte produktområder**         | Alle moduler                                                                              |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                           |

### <a name="german-xml-eu-sales-list"></a>Tysk EU-salgsliste i XML

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | XML-format for rapportering av tysk EU-salgsliste støttes ikke lenger. Bare ELMA5-tekstfilformatet kan brukes til å sende rapportering av EU-salgsliste til det tyske skattekontoret. |
| **Erstattet med en annen funksjon?**   | Nei         |
| **Berørte produktområder**         | Mva        |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.   |

### <a name="gl-ssrs-reports"></a>GL SSRS-rapporter

Rapporter som inkluderer følgende menyelementer, er fjernet: **Råbalansesammendrag**, **Detaljert råbalanse**, **Kontoplan**, **Revisjonsspor**, **Saldoer** og **Saldoliste**.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | SSRS-rapporter (Microsoft SQL Server Reporting Services) er erstattet med Management Reporter-funksjoner og standardrapporter. |
| **Erstattet med en annen funksjon?**   | Management Reporter (kalt **Finansrapportering** i den gjeldende versjonen av Dynamics AX)    |
| **Berørte produktområder**         | Økonomimodul   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.   |

### <a name="infopart-and-formpart-metadata"></a>InfoPart- og FormPart-metadata

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | InfoPart- og FormPart-metadata aktiverte opprettelsen av faktabokser for to forskjellige klienter. |
| **Erstattet med en annen funksjon?**   | InfoPart-metadata, som var en forenklet skjemadefinisjon, konverteres til et skjema ved hjelp av oppgraderingsverktøy. Metadata for FormPart, som refererer til et skjema, erstattes av en mer direkte referanse som opprettes av oppgraderingsverktøy. |
| **Berørte produktområder**         | Alle moduler    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.        |

### <a name="main-account-list-page"></a>Listeside for hovedkonto

En liste over kontoer for den juridiske enheten og tilknyttet saldoinformasjon

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Saldoinformasjon er tilgjengelig på listesiden **Råbalanse** etter konto og dimensjon.  |
| **Erstattet med en annen funksjon?**   | **Hovedkontoer** inneholder den samme listen over kontoer som listesiden **Hovedkonto** inneholdt. Rutenettvisningen i **Hovedkontoer** viser også en enda mindre rutenettlignende visning. |
| **Berørte produktområder**         | Økonomimodul      |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaysia og Singapore bankkontantstrømrapport

Denne funksjonen gjør det mulig for brukeren å skrive ut en kontantstrømrapport som viser transaksjoner og detaljer om inn- og utkontantstrømmene for et valgt datoområde for valgte bankkontoer.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Den samme informasjonen kan hentes fra forespørselsbanktransaksjonen. |
| **Erstattet med en annen funksjon?**   | Forespørselbanktransaksjonen                                            |
| **Berørte produktområder**         | Kontant- og bankbehandling                                                |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.          |

### <a name="mexican-cfd-electronic-invoice"></a>Meksikansk CFD elektronisk faktura

Denne funksjonen aktiverte genereringen av meksikanske elektroniske fakturaer ved hjelp av CFD-metoden (Comprobante Fiscal Digital), der firmaet signerer fakturaen ved å be om relaterte godkjenning fra myndighetene. Denne funksjonen gir også en månedlig rapport som inneholder alle elektroniske fakturaer som ble utstedt i perioden.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Metoden er ikke lenger gjeldende. Generering av elektroniske fakturaer ved hjelp av metoden CFD ble avskrevet av skattemyndighetene og erstattet med CFDI-metoden (Comprobante Fiscal Digital a través de Internet), der signeringen delegeres til tredjepartsleverandøren (PAC). Den månedlige rapporten er fjernet, og et forespørselsalternativ lar brukerne be om historiske transaksjoner. |
| **Erstattet med en annen funksjon?**   | Nei    |
| **Berørte produktområder**         | Kunder, Prosjekt   |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="mexico-realized-and-unrealized-vat"></a>Mexico realisert og urealisert mva

Dynamics AX 2012 administrerte urealisert merverdiavgift (mva) ved å bruke Mexico-spesifikk funksjonalitet for urealisert mva.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Duplikat funksjonalitet  |
| **Erstattet med en annen funksjon?**   | Ja, denne funksjonen er erstattet med standard betinget mva-funksjonaliteten som tilbys av Core. |
| **Berørte produktområder**         | Mva   |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook-integrering


| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonen har blitt erstattet med Microsoft Exchange Server-integrering. |
| **Erstattet med en annen funksjon?**   | Ja                                                                            |
| **Berørte produktområder**         | Salg og markedsføring                                                            |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Privat blokkering av lager- og lagerstyringsjournaler

Lager- og lagerstyringsjournaler støtter ikke lenger muligheten til å merke en journal som privat for en valgt bruker. Bare prosessen med å blokkere journaler som privat for brukergrupper og blokkering under redigering støttes.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Finner ingen bruk av funksjonen. |
| **Erstattet med en annen funksjon?**   | Nei                                     |
| **Berørte produktområder**         | Lagerstyring                   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.         |

### <a name="product-builder"></a>Produktkonfigurator

Produktkonfigurator ble brukt til å konfigurere varer dynamisk fra en salgsordre, en bestilling, en produksjonsordre, et salgstilbud, et prosjekttilbud eller et varebehov. Basert på en produktmodell som hadde modelleringsvariabler, kan brukeren velge verdier for å imøtekomme kundekravene og få en unik produktvariant som hadde en stykkliste og rute.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Produktkonfigurator viste X ++-kode til sluttbrukere og støttes ikke i den gjeldende versjonen av Dynamics AX. Den er fjernet for å unngå dupliserte vedlikeholdsforsøk på overlappende, skalerbare kodebaser.  |
| **Erstattet med en annen funksjon?**   | Ja. Restriksjonsbasert konfigurasjon ble innført i Dynamics AX 2012, der avskrivningen av Produktkonfigurator i fremtidige versjoner allerede var annonsert. Restriksjonsbasert konfigurasjonsteknologi er valgt i produktstandardene for å muliggjøre konfigurasjonen. Hvis du vil ha mer informasjon, kan du se [Oversikt over produktkonfigurasjon](../../../supply-chain/pim/build-product-configuration-model.md). |
| **Berørte produktområder**         | Behandling av produktinformasjon, salg og markedsføring  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.      |

### <a name="production-floor-app"></a>Produksjonsapp
Dette er appen for tavleenheter som kjører Windows 8.1 RT og Windows 8.1 Pro.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Med endringen i en webbasert klient er det mulig å levere lignende funksjonalitet via den opprinnelige Dynamics AX 7.0-klienten. Jobbkortenheten har et brukergrensesnitt for produksjon som er optimalisert for berørings- og tavleformfaktorer. |
| **Erstattet med en annen funksjon?**   | Ja. Jobbkortenheten, som er en innebygd del av Dynamics AX 7.0.                                                                           |
| **Berørte produktområder**         | Produksjonskontroll                                                |
| **Status**                         | Avskrevet: En fjerningsdato fra Microsoft-butikken ikke ennå er satt for denne funksjonen.                                                |


### <a name="rename-product-dimension"></a>Gi nytt navn til produktdimensjon

Med denne funksjonen kan du endre navnet på en av de tre standard produktdimensjonene (størrelse, farge eller stil) til et navn som passer bedre til dine forretningsbehov. Navneendring inkluderte alle etikettene der produktdimensjonsnavnet ble brukt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Den gjeldende versjonen av Dynamics AX støtter ikke etikettendringer under kjøring. |
| **Erstattet med en annen funksjon?**   | Nei                                                                            |
| **Berørte produktområder**         | Behandling av produktinformasjon                                                |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                                |

### <a name="retail-server-connectivity-using-http"></a>Tilkobling til detaljhandelsserver med HTTP

I Dynamics AX 2012 R3 kunne detaljhandelsserveren fungerer ved hjelp av HTTP-kommunikasjon (ikke sikret). Dette var i tillegg til standardkommunikasjonen med HTTPS.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | På grunn av nye sikkerhetskrav støttes nå bare sikret kommunikasjon ved hjelp av TLS 1.2 (eller høyere, hvis tilgjengelig). Det selvbetjente installasjonsprogrammet konfigurerer automatisk datamaskinen for denne kommunikasjonen. |
| **Erstattet med en annen funksjon?**   | Nei. Nå støttes bare standard HTTPS-kommunikasjon. |
| **Berørte produktområder**         | Detaljhandelsserver  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0. |

### <a name="role-center-pages"></a>Rollesentersider

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Rollesentersider ble bygd på den avskrevne Enterprise Portal-plattformen, som er erstattet med den nye webklientplattformen i den gjeldende versjonen av Dynamics AX. |
| **Erstattet med en annen funksjon?**   | Det nye arbeidsområdeskjemamønsteret gir brukerne en prosessentrert design som gir enkel tilgang til ofte brukte oppgaver i denne prosessen.                       |
| **Berørte produktområder**         | Alle moduler    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0   |

### <a name="sales-tax-jurisdictions"></a>Mva-jurisdiksjoner

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Lav kundebruk og begrenset funksjonssett |
| **Erstattet med en annen funksjon?**   | Nei                                           |
| **Berørte produktområder**         | Amerikansk merverdiavgift                                 |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.               |

### <a name="sites-services"></a>Sites Services

Sites Services lar deg bygge webområder som utvider forretningsprosesser til Internett uten IT-støtte.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Microsoft Azure-infrastrukturen som brukes av Dynamics AX, har nye funksjoner som kan brukes i stedet (for eksempel Azure-områder). |
| **Erstattet med en annen funksjon?**   | Nei   |
| **Berørte produktområder**         | Personalerekruttering, saksbehandling, forespørsel om tilbud, leverandørregistrering, samarbeidsområder for salgsmuligheter og kampanjer  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS, strategi for behovsprognose

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Utformingen av funksjonen støttes ikke i den nye skyarkitekturen. |
| **Erstattet med en annen funksjon?**   | Azure Machine Learning, strategi for behovsprognose                           |
| **Berørte produktområder**         | Hovedplanlegging                                                              |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Leverandørfakturapulje uten posteringsdetaljer

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Liten bruk. Denne funksjonaliteten er erstattet av fakturajournalen med funksjonaliteten for arbeidsflyten. |
| **Erstattet med en annen funksjon?**   | Arbeidsflytfunksjoner til fakturajournalen.     |
| **Berørte produktområder**         | Leverandørreskontro |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.    |


### <a name="virtual-company-accounts"></a>Virtuelle firmakontoer

Virtuelle firmaer-funksjonen støttes ikke lenger i Dynamics AX. Virtuelle firmaer-funksjonen lar brukere definere tabeller som kan deles av et sett med firmaer. Hvis du vil ha en beskrivelse av funksjonen, kan du se [Firmakontoer og virtuelle firmakontoer](../../fin-ops/get-started/ax4-content-retired.md). Funksjonen fungerer ved å gruppere tabeller i samlinger som tilordnes til virtuelle firmaer, som er grupper av eksisterende "virkelige" firmaer. Spørringer opprettes slik at alle selskaper i det virtuelle firmaet kan få tilgang til dataene i tabellene til de tilknyttede tabellsamlingene.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | - Virtuelle firmaer må defineres før data lagres i tabellene. Retrotilpasning av virtuelle firmaer på en eksisterende implementering er veldig vanskelig.<br><br>- Fordi det har vært så mye datanormalisering i den gjeldende versjonen av Dynamics AX, har det blitt vanskelig å vite hva du skal legge til i tabellsamlinger. Det er for eksempel vanskelig å vite hvilke tabeller som skal deles. Alle tabellene det refereres til fra tabeller som er i et virtuelt firma, må også legges til. På grunn av tabellnormalisering må selv enkle hoveddata som er spredt over flere tabeller, være en del av det virtuelle firmaet. Eventuelle feil som gjøres her, vil forårsake funksjonsproblemer.<br><br>- Når en tabell er en del av et virtuelt firma, mister den informasjon om opprinnelsen til dataene, og bare det virtuelle firmaet registreres.   |
| **Erstattet med en annen funksjon?** | Globale tabeller kan brukes til å lage tabeller som er tilgjengelige fra alle firmaer. Det er for øyeblikket ingen erstatning. |   
| **Berørte produktområder**       | Alle moduler |   
| **Status**                       | Fjernet fra og med Dynamics AX 7.0.   |   

### <a name="windows-8-tablet-app"></a>Windows 8 nettbrettapp

Windows 8 nettbrettapp inneholdt funksjonalitet for utgiftsregistrering og -godkjenning.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Finance and Operations er kompatibel med nettbrett. Nettbrettappen er ikke lenger nødvendig.    |
| **Erstattet med en annen funksjon?**   | Nei.          |
| **Berørte produktområder**         | Reiseregning og utlegg   |
| **Status**                         | Fjernet: Denne funksjonen er bare tilgjengelig for Dynamics AX 2012 R3. |

### <a name="workplanner"></a>Jobbplanlegger

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Liten bruk |
| **Erstattet med en annen funksjon?**   | Nei, men **Profilrelasjon**-siden som åpnes fra **Profilgrupper**-siden, støtter samme forretningsscenario som den avskrevne **Jobbplanlegger**-siden. |
| **Berørte produktområder**         | Timeregistrering     |
| **Status**                         | Koden har ikke blitt fjernet. Skjemaet JmgWorkPlanner ble imidlertid ikke overført.    |

### <a name="x-financial-statements"></a>X++-regnskapsoppgjør

| &nbsp;  | &nbsp; |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Årsak til avskrivning/fjerning</strong> |                         Funksjonen har blitt erstattet med en annen funksjon.                         |
|  <strong>Erstattet med en annen funksjon?</strong>  | Management Reporter (kalt <strong>Finansrapportering</strong> i den gjeldende versjonen av Dynamics AX) |
|     <strong>Berørte produktområder</strong>     |                                              Økonomimodul                                              |
|             <strong>Status</strong>             |                                      Fjernet fra og med Dynamics AX 2012                                      |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

