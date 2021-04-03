---
title: Feilsøk lagerkonfigurasjon
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du konfigurerer Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1fe285f05e5f1ddcb7bd206290b9954cbdaffc75
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487103"
---
# <a name="troubleshoot-warehouse-configuration"></a>Feilsøk lagerkonfigurasjon

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du konfigurerer Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Jeg får følgende feilmelding: Nummerskiltet eller lokasjonen er ugyldig.

### <a name="issue-description"></a>Problembeskrivelse

Du får denne feilmeldingen når du skanner en nummerskilt-ID eller lokasjon.

### <a name="issue-resolution"></a>Problemløsning

Pass på at nummerskilt-ID-en ikke er reserver av noe annet. Dette problemet oppstod tidligere når verdien som en bruker skannet i lagerappen, var både en gyldig lokasjon og en gyldig nummerskilt-ID. Dette problemet ble imidlertid løst i versjon 10.0.11.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>Jeg får følgende feilmelding: Nummerskilt må angis for denne lokasjonen.

### <a name="issue-description"></a>Problembeskrivelse

Du får denne feilmeldingen hvis du oppretter en overføringsordre ved hjelp av et lager som er aktivert for avansert lagerstyring (WMS), og etter at arbeidet er fullført, prøver du å bekrefte forsendelsen.

### <a name="issue-resolution"></a>Problemløsning

Feltet **Standard mottakssted** er tomt for et transittlager i fra-lageret. Du kan løse dette problemet ved å angi en standard mottakssted i transittlageret. Kontroller at denne plasseringen er nummerskiltkontrollert.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>Jeg får følgende feilmelding: Du kan ikke opprette en arbeidsmallinje for lagerstatusendring fordi arbeidstypen ikke er gyldig. Velg en annen arbeidstype.

### <a name="issue-description"></a>Problembeskrivelse

Du kan ikke velge *Lagerstatusendring* i **Arbeidstype**-kolonnen i delen **Arbeidsmaldetaljer**.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er standard. Arbeidstypen *Lagerstatusendring* brukes bare av systemprosesser. Den kan ikke konfigureres. Fordi listen over arbeidstyper er fast som en opplisting, kan ikke de ekstra postene filtreres ut fra rullegardinmenyen **Arbeidstype**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Jeg får følgende feilmelding: Antallet er ikke gyldig for enhet 1%.

### <a name="issue-description"></a>Problembeskrivelse

Antallet er ikke gyldig for *ea*-enheten når det er et plukkarbeid som har flere nummerskilter på ett sted.

### <a name="issue-resolution"></a>Problemløsning

Kontroller at feltene **Sekvensgruppe-ID for enhet** og **Enhetskonverteringer** i frigitt produkt eller produktvariant er riktig angitt.

Legg merke til at feilmeldingen er forbedret i versjon 10.0.15 (se [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Den nye feilmeldingen er Antallet er ikke gyldig. Forventet %1 %2.

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>I lokasjonsdirektiver for plasseringsarbeid for salgsordre evaluerer ikke alternativet flere SKU-er flere lokasjonsdirektivhandlinger.

### <a name="issue-description"></a>Problembeskrivelse

Lokasjonsdirektiver for *Salgsordre*-arbeidsordretypen og *Plasser*-arbeidstypen evaluerer ikke fler lokasjonsdirektivhandlinger når det **Flere SKU-er** er valgt. Bare den første lokasjonsdirektivhandlingen evalueres.

### <a name="issue-resolution"></a>Problemløsning

En ny funksjon, *Evaluere alle handlinger for lokasjonsdirektiver med flere SKU-er*, er lagt til i versjon 10.0.15 (se [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Denne funksjonen evaluerer alle handlinger for lokasjonsdirektiver med flere SKU-er. Hvis du trenger denne funksjonen, kan du bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere den.

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a>Jeg kan ikke bruke lagerappen til delvis plukking.

### <a name="issue-description"></a>Problembeskrivelse

For salgs- og overføringsordrer kan du ikke hoppe over varer og foreta delvis plukking.

### <a name="issue-resolution"></a>Problemløsning

På siden **Menyelementer på mobilenheten** for hvert menyelement som er konfigurert til å behandle salgsordrer eller overføringsordrer, angir du alternativet **Tillat deling av arbeid** på hurtigfanen **Generelt** til *Ja*.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Hvordan kan jeg utføre en lagerstatusendring for arbeid med delvis antall?

### <a name="issue-description"></a>Problembeskrivelse

Du vil utføre en lagerstatusendring for et delvis antall i et parti.

### <a name="issue-resolution"></a>Problemløsning

Hvis du vil at arbeidere skal kunne utføre denne endringen, kan du opprette et menyelement for lagerappen. Opprett (eller rediger) et menyelement som har følgende innstillinger på siden **Menyelementer på mobilenheten**:

- **Modus:** *Arbeid*
- **Bruke eksisterende arbeid:** *Nei*
- **Arbeidsopprettelsesprosess:** *Flytting*
- **Vis beholdningsstatus:** *Ja*

Du kan angi andre felter på siden slik du ønsker.

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>Sonebehandlingsprofilen for en lokasjonsprofil hindrer ikke at lagertypene blir kombinert.

### <a name="issue-description"></a>Problembeskrivelse

Du bruker *policyer for forsendelseskonsolidering*. Du har definert en *sonebehandlingsprofil* for en *lokasjonsprofil*, men når arbeidet opprettes, er lagertypene kombinert ved den endelige lokasjonen.

### <a name="issue-resolution"></a>Problemløsning

Sonebehandlingsprofiler krever at arbeid deles på forhånd. Med andre ord forventer sonebehandlingsprofilen at et arbeidshode ikke vil ha flere plasseringslokasjoner.

Du må konfigurere et arbeidshodeskift for at sonebehandlingsprofilen skal kunne styre kombinasjonen av lager på en effektiv måte.

I dette eksemplet konfigureres vår sonebehandlingsprofil slik at **Lagertyper som ikke skal kombineres**, settes til *Forsendelses-ID*, og vi konfigurerer et hodeskift for profilen:

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Velg **arbeidsordretypen** du vil redigere (for eksempel *Bestillinger*).
1. Velg arbeidsmalen du vil redigere.
1. I handlingsruten velger du **Rediger spørring**.
1. Åpne fanen **Sortering**, og legg til en rad med følgende innstillinger:
    - **Tabell** - *Midlertidige arbeidstransaksjoner*
    - **Avledet tabell** - *Midlertidige arbeidstransaksjoner*
    - **Felt** - *Forsendelses-ID*
1. Velg **OK**.
1. Du kommer tilbake til siden **Arbeidsmaler**. Velg **Arbeidshodeskift** i handlingsruten.
1. I handlingsruten velger du **Rediger**.
1. Merk av i avmerkingsboksen som er knyttet til **Feltnavn** *Forsendelses-ID*.
1. Velg **Lagre** i handlingsruten.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
