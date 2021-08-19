---
title: Posteringsoppsett for rabattbehandling
description: Dette emnet beskriver hvordan du setter opp posteringsprofiler. Posteringsprofiler brukes til å bestemme posteringsoppføringer for beregningslinjer i Rabattbehandling.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 4eb0c38baa0b46c535e9394673d5a046f761ac71a9633edcc6ee7f237ff7691d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725680"
---
# <a name="rebate-management-posting-setup"></a>Posteringsoppsett for rabattbehandling

[!include [banner](../includes/banner.md)]

Posteringsprofiler i Rabattbehandling brukes til å bestemme posteringsoppføringer for beregningslinjer i Rabattbehandling. Når en posteringsprofil er valgt på avtalehodet, gjelder den for alle avtalelinjer.

Denne funksjonen fungerer på tvers av firmaer (juridiske enheter). Du kan angi firmaet som avsetningene skal avsettes til, og som krav vil bli betalt av. Du kan også angi ulike avsetningsdebetkontoer og avskrivingskreditkontoer per kildeposteringsfirma.

Hvis du vil definere posteringsprofiler for rabattstyring for kunder og leverandører, kan du gå til **Rabattbehandling \> Posteringsoppsett for rabattbehandling \> Posteringsprofiler i Rabattbehandling**. Siden **Posteringsprofiler i Rabattbehandling** inneholder en listerute som viser alle de eksisterende profilene dine. Du kan bruke knappene i handlingsruten til å legge til profiler i listen eller fjerne dem.

Resten av delene i dette emnet beskriver hvordan du bruker de tilgjengelige feltene når du oppretter eller redigerer en profil.

## <a name="posting-profile-header"></a>Posteringsprofilhode

I tabellen nedenfor beskrives innstillingene som er tilgjengelige i hodedelen i hver posteringsprofil i Rabattbehandling.

| Felt | beskrivelse |
|---|---|
| Posteringsprofil | Angi et unikt navn for profilen. |
| beskrivelse | Angi en beskrivelse av profilen. |
| Modul | Velg modulen som rabatter og royalty for profilen er forbundet med (*Kunde* eller *Leverandør*). |
| Type | Velg profiltypen (*Rabatt* eller *Royalty*). |
| Betalingsmiddel | <p>Dette feltet bestemmer formatet for de posterte rabattutdataene.<p><p>Når **Type**-feltet er satt til *Rabatt*, er følgende verdier tilgjengelige:</p><ul><li>*Betal ved å bruke leverandør* – Når du posterer en kunderabatt, opprettes det en leverandørfaktura for remitteringsleverandøren som er definert for rabattkunden. Når du posterer en leverandørrabatt, opprettes det en leverandørfaktura for rabattleverandørkunden.</li><li>*Kundefradrag* – Når du posterer rabatten, opprettes det en kundefradragsjournal for rabattkunden.</li><li>*Kundefradrag for avgiftsfaktura* – Når du posterer rabatten, opprettes det en fritekstfaktura for rabattkunden.</li><li>*Forretningsutgifter* – Når du posterer rabatten, opprettes det en kundefradragsjournal for rabattkunden.</li><li>*Rapportering* – Når du posterer rabatten, opprettes det en kundefradragsjournal for rabattkunden.</li></ul><p>Når **Type**-feltet er satt til *Royalty*, er følgende verdier tilgjengelige:</p><ul><li>*Betal ved å bruke leverandør* – Når du posterer rabatten, opprettes det en leverandørfaktura for rabattleverandørkunden.</li><li>*Rapportering* – Når du posterer rabatten, opprettes det en leverandørfaktura for rabattleverandørkunden.</li></ul><p>Hvis du vil ha mer informasjon, kan du se delen [Betalingstyper](#payment-types) nedenfor. |
| Bedrift | Velg firmaet (juridisk enhet) som avsetningene skal avsettes til, og som krav vil bli betalt av. |

### <a name="payment-types"></a>Betalingstyper

Tabellen nedenfor oppsummerer hvordan de forskjellige innstillingene i **Betalingstype**-feltet påvirker hvor betalingene posteres. Betalinger kan posteres til en kundekonto, leverandørkonto eller remitteringskonto, avhengig av måltransaksjonen og rabattypen.

| Betalingsmiddel | Måltransaksjonstype | Rabattype | Betaling til (fakturakonto) |
|---|---|---|---|
| Betal ved å bruke leverandører | Leverandørfakturajournal | Kunderabatt | Kundens remitteringsleverandørkonto |
| Betal ved å bruke leverandører | Leverandørfakturajournal | Kunderoyalty | Leverandørnummer |
| Betal ved å bruke leverandører | Leverandørfakturajournal | Leverandørrabatt | Leverandørnummer |
| Kundefradrag | Daglig journal | Kunderabatt | Kundekonto |
| Fradrag for avgiftsrakturakunde | Fritekstfaktura | Kunderabatt | Kundekonto |
| Forretningsutgifter | Daglig journal | Kunderabatt | Kundekonto |
| Rapportering | Daglig journal | Kunderabatt | Kundekonto |
| Rapportering | Leverandørfakturajournal | Kunderoyalty | Leverandørnummer |
| Rapportering | Leverandørfakturajournal | Leverandørrabatt | Leverandørnummer |

> [!NOTE]
> Vurder følgende punkter når du setter opp [Rabattbehandlingsavtaler](rebate-management-deals.md):
>
> - For avtaler der feltet **Avstem etter** er satt til *Avtale*, kan du ikke bruke den dynamiske avtalekontoen under postering. Du må bruke en angitt kunde- eller leverandørkonto.
> - For avtaler der feltet **Avstem etter** er satt til *Linje*, kan du bruke en posteringsprofil som utligner til en dynamisk avtalekonto på avtalelinjen, fordi kunden eller leverandøren er definert per avtalelinje.

## <a name="posting-fasttab"></a>Hurtigfanen Postering

I tabellen nedenfor beskrives feltene som er tilgjengelige på hurtigfanen **Postering** i hver posteringsprofil i Rabattbehandling.

| Felt | beskrivelse |
|---|---|
| Kredittype | Velg om du vil kreditere en finanskonto eller en kunde. Hvis **Betalingstype**-feltet i hodet er satt til *Fradrag for avgiftsrakturakunde*, settes dette feltet til *Finanskonto*. For leverandørfakturaer er dette feltet satt til *Finanskonto*. |
| Kreditkonto | Velg kontoen som kreditbeløpene posteres til når det utføres rabattavsetninger. Denne kontoen blir også brukt som en motkonto når rabatten posteres for å kreditere kunden eller debitere leverandøren. |
| Journalnavn<br>(I **Avsetning**-delen) | Velg navnet på journalen som skal brukes til å registrere den posterte avsetningen. |
| Type | Velg om du vil postere rabatten til en finanskonto eller til en kunde eller leverandør. Hvis **Betalingstype**-feltet i hodet er satt til *Fradrag for avgiftsrakturakunde*, settes dette feltet til *Kunde/leverandør*. |
| Bruk kontokilde | <p>Velg én av følgende verdier:</p><ul><li>*Fast konto* – Hvis du velger denne verdien, må du angi en konto i **Rabattkonto**-feltet.</li><li>*Avtalelinjekonto* – Bruk kunde- eller leverandørkontoen som er angitt på rabattlinjen. Du kan bare velge denne verdien for avtaler der feltet **Avstem etter** er satt til *Linje*, og for avtalelinjer der feltet **Kontokode** er satt til *Tabell*. Den gjelder ikke kundeposteringsprofiler eller leverandørrabatter som er basert på salgsordrer.</li></ul> |
| Rabattkonto | Kontoen som den faktiske rabattutgiften blir postert til. |
| Journalnavn<br>(I feltgruppen **Rabattbehandling**) | Velg navnet på journalen som skal brukes til å postere en kreditnota for rabattbeløpet til kunden eller leverandøren. Dette feltet er utilgjengelig når **Betalingstype**-feltet i hodet er satt til *Fradrag for avgiftsfakturakunde*. For kunderabatter vil journalnavn av journaltypen *Daglig* være tilgjengelige. For kunde royalty- og leverandørrabatter vil journalnavn av journaltypen *Registrering av leverandørfaktura* være tilgjengelige. |
| Varens mva-gruppe | Angi om rabatten er avgiftspliktig. |
| Journalnavn<br>(I feltgruppen **Avskrive**) | Hvis rabatten som posteres, ikke er lik avsetningen, kan differansen skrives av. Velg navnet på journalen som skal brukes til å registrere den posterte avskrivningen. |

## <a name="posting-by-company-fasttab"></a>Hurtigfanen Postering etter firma

Med hurtigfanen **Postering etter firma** i hver posteringsprofil i Rabattbehandling kan du angi posteringskontoen som brukes av hvert firma (juridisk enhet) i rutenettet.

Bruk knappene på verktøylinjen til å legge til firmaer i rutenettet eller fjerne dem. Hver gang du legger til en rad i rutenettet, bruker du **Firma**-feltet til å angi den juridiske enheten for denne raden. **Navn**-feltet angis deretter automatisk.

Merk raden for hvert firma, og skriv deretter inn følgende informasjon ved hjelp av feltene under rutenettet:

- **Debettype** – Velg om du vil debitere en finanskonto eller en leverandør. For kunderabatter og royalties er dette feltet satt til *Finanskonto*.
- **Debetkonto** – Angi kontoen som debetbeløpet skal posteres til når det utføres rabattavsetninger.
- **Hovedkonto** – Velg hovedkontoen for avskrivninger.
