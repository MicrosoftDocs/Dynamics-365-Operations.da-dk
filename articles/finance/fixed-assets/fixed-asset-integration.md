---
title: Integration af anlægsaktiver
description: Anlægsaktiver kan integreres med Finans, Lagerstyring, Debitor, Kreditor og Debitor. Du kan også oprette anlægsaktiver, der kan integreres med indkøbsordrer.
author: ShylaThompson
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e6be2aeb263c339f4e733b98ea4e01194973a9f
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189778"
---
# <a name="fixed-assets-integration"></a>Integration af anlægsaktiver

[!include [banner](../includes/banner.md)]

Anlægsaktiver kan integreres med Finans, Lagerstyring, Debitor, Kreditor og Debitor. Du kan også oprette anlægsaktiver, der kan integreres med indkøbsordrer.

## <a name="general-ledger"></a>Finans

I Finans opsummeres værdien af alle anlægsaktiver normalt på flere hovedkonti, der skal bruges ved regnskabsaflæggelse. Du kan imidlertid oprette mange poster til anlægsaktivet på siden **Anlægsaktiver**. Disse poster kan indeholde oplysninger, f.eks. anskaffelsespris, afskrivning og værdiansættelse. Hver gang du bogfører en posteringer for et anlægsaktiv, opdateres de relevante hovedkonti. Anlægsaktivernes hovedkonti viser altid den opdaterede værdi af anlægsaktiverne.

Du definerer de hovedkonti, som posteringer i bogen for anlægsaktiver bogføres til, på siden **Posteringsprofiler for anlægsaktiver**. Du kan også angive typer af anlægsaktivposter, der bogføres på hver hovedkonto. Du kan oprette forskellige kombinationer af hovedkonti for anlægsaktiver, afhængigt af den ønskede detaljeringsgrad for anlægsaktiverne i finansmodulet. Hovedkontiene kan baseres på posteringstyper, bøger og andre hovedkonti.

## <a name="inventory-management"></a>Lagerstyring
Du kan angive anskaffelsen af anlægsaktiver, som den juridiske enhed har produceret eller fremstillet til sig selv, i lagerkladden til anlægsaktiver. Du kan derefter overføre lagervarer til anlægsaktiver, som en anskaffelse eller som del af en anskaffelse. 

Du kan også anskaffe aktiver ved hjælp af indkøbsordrer. Når indkøbsordrer indeholder lagervarer, der er angivet som anlægsaktiver, bestemmer indstillingen i feltet **Tillad aktivanskaffelse fra Indkøb** på siden **Anlægsaktivparametre**, om anskaffelsen bogføres for anlægsaktivet, når fakturaen bogføres. En indkøbslinje opretter ét anlægsaktiv uanset antallet. Hvilken effekt anskaffelsen af anlægsaktiver har på lageret afhænger af opsætningen af en juridisk enhed. 

Når en lagervare ændres til en anlægsaktivanskaffelse, enten via lagerkladden, en indkøbsordre eller et anskaffelsesforslag, oprettes der en anlægsaktivpostering for bogen. Hvis en boganskaffelse inkluderer en afledt bog, oprettes der også en anskaffelsespostering for den afledte bog. 

Posteringsregler, der oprettes på siden **Postering** i Lagerstyring, kontrollerer lagerreduceringen, når en anskaffelse posteres. Du reducerer imidlertid ikke altid lagerbeholdningen, når du bogfører fakturaer, der vedrører anlægsaktiver. I nogle tilfælde kan anlægsaktiverne købes til intern brug. Et eksempel er en bærbar computer, der er købt til salgsafdelingen. Når du arbejder med indkøbsordrer, kan du bruge varer, der både er angivet til videresalg og internt brug. 

Hvis du bruger bestemte tilgangs- og afgangskonti for anlægsaktiver i varegrupper, kan du bruge samme lagervare for både interne køb og som lager til videresalg. 

Anlægsaktiver, der er til intern brug, er konfigureret, så de har kontotypen **Kvittering for anlægsaktiv**. Denne kontotype bruges til at spore modtagelsen af anlægsaktivet. Når du bogfører en kreditorfaktura, skal du bruge tilgangskontoen for anlægsaktivet, hvis en af følgende betingelser er opfyldt:

-   Fakturalinjen indeholder et eksisterende anlægsaktiv til interne formål.
-   Afkrydsningsfeltet **Nyt anlægsaktiv** er markeret for den produktkvitteringslinje, der er bogført.
-   Afkrydsningsfeltet **Opret et nyt anlægsaktiv** er markeret for kreditorfakturalinjen.

Denne konto er som regel en udgiftskonto. Du kan oprette kontotypen **Kvittering for anlægsaktiv** for enten en varegruppe eller en enkelt vare ved hjælp af fanen **Indkøbsordre** på siden **Varegruppe** eller **Postering**.

På samme måde kan anlægsaktiver til intern brug konfigureres, så de har kontotypen **Anlægsaktivafgang**. Denne kontotype bruges til at spore udstedelse af anlægsaktivet til modtageren. Når et anlægsaktiv anskaffes ved hjælp af en indkøbsordre, udligner anlægsaktivafgangskontoen anlægsaktivets debetkonto. Anskaffelse af anlægsaktiver kan bogføres, når du bogfører en kreditorfaktura, eller når du bogfører anskaffelsen af anlægsaktivet i kladden Anlægsaktiver, eventuelt ved at bruge et anskaffelsesforslag. Du kan oprette kontotypen **Anlægsaktivafgang** for enten en varegruppe eller en enkelt vare ved hjælp af fanen **Lager** på siden **Varegruppe** eller **Varebogføring**. 

Endelig bestemmes de hovedkonti, der bruges til bogføring, af indstillingerne for finansintegration, der er angivet for varemodelgruppen. Hvilke hovedkonti, der bruges, varierer, afhængigt af om et aktiv er tildelt til indkøbsordrelinjen. Kontiene er afledt af posteringsprofilen for de enkelte varegrupper. 
**Bemærk:** Hvis der findes en lagerreservation, når produktkvitteringer bogføres, kan du ikke tildele et anlægsaktiv eller oprette et anlægsaktiv fra linjen. 

Hvilke konti, anlægsaktivposteringerne bogføres på, afhænger af to faktorer: Om anlægsaktiverne er købt eller fremstillet af den juridiske enhed samt af posteringstypen for anlægsaktivet. 

Posteringstypen forbinder lagertransaktionen med posteringsprofilen i Anlægsaktiver. Da posteringsprofilen for anlægsaktiverne definerer, hvilke konti der skal opdateres, er valget af posteringstype for et anlægsaktiv også indirekte et valg af de hovedkonti, som transaktionen skal bogføres på. Posteringstypen vil normalt være **Anskaffelse** eller **Anskaffelsesregulering** både for fremstillede og købte anlægsaktiver.

## <a name="accounts-receivable"></a>Debitor
Integration af anlægsaktiver med Debitor bruger posteringsprofiler, der oprettes i Anlægsaktiver. Disse posteringsprofiler aktiveres, når et anlægsaktiv, en bog og anlægsaktivets posteringstype er valgt til en debitorfaktura, før debitorfakturaen bogføres. Da anlægsaktiverne ikke er en del af lagerstyringen, skal du bruge siden **Fritekstfaktura**, når du sælger et anlægsaktiv. 

Hvis bogen indeholder en afledt bog, oprettes der en postering for den afledte bog, når du bogfører debitorfakturaen.

## <a name="accounts-payable"></a>Kreditor
Anlægsaktiver købes normalt af eksterne leverandører. Du kan bruge siden **Anlægsaktivparametre** til at angive, om anskaffelser af aktiver altid skal bogføres, når du bogfører kreditorfakturaer, eller om anskaffelser af aktiver kun kan bogføres fra Anlægsaktiver. Hvis du aktiverer bogføring af anskaffelse af anlægsaktiver fra Kreditor, opdateres anlægsaktivkonti, hver gang der bogføres en kreditorfaktura for anskaffelse af et anlægsaktiv. 

Hvis systemet er konfigureret til at bogføre anskaffelsesposteringer, når en faktura bogføres, bogføres posteringen i overensstemmelse med de posteringsprofiler, der er oprettet i Anlægsaktiver til forskellige posteringstyper for anlægsaktiver. Bogføringen foretages på baggrund af det anlægsaktiv, den bog og den posteringstype for anlægsaktiver, der er valgt på siden **Indkøbsordre**, før kreditorfakturaen bogføres. 

Hvis bogen indeholder en afledt bog, oprettes der en postering for den afledte bog, når du bogfører kreditorfakturaen.

Integrationen aktiveres for hver ordrelinje under fanen **Anlægsaktiver** i oversigtspanelet **Linjedetaljer** på siden **Indkøbsordre**. Du kan sende en indkøbsordre for et anlægsaktiv til leverandøren. Men anlægsaktiverne og hovedkontiene opdateres kun, når du bogfører kreditorfakturaen, efter at anlægsaktivet er modtaget. Hvilken effekt anskaffelsen af anlægsaktiver har på lageret afhænger af opsætningen af en juridisk enhed, da indkøbsordrer kun kan indeholde lagervarer.

## <a name="project-management-and-accounting"></a>Projektstyring og regnskab
Du kan knytte et projekt til et anlægsaktiv, der er berørt af projektet. Du kan også knytte hver fase, opgave eller hvert underprojekt til et andet aktiv. Et aktiv kan være knyttet til hver projektpost. Du kan oprette tilknytningen, når du indtaster et anlægsaktivnummer i feltet **Anlægsaktiver** på siden **Projekter**. Projekttypen skal enten være **Intern** eller **Omkostningsprojekt**. 

Du kan også bruge siden **Projekter** til at få vist detaljer om aktiver, der er knyttet til projekter. Hvis du vil have vist anlægsaktivposten, skal du klikke på aktivets link i oversigtspanelet **Konfiguration** for at åbne siden **Anlægsaktiver**. Klik derefter på **Projekter** &gt; **Alle projekter** for at få vist de projekter, der er knyttet til anlægsaktivet. 

Du knytter som regel anlægsaktiver til projekter, når projekterne er relateret til arbejde, vedligeholdelse eller forbedring af aktivet. Når projektet er fuldført, oprettes der ikke automatisk en opskrivningsregulering for aktivet. Derfor skal du oprette opskrivningsreguleringen manuelt, hvis den kræves. 

Hvis du vil slette en tilknytning mellem et projekt og et aktiv, skal du fjerne markeringen i feltet **Nummer på anlægsaktiv** på siden **Projekter**. 

Du kan også angive et anlægsaktiv, du opretter eller producerer som led i et forkalkuleret projekt. Ved afslutningen af det forkalkulerede projekt kan du automatisk bogføre en anskaffelsespostering for et aktiv.

Du kan finde flere oplysninger under [Anskaffelse af aktiver via indkøb](acquire-assets-procurement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]