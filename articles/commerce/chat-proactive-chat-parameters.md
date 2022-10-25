---
title: Proaktive chatparametre til Commerce-chatmodulet
description: Denne artikel beskriver de proaktive chatparametre for Commerce-chatmoduler i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691055"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Proaktive chatparametre til Commerce-chatmodulet

[!include [banner](includes/banner.md)]

Denne artikel beskriver de proaktive parametre for Commerce-chat med Omnikanal til Customer Service og Commerce-chat med Power Virtual Agents-chatmoduler i Microsoft Dynamics 365 Commerce.

## <a name="proactive-chat-properties"></a>Proaktive chategenskaber

De proaktive chategenskaber findes i egenskabsruden for Commerce-chat med Omnikanal til Customer Service og Commerce-chat med Power Virtual Agents-moduler i Commerce-webstedsgeneratoren.

> [!NOTE]
> Som standard er alle de proaktive chategenskaber, der vises her, tomme. Det anbefales, at du får mere at vide om disse egenskaber og kun angiver dem efter behov. Denne metode gør det lettere at reducere forkerte proaktive chatbeskeder.

### <a name="proactive-chat"></a>Proaktiv chat

| Brugervenligt navn | Beskrivende tekst | Standardværdi |
|---------------|-------------|---------------|
| Aktiveret | Proaktivt engagere kunder baseret på forskellige udløsere. | Deaktiveret |
| Chathilsen | Den hilsen, der bruges, når en proaktiv chat er blevet udløst. | Tom |

### <a name="wait-time-proactive-chat"></a>Ventetid (proaktiv chat)

| Brugervenligt navn | Beskrivende tekst |
|---------------|-------------|
| Ventetid (sek) | Den tid (i sekunder), som webstedsbrugere tilbringer på en webside, før der udløses en proaktiv chat. |
| Chathilsen | Den hilsen, der bruges, når en proaktiv chat er blevet udløst. |

### <a name="number-of-page-visits-proactive-chat"></a>Antal sidebesøg (proaktiv chat)

| Brugervenligt navn | Beskrivende tekst |
|---------------|-------------|
| Antal sidebesøg | Antallet af sidebesøg, før der udløses en proaktiv chat. Webstedsbrugere skal først acceptere prompten i banneret til cookies-accept. |
| Chathilsen | Den hilsen, der bruges, når en proaktiv chat er blevet udløst. |

### <a name="specific-pages-proactive-chat"></a>Specifikke sider (proaktiv chat)

| Brugervenligt navn | Beskrivende tekst |
|---------------|-------------|
| Side(r) | En liste over sider, der udløser en proaktiv chat, når de besøges. |
| Chathilsen | Den hilsen, der bruges, når en proaktiv chat er blevet udløst. |

### <a name="from-specific-pages-proactive-chat"></a>Fra specifikke sider (proaktiv chat)

| Brugervenligt navn | Beskrivende tekst |
|---------------|-------------|
| Side(r) | En liste over sider, der udløser en proaktiv chat, når brugere navigerer væk fra dem. |
| Chathilsen | Den hilsen, der bruges, når en proaktiv chat er blevet udløst. |

### <a name="specific-countryregion-proactive-chat"></a>Bestemt land/område (proaktiv chat)

| Brugervenligt navn | Beskrivende tekst |
|---------------|-------------|
| Landekode | Brugere, der besøger fra bestemte lande eller områder, udløser en proaktiv chat. Lande-/områdekoder skal være to store bogstaver (f.eks. **US**). |
| Chathilsen | Den hilsen, der bruges, når en proaktiv chat er blevet udløst. |

### <a name="date-range-proactive-chat"></a>Datointerval (proaktiv chat)

| Brugervenligt navn | Beskrivende tekst |
|---------------|-------------|
| Startdato (dd/mm/åååå) | Den dato, hvor eller hvorefter der udløses en proaktiv chat. |
| Slutdato (dd/mm/åååå) | Den dato, hvor eller før hvilken der udløses en proaktiv chat. |
| Chathilsen | Den hilsen, der bruges, når en proaktiv chat er blevet udløst. |

### <a name="total-amount-in-cart-proactive-chat"></a>Samlet beløb i indkøbskurv (proaktiv chat)

| Brugervenligt navn | Beskrivende tekst |
|---------------|-------------|
| Minimum | Det minimale pengebeløb (inklusive) i indkøbskurven, der udløser en proaktiv chat, når brugerne besøger indkøbskurvens side. |
| Maksimum | Det maksimale pengebeløb (inklusive) i indkøbskurven, der udløser en proaktiv chat, når brugerne besøger indkøbskurvens side. |
|Chathilsen | Den hilsen, der bruges, når en proaktiv chat er blevet udløst. |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>Det samlede antal varer i indkøbskurv (proaktiv chat)

| Brugervenligt navn | Beskrivende tekst |
|---------------|-------------|
| Minimum | Det minimale antal varer (inklusive) i indkøbskurven, der udløser en proaktiv chat, når brugerne besøger indkøbskurvens side. |
| Maksimum | Det maksimale antal varer (inklusive) i indkøbskurven, der udløser en proaktiv chat, når brugerne besøger indkøbskurvens side. |
| Chathilsen | Den hilsen, der bruges, når en proaktiv chat er blevet udløst. |

### <a name="specific-products-in-cart-proactive-chat"></a>Specifikke produkter i indkøbskurv (proaktiv chat)

| Brugervenligt navn | Beskrivende tekst |
|---------------|-------------|
| Produkt-id/SKU | En liste over produkt-ID'er/SKU-numre (lagerenhed), der udløser en proaktiv chat, når brugerne besøger indkøbsvognssiden. |
| Chathilsen | Den hilsen, der bruges, når en proaktiv chat er blevet udløst. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Commerce-chatfunktioner](commerce-chat-overview.md)

[Commerce-chat med Omnikanal til Customer Service-modulet](commerce-chat-module.md)

[Commerce-chat med Power Virtual Agents-modul](chat-module-pva.md)
