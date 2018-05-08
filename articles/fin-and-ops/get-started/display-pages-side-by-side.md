---
title: "Vise sider side ved side ved å bruke ikonet Åpne i nytt vindu"
description: Denne artikkelen beskriver hvordan du viser sider side-ved-side i Microsoft Dynamics 365 for Finance and Operations.
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4a575665a2b893745a2f2044cd97177917ee1a33
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>Vise sider side ved side ved å bruke ikonet Åpne i nytt vindu

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du viser sider side-ved-side i Microsoft Dynamics 365 for Finance and Operations.

Microsoft Dynamics 365 for Finance and Operations kan gjøre det enklere å utføre oppgaver på en effektiv måte. I noen tilfeller vil du kanskje vise flere sider side ved side for å fullføre en oppgave raskt. Du vil for eksempel kanskje validere eller registrere linjer i flere journaler. Vanligvis vil du måtte gå frem og tilbake mellom siden som viser en liste over journaler, og siden som viser linjer for en bestemt journal. Funksjonen **Åpne i nytt vindu** gjør at du kan vise disse sidene side ved side, slik at du kan gjøre oppgavene raskt. 

La oss fortsette med eksemplet ovenfor. Når du viser linjene, kan du klikke ikonet **Åpne i nytt vindu**. 

[![åpne-i-nytt-vindu-ikon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) 

Når du klikker ikonet **Åpne i nytt vindu**, åpnes linjesiden i et nytt popup-nettleservindu, og det opprinnelige nettleservinduet navigeres tilbake i historikken til siden der listen over journaler vises. Du kan dermed vise begge sidene side ved side. Når du er ferdig med å vise en journal, kan du endre den valgte journalen på journallistesiden, og dermed vises linjene i den nylig valgte journalen automatisk på linjesiden i popup-vinduet. 

[![sider-vist-side-om-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) 

Den dynamiske koblingen og oppdateringen skjer på grunn av relasjonene mellom dataene som ligger bak disse sidene. Hvis systemet ikke er klar over relasjonen mellom dataene, oppdateres ikke popup-vinduet automatisk som svar på en endring i vinduet det stammer fra. 

Noen sider har flere visninger, for eksempel Rutenettvisning, Topptekstvisning og Detaljvisning. Ikonet **Åpne i nytt vindu** fører til at hele siden åpnes i det nye nettleservinduet. Derfor kan du ikke ha to visninger av den samme siden side-ved-side ved hjelp av funksjonen **Åpne i nytt vindu**. Nesten alle slike sider har imidlertid en navigasjonsliste du kan bruke til å bytte mellom poster og få en lignende opplevelse. 

Før du bruker funksjonen **Åpne i nytt vindu**, konfigurerer du popup-blokkeringen i nettleseren slik at den tillater popup-vinduer fra URL-adressen til området for Finance and Operations. Du kan for eksempel tillate popup-vinduer fra "\*.dynamics.com". 

Funksjonen **Åpne i nytt vindu** er bare tilgjengelig når det er flere sider åpne i vinduet. I tillegg lukkes popup-vinduet automatisk når ingen flere sider er åpne (det vil si når den siste siden lukkes i dette vinduet). Finance and Operations lukker også åpne sider når du går til et annet område i programmet. Hvis du har popup-vinduer åpne og går til et annet område i programmet, lukkes derfor popup-vinduene automatisk fordi sidene i disse vinduene ble lukket av systemet. 

Den øverste linjen i popup-vinduene viser informasjon om firmaet siden ble åpnet i, og er skrivebeskyttet. Popup-vinduene er også avhengig av hovednettleservinduet for Finance and Operations. Hvis hovedvinduet lukkes eller oppdateres, blir alle åpne popup-vinduer skrivebeskyttet. Dette betyr at du kan fortsatt kan vise informasjonen i disse vinduene, men du kan ikke bruke dem.




