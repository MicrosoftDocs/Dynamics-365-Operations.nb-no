---
title: Feilsøk stykkproduksjon
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med stykkproduksjon.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b9c43d59e8022a365853f4b9cbb32ac3c3074e3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810924"
---
# <a name="troubleshoot-discrete-manufacturing"></a>Feilsøk stykkproduksjon

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med stykkproduksjon.

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>Jeg får følgende feilmelding: Lagerstyringsprosesser brukes for øyeblikket. Hvis arbeidslinjer ennå ikke er registrert, kan du avbryte opprettet arbeid og eventuelle last- eller forsendelseslinjer, og deretter fortsette med plukkingen eller forsendelsen.

### <a name="issue-description"></a>Problembeskrivelse

Dette problemet oppstår hvis du prøver å reservere eller frigi arbeid for en linje, men lagertransaksjonen har statusen *Plukket*, som indikerer at materialet er plukket.

### <a name="issue-resolution"></a>Problemløsning

Følg en av fremgangsmåtene nedenfor for å løse problemet.

- Endre statusen for produksjonsordren tilbake til *Estimert* eller *Frigitt*.
- Åpne siden med detaljer for den relevante produksjonsordren. I handlingsruten i **Lager**-fanen i **Stopp**-gruppen velger du **Stopp og legg tilbake** for å oppheve plukking av alle plukkede transaksjoner. Velg deretter **Fjern stopp** for å behandle produksjonsordren.

Her er en forklaring på funksjonene *Legg tilbake* og *Stopp*:

- **Legg tilbake** – Denne funksjonen tilbakefører statusen for lagertransaksjoner for stykklistelinjer og formellinjer som har statusen *Plukket* via *I ordre*. Når arbeid for plukking av råvarer er fullført, settes statusen for linjene til *Plukket*. Denne statusen hindrer at produksjonsordren tilbakestilles til statusen *Opprettet*. I dette tilfellet kan du bruke *Legg tilbake*-funksjonen til å tilbakeføre transaksjonene fra statusen *Plukket*, og deretter tilbakestille produksjonsordren til statusen *Opprettet*.
- **Stopp** – Denne funksjonen angir et **Stoppet**-flagg på produksjonsordren for å hindre statusoppdateringer på ordren. Du finner **Stoppet**-flagget i hurtigfanen **Lager** på siden for produksjonsordredetaljer.

> [!NOTE]
>
> - Knappene vises bare når produksjonsordren opprettes for varer som er aktivert for lagerprosesser.
> - **Stopp**-gruppen vises bare i fanen **Lager** i handlingsruten på siden for detaljer om produksjonsordre. Den vises ikke i hurtigfanen **Lager** på listesiden **Produksjonsordrer**.

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>Det samsvarende ressursnavnet oppdateres ikke etter at jeg har endret et arbeidernavn i den globale adresseboken.

### <a name="issue-description"></a>Problembeskrivelse

Hvis du endrer et arbeidernavn i den globale adresseboken, oppdateres ikke samsvarende ressursnavn i ressursgruppemalen.

### <a name="issue-resolution"></a>Problemløsning

Dette scenarioet støttes for øyeblikket ikke. Hvis du vil løse problemet, må du oppdatere ressursnavnet manuelt.

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>Når jeg oppretter en ny produksjonsordre, får jeg ikke følgende melding: Vil du sette inn den aktive versjonen av stykkliste og rute?

### <a name="issue-description"></a>Problembeskrivelse

Når du oppretter en ny produksjonsordre etter at du har angitt varenummeret, settes feltene **Område** og **Lager** automatisk til standardområdet og -lageret som er definert på siden **Standard ordreinnstillinger** for ferdigvarer. I tillegg angis det aktive stykklistenummeret og rutenummeret automatisk. Du får ikke følgende melding som ber deg om disse verdiene:

> Vil du sette inn aktiv versjon for stykkliste og rute?

### <a name="issue-resolution"></a>Problemløsning

Du blir ikke bedt om å sette inn stykkliste- og rutenumre hvis du velger et produkt som et område eller et lager er definert for, på siden **Standard ordreinnstillinger**. Du vil bare bli spurt hvis disse verdiene ikke er definert for det valgte produktet.

## <a name="production-orders-arent-shown-on-the-marking-page"></a>Produksjonsordrer vises ikke på Merking-siden.

### <a name="issue-description"></a>Problembeskrivelse

Noen produksjonsordrer vises ikke på **Merking**-siden.

### <a name="issue-resolution"></a>Problemløsning

Produkter med følgende konfigurasjon er ikke tilgjengelige for merking. De vises derfor ikke på **Merking**-siden:

- Produktene defineres som produkter av typen *faktisk vekt*.
- De er aktivert for de avanserte lagerprosessene.
- De er konfigurert til å bli kontrollert av *Standardkostnad*-prinsippet.

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>Når jeg prøver å avslutte en produksjonsordre, får jeg følgende feilmelding: Beregnede consumptionCost-verdien for stykkliste må være negativ ved utstedelse fra lager.

Dette problemet ble løst i utgivelse 10.0.15.

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>Når statusen for en produksjonsordre endres fra Ferdigmeldt til Slutt, får jeg følgende feilmeldinger: Oppdateringskonflikt. Standardkostnaden samsvarer ikke med den økonomiske lagerverdien etter oppdateringen. og Det har oppstått en kritisk feil i funksjonen InventCostMovement.checkVariance.

Dette problemet oppstår fordi de underliggende dataene ble endret av en annen prosess. Prosessen vil prøve å oppdatere dataene opptil fem ganger. Hvis konflikten fremdeles finnes etter fem forsøk, får du følgende feilmeldinger:

> Oppdateringskonflikt. Standardkostnaden samsvarer ikke med den økonomiske lagerverdien etter oppdateringen.

> Det har oppstått en kritisk feil i funksjonen InventCostMovement.checkVariance.

Denne virkemåten er standard. Du kan redusere problemet ved å gjenoppta den satsvise jobben. Den skal slutte å kjøre.

Hvis den satsvise jobben ikke fungerer etter at du har gjenopptatt den, må du kontrollere at avrundingspresisjonen for finansstandardvalutaen er kompatibel med avrundingen som brukes på verdier i InventSum-tabellen. Hvis avrundingspresisjonen er endret til en ikke-kompatibel verdi, må du sannsynligvis endre den tilbake til en kompatibel verdi. Se etter **ModifiedDateTime**. I dette tilfellet vil verdien vanligvis vise at avrundingspresisjonen nylig ble endret.

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>Når jeg frigir til et lager, får jeg følgende feilmelding: Vare RM kan ikke reserveres fullt. Kontroller at hele antallet er tilgjengelig, eller reserver varene manuelt hvis Reservasjon-feltet på stykklistelinjen er angitt til Manuell eller Startet. Kan ikke frigi ordren til lager fordi noen materialer ikke kan reserveres. Statusen oppdateres imidlertid til Frigitt.

### <a name="issue-description"></a>Problembeskrivelse

Hvis ikke alle stykklistelinjevarer er fysisk tilgjengelige når en produksjonsordre frigis, og **Frigi til lager**-policy er satt til *Krever full reservasjon* på produksjonsordren, vil du få følgende feilmelding:

> Varen RM kan ikke reserveres fullt ut. Kontroller at hele antallet er tilgjengelig, eller reserver varene manuelt hvis Reservasjon-feltet på stykklistelinjen er angitt til Manuell eller Startet. Kan ikke frigi ordren til lager fordi noen materialer ikke kan reserveres.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er standard og fungerer som forventet.

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>Når jeg prøver å avslutte en produksjonsordre og ferdigmelde, får jeg følgende feilmelding: Samlet korrekt antall som ferdigmeldes for produksjonen, vil være %1. På siste operasjon er det i alt tilbakemeldt 0,00.

### <a name="issue-description"></a>Problembeskrivelse

Når du prøver å postere en rapport som ferdigmeldingsjournal på en produksjonsordre, får du følgende feilmelding:

> Totalt antall korrekte som ferdigmeldes for produksjonen, blir %1. På siste operasjon er det i alt tilbakemeldt 0,00.

### <a name="possible-cause"></a>Mulig årsak

Dette problemet oppstår hvis antallet som ble postert i de siste operasjonene, var feil. Hvis for eksempel produksjonen startes, men antallet som må startes, ikke er tilordnet, posteres rutekortjournalen uten linjer. Hvis du vil bekrefte situasjonen, åpner du produksjonsordren, og deretter velger du **Rutekort** i handlingsruten i fanen **Vis**.

### <a name="workaround"></a>Løsning

Du kan løse dette problemet ved å postere flere journaler for operasjonene som journalene ikke var riktig postert for. Start produksjonsordren på nytt, og velg om du vil postere tilleggsjournalene. Denne handlingen vil ikke starte produksjonsordren, men den vil postere journalene. Deretter skal rutekortet vise antallet som ble postert, og du skal kunne avslutte produksjonsordrene.

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>Kan jeg ferdigmelde en produksjonsordre mens jeg rapporterer antall feil, men ikke mens jeg rapporterer tiden eller materialantallet?

Du kan ikke rapportere antallet feil i en produksjonsordre med mindre du også rapporterer det korrekte antallet. Dette scenarioet støttes **ikke**. Ferdigmeldingsoppdateringen vil til slutt mislykkes når du prøver å avslutte produksjonsordren, og du får følgende feilmelding:

> Manglende ferdigmeldt antall.

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>Kan jeg spore serienumrene på ferdigvarer mot serienumrene for forbrukte varer?

Du kan ikke spore serienumre for ferdigvarer mot de serienumrene til et materiale som en produksjonsordre forbruker for å lage disse ferdigvarene. Dette scenarioet støttes for øyeblikket ikke. Løsningen er å opprette produksjonsordrer for et antall på 1.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]