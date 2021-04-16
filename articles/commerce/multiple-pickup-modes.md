---
title: Aktiver flere henteleveringsmåter for kundeordrer
description: Dette emnet forklarer funksjonaliteten i Microsoft Dynamics 365 Commerce som lar deg opprette kundeordrer for henting i en butikk.
author: hhainesms
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: c32ffc8435c05c644bf836bb184400d067269208
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796888"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Aktiver flere henteleveringsmåter for kundeordrer

[!include [banner](includes/banner.md)]


I Microsoft Dynamics 365 Commerce, versjon 10.0.16 og nyere kan organisasjoner definere flere leveringsmåter som kunder eller selgere kan velge mellom når de oppretter en ordre som skal hentes i en butikk. På denne måten kan organisasjoner tilby flere hentealternativer til kundene sine. Mange forhandlere tilbyr for eksempel kunder alternativet om å hente i butikk eller hente utenfor butikk i ordrene deres. Commerce støtter konfigurering av disse forskjellige henteleveringsmåtene. Brukere kan dra nytte av dem når de oppretter kundeordrer i en hvilken som helst støtte Commerce-kanal som støttes (e-handel, kundesenter eller butikk).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Aktiver og konfigurer henteleveringsmåter

Hvis du vil bruke denne funksjonaliteten, aktiverer du funksjonen **Støtte for flere henteleveringsmåter** i arbeidsområdet **Funksjonsbehandling** i Commerce Headquarters. Når du har aktivert funksjonen, kreves ytterligere konfigurasjon.

I Commerce, versjon 10.0.15 og tidligere kan organisasjoner bare definere én leveringsmåte som den utpekte henteleveringsmåten. Denne definisjonen gjøres på siden **Commerce-parametere**. Når du aktiverer funksjonen **Støtte for flere henteleveringsmåter** i versjon 10.0.16 og nyere, kopieres leveringsmåten som tidligere ble definert som henteleveringsmåten på siden **Commerce-parametere**, automatisk til den nye konfigurasjonen for henteleveringsmåter.

![Henteleveringsmåter på siden Commerce-parametere](media/multiplepickupparameter.png)

Når du har aktivert funksjonen **Støtte for flere henteleveringsmåter**, kan du definere flere leveringsmåter i rutenettet **Henteleveringsmåte** i hurtigfanen **Leveringsmåter** i fanen **Kundeordrer** på siden **Commerce-parametere**.

Feltene **Utbæringsleveringsmåte** og **Elektronisk leveringsmåte**, og alternativet **Vis bare transportøralternativer for forsendelsesordrer**, er omplassert til denne hurtigfanen.

Før du konfigurerer flere henteleveringsmåter, må du definere leveringsmåtene. På siden **Leveringsmåter** i Commerce Headquarters legger du til leveringsmåter som skal regnes som henteleveringsmåter. Kontroller at hele konfigurasjonen er fullført. Kontroller for eksempel at leveringsmåten er koblet til riktige kanaler og varer. Når du er ferdig, kjører du jobben **Behandle leveringsmåter** for å opprette relasjonene mellom leveringsmåten, kanalene og varene. Når jobben er ferdig, åpner du siden **Distribusjonsplan** i Commerce Headquarters og kjører **1120**-distribusjonsjobben for å sikre at de relevante Commerce-kanaldatabasene oppdateres med den nye leveringsmåtekonfigurasjonen.

![Eksempel på en leveringsmåtekonfigurasjon for henting utenfor butikk](media/pickupmodes.png)

Når du har definert ekstra henteleveringsmåter, legger du dem til i rutenettet **Henteleveringsmåte** på siden **Commerce-parametere**. Deretter kjører du de aktuelle distribusjonsjobbene for å oppdatere de relevante Commerce-kanaldatabasene med konfigurasjonsendringen.

> [!NOTE]
> Bortsett fra den eksisterende henteleveringsmåten som kopieres til **Henteleveringsmåte**-rutenettet når du aktiverer funksjonen **Støtte for flere henteleveringsmåter**, bør du konfigurere nye henteleveringsmåter for hver ekstra leveringsmåtekonfigurasjon. Når du legger til leveringsmåter i **Henteleveringsmåte**-rutenettet, validerer Commerce om noen aktive åpne salgslinjer allerede bruker dem. Hvis det finnes åpne salgslinjer, får du en feilmelding. Leveringsmåter betraktes ikke som henteleveringsmåter før alle åpne salgslinjer som bruker dem, har blitt lukket (enten fakturert eller avbrutt).

> [!IMPORTANT]
> Når du har definert mer enn én henteleveringsmåte på siden **Commerce-parametere**, blir funksjonen **Støtte for flere henteleveringsmåter** obligatorisk og kan ikke lenger være deaktivert. Hvis du må deaktivere denne funksjonen, fjerner du alle henteleveringsmåtene unntatt én fra **Henteleveringsmåte**-rutenettet. Når bare én henteleveringsmåte er definert, blir ikke funksjonen lenger ansett som obligatorisk, og den kan deaktiveres.

### <a name="e-commerce-site-configurations"></a>E-handelsområdekonfigurasjoner

Når funksjonen **Støtte for flere henteleveringsmåter** er aktivert, viser følgende moduler på e-handelssider de nye henteleveringsmåtene som konfigurert:

- Kjøpsboks
- Butikkvelger
- Handlekurv
- Plukkinformasjon
- Ordrebekreftelse
- Ordredetaljer

Det kreves ingen flere trinn på e-handelssider for å gjøre henteleveringsmåtene tilgjengelige.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Arbeide med flere henteleveringsmåter

Når flere henteleveringsmåter er tilgjengelige for en kanal, gis det en bedre opplevelse til kunder når de kjøper produkter som blir hentet. 

- I e-handelskanaler kan kunder velge en hvilken som helst gyldig henteleveringsmåte som er tilgjengelig. En forhandler definerer for eksempel to henteleveringsmåter (henting i butikk og henting utenfor butikk), begge konfigureres i **Henteleveringsmåte**-rutenettet, og begge er gyldige for ordreoppfyllelseskanalen og produktet som en kunde for øyeblikket kjøper. I dette tilfellet kan kunden velge foretrukket henteleveringsmåte. Den valgte henteleveringsmåten blir da den leveringsmåten som er knyttet til salgsordrelinjen når ordren opprettes i Commerce Headquarters.

    ![Velge et hentealternativ i e-handel](media/pickupecommerce.png)

- Hvis en kundeordre for henting opprettes via salgsstedet i butikkanaler, blir salgstilknytningen bedt om å velge blant de tilgjengelige henteleveringsmåtene, hvis noen er konfigurert. Hvis bare én gyldig henteleveringsmåte er tilgjengelig for kanalen og varen, blir ikke salgstilknyttingen bedt om å velge den. I stedet brukes den tilgjengelige henteleveringsmåten automatisk på ordrelinjene.

    ![Velge et hentealternativ i salgsstedsappen](media/pickuppos.png)

- Når brukere oppretter henteordrer i kundesenterkanaler, kan de manuelt velge en eventuell definert henteleveringsmåte som er koblet til kundesenterkanalen. Systemet validerer deretter at den valgte henteleveringsmåten kan brukes når varen som kobles til den, er bestilt. Når en henteleveringsmåte er valgt i kundesentermodulen, må salgsordrelinjene være koblet til et gyldig butikklager. Hvis et butikklager ikke er definert på en kundesentersalgslinje, kan ikke en henteleveringsmåte angis på denne salgslinjen.
- Selgere kan bruke operasjonen **Ordretilbakekalling** eller **Ordreoppfyllelse** i salgsstedsappen til å hente en liste over ordrer eller ordrelinjer for henting. Hvis en selger bruker et forhåndsdefinert søkefilter til å vise alle ordrer som blir hentet i den gjeldende butikk, blir spørringene endret for å sikre at søkeresultatene omfatter alle berettigede ordrer som bruker en henteleveringsmåte. Salgsstedsbrukere kan også bruke eksisterende filtre til å begrense listen med ordrer til en bestemt henteleveringsmåte. De kan for eksempel bare vise ordrer for henting utenfor butikk.

    ![Filter for henteleveringsmåter som er brukt på en liste over tilbakekallingsordrer](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Hensyn for behandling av distribuert ordre

Funksjonene [Behandling distribuert ordre (DOM)](https://docs.microsoft.com/dynamics365/commerce/dom) i Commerce ignorerer alle salgslinjer som er merket for henting i butikk. Disse funksjonene er oppdatert for å sikre at salgslinjer som er koblet til konfigurerte henteleveringsmåter, omgår DOM-logikken og ikke blir tilordnet på nytt til et nytt oppfyllelseslager.


[!INCLUDE[footer-include](../includes/footer-banner.md)]