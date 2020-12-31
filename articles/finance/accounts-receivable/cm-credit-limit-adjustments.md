---
title: Kredittgrensejusteringer
description: Dette emnet forklarer hvordan du definerer og legger til kredittgrensejusteringer.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d55a7c5e24213f70a1b71f89691f0e5be8c36f10
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446363"
---
# <a name="credit-limit-adjustments"></a>Kredittgrensejusteringer 

[!include [banner](../includes/banner.md)]

Kredittgrensejusteringer lar kredittledere oppdatere kredittgrensene og utløpsdatoene for en enkelt kunde, en gruppe kunder eller alle kunder via en posteringsprosess. Du kan legge til oppføringer for kredittgrensejusteringer for å oppdatere kunder og kundekredittgrupper, eller du kan bruke dem til å beregne automatiske kredittgrenser. Postene kan deretter gjennomgås, sendes til godkjenning via en arbeidsflyt og posteres til kundekontoer.

## <a name="set-up-credit-limit-adjustments"></a>Definere kredittgrensejusteringer

Du kan opprette oppføringer i journalen for kredittgrensejustering på siden **Kredittgrensejustering** (**Kredittbehandling \> Kredittgrensejusteringer \> Kredittgrensejusteringer**).

1. Velg **Ny**. Det opprettes en ny gruppe med poster som har et kredittgrensejusteringsnummer.
2. Velg type kredittgrensejustering:

    - Velg **Kredittgrense** for å endre kundens kredittgrense.
    - Velg **Midlertidig kredittgrense** for å opprette en midlertidig kredittgrense i stedet for å endre kundens gjeldende kredittgrense. Midlertidige kredittgrenser overstyrer en kundes kredittgrense for en definert periode. Når denne perioden er slutt, brukes kundens kredittgrense igjen.
3. Angi en beskrivelse. 

Hvis det er merket av for **Postert**, er kredittgrensene brukt. **Godkjenningsstatus**-feltet angir journalens arbeidsflytstatus. En arbeidsflyt er valgfritt.

### <a name="add-credit-limit-adjustments"></a>Legge til kredittgrensejusteringer

Hvis du vil legge til kredittgrensejusteringer manuelt, velger du **Linjer** og følger denne fremgangsmåten.

1. Hvis du vil legge til en kredittgrensejustering for en kunde , bruker du **Kundejusteringer**-menyen. Hvis du vil legge til en kredittgrense for en kundekredittgruppe, velger du **Kundekredittgruppejusteringer**.
2. Angi en kundekonto for fakturakundekontoen som skal oppdateres med den nye kredittgrensen. Hvis du valgte **Kundekredittgruppejusteringer** i trinn 1, angir du kundekredittgruppen. Du kan ikke angi både en kundekonto og en kundekredittgruppe-ID på samme journallinje.

    Gjeldende kredittgrense vises, og navnet vises automatisk.

3. Angi den nye kredittgrensen som skal erstatte den gjeldende kredittgrensen når kredittgrenseoppføringen posteres.
4. Angi en dato for å definere den nye utløpsdatoen for kundekredittgrensen. Du må angi en utløpsdato for kredittgrensen når du oppretter en kredittgrensejustering.

**Godkjenningsstatus**-feltet angir arbeidsflytstatusen på journallinjen.

Hvis du vil at kredittgrensejusteringer skal genereres automatisk, kan du bruke **Generer**-menyen i handlingsruten.
 
### <a name="add-temporary-credit-limit-adjustments"></a>Legge til midlertidige kredittgrensejusteringer

Hvis du vil legge til midlertidige kredittgrensejusteringer manuelt, følger du denne fremgangsmåten for journallinjene.

1. Hvis du vil legge til en kredittgrensejustering for en kunde , bruker du **Kundejusteringer**-menyen. Hvis du vil legge til en kredittgrense for en kundekredittgruppe, velger du **Kundekredittgruppejusteringer**.
2. Angi en kundekonto for fakturakundekontoen som skal oppdateres med den nye kredittgrensen. Hvis du valgte **Kundekredittgruppejusteringer** i trinn 1, angir du kundekredittgruppen. Du kan ikke angi både en kundekonto og en kundekredittgruppe-ID på samme journallinje.

    Hvis det allerede finnes en aktiv eller fremtidig midlertidig kredittgrense, vises den gjeldende midlertidige kredittgrensen og datoområdet for hver midlertidige kredittgrense. Navnet vises automatisk.

3. Angi den nye kredittgrensen som skal erstatte gjeldende kredittgrense.
4. I feltene **Ny fra dato** og **Ny til dato** definerer du perioden som den fremtidige kredittgrensen er gyldig i. Du må angi utløpsdatoer for kredittgrense når du oppretter en kredittgrensejusteringsjournal.

**Godkjenningsstatus**-feltet angir arbeidsflytstatusen på journallinjen.

## <a name="generate-credit-limit-adjustments"></a>Generere kredittgrensejusteringer

Du kan også få kredittgrenser justert automatisk. I handlingsruten velger du **Generer**, og velger deretter ett av følgende alternativer:

- Fra eksisterende kunde
- Fra eksisterende kundekredittgruppe
- Automatiske kredittgrenser

### <a name="from-existing-customer"></a>Fra eksisterende kunde

Du kan opprette journallinjer fra eksisterende kunder. Når du velger **Generer \> Fra eksisterende kunde**, vises en dialogboks der du kan angi kriterier for å velge kunder og beregne de nye grensene.

1. Angi en justeringsverdi for å legge til eller trekke fra et beløp fra kredittgrensen. Angi en negativ verdi for å redusere den gjeldende kredittgrensen eller en positiv verdi for å øke den.
2. I **Verditype**-feltet velger du hvordan verdien du angav i trinn 1, skal brukes til å beregne den nye kredittgrensen:

    - Velg **Fast verdi** for å endre kredittgrensen med et beløp.
    - Velg **Prosent** for å endre kredittgrensen med en prosent.

3. Angi en verdi som brukes til å avrunde den beregnede kredittgrensen. Angi for eksempel **10,00** for å avrunde kredittgrensen til de nærmeste 10,00-valutaenhetene.
4. Angi **Avrundingsform**-feltet for å angi om resten skal rundes opp eller ned.
5. Velg metoden som brukes til å justere datoer.

    - Hvis du velger **Absolutt**, kan du angi datoer som definerer datoområdet for kredittgrensene.
    - Hvis du velger **Relativ**, kan du angi forskyvningsdatoer for området. Det gjeldende datoområdet for kredittgrensen justeres med forskyvningen.

6. Bruk hurtigfanen **Poster som skal inkluderes** for å filtrere listen over kunder som er inkludert. Hvis du ikke inkluderer filtre, genereres kredittgrenseposter for alle kunder.
7. Velg **OK** for å opprette oppføringene for kredittgrensejusteringer.

### <a name="from-existing-customer-credit-group"></a>Fra eksisterende kundekredittgruppe

Du kan opprette journallinjer fra eksisterende kundekredittgrupper. Når du velger **Generer \> Fra eksisterende kundekredittgruppe**, vises en dialogboks der du kan angi kriterier for å velge kundekredittgrupper og beregne de nye grensene. Kriteriene er de samme kriteriene som brukes til å opprette journallinjer fra eksisterende kunder. Se trinnene i den forrige delen.

### <a name="automatic-credit-limits"></a>Automatiske kredittgrenser

Du kan opprette automatiske kredittgrenser for å definere og oppdatere kundekredittgrenser. De automatiske kredittgrensene opprettes for en risikogruppe, og de er basert på bestemte verdier som brukes i resultatgruppene. Du kan bruke disse automatiske kredittgrensene til å generere kredittgrenseoppføringer. Hvis en kunde er tilordnet en bestemt risikogruppe, og kundens kredittinformasjon samsvarer med kriteriene for en automatisk kredittgrense, opprettes en post for kredittgrensejustering.

#### <a name="create-automatic-credit-limits"></a>Opprette automatiske kredittgrenser

Du oppretter automatiske kredittgrenser ved hjelp av kredittgrensejusteringer. Når du velger **Generer \> Automatiske kredittgrenser**, vises en dialogboks der du kan angi en utløpsdato for de nye kredittgrensene som opprettes, basert på risikogruppene som kunder er tilordnet. Når du er ferdig, velger du **OK** for å opprette kredittgrensejusteringslinjer.

### <a name="post-adjustments"></a>Postere justeringer

Når du har opprettet justeringslinjer for kredittgrense, kan du bruke **Poster**-knappen i handlingsruten til å postere postene og oppdatere kundekredittgrensene. Hvis du har definert en arbeidsflyt, må du imidlertid velge **Arbeidsflyt \> Send** i handlingsruten for å sende journalen til godkjenning.

### <a name="credit-limit-adjustments-workflows"></a>Arbeidsflyter for kredittgrensejusteringer

Arbeidsflytene for **kredittgrensejusteringer** kan brukes til å sende kredittgrensejusteringer via en godkjenningsprosess for arbeidsflyt. Du kan opprette to arbeidsflyter på siden **Arbeidsflyt for kredittbehandling** (**Kredittbehandling \> Oppsett \> Arbeidsflyt for kredittbehandling**):

- **Kredittgrensejusteringer** – Denne arbeidsflyten kan brukes til å godkjenne oppføringer på hodenivå.
- **Linje for kredittgrensejusteringer** – Denne arbeidsflyten kan brukes til å godkjenne justeringsoppføringene, slik at oppføringene kan godkjennes av forskjellige personer, basert på kriteriene i arbeidsflyten.

> [!NOTE]
> Når du oppretter arbeidsflyten **Kredittgrensejusteringer**, kan du konfigurere den slik at justeringene automatisk posteres etter at linjene er godkjent. Du må bare ta med oppgaven **Poster journal automatisk** i arbeidsflyten.
