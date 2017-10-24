--- 
title: "Slå opp gjeldende priser og rabatter"
description: "Denne fremgangsmåten viser hvordan du finner prisen og/eller rabatten for et produkt som for øyeblikket er gyldig for en bestemt kunde, uten å opprette en salgsordre."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f372db3d2e358cde6a5e65b01f4dc499c69fe022
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="look-up-applicable-prices-and-discounts"></a>Slå opp gjeldende priser og rabatter

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du finner prisen og/eller rabatten for et produkt som for øyeblikket er gyldig for en bestemt kunde, uten å opprette en salgsordre. Fremgangsmåten hjelper deg med et konkret eksempel, og du må følge dette eksemplet ved hjelp av USMF-demofirmaet for å velge de nødvendige verdiene.


## <a name="find-the-applicable-price"></a>Finne den aktuelle prisen
1. Gå til Salg og markedsføring > Priser og rabatter > Søk etter priser.
2. Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.
3. Finn og velg kunde US-001 i listen.
4. Klikk koblingen i den valgte raden i listen.
5. Skriv inn T0004 i feltet Varenummer.
    * Antall-feltet er som standard satt til 1. Men hvis du vet størrelsen på ordren som kunden har til hensikt å plassere for det aktuelle produktet, angir du denne verdien i stedet. Denne informasjonen er relevant hvis forretningsavtalene med kunden har antallsintervaller, det vil si at produktets pris avhenger av det minste antallet som kjøpes.  
6. Angi en dato for når kunden forventes å plassere en ordre, i feltet Dato. 
    * Datoen kan være dagens dato eller en dato i fremtiden.  
    * Systemet returnerer nå prisen som gjelder for det valgte produktet når det kjøpes av den valgte kunden på den valgte datoen med et angitt antall. Hvis kunden US-001 i dette eksemplet kjøper i dag 1 enhet av produktet T0004, vil de bli belastet CAD 350 per enhet. Denne prisen kommer fra en eksisterende og aktiv forretningsavtale med kunden.      Andre felt på siden inneholder flere detaljer om produktet pris og kostnader (hvis konfigurert på produktstandarden), og beregnet fortjeneste.  
    * Hvis alternativet Vis relaterte produktvarianter er valgt, betyr det at det finnes flere forretningsavtaler for produktets varianter.  
7. Klikk avmerkingsboksen Vis relaterte produktvarianter.
    * En liste over produktvariantene vises med informasjon om dimensjonene.  
8. I listen merker du linjen som representerer fargen hvit.
    * Legg merke til at produktprisen nå er forskjellig fra den som ble vist tidligere da den ikke ble angitt per dimensjon.  
9. Klikk Vis salgspriser.
    * Siden Pris (salg) viser alle forretningsavtalene som gjelder for produktet, inkludert variantene.  
10. Lukk siden.

## <a name="find-the-applicable-discount"></a>Finne den aktuelle rabatten
    * Kontroller at Kundekonto-feltet inneholder kundenummeret US-001    
1. Skriv inn T0012 i feltet Varenummer.
    * Kontroller at Antall-feltet er satt til 1.  
    * De følgende prissettingsdetaljene som vises for produktet T0012, kommer fra én eller flere forretningsavtaler: enhetsprisen er CAD 1 000 og rabattprosenten er 5.  
2. Sett verdien for Antall til 20.
    * Det økte ordreantallet fører til at linjerabatten som tilbys til kunden, endres fra 5 til 7 prosent.  
    * Nettobeløpet beregnes basert på enhetspris, rabatt og det totale antallet.  
3. Klikk Vis linjerabatt.
    * Det finnes to linjerabattavtaler for produktet T0012, som angir en rabatt på 5 prosent for et ordrelinjeantall fra 1 til 10 og 7 prosent rabatt for ordremengder som overstiger 10. Legg merke til at rabattene brukes i en gruppe med produkter, i dette eksemplet gruppekoden 01, som produkt T0012 er et medlem av.  
4. Lukk siden.


