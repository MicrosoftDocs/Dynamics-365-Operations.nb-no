--- 
title: "Definere validering av leverandørfakturakontroll"
description: Denne registreringen bruker demonstrasjonsfirmaet USMF.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9bf83269c34133509734691fd018ee703c40626
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Definere validering av leverandørfakturakontroll

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne registreringen bruker demonstrasjonsfirmaet USMF. Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene. Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt. Hvis den juridiske enheten sporer utgifter, for eksempel frakt, ved hjelp av tillegg, må du kontrollere at konfigurasjonsnøkkelen for Tillegg er valgt.  Fakturasamsvar for leverandører er prosessen med å sjekke samsvar mellom leverandørfakturaen, bestillingen og produktkvitteringsinformasjonen. Forskjeller mellom disse dokumentene kalles samsvarende avvik. Samsvarende avvik blir sammenlignet med toleransen som er angitt. Hvis et samsvarende avvik er større enn toleranseprosenten eller -beløpet, vises ikoner for samsvarsavvik i skjemaet Leverandørfaktura og i skjemaet Fakturakontrolldetaljer.

1. Gå til Leverandører > Oppsett > Leverandørparametere.
2. Klikk kategorien Fakturavalidering.
3. Merk av eller fjern merket for Aktiver validering av fakturakontroll.
    * Velg om godkjenning skal kreves før en faktura som inneholder avvik for fakturakontroll, kan posteres. Hvis dette er satt til Tillat med advarsel, vises visuell indikasjon når et avvik for fakturasamsvar overskrider toleransen. Du vil imidlertid kunne postere fakturaen. Hvis du vil bruke arbeidsflyter sammen med validering av fakturakontroll, må du sørge for at feltet Poster faktura med avvik er satt til Tillat med advarsel for å unngå å godkjenne flere ganger.  
    * I feltet Oppdater status for fakturahodekontroll automatisk velger du om samsvar vil bli utført automatisk under registrering av data i systemet. Den anbefalte innstillingen er Ja, med mindre du opplever ytelsesproblemer med dataregistrering. Deaktivering av automatiske oppdateringer kan gi raskere systemytelse fordi validering av fakturakontroll vil hoppes over under dataregistrering. Dataregistrereren må manuelt oppdatere fakturaens samsvarsstatus for å se valideringsresultater av fakturakontroll når det er satt til Nei.  
4. Aktiver/deaktiver utvidelsen av delen Samsvar av fakturatotaler.
5. Merk av eller fjern merket for Samsvar fakturatotaler for å samsvare faktiske fakturatotaler med forventede summer.
    * Velg om et ikon skal vises hvis et avvik for fakturakontroll overskrider toleransen. Du kan velge å vise ikonet når et positivt avvik overskrider toleransen, eller når enten et positivt eller et negativt avvik overskrider toleransen.  
    * Toleransen er for eksempel 5 prosent, og det totale fakturabeløpet, basert på bestillingen, er 100,00. Derfor vises et ikon for prissamsvar hvis det totale fakturabeløpet overskrider 105,00. Hvis du velger Hvis større eller mindre enn toleransen, vises også et ikon hvis fakturabeløpet er mindre enn 95,00.  
6. Angi et tall i feltet Toleranseprosent for fakturatotaler.
7. Aktiver/deaktiver utvidelsen av delen Pris- og antallssamsvar.
    * I feltet Linjekontrollpolicy velger du en verdi som skal brukes som standardpolicy for den juridiske enheten du arbeider med. "Ikke nødvendig" betyr at det ikke kreves noen kontroll av individuelle fakturalinjepriser til bestillingspris eller fakturaantall til antallet på følgeseddelen. "Toveis samsvar" betyr at det kreves bekreftelse av fakturalinjer, men bare bestillingen og leverandørens fakturadokumenter er involvert i kontrollen. Produktkvitteringen tas ikke med i de samsvarende valideringene. "Treveis samsvar" betyr at fakturaens nettoenhetspris skal sammenlignes med bestillingens nettoenhetspris, og antallet produktkvitteringer skal sammenlignes med fakturaantallet.  
    * Hvis du bruker en linjekontrollpolicy med toveis eller treveis samsvar, kan du definere pristoleranseprosenter for juridisk enhet, varer og leverandører på siden for pristoleranse for vare. Når leverandørfakturaer blir sammenlignet med informasjonen i bestillinger, søkes det etter den aktuelle pristoleranseprosenten.  
8. Velg et alternativ i feltet Linjekontrollpolicy.
    * Hvis du vil gjøre det mulig å bruke et annet samsvarsnivå for en vare, leverandør, leverandør og varekombinasjonen eller bestillingslinje, velger du en verdi i feltet Tillat overstyring av kontrollpolicy. Linjekontrollpolicyen for juridisk enhet kan overstyres for en bestemt leverandør, vare eller kombinasjon av leverandør og vare på Kontrollpolicy-siden.  
    * Hvis du vil samsvare pristotaler for linjeelementer på fakturaer, velger du en verdi i feltet Tilpass samlet pris. Denne typen samsvar er nyttig når leverandøren sender flere fakturaer for samme bestillingslinje. Du kan sammenligne prisinformasjon for nettobeløpet for hver linje på fakturaen, og alle ventende og tidligere posterte fakturalinjer, med nettobeløpet for den tilhørende bestillingslinjen.  
9. Velg et alternativ i feltet Tilpass samlet pris.
10. Angi et tall i feltet Toleranse for total innkjøpspris.
11. Aktiver/deaktiver utvidelsen av delen Samsvar av tillegg.
12. Når du skal samsvare faktiske tillegg med forventede tillegg, basert på opplysningene i bestillingen, merker du av for Samsvar tillegg.
13. Lukk siden.


