---
title: Feilsøke produktinformasjon
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med produktinformasjon.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 87b04998889b86a79fd8dabde422147c5494b003
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516849"
---
# <a name="troubleshoot-product-information"></a>Feilsøke produktinformasjon

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med produktinformasjon.

## <a name="i-cant-delete-a-released-product"></a>Jeg kan ikke slette et frigitt produkt.

### <a name="issue-description"></a>Problembeskrivelse

Du kan bare slette et frigitt produkt og alle variantene av det hvis det frigitte produktet ikke har noen tilknyttede transaksjoner.

### <a name="issue-resolution"></a>Problemløsning

Følg denne fremgangsmåten for å slette et frigitt produkt eller en frigitt produktstandard.

1. Lukk alle åpne transaksjoner for varene.
1. Reduser lageret til 0 (null).
1. Utfør lagerlukking.
1. Slett alle produktvarianter for produktstandarden du vil slette.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Kan jeg endre varenummeret til et frigitt produkt?

I de fleste tilfeller kan du ikke redigere varenumre for frigitte produkter, fordi denne endringen vil føre til at data blir ødelagt. Du kan bare redigere varenummeret hvis du må reparere skadede data som ble forårsaket av en tidligere endring av navnet til primærnøkkelen for det frigitte produktet, som nevnt i listen over [fjernede eller avskrevne funksjoner for Finance and Operations 10.0.0 med Platform Update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).

Hvis du vil ha muligheten til å redigere varenumre for frigitte produkter, må du [stemme på dette forslaget i Ideer-portalen](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>Standard trekkprinsipp fra produktet blir ikke angitt i stykklistelinjen.

### <a name="issue-description"></a>Problembeskrivelse

Når du legger til en vare i en stykklistelinje, bruker ikke systemet standardinformasjonen for trekkprinsippet som er definert for varen. Med andre ord vises ikke trekkprinsippet fra varen på siden **Stykklistelinje**.

### <a name="issue-resolution"></a>Problemløsning

Hvis du angir et trekkprinsipp på en stykklistelinje, vil dette gjelde for denne stykklistelinjen. Hvis trekkprinsippet for eksempel er tomt, eller hvis det ikke er angitt på en stykklistelinje, vil trekkprinsippet som er angitt på varen, fortsatt gjelde for denne stykklistelinjen, selv om det ikke vises på stykklistelinjen.

Standardlogikken for andre funksjoner i Microsoft Dynamics 365 Supply Chain Management fungerer vanligvis ikke på denne måten. Gjeldende virkemåte kan imidlertid ikke endres. Hvis ikke kan noen eksisterende tilpasninger som er avhengige av det, bli ødelagt.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Systemet lar meg lagre duplikatstrekkoder for ulike varer eller for samme vare som har forskjellige dimensjoner.

Systemet håndhever for øyeblikket ikke unike strekkoder, og tillegget av denne begrensningen vil være en oppdelingsendring. Microsoft har faktisk bevis på at noen eksisterende kundeinstallasjoner vil bli ødelagt av denne endringen. Vi vil imidlertid vurdere en større endring i utformingen for å aktivere denne funksjonen i fremtiden.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>Jeg får følgende feilmelding når jeg redigerer maler for vareposter: Lagerlokasjonen kan ikke opprettes fordi varen ikke er lagerført. For lagerførte varer må Lagerført produkt-alternativet i den tilknyttede varemodellgruppen velges.

### <a name="issue-description"></a>Problembeskrivelse

Dette problemet oppstår hvis du følger denne fremgangsmåte for å forsøke å opprette en mal for en vare som ikke er lagerført.

1. Åpne et frigitt produkt som ikke er lagerført.
1. Velg **Portinformasjon** i fanen **Alternativer** i handlingsruten.
1. Velg **Firmakontomal** i dialogboksen **Postinformasjon**.

I dette tilfellet får du følgende feilmelding:

> Lagerlokasjonen kan ikke opprettes fordi varen ikke er lagerført. For lagerførte varer må Lagerført produkt-alternativet i den tilknyttede varemodellgruppen velges.

### <a name="issue-resolution"></a>Problemløsning

Prosessen med å opprette produktmaler krever ekstra, produktspesifikk logikk. Derfor kan du ikke bruke den generelle knappen **Firmakontomal** til dette formålet. Følg i stedet denne fremgangsmåten.

1. Åpne et frigitt produkt.
1. I handlingsruten, i **Produkt**-fanen og **Ny**-gruppen velger du **Mal \> Opprett delt mal**.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Standard hjelpetekst som legges til i produktattributter, er ikke angitt i et frigitt produkt.

En beskrivelse og hjelpetekst som legges til i produktattributtene, vises ikke eller angis ikke som standard i de frigitte produktene. Denne virkemåten er standard.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>Standardantallet som er angitt, er forskjellig når det er registrert fra en stykkliste, og når det er registrert fra en stykklisteversjon.

### <a name="issue-description"></a>Problembeskrivelse

Når du legger til en vare i en stykkliste, settes antallet som standard til 1 i stedet for antallet som er definert i **Minimumsordre**-feltet på siden **Standard ordreinnstillinger** for et valgt produkt. Når du imidlertid legger til en vare fra en stykklisteversjon, og varen og varianten velges, tar antallet som er angitt som standard, hensyn til minimumsantallet som er angitt i standard ordreinnstillinger for de bestemte dimensjonene.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er forventet. Men det at logikken er forskjellig i stykklisten og stykklisteversjonen, er et kjent problem. Denne virkemåten vil likevel ikke bli endret fordi en endring kan påvirke mange forskjellige kundescenarioer.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>I detaljene for det frigitte produktet kan jeg ikke endre de vedlagte bildene som ble lastet opp fra dataenheten for produktdokumentvedlegg.

### <a name="issue-description"></a>Problembeskrivelse

Dette problemet kan oppstå når du knytter et bilde til en vare ved hjelp av dataenheten for *produktdokumentvedlegg* . I dette tilfellet vises varebildet for varen. Hvis du imidlertid velger **Endre bilde**, vises ingenting i listen over opplastede bilder. Det vises heller ingen vedlegg for varen.

### <a name="issue-resolution"></a>Problemløsning

Enheten *EcoResProductDocumentAttachmentEntity* (*produktdokumentvedlegg*) importerer dokumentvedlegg for *produkter*, men ikke for *frigitte produkter*. (Frigitte produkter er også kjent som *varer*). Hvis du vil vise vedleggene for en vare på siden **Detaljer om frigitt produkt**, må du bruke enheten *EcoResReleasedProductDocumentAttachmentEntity* (*dokumentvedlegg for frigitt produkt*) i stedet.

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Microsoft Flow-koblingen viser følgende feilmelding: Oppdatering ikke tillatt for feltet ProductNumber.

### <a name="issue-description"></a>Problembeskrivelse

Dette problemet oppstår hvis du prøver å oppdatere **Produktnummer**-feltet ved hjelp av enheten *Frigitte produkter* V2 og Microsoft Flow.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er forventet. Muligheten til å redigere produktnummeret for et frigitt produkt ble fjernet i Dynamics 365 Finance and Operations 10.0.0 med Platform Update 24 for å bidra til å hindre ødelagte data. I uvanlige tilfeller der du må reparere skadede data som var forårsaket av en tidligere endring av navnet til primærnøkkelen for et frigitt produkt, kan du be Microsoft Kundestøtte om å fjerne denne begrensningen midlertidig.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Jeg kan ikke opprette en frigitt produktvariant i en annen juridisk enhet.

### <a name="issue-description"></a>Problembeskrivelse

Hvis du prøver å frigi en produktstandard uten varianter, og deretter oppretter variantene i hver juridiske enhet (firma) etter behov, kan du ikke frigi variantene ved hjelp av variantforslag. Du vil heller ikke kunne opprette variantene manuelt.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er standard. Relasjonene mellom en produktstandard og dimensjonene som standarden kan ta, beholdes på et delt nivå. Derfor kan du ikke opprette tilgjengelige dimensjoner for en delt produktstandard i den bestemte juridiske enheten der disse dimensjonene er frigitt, og deretter replikere prosessen i hver juridiske enhet der dimensjonene er påkrevd. I stedet må du endre frigivelsesprosessen for å tilpasse til den utformede prosessen.

Her er prosessen for frigivelse av produkter.

1. Opprett den delte produktstandarden og dimensjonene som kan frigis til de juridiske enhetene.
1. Frigi produktene til de juridiske enhetene enten ved å bruke variantforslag, eller ved å legge til kombinasjonene som skal frigis, manuelt.

Du kan også opprette det frigitte produktet direkte.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>Når jeg frigir en variant i et annet firma, får jeg følgende feilmelding: Produktvariant med angitte dimensjoner er allerede opprettet.

### <a name="issue-description"></a>Problembeskrivelse

Hvis en produktvariant allerede er frigitt i et firma A, og du prøver å frigi den i firma B ved hjelp av **Ny**-knappen på siden **Frigitte produktvarianter**, vil du få følgende feilmelding:

> Produktvariant med angitte dimensjoner er allerede opprettet.

### <a name="issue-resolution"></a>Problemløsning

**Ny**-knappen på siden **Frigitte produktvarianter** oppretter varianten og frigir den i firmakonteksten. Hvis varianten allerede er opprettet, kan du ikke bruke **Ny**-knappen til å frigi den i et annet firma.

Du kan løse problemet ved å åpne siden **Produktstandard** og velge **Frigi produkt** for å frigi den eksisterende varianten i ønsket firma.
