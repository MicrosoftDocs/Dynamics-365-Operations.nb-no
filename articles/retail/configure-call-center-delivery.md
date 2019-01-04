---
title: "Konfigurere leveringsmåter og tillegg for telefonsenter"
description: "Dette emnet beskriver hvordan du setter opp leveringsmåter og tillegg for en telefonsenterordre i Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 04/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: dc2ab66bf6e3195e1ebf394f99182f59c3ee2125
ms.openlocfilehash: ebc8ee52da7d10ca18147684a0190e52a495ad5a
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---

# <a name="configure-call-center-delivery-modes-and-charges"></a>Konfigurere leveringsmåter og tillegg for telefonsenter

[!INCLUDE [banner](includes/banner.md)]

Når en salgsordre er plassert i Microsoft Dynamics 365 for Retail, og personen som la inn salgsordren, er koblet til en telefonsenterkanal, brukes logikk og regler til å validere leveringsmåten og beregne tillegg for ordren.

Når du oppretter en salgsordre, kan du velge en leveringsmåte i salgsordrehodet og salgsordrelinjene. Leveringsmåten du velger i hodet, brukes som standard for alle salgsordrelinjer. Du kan imidlertid overstyre standard leveringsmåte på individuelle salglinjer etter behov. Du kan også definere en leveringsmåte i en kundepost. Deretter, når ordrer opprettes for kunden, brukes denne leveringsmetoden som standard i salgsordrehodet.

Retail har funksjoner som lar brukere begrense leveringsmodiene som kan brukes av en kanal, leveringsmåter som kan brukes for et produkt, og leveringsmåter som gjelder for bestemte forsendelsesmål. Tillegg kan også defineres, slik at tilleggsgebyrer legges til i en kundeordre basert på leveringsmåtene som velges for salgsordren og den totale ordreverdien.

## <a name="define-delivery-modes"></a>Definer leveringsmåter

Før du angir hvilke leveringsmåter som kan brukes for telefonsenterordrer, og definere tilknyttede regler og tillegg, må du definere leveringsmåtene. Gå til **Salg og markedsføring \> Oppsett \> Distribusjon \> Leveringsmåter**. Velg **Ny** for å opprette en ny leveringsmåte. Du kan også velge en eksisterende leveringsmåte i listen og deretter velge **Rediger** for å gjøre endringer.

I **Leveringsmåte**-feltet kan du angi en hvilken som helst kombinasjon av alfanumeriske tegn basert på dine forretningsbehov. Du kan deretter bruke **Beskrivelse**-feltet for å gi ekstra kontekst. **Tilleggsgruppe**- og **Ekspeder**-feltene er valgfrie og forklares mer detaljert senere i dette emnet.

I **Detaljhandelskanaler**-hurtigkategorien legger du til en detaljhandelskanal som skal tillates å bruke leveringsmåten når salgstransaksjoner opprettes i denne kanalen.

I **Produkter**-hurtigkategorien kan du angi hvilke produkter og/eller produktkategorier leveringsmåten kan og ikke kan brukes til. Hvis et produkt ikke kan sendes med fly på grunn av farlig materiale, må du kontrollere at produktet eller produktkategori utelates fra alle leveringsmåter som involverer transport med fly.

I **Adresser**-hurtigkategorien kan du angi hvilke land eller regioner, eller stater, leveringsmåten kan og ikke kan brukes til. Ordrer som eksempelvis sendes til Hawaii eller Alaska, er ikke kvalifisert for levering på land. Derfor bør disse statene utelates fra leveringsmåter som er knyttet til en tjeneste for levering på land, men inkludert i en hvilken som helst leveringsmåte som er knyttet til en tjeneste for levering med fly.

## <a name="validate-delivery-modes-for-a-call-center-order"></a>Validere leveringsmåter for en telefonsenterordre

Når leveringsmodiene er definert, må du kjøre den satsvise jobben **Behandle leveringsmåter**. Med denne jobben blir leveringsmodiene tilgjengelige, slik at de kan brukes i salgsordreprosesser for detaljhandelskanaler. For å kjøre **Behandle leveringsmåter**-jobben, gå til **Retail \> IT for detaljhandel \> Behandle leveringsmåter**. Denne jobben skal kjøres hver gang nye leveringsmåter legges til i en detaljhandelskanal, eller det gjøres endringer i eksisterende relasjoner for leveringsmodus/-kanal.

Når du har kjørt den satsvise jobben **Behandle leveringsmåter**, kan du gå til **Retail \> Kanaler \> Telefonsentre \> Alle telefonsentre**. På **Alle telefonsentre**-siden, i handlingsruten i kategorien **Oppsett**, velg **Leveringsmåter**. **Leveringsmåter**-siden viser alle gyldige leveringsmåter for den valgte telefonsenterkanalen. Hvis du vil redigere eksisterende leveringsmåter eller legge til nye leveringsmåter, velger du **Behandle leveringsmåter**. Legg merke til at **Behandle leveringsmåter**-jobben må kjøres når det gjøres endringer.

## <a name="define-charges-for-delivery-services"></a>Definer tillegg for leveringstjenestene

Når det opprettes salgsordrer for kunder, kan det hende at et selskap vil legge til tillegg som beregnes automatisk basert på leveringsmodiene som er valgt for ordren. Disse tilleggene kan konfigureres slik at de er de samme for alle kunder og leveringsmåter. Tilleggene kan variere avhengig av kunden og/eller leveringsmodiene som er valgt for salgsordren.

Hvis du vil definere tilleggene, kan du gå til **Retail \> Kanaloppsett \> Tillegg \> Automatiske tillegg**. Velg **Ny** for å legge til nye tillegg. Du kan også velge en eksisterende oppføring, og velg deretter **Rediger**.

Tillegg kan defineres slik at de blir beregnet på nivået for ordrehodet eller ordrelinjene. Bruk **Nivå**-feltet for å velge ønsket nivå.

Tillegg kan defineres for en bestemt kunde, en kundegruppe eller alle kunder. I **Kontokode**-feltet velger du **Tabell** for å definere tillegg som gjelder bare for en bestemt kunde. Velg **Gruppe** for å definere tillegg for en bestemt kundegruppe. Velg **Alle** for å legge til tilleggene for alle kunder som foretar en salgsordre som bruker den relaterte leveringsmåten. Hvis du har valgt **Tabell** eller **Gruppe** i **Kontokode**, velger du kunden eller kundegruppen i **Kontorelasjon**-feltet.

Tillegg kan konfigureres slik at de tas i bruk for en bestemt leveringsmåte, en leveringsmodusgruppe eller alle leveringsmåter. Hvis du velger **Tabell** i **Kode for leveringsmåte**-feltet, må du velge en bestemt leveringsmåte i **Relasjon for leveringsmåte**-feltet. Hvis du velger **Gruppe**, må du velge en leveringsmodusgruppe i **Relasjon for leveringsmåte**-feltet. Leveringsmodusgrupper er definert på **Detailjhandel \> Kanaloppsett \> Tillegg \> Leveringsgebyrgruppe**. De kan deretter knyttes til én eller flere leveringsmåter på **Leveringsmåter**-siden. Hvis du velger en gruppe når du definerer tillegg, bruker alle leveringsmåter som er knyttet til den valgte leveringsgruppen, disse tilleggene. Til slutt, hvis du velger **Alle** i **Kode for leveringsmåte**-feltet, bruker alle leveringsmåter tilleggene. Derfor velger du ikke en verdi i **Relasjon for leveringsmåte**-feltet.

I **Linjer**-delen kan du definere én eller flere tillegg per valuta, etter behov. Tillegg må være koblet til en tilleggskode som definerer økonomiske posteringsreglene for tillegget. **Kategori**-feltet brukes til å definere hvordan tillegg beregnes. Hvis for eksempel kunder skal belastes en flat sats på $9.95 på en ordre som er sendt med en bestemt leveringsmåte, bruker du **Fast**-kategorien. Hvis selskapet bestemmer seg for å belaste kunder med en prosent av totalsummen for å dekke leveringstilleggene, bruk **Prosent**-kategorien. Faktisk tillegg til kundene er definert i **Gebyrverdi**-feltet.

Detaljhandelsfirmaer konfigurerer ofte fordelte tillegg. I slike tilfeller er beløpet som kunder betaler for levering, basert på ordreverdien. For å konfigurere fordelte tillegg angir du verdier i feltene **Fra beløp** og **Til beløp** i tillegg til å definere selve tillegget i **Gebyrverdi**-feltet. For eksempel for alle ordrer som har en verdi som er mindre enn $50, krever en forhandler $5.95 for frakt på land. For ordrer som har en verdi som er lik eller større enn $50, men mindre enn $100, krever en forhandleren $7.95. For ordrer som har en verdi som er lik eller større enn $100, gir forhandleren gratis frakt. Illustrasjonen nedenfor viser konfigurasjonen av disse tilleggene.

![Eksempel på fast fordelte tillegg](media/fixedtieredcharges.png)

Du kan bruke en blanding av kategorier for tillegg, avhengig av dine forretningsbehov. For eksempel for alle ordrer som har en verdi som er mindre enn $100, er det et fast tillegg på $9.95 for frakt. For ordrer som har en verdi som er lik eller større enn $100, beregnes leveringstillegg med en sats på 5 prosent av ordreverdien. Illustrasjonen nedenfor viser konfigurasjonen av disse tilleggene.

![Eksempel på blandede fordelte tillegg](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a>Bruk leveringsmåter under ordreregistrering i et telefonsenter

Når det opprettes en ny salgsordre, må det angis en verdi i **Leveringsmåte**-feltet i hurtigfanen **Levering** i salgsordrehodet. Dette feltet kan fylles ut automatisk, basert på standardverdier fra kundeposten.

Leveringsmåten som er definert i ordrehodet, kopieres automatisk til salgsordrelinjene når de opprettes. Du kan imidlertid endre leveringsmodusoppsettet for en bestemt linjevare i **Levering**-kategorien i **Linjedetaljer**-delen på siden for salgsordreregistreringen.

Hvis den valgte leveringsmåten ikke er gyldig for produktet eller leveringsadressen som er definert for bestillingen eller bestillingslinjen, får du en feilmelding. Deretter må du velge en leveringsmåte som er definert for å støtte produkt- eller adressekonfigurasjonen.

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a>Beregning av leveringstillegg under registrering av ordre

Hvis innstillingen **Aktiver ordrefullføring** er slått på for telefonsenterkanal, beregnes forsendelseskostnadene automatisk for salgsordrer når brukere velger **Fullstendig**. Følgende melding vises på toppen av **Salgsordresammendrag**-siden: "Fordelte tillegg beregnet". Tilleggene som er beregnet, legges til verdien for **Salgstotal**-feltet. På **Beløp**-hurtigfanen viser **Tillegg**-feltet det totale beløpet for alle tillegg som er beregnet for ordren og linjene. For å se en mer detaljert spesifikasjon av tilleggene velg **Ordre** på **Salgsordresammendrag**-siden, og velg deretter **Tillegg**-alternativet for å vise, legge til eller redigere tilleggene. Legg merke til at beregningen av leveringstilleggene i ordrehodet er basert på leveringsmåten som er knyttet til hodet. Leveringstillegg på linjenivå beregnes basert på leveringsmåten som er konfigurert for salgslinjen. Hvis flere leveringsmåter brukes på forskjellige linjer, kan flere tillegg brukes og legges sammen. Totalbeløpet vises deretter i **Tillegg**-feltet på **Salgsordresammendrag**-siden.

Hvis **Aktiver ordrefullføring**-innstillingen er deaktivert, må brukere aktivere beregningen av tillegg manuelt. På **Salgsordre**-siden, i handlingsruten i kategorien **Selg** i gruppen **Beregn**, velg **Fordelte tillegg**. Meldingen "Fordelte tillegg beregnet" vises. Deretter kan du velge **Tillegg**-alternativet i **Selg**-kategorien for å vise, redigere eller slette beregnede tillegg.

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a>Bruk ekspederte leveringsmåter for telefonsenterordrer

Eventuelt kan du knytte en kode for ekspeder til en hvilken som helst leveringsmåten du konfigurerer. Denne koden brukes som et prioriteringsverktøy for sortering og rapportering. Den fører ikke til at tilleggsgebyr brukes på ordren. For å sette opp ekspederingskoder går du til **Salg og markedsføring \> Oppsett \> Distribusjon \> Ekspederingskoder**.

For eksempel for ordrer som skal sendes med fly neste dag, må plukking gjøres i lageret kl. 13:00 hver dag. I dette tilfellet kan du opprette en ekspederingskode, og denne koden kan kobles til en hvilken som helst neste dag-leveringsmåte som er konfigurert i systemet. Når lageret oppretter plukkbølgen sin, kan riktig ekspederingskode i **Ekspeder**-feltet brukes som filter, slik at plukking bare utføres for ordrer som har leveringsmåter som er knyttet til koden.

I tillegg, når det angis en telefonsenterordre, kan en ekspederingskode brukes manuelt på salgsordrehodet eller en individuell salgsordrelinje. Igjen, koden kan brukes til sorterings- eller rapporteringsformål. Noen ganger må en ordre håndteres forsiktig på grunn av problemer med kundeservice. I dette tilfellet kan en bestemt ekspederingskode brukes på ordrehodet eller -linjene for å identifisere og prioritere ordren under prosessen med å utføre.

