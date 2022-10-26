---
title: Arbeidsområde for Invoice Capture-løsning
description: Denne artikkelen gir informasjon om arbeidsområdet for Invoice capture-løsningen.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691193"
---
# <a name="invoice-capture-solution-workspace"></a>Arbeidsområde for Invoice Capture-løsning

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Side-ved-side-visningsprogram for Invoice capture-løsningen

Registrering av fakturaer i systemet har vanligvis vært en tidkrevende prosess som er utsatt for feil, fordi assistenter må navigere i flere vedleggsfiler og vinduer for å samle inn riktig informasjon. Side-ved-side-dokumentvisningen vil hjelpe deg når du arbeider på fakturaer, ved å gjøre prosessen enklere, mer effektiv og mer nøyaktig.

I side-ved-side-dokumentvisningen kan brukere vise det opprinnelige dokumentet og fakturaen side om side i samme vindu. Fakturasiden fylles ut med informasjon som kommer fra det opprinnelige fakturadokumentet. Visningen bygger opp koblingen mellom fakturasidefeltene og det opprinnelige fakturadokumentet. Visningsprogrammet hjelper også brukere med å finne eventuelle feil som finnes på fakturasiden.

### <a name="open-the-side-by-side-viewer"></a>Åpne side-ved-side-visningsprogrammet

I Microsoft Dynamics 365 Finance kan du åpne visningsprogrammet for side-ved-side fra listen på sammendragssiden eller fra fakturalistesiden. Du kan også åpne den ved å dobbelttrykke (eller dobbeltklikke) en post eller ved å velge fakturanummeret.

### <a name="using-the-side-by-side-viewer"></a>Bruke side-ved-side visningsprogram

#### <a name="manually-review-an-invoice"></a>Se gjennom en faktura manuelt

Et fakturadokument som er importert, kan kreve manuell gjennomgang på grunn av feil eller advarsler. I side-ved-side-visningsprogrammet viser dokumenthodet statusen **Importert**, og gjeldende versjon vil være **Originalversjon**.

Hvis du vil begynne å se gjennom fakturaen, velger du **Start gjennomgang**. Alle feltene blir redigerbare. **Status**-feltet oppdateres til **Til vurdering**, og feltet **Gjeldende versjon** oppdateres til **Endret versjon**.

#### <a name="view-and-work-with-messages"></a>Vise og arbeide med meldinger

Brukere bør starte kontrollprosessen fra meldingsruten. Feilmeldinger angis av en rød X, advarselsmeldinger angis av et triangel, og informasjonsmeldinger angis av en sirkel. Konfidensresultat–tilknyttede meldinger kan klassifiseres som enten advarsler eller feil, avhengig av terskelen som er definert av konfigurasjonsgruppen. Hvis du vil ha mer informasjon, kan du se [Konfigurasjonsgrupper for Invoice Capture-løsning](invoice-capture-config-group.md).

Advarsel og feilmeldinger kan ignoreres fra meldingsruten, fakturahodet eller fakturalinjene. Etter at en melding er ignorert, vises den ikke lenger som en feil eller en advarsel, og fakturaen vil ikke mislykkes validering.

- Velg **Ignorer** hvis du vil ignorere meldinger fra meldingsruten. Hvis du vil tilbakestille en melding som er ignorert, velger du **Ignorer** på nytt. Typen blir deretter endret fra feil eller advarsel til informasjon.
- Hvis du vil ignorere meldinger fra fakturahodet eller fakturalinjen, velger du **Ignorer** i feltet. Meldingssymbolet forsvinner. Den vises imidlertid på nytt hvis meldingen tilbakestilles fra meldingsruten.

For meldinger som er relatert til fakturahodefelt, flyttes markøren til det tilsvarende feltet i hodedelen når du velger meldingen i meldingsruten.

#### <a name="proofread-and-edit-fields"></a>Korrekturlese og redigere felt

Hvis verdien til et felt leses fra den opprinnelige fakturaen via optisk tegngjenkjenning (OCR), vises et symbol i feltet. Hvis du velger symbolet, vil dokumentvisningsprogrammet markere stedet feltverdien leses fra, for å hjelpe deg med å bekrefte fakturadataene.

Følg én av disse trinnene for å tilbakestille dokumentvisningen til den opprinnelige forstørrelsen:

- Velg det samme symbolet som du valgte tidligere.
- Velg knappen i hjørnet øverst til høyre i dokumentvisningsprogrammet.

Rediger feltene etter behov. Redigeringer lagres automatisk når markøren går ut av et felt. Et symbol til høyre for et felt angir at feltet er oppdatert manuelt. Når siden oppdateres, fjernes symbolet.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>Kontrollere en faktura for å få oppdaterte meldinger

Når du redigerer et felt, oppdateres feltverdien, men nye valideringsmeldinger genereres ikke. Velg **Sjekk** for å få oppdaterte valideringsmeldinger. Meldingene i meldingsruten, i fakturahodet og på fakturalinjene oppdateres.

#### <a name="complete-the-review"></a>Fullføre gjennomgangen

Velg **Fullfør gjennomgang** for å fullføre gjennomgangen. Fakturaene valideres. Hvis det blir funnet feil, beholdes dokumentstatusen **Til vurdering**, og det vises en meldingslinje. Alle meldinger i meldingsruten og i fakturahodet og -linjene oppdateres automatisk for å gi informasjon om årsakene til den mislykkede valideringen.

Når alle blokkeringsfeilene er reparert, kan gjennomgangen fullføres. Dokumentstatusen oppdateres til **Gjennomgått**, og feltene kan ikke lenger redigeres. Du kan starte gjennomgangen på nytt ved å velge **Start gjennomgang** på nytt.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Generere en ventende leverandørfaktura i Finance

Hvis du vil sende fakturadokumentet til det tilknyttede Finance-miljøet, velger du **Generer**. Hvis fakturagenereringen mislykkes, vises det en feilmelding i en meldingslinje.

#### <a name="void-an-invoice"></a>Annullere en faktura

Hvis du vil annullere en faktura, velger du **Annullert**. Annullerte fakturaer kan ikke gjennomgås, og innhold vises ikke i listen **Fakturaer krever manuell gjennomgang**.

### <a name="validation-logic"></a>Valideringslogikk

Noen nøkkelfelt i side-ved-side-visningsprogrammet finnes ikke i fakturasamlingsdataene, men er nødvendige for å generere utestående fakturaer i Finance. Disse feltene er avledet fra en kombinasjon av gjeldende fakturaoppsamlingsdata og hoveddata fra Finance.

Feltene som må avledes, er **Juridisk enhet**, **Leverandørkonto** og **Varenummer**. De må avledes i denne rekkefølgen. Hvis avledningen av et felt mislykkes, stopper prosessen.

1. **Juridisk enhet** – Den juridiske enheten avledes først. Hvis det blir funnet en aktiv tilordningsregel for den juridiske enheten, avledes den juridiske enheten basert på firmanavnet og firmaadressen.
2. **Leverandørkonto** – Deretter avledes leverandørkontoen basert på en aktiv tilordningsregel og en kombinasjon av den avledede juridiske enheten og leverandørens navn og leverandøradresse.
3. **Varenummer** – Til slutt avledes varenavnet fra oppsamling, basert på følgende tre typer informasjon:

    - En konfigurert tilordningsregel
    - Den avledede juridiske enheten
    - Den avledede leverandørkontoen

Hvis du vil kjøre en validering, velger du **Sjekk** i visningsprogrammet side ved side. For øyeblikket utfører valideringen følgende kontroller:

- **Obligatorisk kontroll** – Denne kontrollen validerer de obligatoriske feltene for visningsprogrammet side ved side. Brukerne kan velge hvilke felt som må være obligatoriske, på siden **Konfigurasjonsinnstillinger**.
- **Konfidenspoeng** – Brukere kan angi varselsterskelen og feilterskelen for konfidensresultat. Denne kontrollen fokuserer på konfidensresultatet fra OCR som er under disse terskelverdiene. Feilmeldinger eller advarsler vil bli vist basert på valideringsresultatet.
- **Juridisk enhet** – Denne kontrollen validerer at en juridisk enhet er i Finance. Hvis den juridiske enheten ikke eksisterer i Finance-miljøet, mislykkes valideringen.

Når visningsprogrammet side-ved-side brukes for første gang, og brukeren velger **Sjekk**, kjøres avledingen og valideringsprosessen. Hvis fakturaene er nøyaktige, kjøres valideringsprosessen når brukeren velger **Fullført gjennomgang**. Den kjøres også når brukeren velger **Generer leverandørfaktura**.

Avledingsprosessen skjer før valideringsprosessen, og alle advarsler eller feil kommer fra valideringsprosessen. Advarslene og feilene blir logget i Finance.
