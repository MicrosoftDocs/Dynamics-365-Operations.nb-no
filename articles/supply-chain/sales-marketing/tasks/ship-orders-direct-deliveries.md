---
title: Sende ordrer som direkte leveringer
description: Dette emnet viser hvordan du oppretter en direktelevering for en salgsordre.
author: Henrikan
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart, PurchEditLines, PurchTable, PurchTableReferences, MCRDropShipWorkbench, SalesShippingLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 94890b0915a49052c298090f124cf2b91c462de8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572447"
---
# <a name="ship-orders-as-direct-deliveries"></a>Sende ordrer som direkte leveringer

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du oppretter en direktelevering for en salgsordre. Du bruker direktelevering når du vil levere varer til kunden direkte fra leverandøren, i stedet for å levere dem først til ditt eget lager. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. For å fullføre den andre underordnede oppgaven "Opprette direkte leveringer fra arbeidsbenken" kontroller at varen du velger i salgsordren, har en standard leverandør angitt på hurtigfanen Kjøp i produktstandarden Frigitt.

## <a name="set-an-individual-order-for-direct-delivery"></a>Angi en enkelt ordre for direkte levering
1. Gå til **Navigasjonsrute > Moduler > Kunder > Ordrer > Alle salgsordrer**.
2. Velg **Ny**.
3. Angi eller velg en verdi i **Kundekonto**-feltet, og velg deretter **OK**.
4. Angi eller velg verdier i feltene **Varenummer** og **Område**, og velg deretter **Lagre**.
5. Velg deretter **Direkte levering** i **Salgsordre**-fanen i handlingsruten. Opprett levering-siden viser alle de åpne salgsordrelinjene som kopiert fra salgsordren. Du kan se gjennom ordredetaljene, og om nødvendig kan du endre detaljer som for eksempel innkjøpsantall og prisvilkår før du oppretter den direkte leveringen.  
6. Velg **Ja** i feltet **Inkluder alt**.
    - Hvis du vil generere en direkte levering for bare et delsett av salgsordrelinjene, velger du disse individuelt.  
    - **Leverandørkonto**-feltet kan eller kan ikke allerede være utfylt med et leverandørnummer. Hvis standardleverandøren er definert for produktet (på den tilknyttede varedekningen), vil denne leverandøren kopieres til linjen. Hvis ikke, må du angi en leverandør manuelt. I dette eksemplet velger vi en ny leverandør i neste trinn, selv om en allerede fylt ut.   
7. Angi eller velg en verdi i **Leverandørkonto**-feltet, og velg deretter **OK**. Meldingen forteller deg at bestillingen er nå blitt opprettet.   
8. Vis delen **Linjedetaljer**.
9. Velg fanen **Levering**, og kontroller at feltet **Direkte levering** er satt til **Ja**.
10. Klikk på **Generelt** i handlingsruten.
11. Velg **Relaterte ordrer**.
12. Velg koblingen i **Bestilling**-feltet.
13. Utvid delen **Linjedetaljer**, og velg fanen **Adresse**.
    - Leveringsadressen for denne bestillingslinjen er kundens leveringsadresse og ikke firmaets adresse.  
    - Hvis du endrer leveringsadressen på bestillingslinjen eller den opprinnelige salgsordrelinjen, oppdateres adressen på den tilsvarende ordrelinjen automatisk.  
14. Velg fanen **Levering**.
    - Som salgsordrelinjen settes også den tilknyttede bestillingslinjetypen til Direktelevering.  
    - Leveringsdato og bekreftet leveringsdato for bestillingslinjen er satt til henholdsvis ønsket leveringsdato og bekreftet leveringsdato for den opprinnelige salgsordrelinjen.   
    - Hvis du oppdaterer noen av disse datoene på bestillingslinjen eller salgslinjen, oppdateres datoene i den tilhørende ordren automatisk.     
    - Bestillingen som er angitt for å levere varene direkte til kunden, er koblet til den opprinnelige salgsordren ved hjelp av en spesiell tilknytning. Denne tilknytningen bruker regelen om at følgeseddeloppdateringen av salgsordren ikke kan utføres fra selve ordren og må utføres ved hjelp av bestillingen. Kundefakturering må imidlertid utføres fra salgsordren.  
15. Klikk på **Innkjøp** i handlingsruten.
16. Velg **Bekreftelse**.
17. Velg **OK**.
18. Klikk på **Mottak** i handlingsruten.
19. Velg **Produktkvittering**.
20. Skriv inn en verdi i feltet **Produktkvittering**.
21. Velg **OK**.
22. Klikk på **Generelt** i handlingsruten.
23. Velg **Relaterte ordrer** og uthev den ønskede posten.
    - Når bestillingen er oppdatert som mottatt, eller med andre ord, når leverandøren har sendt varene til kundens adresse, oppdateres statusen for den opprinnelige salgsordren automatisk til Levert.  
    - Salgsordren kan nå faktureres.    
24. Velg **OK**.
25. Lukk siden.
26. Velg **OK**. Lukk sidene og gå tilbake til startsiden.

## <a name="create-direct-deliveries-from-the-workbench"></a>Opprette direkte leveringer fra arbeidsbenk
1. Gå til **Navigasjon > Moduler > Kunder > Ordrer > Alle salgsordrer**.
2. Velg **Ny**.
3. Angi eller velg en verdi i **Kundekonto**-feltet, og velg deretter **OK**.
4. Angi eller velg en verdi i feltene **Varenummer** og **Område**.
5. Vis delen **Linjedetaljer**, og velg deretter fanen **Levering**. I stedet for å opprette en direkte levering som en del av salgsordrebehandlingen som i forrige prosedyre, kan du velge å overføre denne oppgaven til en innkjøpsansvarlig. Hvis du vil ta med salgsordrelinjen i håndteringsprosessen for direkte levering, må du merke linjen for direkte levering.  
6. Velg **Ja** i feltet **Direktelevering**.
    - Hvis varen er allerede definert for direkte levering som standard, vil feltet automatisk bli satt til Ja i ordrelinjeregistreringen. Du kan definere et element for direkte levering i standarden for det frigitte endelige produktet ved å angi alternativet Direktelevering til Ja og velge et standardlager for direkte levering.  
    - Fordi bestillingen ennå ikke er opprettet, settes statusen for direkte levering til Skal leveres direkte.   
7. Velg **Lagre**.
8. Lukk sider til du er tilbake på startsiden.
9. Skriv inn `Direct delivery` i søkefeltet.
    - Direktelevering-siden fungerer som en arbeidsbenk som gir innkjøpsagenten en oversikt over alle salgsordrelinjene som skal leveres direkte, og den gjør det mulig å opprette de respektive bestillingene. I tillegg kan de vise og åpne direkteleveringsordrer og de bekreftede bestillingene i fanene Bekreftelse og Levering.  
    - Etter at du har opprettet en direkte leveringsordre, flyttes den automatisk til fanen Bekreftelse. Du kan velge å bekrefte bestillingen direkte fra denne siden. Når bestillingen er bekreftet, flyttes den automatisk til fanen Levering, som kan du registrere mottaket fra.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]