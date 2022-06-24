---
title: Arbeidsområde for fordelsbehandling
description: Denne artikkelen beskriver arbeidsområdet Fordelsbehandling i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7975d1723e07ae390961d4f44e0f34f2ff2df44d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902925"
---
# <a name="benefits-management-workspace"></a>Arbeidsområde for fordelsbehandling


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Denne artikkelen beskriver arbeidsområdet **Fordelsbehandling** i Dynamics 365 Human Resources.

> [!NOTE]
> Hvis du vil vise arbeidsområdet **Fordelsbehandling**, må du først aktivere arbeidsområdet **(Forhåndsversjon) Arbeidsområdet Fordelsbehandling** i Funksjonsstyring. Hvis du vil ha mer informasjon om hvordan du aktiverer forhåndsvisningsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).<br><br>![Aktivere arbeidsområdet Fordelsbehandling.](./media/hr-benefits-management-workspace-enable.png)

Arbeidsområdet **Fordelsbehandling** gir deg rask oversikt over fordeler som krever din oppmerksomhet. På denne siden vises følgende:

- Totaler for varer som venter på handling
- Arbeidere med ikke-bekreftede valg
- Arbeidere som nylig registrerte seg i fordeler
- Arbeidere med fremtidige livshendelser
- Nyansettelser som ikke er registrert
- Arbeidere med aktive livshendelser
- Arbeidere med åpne registreringer som ikke har valgt noen planer

![Arbeidsområde for fordelsbehandling.](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Vise handlingselementer

Du kan vise handlingselementene ved å velge en flis eller en fane. Hvis du velger en fane, kan du vise og velge arbeidere fra arbeidsområdesiden.

![Handlingselementer.](./media/hr-benefits-management-workspace-action-items.png)

Hvis du velger en flis, går du til siden for dette området. Hvis du for eksempel velger en av disse flisene, vises siden **Planer for arbeidsfordeler** filtrert for ansatte du må utføre en handling med:

- **Ubekreftede valg**
- **Åpne registreringer uten utsjekkede planer**
- **Registrert i fordeler**
- **Ny ansatt ikke registrert**

![Fordelsplaner for arbeider.](./media/hr-benefits-management-workspace-plans.png)

Hvis du velger flisen **Aktive livshendelser** eller **Fremtidige livshendelser** kommer du til en liste over aktive eller fremtidige livshendelser.

![Levetidshendelser.](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Behandler

Hvis du vil behandle registreringsrettighet, livshendelser eller endringsoppdateringer for satser, velger du det riktige elementet i navigasjonslinjen.

![Behandles.](./media/hr-benefits-management-workspace-processing.png)

Hvis du vil vise prosessresultater, velger du **Prosessresultater** på siden.

![Prosessresultater.](./media/hr-benefits-management-workspace-process-results.png)

Hvis du vil ha mer informasjon om fordelsbehandling, kan du se:

- [Behandle registreringsberettigelse](hr-benefits-process-enrollment-eligibility.md)
- [Behandle endringer i levetidshendelse](hr-benefits-process-life-event-changes.md)
- [Behandle rettighet for levetidshendelse](hr-benefits-process-life-event-eligibility.md)
- [Behandle levetidshendelser](hr-benefits-process-life-events.md)
- [Behandle satsendringer](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Endre periode

Hvis du vil vise en annen fordelsperiode, velger du den fra rullegardinlisten **Periode**.

![Endre periode.](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>Åpne registreringsfanen

Du kan vise handlingselementene ved å velge en flis eller en fane. Hvis du velger en fane, kan du vise og velge arbeidere på arbeidsområdesiden.
Kategorien **Åpne registrering** gir hovedmetrikk for den åpne registreringsprosessen. 

Informasjon om åpen registrering vises 30 dager før **startdatoen for registrering**. Dette er definert i **Perioder**-oppsettet i **Fordelsbehandling** > **Koblinger** > **Perioder**, i feltet **Startdato for registrering**.  Hvis du vil endre denne innstillingen, kan du gå til **Delte parametere for Human Resources** > **Fordelsbehandling** > **Åpne registreringsalternativer** og oppdetere **Antall**-feltet.  

Følgende informasjon er tilgjengelig i kategorien **Åpne registrering**:
 - Ansatte som ikke har startet den åpne innmeldingsprosessen
 - Ansatte som har pågående valg
 - Ansatte som har fullført valgprosessen
 - Ubekreftede valg

**Sammendrag-fliser**

- **Ikke startet** – **Ikke startet**-flisen viser en telling av ansatte som ikke har startet registreringsprosessen. **Ikke startet**-flisen er en filtrert liste som bare viser de ansatte som ikke har planer valgt, frafalt eller sjekket ut for den åpne registreringsplanperioden. Obligatoriske planer ignoreres og tas ikke med fordi de er valgt som standard for den ansatte.  Du kan drille tilbake på denne flisen for å se en liste over ansatte som ikke har startet den åpne registreringsprosessen på siden **Forselsplaner for arbeider**.

  > [!NOTE]
  > Hvis du ikke vil spore den åpne registreringsfremdriften for en **Plantype**, kan du utelate den ved å gå **Fordelsbehandling** > **Lenker** > **Parametere for ansattselvbetjening** > **Oppsett av fordelsplanflis** og oppdatere feltet **Spor åpen registreringsfremdrift**.  Du kan for eksempel ha planer opprettet der **Plantype** = **Annet**. Disse planene kan være valgfrie planer som du ikke vil spore fremdriften for registrering for. Hvis du ikke velger denne plantypen, blir planer av disse typene ignorert ved sporing av fremdrift for registrering eller fullføring i kategorien **Åpne registrering**. Denne innstillingen gjelder for plantypen som er valgt for alle perioder og juridiske enheter.

- **Pågår** – **Pågår**-flisen viser antall ansatte som har valg som pågår. Flisen **Pågår** er en filtrert liste som bare viser ansatte som har minst én plan som er fratatt eller valgt. Obligatoriske planer ignoreres og tas ikke med fordi de er valgt som standard for den ansatte. Du kan drille tilbake fra denne flisen for å se de valgte og frafalte planene på siden for **masseoppdatering av fordeler for fordelsplaner**.

- **Registrert i fordeler** – Flisen **Registrert i fordeler** viser et antall ansatte som er fullt registrert i fordeler. Flisen **Registrert i fordeler** er en filtrert liste som viser ansatte som enten har valgt eller fratatt seg alle planer. Spørringen ekskluderer planer som ikke spores for åpen registrering på siden **Parametere for ansattselvbetjening**. Du kan drille tilbake fra denne flisen for å se en liste over ansatte på siden **Fordelsplaner for arbeider**.

- **Ubekreftede valg** – Flisen **Ubekreftede valg** viser antallet ansatte som har planer som er valgt eller frafalt og som må bekreftes. Du kan drille tilbake fra denne flisen for å se siden for **masseoppdatering av fordeler for fordelsplaner**.

**Aktivitet**

- **Ikke startet** – **Ikke startet**-fanen viser en liste over ansatte som ikke har startet registreringsprosessen. **Ikke startet**-flisen er en filtrert liste som bare viser ansatte som ikke har planer valgt, frafalt eller sjekket ut for den åpne registreringsplanperioden. Obligatoriske planer ignoreres og tas ikke med fordi de er valgt som standard for den ansatte. Du kan drille ned på arbeideren for å vise detaljsiden for **Fordelsplaner for arbeider**.

- **Valg som pågår** – Flisen **Valg som pågår** viser en liste over ansatte som har valg som pågår. Flisen **Valg som pågår** er en filtrert liste som viser ansatte som har minst én plan som er fratatt eller valgt. Obligatoriske planer ignoreres og tas ikke med fordi de er valgt som standard for den ansatte. Du kan drille ned på arbeideren for å vise detaljsiden for **Fordelsplaner for arbeider**.

## <a name="view-more-options"></a>Vise flere alternativer

Hvis du vil vise mer informasjon og flere handlinger, velger du **Koblinger**.

![Koblinger.](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Se også

[Oversikt over fordelsbehandling](hr-benefits-management-overview.md)
