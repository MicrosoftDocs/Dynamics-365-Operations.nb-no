---
title: Aktiver flere henteleveringsmåter for kundeordrer
description: Denne artikkelen forklarer funksjonaliteten i Microsoft Dynamics 365 Commerce som lar deg opprette kundeordrer for henting i en butikk.
author: hhainesms
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e4d8883b3dc1c4a0e12bcb00b6441f76d73da92e
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831591"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Aktiver flere henteleveringsmåter for kundeordrer

[!include [banner](includes/banner.md)]


I Microsoft Dynamics 365 Commerce kan organisasjoner definere flere leveringsmåter som kunder eller selgere kan velge mellom når de oppretter en ordre som skal hentes i en butikk. På denne måten kan organisasjoner tilby flere hentealternativer til kundene sine. Mange forhandlere tilbyr for eksempel kunder alternativet om å hente i butikk eller hente utenfor butikk i ordrene deres. Commerce støtter konfigurering av disse forskjellige henteleveringsmåtene. Brukere kan dra nytte av dem når de oppretter kundeordrer i en hvilken som helst støtte Commerce-kanal som støttes (e-handel, kundesenter eller butikk).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Aktiver og konfigurer henteleveringsmåter

Funksjonen **Støtte for flere henteleveringsmåter** i arbeidsområdet **Funksjonsbehandling** i Commerce headquarters er gjort obligatorisk og må være aktivert i miljøet.

Hvis du tidligere har definert en henteleveringsmodus på siden **Commerce-parametere**, vises denne modusen i den gjeldende konfigurasjonen for henteleveringsmoduser.

![Henteleveringsmåter på siden Commerce-parametere.](media/multiplepickupparameter.png)

Du kan definere flere henteleveringsmåter i **Henteleveringsmåte**-rutenettet i fanen **Commerce-parametere** > **Kundeordrer** > **Leveringsmåter**-hurtigfanen.  

Feltene **Utbæringsleveringsmåte** og **Elektronisk leveringsmåte**, og alternativet **Vis bare transportøralternativer for forsendelsesordrer**, er omplassert til denne hurtigfanen.

Før du konfigurerer flere henteleveringsmåter, må du definere leveringsmåtene. På siden **Leveringsmåter** i Commerce Headquarters legger du til leveringsmåter som skal regnes som henteleveringsmåter. Kontroller at hele konfigurasjonen er fullført. Hvis du for eksempel tilbyr henting utenfor butikk som leveringsalternativ for netthandlere i noen butikker, må du opprette en ny leveringsmåte for dette formålet. Du kan opprette denne leveringsmåten ved å bruke «henting utenfor butikk» som beskrivelse. Du må deretter sørge for at leveringsmåten «henting utenfor butikk» tilordnes til alle Commerce-kanalene som tilbyr det, inkludert nettbutikker som kan tilby dette alternativet, og de individuelle butikkanalene som tilbyr denne oppfyllingsmetoden. Leveringsmåter må også knyttes til produktene. Hvis det i dette eksemplet er visse produkter som ikke kan leveres ved å bruke «henting utenfor butikk», må du sørge for at disse varene utelates. Når du er ferdig å legge til eventuelle nye leveringsmåter, kjører du jobben **Behandle leveringsmåter** for å opprette relasjonene mellom leveringsmåten, kanalene og varene. Når jobben er fullført, åpner du siden **Distribusjonsplan** i Commerce Headquarters og kjører **1120**-distribusjonsjobben for å sikre at de relevante Commerce-kanaldatabasene oppdateres med den nye leveringsmåtekonfigurasjonen.

![Eksempel på en leveringsmåtekonfigurasjon for henting utenfor butikk.](media/pickupmodes.png)

Når du har definert ekstra henteleveringsmåter, legger du dem til i rutenettet **Henteleveringsmåte** på siden **Commerce-parametere**. Deretter kjører du de aktuelle distribusjonsjobbene for å oppdatere de relevante Commerce-kanaldatabasene med konfigurasjonsendringen.

> [!NOTE]
> Bortsett fra den eksisterende henteleveringsmåten som kopieres til **Henteleveringsmåte**-rutenettet når du aktiverer funksjonen **Støtte for flere henteleveringsmåter**, bør du konfigurere nye henteleveringsmåter for hver ekstra leveringsmåtekonfigurasjon. Når du legger til leveringsmåter i **Henteleveringsmåte**-rutenettet, validerer Commerce om noen aktive åpne salgslinjer allerede bruker dem. Hvis det finnes åpne salgslinjer, får du en feilmelding. Leveringsmåter betraktes ikke som henteleveringsmåter før alle åpne salgslinjer som bruker dem, har blitt lukket (enten fakturert eller avbrutt).


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

    ![Velge et hentealternativ i e-handel.](media/pickupecommerce.png)

- Hvis en kundeordre for henting opprettes via salgsstedet i butikkanaler, blir salgstilknytningen bedt om å velge blant de tilgjengelige henteleveringsmåtene, hvis noen er konfigurert. Hvis bare én gyldig henteleveringsmåte er tilgjengelig for kanalen og varen, blir ikke salgstilknyttingen bedt om å velge den. I stedet brukes den tilgjengelige henteleveringsmåten automatisk på ordrelinjene.

    ![Velge et hentealternativ i salgsstedsappen.](media/pickuppos.png)

- Når brukere oppretter henteordrer i kundesenterkanaler, kan de manuelt velge en eventuell definert henteleveringsmåte som er koblet til kundesenterkanalen. Systemet validerer deretter at den valgte henteleveringsmåten kan brukes når varen som kobles til den, er bestilt. Når en henteleveringsmåte er valgt i kundesentermodulen, må salgsordrelinjene være koblet til et gyldig butikklager. Hvis et butikklager ikke er definert på en kundesentersalgslinje, kan ikke en henteleveringsmåte angis på denne salgslinjen.
- Selgere kan bruke operasjonen **Ordretilbakekalling** eller **Ordreoppfyllelse** i salgsstedsappen til å hente en liste over ordrer eller ordrelinjer for henting. Hvis en selger bruker et forhåndsdefinert søkefilter til å vise alle ordrer som blir hentet i den gjeldende butikk, blir spørringene endret for å sikre at søkeresultatene omfatter alle berettigede ordrer som bruker en henteleveringsmåte. Salgsstedsbrukere kan også bruke eksisterende filtre til å begrense listen med ordrer til en bestemt henteleveringsmåte. De kan for eksempel bare vise ordrer for henting utenfor butikk.

    ![Filter for henteleveringsmåter som er brukt på en liste over tilbakekallingsordrer.](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Hensyn for behandling av distribuert ordre

Funksjonene [Behandling distribuert ordre (DOM)](./dom.md) i Commerce ignorerer alle salgslinjer som er merket for henting i butikk. Disse funksjonene er oppdatert for å sikre at salgslinjer som er koblet til konfigurerte henteleveringsmåter, omgår DOM-logikken og ikke blir tilordnet på nytt til et nytt oppfyllelseslager.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
