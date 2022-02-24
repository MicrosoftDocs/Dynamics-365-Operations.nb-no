---
title: Oversikt over leverandørfakturaer
description: Dette emnet inneholder generell informasjon om leverandørfakturaer. Leverandørfakturaer er forespørsler om betaling for produkter og tjenester som er mottatt. Leverandørfakturaer kan representere en faktura for pågående tjenester, eller den kan være basert på bestillinger for bestemte varer og tjenester.
author: abruer
manager: AnnBe
ms.date: 07/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d51a5ff2dca764a534ea4bf92c30bcf0bf0a5dad
ms.sourcegitcommit: 51cd470ee885d12f7d51c66201b092aaa16dfaa6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2020
ms.locfileid: "4701682"
---
# <a name="vendor-invoices-overview"></a>Oversikt over leverandørfakturaer

[!include [banner](../includes/banner.md)]

Dette emnet inneholder generell informasjon om leverandørfakturaer. Leverandørfakturaer er forespørsler om betaling for produkter og tjenester som er mottatt. Leverandørfakturaer kan representere en faktura for pågående tjenester, eller den kan være basert på bestillinger for bestemte varer og tjenester.

## <a name="vendor-invoices"></a>Leverandørfakturaer

En leverandørfaktura fra en bestilling er en faktura som lages når produkter eller tjenester er mottatt i henhold til en bestilling som ble plassert hos en leverandør. Leverandørfakturaen inneholder et hode og én eller flere linjer for varer eller tjenester. En leverandørfaktura fullfører syklusen fra bestilling til produktkvittering og leverandørfaktura.

Selv om noen leverandørfakturaer er koblet til en bestilling, kan også leverandørfakturaer inneholde linjer som ikke samsvarer med bestillingslinjer. Du kan også opprette leverandørfakturaer som ikke er knyttet til noen bestilling. Disse leverandørfakturaene kan representere pågående tjenester, for eksempel en strømregning, og du trenger ikke å referere til en bestilling når du legger dem til.

Det finnes flere måter å angi en leverandørfaktura:

- I leverandørfakturaregisteret kan du raskt skrive inn fakturaer som ikke refererer til en bestilling, slik at du kan avsette utgiften. Ved hjelp av journalen for godkjenning av leverandørfaktura kan du velge disse fakturaene og postere dem til leverandørsaldoen for å reversere avsetningen.
- I leverandørfakturajournalen kan du raskt skrive inn fakturaer som ikke refererer til en bestilling, i én operasjon.
- Leverandørfakturapuljen i kombinasjon med leverandørfakturaregisteret lar deg raskt skrive inn fakturaer for å avsette utgiften. Du kan åpne de tilknyttede bestillingene senere for å postere fakturaen mot utgiftskontoen.
- På sidene **Åpne leverandørfakturaer** og **Ventende leverandørfakturaer** kan du opprette leverandørfakturaer fra bekreftede bestillinger.

Følgende diskusjon inneholder mer informasjon om hvordan du bruker siden **Åpne leverandørfakturaer** eller **Ventende leverandørfakturaer** til å opprette en leverandørfaktura fra en bestilling.

## <a name="understanding-invoice-line-quantities"></a>Forstå fakturalinjeantall

Når du åpner en leverandørfaktura fra en tilknyttet bestilling, opprettes fakturalinjer fra bestillingen. Som standard hentes antallet fra produktkvitteringsantallet. Du kan imidlertid bruke et av følgende standardvalg:

- **Motta nå-antall** – Bruk dette alternativet for delvise leveringer. Standardverdien i feltet **Antall** hentes fra antallet som er angitt i **Motta nå**-feltet på innkjøpsordren.
- **Bestilt antall** – Bruk dette alternativet for komplette forsendelser. Standardverdien i feltet **Antall** hentes fra antallet som er angitt i **Bestilt**-feltet på innkjøpsordren.
- **Registrert antall** – Bruk dette alternativet hvis varen krever registrering, som angitt på **Varemodellgrupper**-siden. Standardverdien i **Antall**-feltet er det fysiske oppdaterte antallet som er registrert.
- **Produktkvitteringsantall** – Bruk dette alternativet hvis en produktkvittering allerede er mottatt for ordren. Standardverdien i **Antall**-feltet er hentet fra totalt antall for tilgjengelige produktkvitteringer.
- **Registrerte antall og tjenester** – Bruk dette alternativet hvis antall som er registrert i ankomstjournaler for lagerførte varer eller varer som ikke er på lager. Dette alternativet omfatter tjenester også, uavhengig av om de er registrert.

Hvis den juridiske enheten bruker fakturakontroll, kan du vise resultatene av antallssamsvaret i **Samsvar i antall i produktkvittering**-kolonnen. Du kan også bruke **Samsvarende detaljer**-knappen på **Gjennomgang**-fanen i handlingsruten for å vise resultatene av antallssamsvaret.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Legger til en linje som ikke var på bestillingen.

Du kan legge til en linje som ikke var på bestillingen, i leverandørfakturaen. Du må velge et varenummer eller en innkjøpskategori. Du kan deretter legge til antall, priser og beløp på linjen. Linjen inkluderes bare i kontrollpolicyer for fakturatotaler.

## <a name="submitting-a-vendor-invoice-for-review"></a>Sende en leverandørfaktura til vurdering

Organisasjonen kan bruke arbeidsflyter til å administrere vurderingsprosessen for leverandørfakturaer. Det kan bli nødvendig med arbeidsflytvurdering for fakturahodet, fakturalinjen eller begge. Arbeidsflytkontrollene gjelder for hodet eller linjen, avhengig av hvor fokuset er når du velger kontrollen. I stedet for **Poster**-knappen vises en **Send**-knapp som du kan bruke til å sende leverandørfakturaen gjennom vurderingsprosessen.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>Forhindre faktura fra å sendes til arbeidsflyt 

Nedenfor finner du flere måter du kan forhindre at en faktura sendes til en arbeidsflyt på.

- **Fakturatotal og den registrerte totalen er ikke like.** Personen som sendte fakturaen, mottar et varsel om at totalene ikke er like, slik at de kan rette opp saldoene før fakturaen sendes til arbeidsflyten på nytt. Denne funksjonen er tilgjengelig hvis parameteren **Forhindre innsending til arbeidsflyt når fakturatotal og registrert fakturatotal ikke er like** på siden **Funksjonsbehandling** er slått på. 

- **Fakturaen inneholder utildelte tillegg.** Personen som sendte fakturaen, mottar et varsel om at fakturaen har utildelte tillegg, slik at de kan rette opp fakturaen før den sendes til arbeidsflyten på nytt. Denne funksjonen er tilgjengelig hvis parameteren **Forhindre innsending til arbeidsflyt når det finnes utildelte tillegg på en leverandørfaktura** på siden **Funksjonsbehandling** er slått på.

- **Fakturaen inneholder samme fakturanummer som en annen postert faktura.** Personen som sendte fakturaen, mottar et varsel om at en faktura med et duplisert nummer ble funnet, slik at de kan rette den opp før den sendes til arbeidsflyten på nytt. Dette varselet vises når Leverandør-parameteren merket **Kontroller fakturanummeret som er brukt** er satt til **Avvis duplikat**. Denne funksjonen er tilgjengelig hvis parameteren **Forhindre innsending til arbeidsflyt når fakturanummeret allerede finnes på en postert faktura, og systemet ikke er konfigurert til å godta dupliserte fakturanumre** på siden **Funksjonsbehandling** er slått på.  

## <a name="matching-vendor-invoices-to-product-receipts"></a>Samsvare leverandørfakturaer med produktkvitteringer

Du kan angi og lagre informasjon for leverandørfakturaer, og du kan samsvare fakturalinjer med produktkvitteringslinjer. Du kan også samsvare delvist antall for en linje.

Du kan opprette en leverandørfaktura basert på linjeelementene for produktkvittering som er mottatt til gjeldende dato, selv om ikke alle varene i en bestemt bestilling er mottatt ennå. Du kan for eksempel bruke dette alternativet hvis en leverandør sender én faktura per måned som dekker alle leveringer som er sendt i løpet av den måneden. Hver produktkvittering representerer en delvis eller komplett levering av varene i bestillingen.

Når du posterer fakturaen, oppdateres **Fakturarest**-antallet for hver vare til totalantallet som er mottatt for de valgte produktkvitteringene. Hvis både **Fakturarest**-antallet og **Gjenstående levering**-antallet for alle varer på bestillingen er 0 (null), endres statusen for bestillingen til **Fakturert**. Hvis **Fakturarest**-antallet ikke er 0, endres ikke statusen for bestillingen, og flere fakturaer kan registreres på den.

Dette alternativet forutsetter at minst én produktkvittering er postert for bestillingen. Leverandørfakturaen er basert på disse produktkvitteringene og gjenspeiler antallet i dem. Finansinformasjonen for fakturaen er basert på informasjonen du angir når du posterer fakturaen.

Hvis du vil ha mer informasjon, se [Registrere leverandørfaktura og avstemme mot mottatt antall](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>Konfigurere en automatisert oppgave for arbeidsflyt for leverandørfaktura for å postere leverandørfakturaen ved hjelp av en satsvis jobb

Du kan legge til en automatisert posteringsoppgave i arbeidsflyten for leverandørfaktura, slik at fakturaer behandles i en bunke. Ved å postere fakturaer i en bunke, kan arbeidsflytprosessen fortsette uten å måtte vente til posteringen er fullført, noe som forbedrer den generelle ytelsen til alle oppgavene som er sendt til arbeidsflyten.

Hvis du vil postere en leverandørfaktura i en bunke, aktiverer du parameteren **Satsvis postering av leverandørfaktura** på siden **Funksjonsbehandling**. Arbeidsflyter for leverandørfaktura konfigureres ved å gå til **Leverandører > Oppsett > Arbeidsflyter for leverandørreskontro**.

Du kan se oppgaven **Poster leverandørfakturaen ved hjelp av et parti** i redigeringsprogrammet for arbeidsflyt, uansett om funksjonsparameteren, **Satsvis postering av leverandørfaktura**, er aktivert. Når funksjonsparameteren ikke er aktivert, vil ikke en faktura som inneholder oppgaven **Poster leverandørfakturaen ved hjelp av et parti**, behandles i arbeidsflyten før parameteren er aktivert. Oppgaven **Poster leverandørfakturaen ved hjelp av et parti** må ikke brukes i samme arbeidsflyt som den automatiserte oppgaven **Poster leverandørfakturaer**. Oppgaven **Poster leverandørfakturaen ved hjelp av et parti** bør også være det siste elementet i arbeidsflytkonfigurasjonen.

Du kan angi antall fakturaer som skal inkluderes i partiet, og antall timer du må vente før du planlegger en bunke på nytt, ved å gå **Leverandører > Oppsett > Leverandørparametere > Faktura > Fakturaarbeidsflyt**. 

## <a name="working-with-multiple-invoices"></a>Arbeide med flere fakturaer

Du kan arbeide med flere fakturaer samtidig og postere alle samtidig. Hvis du må opprette flere fakturaer, bruker du **Ventende leverandørfakturaer**-siden. Hvis du må postere og skrive ut flere leverandørfakturaer, bruker du fakturagodkjenningsjournalen. Hvis du bruker fakturagodkjenningsjournalen, må minst én produktkvittering posteres for bestillingen, og en faktura for bestillingen må posteres i en ankomstregistrering. Den økonomiske informasjonen for fakturaen kommer fra fakturaen som ble postert i registret.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Gjenopprette leverandørfakturaer som er i bruk

Når en leverandørfaktura er i bruk, kan den ikke kan redigeres av en annen bruker. Imidlertid kan statusen for en faktura noen ganger indikere at fakturaen er i bruk, selv om den ikke redigeres aktivt. Programmet kan for eksempel ha sluttet å svare mens fakturaen ble redigert, eller en bruker kan ved en feiltakelse ha latt fakturaen være åpen i programmet.

Du kan bruke siden **Gjenopprett leverandørfakturaer** til å gjenopprette eller frigi leverandørfakturaer som har vært i bruk i mer enn fire timer, slik at de kan redigeres. Du kan åpne denne siden fra **Periodisk oppgave**-navigasjonen eller en flis i arbeidsområdet **Leverandørfakturaregistrering**. Når en faktura er gjenopprettet, vil den være tilgjengelige for redigering på siden **Leverandørfaktura**.

Du kan få tilgang til siden **Gjenopprett leverandørfakturaer** bare hvis **Gjenopprett leverandørfakturaer i bruk**-sikkerhetsplikten og -rettigheten er tilordnet til deg. I tillegg må **Tillat gjenoppretting av leverandørfaktura**-parameter på siden **Leverandørparametere** være aktivert.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Tilbakestille arbeidsflytstatusen for leverandørfakturaer fra Uopprettelig til Utkast

En arbeidsflytforekomst som er stoppet på grunn av en uopprettelig feil, vil ha arbeidsflytstatusen **Uopprettelig**. Når statusen til en leverandørfakturaarbeidsflyt er **Uopprettelig**, kan du tilbakestille den til **Utkast** ved å velge **Tilbakekall**. Du kan deretter redigere leverandørfakturaen. Denne funksjonen er tilgjengelig hvis parameteren **Tilbakestille arbeidsflytstatusen for leverandørfakturaer fra Uopprettelig til Utkast** på siden **Funksjonsbehandling** er slått på.

Du kan bruke siden **Arbeidsflytlogg** for å tilbakestille arbeidsflytstatusen til **Utkast**. Du kan åpne denne siden fra **Leverandørfaktura** eller fra **Felles > Forespørsler > Arbeidsflyt**. Hvis du vil tilbakestille arbeidsflytstatusen til **Utkast**, velger du **Tilbakekall**. Du kan også tilbakestille arbeidsflytstatusen til Utkast ved å velge handlingen **Tilbakekall** på siden **Leverandørfaktura** eller **Ventende leverandørfakturaer**. Når arbeidsflytstatusen er tilbakestilt til **Utkast**, blir den tilgjengelig for redigering på siden **Leverandørfaktura**.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>Vise fakturatotalen på siden Ventende leverandørfakturaer
Du kan vise fakturatotalen på siden **Ventende leverandørfakturaer** ved å aktivere parameteren **Vis fakturatotal på listen over leverandørfakturaer på vent** på siden **Leverandørparametere**. 



## <a name="additional-resources"></a>Tilleggsressurser

- [Definer leverandørfakturapolicyer](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Hovedfakturadata i AP-systemet ved hjelp av leverandørfaktura](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Registrere fakturadata i Leverandører ved hjelp av en godkjenningsjournal](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Registrere fakturadata i AP-systemet ved hjelp av fakturapulje](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Registrere en leverandørfaktura i fakturajournalen](tasks/record-vendor-invoice-invoice-journal.md)
