---
title: Inntektsføringsbunter
description: Dette emnet beskriver buntfunksjonaliteten som er inkludert i inntektsføringsfunksjonaliteten i Kunder. En bunt består av en overordnet vare og flere komponentvarer.
author: kweekley
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: bce824267f435d9de0acd43ca145e0d148dfe67c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816274"
---
# <a name="revenue-recognition-bundles"></a>Inntektsføringsbunter

[!include [banner](../includes/banner.md)]

Dette emnet beskriver buntfunksjonaliteten som er inkludert i inntektsføringsfunksjonaliteten i Kunder. En bunt består av en overordnet vare og flere komponentvarer. Den overordnede varen registreres på en salgsordre, slik at ordreregistreringen blir mer effektiv. Den deles imidlertid opp i komponentvarene. Interne dokumenter, for eksempel følgeseddelen, viser komponentvarer. Eksterne dokumenter vil imidlertid bare vise den overordnede varen.

> [!NOTE]
> Microsoft Dynamics 365 Commerce-kanaler, for eksempel online, salgssted og telefonsentre, støtter ikke inntektsføringen (inkludert buntfunksjonaliteten). Dette omfatter også kundeemnet til kontantløsning for Dynamics 365 Supply Chain Management og Dynamics 365 Sales. Varer som er konfigurert til å bruke inntektsføring, bør ikke legges til i ordrer eller transaksjoner som opprettes i Commerce-kanaler, eller i kundeemnet til kontantløsning.

Hvis du vil definere bunter, må du angi konfigurasjonsnøklene for inntektsføring. Du kan imidlertid bruke bunter selv om inntektsføring ikke er konfigurert. På samme måte kan du bruke inntektsføring hvis bunter ikke er konfigurert. Hvis inntektsføring er konfigurert, bestemmer komponentvarene inntektsprisen og inntektsplanen som brukes til inntektsføring eller periodisering når en salgsordre faktureres.

Konfigurasjonen for bunter bruker stykklistefunksjonaliteten (BOM). Hvis du vil ha mer informasjon om hvordan du konfigurerer en buntvare, kan du se [Inntektsføringsoppsett](revenue-recognition-setup.md). Hvis den overordnede varen er flagget som en bunt, behandles den på en annen måte enn andre stykklistevarer. Her er en liste over forskjellene:

- Bunter må deles opp via salgsordrebekreftelse ved å velge **Bekreft salgsordre** på fanen **Selge** i handlingsruten på salgsordresiden. Buntvarer må aldri deles opp ved å velge **Stykklistelinje** under **Del opp** på menyen **Salgsordrelinje** i hurtigfanen **Salgsordrelinjer**. Ellers behandles varen som en stykkliste, ikke som en bunt.
- En salgsordre som inneholder en buntvare, må bekreftes før følgeseddelen eller fakturaen opprettes.
- Når en bunt deles opp via salgsordrebekreftelse, annulleres den overordnede varen, og enhetsprisen og rabattene tilordnes komponentvarene for bunten.
- Summen av komponentvarene må alltid være lik prisen på den overordnede varen. Derfor er det begrensninger på feltene som kan oppdateres eller endres for komponentvarer. Enhetsprisen kan for eksempel ikke endres manuelt. Den kan heller ikke endres indirekte ved at en ny prisavtale trer i kraft. Hvis du vil hindre en ny prisavtale, kan ikke lagerdimensjonene endres på komponentvarene.
- Når et eksternt dokument, for eksempel salgsordrebekreftelsen eller fakturaen, skrives ut, blir den overordnede varen skrevet ut, ikke komponentvarene.

## <a name="bundles-on-sales-orders"></a>Bunter på salgsordrer

Demonstrasjonsfirmaet USMF inkluderer følgende buntoppsett. Legg merke til at alle oppsett for inntektsføring, for eksempel oppsett av inntektsplaner, er fjernet fra varene som er inkludert i dette scenarioet.

**Overordnet vare:** Bunt for bærbar datamaskin

- **Komponentvare:** Et antall på 1 av varen 1000
- **Komponentvare:** Et antall på 1 av varen S0021
- **Komponentvare:** Et antall på 1 av varen Support

Den *grunnleggende salgsprisen* for komponentvarene er en viktig del av oppsettet av komponentene. Den grunnleggende salgsprisen er definert på fanen **Selge** for en vare. Den brukes til å beregne tildelingsfaktoren når den overordnede varens enhetspris tilordnes til komponentvarene. Salgsprisene for handelsavtalen brukes aldri til dette formålet.

Følgende grunnleggende salgspriser er definert for komponentvarer:

- **1000:** USD 1 900,00
- **S0021:** USD 150,00
- **Støtte:** USD 500,00

En salgsordre angis for kunden US-004, Cave Wholesales. Den eneste linjen som angis, er for buntvaren Bærbar datamaskin. Standard enhetspris for den overordnede linjen kan tas fra en rekke steder, for eksempel handelsavtalen eller den grunnleggende salgsprisen. I dette eksemplet ble USD 2 300 angitt som enhetspris manuelt.

[![Buntvaren Bærbar datamaskin i en salgsordre](./media/bundle-01.png)](./media/bundle-01.png)

Salgsordren inneholder en bunt, og derfor må den bekreftes. Bekreftelsesdialogboksen viser komponentene i bunten.

[![Dialogboksen Bekreft salgsordre som viser komponentvarer](./media/bundle-02.png)](./media/bundle-02.png)

Den utskrevne bekreftelsesrapporten vil imidlertid vise den overordnede varen til bunten, ettersom denne rapporten er det eksterne dokumentet for kunden.

[![Bekreftelsesrapport som viser bare den overordnede varen](./media/bundle-03.png)](./media/bundle-03.png)

Etter at salgsordren er bekreftet, vises den overordnede varen fremdeles på salgsordren, men statusen er endret til **Avbrutt**. I tillegg spores nettobeløpet i feltet **Nettobeløp for bunt**. Dette beløpet kreves for å skrive ut fakturaen, fordi fakturaen viser den overordnede varen, ikke komponentvarene.

Summen av komponentvarene må være lik verdien for **Nettobeløp for bunt** for den overordnede varen, fordi denne verdien er beløpet som presenteres for kunden på den utskrevne fakturaen. For å sikre at fakturaen samsvarer med beløpene som posteres til økonomimodulen, er endringer i komponentvarer begrenset. Området og lageret kan for eksempel ikke endres, ettersom disse endringene kan utløse en prisendring basert på en handelsavtale.

Enhetsprisen fra linjen for den overordnede varen tildeles komponentene på følgende måte:

**Totale basissalgspriser fra komponenter:** USD 1 900 + USD 500 + USD 150 = USD 2 550

- **Komponent 1:** USD 2 300 × (1 900 ÷ 2 550) = USD 1 713,73
- **Komponent 2:** USD 2 300 × (500 ÷ 2 550) = USD 450,98
- **Komponent 3:** USD 2 300 × (150 ÷ 2 550) = USD 135,29

Summen av komponentene må være lik USD 2 300, og det er den (USD 1 713,73 + USD 450,98 + USD 135,29 = USD 2 300).

Hvis det kreves endringer for alle komponentvarer, kan den overordnede varen fjernes. I dette tilfellet fjernes også komponentvarer. Den overordnede varen kan deretter legges til på nytt, og de nødvendige endringene kan fullføres før salgsordren bekreftes.

[![Buntvare som inneholder endringer i komponentvarene.](./media/bundle-04.png)](./media/bundle-04.png)

Når salgsordren plukkes og pakkes, vil dokumentene bare omfatte komponentene i bunten. Følgeseddelen og fakturaen må inneholde en fullstendig bunt. Hvis ikke kan de ikke posteres. Dialogboksen viser for eksempel tre komponentvarer. Hvis du prøver å slette en av dem, får du en feilmelding som angir at alle produkter i bunten må sendes før de kan faktureres.

En bunt må sendes og faktureres som en fullstendig bunt. Hvis du for eksempel endrer antallet for vare 1 000 til 4, men du lar antallet av de andre komponentvarene være 5, kan ikke følgeseddelen og fakturaen posteres.

Et delvis beløp kan bare sendes og faktureres hvis antallet reduseres for alle komponentene i bunten. Et antall på 5 av buntvaren Bærbar datamaskin angis for eksempel på en salgsordre. Når salgsordren er bekreftet, vises de tre komponentvarene på salgsordren, og antallet for hver er 5. Som standard vil antallet settes til 5 for hver komponent under forsendelse og fakturering. Du kan imidlertid justere antallet ned til 3 for alle tre komponentvarer. I dette tilfellet blir tre fullstendige bunter sendt og fakturert. De gjenværende to buntvarene (et antall på 2 av hver av de tre komponentvarene) kan sendes og faktureres senere.

Det siste trinnet er å fakturere salgsordren. Fakturadialogboksen viser komponentvarene under fakturering.

[![Dialogboksen Faktura som viser komponentvarer](./media/bundle-06.png)](./media/bundle-06.png)

Fakturaen som er skrevet ut, vil imidlertid bare vise den overordnede varen.
 
[![Utskrevet faktura som viser bare den overordnede varen](./media/bundle-07.png)](./media/bundle-07.png)

Fakturajournalen som opprettes etter at posteringen skjer, omfatter ikke den overordnede varen fra bunten, fordi denne varen har statusen **Avbrutt**.

[![Fakturajournal som ikke omfatter den overordnede varen](./media/bundle-08.png)](./media/bundle-08.png)

Det er viktig at fakturajournalen ikke inneholder den overordnede varen fra bunten, fordi prosesser som utføres etter at fakturaen er postert, er basert på den fakturajournalen. Hvis du for eksempel oppretter en kreditnota fra fanen **Selge** i handlingsruten, vil kreditnotaen som opprettes, inkludere komponentvarene og ikke den overordnede varen.

[![Kreditnota som viser komponentvarene, men ikke den overordnede varen](./media/bundle-09.png)](./media/bundle-09.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]