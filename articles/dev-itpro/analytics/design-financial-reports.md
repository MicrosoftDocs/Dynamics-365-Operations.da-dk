---
title: "Vise og designe økonomirapporter"
description: "Denne artikel indeholder øvelser, der hjælper dig med visning og oprettelse af økonomirapporter til Microsoft Dynamics 365 for Finance and Operations."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReportingSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 86597a81b4dcfb14cbc88667fbb1db214133c6e5
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="view-and-design-financial-reports"></a>Vise og designe økonomirapporter

[!include [banner](../includes/banner.md)]

Denne artikel indeholder øvelser, der hjælper dig med visning og oprettelse af økonomirapporter til Microsoft Dynamics 365 for Finance and Operations. Økonomirapportering består af en visuel oplevelse i Finance and Operations og en ClickOnce-rapportdesigner, hvor du kan oprette og redigere økonomirapporter.  

<a name="exercise-1-generate-and-explore-a-default-financial-report"></a>Øvelse 1: Oprette og udforske en økonomisk standardrapport
-----------------------------------------------------------

I denne øvelse skal du generere og udforske en eksisterende standardrapport. Denne rapport omfatter alle konti og indeholder også kontoegenskaber (attributter) for kontiene. Du skal foretage detailudledning i transaktionsdetaljer, anvende dimensionsfiltre, ændre valutaen på rapporten. Først skal vi opdatere visningsrækkefølgen af dimensioner til økonomirapportering. Her kan du vælge, hvordan dimensioner skal vises, ikke blot mens økonomiske rapporter designes og vises.

1.  Gå til **Konfiguration af økonomisk dimension til integrering af programmer** under **Dimensioner i kontoplanen** i Finans.
2.  Flyt dimensioner, så de er i følgende rækkefølge:
    1.  Hovedkonto
    2.  Virksomhedsenhed
    3.  Bærer
    4.  Afdeling

    Bemærk! De andre dimensioner kan forblive i den rækkefølge, de er i i øjeblikket.
3.  Gem konfigurationen af dimensionen. Dernæst skal vi generere en rapport og udforske data i rapporten.
4.  Gå til **Økonomirapporter** under **Forespørgsler og rapporter** i Finans.
5.  Vælg rækken for rapporten med navnet **Finansdetaljer – standard.**
6.  Vælg **Rediger.** Bemærk! Du bliver bedt om at hente Report Designer og logge på. Du kan bruge dine legitimationsoplysninger til at logge på.
7.  Ret basisåret til 2012, og vælg **Generer**. Når der oprettes en rapport fra rapportdesigneren, åbnes den i en ny fane i browseren. Du kan enten udforske rapporten i den nye fane i browseren, eller gå til den oprindelige browserfane og åbne rapporten i denne ved at vælge den på listen **Økonomirapporter**.
8.  I den åbnede rapport skal du vælge t af beløbene for at dykke ned i kontodetaljerne for rapporten.
9.  Én gang i kontooplysninger skal du vælge en konto med data og **dykke til rapportens transaktionsniveau**. Du kan se de egenskaber (attributter), der er inkluderet i denne rapports design, på rapportens posteringsniveau. Afhængigt af posteringen og konto, vise nogle eller alle attributterne muligvis.
10. Luk rapportposteringsniveauet.
11. Vælg den samme eller en anden konto og **åbn bilagsposteringer.** Bilagsposteringer er filtreret efter kombination af periode, år og konto + dimension for den valgte konto. Du kan vælge at udforske andre oplysninger om transaktionen fra posteringer på bilag.
12. Luk bilagstransaktioner. Du kan vælge at se data for en anden periode og år eller med forskellige egenskaber og dimensioner, der anvendes inden for en økonomirapport. Det gøres med brug af **Rapportindstillinger**.
13. Vælg **Rapportindstillinger**.
14. Vælg **Tilføj et dimensionsfilter** , og vælg **Virksomhedsenhed**.
15. Skriv 001 i feltet, og vælg **OK**. Rapporten viser nu kun data for 001 virksomhedsenheden. Dette er en personlig visning af rapporten og er ikke tilgængelig for andre.
16. Luk den filtrerede rapport. Økonomirapporter kan vises i en hvilken som helst valuta, der er føjet til Finance and Operations.
17. Vælg **Valuta**, og vælg derefter **EUR.** Rapporten vises nu i euro. Alle valutakoder og valutasymboler, der er med i rapportdesignet, vises nu i den valuta, der er anvendt. Hvis intet valutasymbol er defineret for en valuta, vises valutasymbolet ikke.
18. Luk rapporten **Finansdetaljer**.
19. Luk **Report Designer**.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>Opgave 2: Føj ekstra kontoegenskaber til et rapportdesign
I denne øvelse skal du redigere en eksisterende standardrapport. Du opdaterer både rækkedefinitionen for at medtage alle konti, og du skal opdatere kolonnedefinitionen for at få attributter for kontoen. Når opdateringerne er fuldført, skal du generere den nyoprettede rapport og gennemse den. Vi starter fra listen over økonomiske rapporter.

1.  Gå til **Økonomirapporter** under Forespørgsler og rapporter i Finans.
2.  Vælg rækken for rapporten med navnet **Råbalanceoversigt – standard.**
3.  Vælg **Rediger**. **Oversigt over råbalance – standard** åbnes i Report Designer.
4.  Vælg **Filer**, derefter **Gem som**, og navngiv rapporten Detaljeret råbalance med attributter. Bemærk! Hver gang en ny rapport i Report Designer, opdateres listen over økonomirapporter i Finance and Operations.
5.  Fra rapportdefinition skal du vælge ikonet for rækkedefinitionen for at åbne **Råbalance – standardrækkedefinition**.
6.  Gem rækkedefinitionen, som **Detaljeret råbalance med attributter**
7.  Placer markøren på række 50, Vælg **Rediger**, derefter **Indsæt rækker fra dimensioner**. Med Indsæt rækker fra dimensioner kan du vælge, hvilke dimensioner du vil have i din rækkedefinition. I denne øvelse skal vi til at bygge rækkedefinitionen ved hjælp af hovedkonto.
8.  Sørg for, at **Hovedkonto** indeholder og-tegn (&), og vælg **OK**. Rækkedefinitionen indeholder nu alle hovedkonti for den juridiske enhed USMF.
9.  Rul ned til række 11110, og Slet række 11110.
10. Vælg i række 11080 **---(understregningsbeløb)**.
11. Skriv i række 11140 **Total for alle konti** i kolonne B.
12. Vælg i kolonne C, **TOTt** på rullelisten.
13. Type **50:11080** i kolonne D.
14. **Gem** rækkedefinitionen. Rækkedefinitionen indeholder nu alle konti samt en totalrække til at føje alle konti sammen. Dernæst opdaterer vi kolonnedefinitionen for at medtage ekstra kontoattributter.
15. Fra rapportdefinitionen **Detaljeret råbalance med attributter** skal du markere kolonnedefinitionsikonet for at åbne kolonnedefinitionen **Råbalanceoversigt – standard**.
16. Gem kolonnedefinitionen, som **Detaljeret råbalance med attributter**. Kolonnedefinitionen indeholder kolonner af økonomiske data, en kolonne med beskrivelse og beregningskolonner. Vi vil føje attributkolonner til kolonnedefinitionen for at give yderligere detaljer om kontiene.
17. Følgende attributter skal føjes til kolonnedefinitionen:
    -   Kladdenummer
    -   Beskrivelse af kladde
    -   Posteringsdato
    -   Oprettet af
    -   Senest ændret af

18. Vælg i kolonnen **ATTR** som kolonnetype. Vælg derefter **Kladdenummer** som attributkategori.
19. Fortsæt med at tilføje kolonner for de resterende attributter.
20. I rækken **Overskrift 2** skal du tilføje beskrivelser til hver af de nye kolonner, der er tilføjet.
21. Gem kolonnedefinition. Nu da definition af række og kolonnedefinition er blevet opdateret, skal vi føje dem til rapportdefinitionen.
22. Fra rapportdefinitionen **Detaljeret råbalance med attributter** skal du markere Detaljeret råbalance med attributter for både række- og kolonnedefinitionen.
23. Ret basisåret til **2012.**
24. **Gem** rapportdefinitionen og **generer**. Når rapporten er fuldført, oprettes og åbnes, kan du undersøge rapporten, som du gjorde i den første øvelse. Foretag detaljeudledning for flere konti for at se, hvordan de ekstra attributter vises.
25. Luk rapporten **Detaljeret råbalance med attributter**.
26. Luk **Report Designer**.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>Øvelse 3: Opret en flerdimensional rapport ved hjælp af et rapporteringstræ
I denne øvelse skal du redigere en eksisterende standardrapport. Du opretter et rapporteringstræ og føjer til en rapportdefinition for producere en bærer/Divisional-resultatopgørelse. Når opdateringerne er fuldført, skal du generere bærer/Divisional-resultatopgørelse og udforske rapporten ved hjælp af rapporteringstræet. Vi starter fra listen over økonomiske rapporter.

1.  Gå til **Økonomirapporter** under Forespørgsler og rapporter i Finans.
2.  Vælg rækken for rapporten med navnet **Resultatopgørelse – standard.**
3.  Vælg **Rediger**. **Resultatopgørelse – standard** åbnes i Report Designer.
4.  Klik på **Filer** i menuen, peg på **Ny**, og klik derefter på **Rapporteringstrædefinition**.
5.  I menuen **Rediger** skal du klikke på **Indsæt rapporteringsenheder fra dimensioner**.
6.  Fjern markeringen i afkrydsningsfelterne for alle dimensioner med undtagelse af **Bærer**.
7.  Klik på feltet **Fra dimensiona** for bærer-dimensionen Bærer, skriv **007**, og tryk derefter på Tab-tasten. I feltet **Til dimension** skal du skrive **018**.
8.  **Gem** det resulterende træ med navnet **Bærere efter division.** Nu, hvor rapporteringstræet er blevet oprettet, skal du ændre træet, så det indeholder tre nye opdateringspakkeenheder; Marketing, operationer og Detail.
9.  I menuen **Vindue** skal du klikke på **Bærere efter division**. (Hvis rapporteringstræet er blevet lukket, skal du vælge det rapporteringstrædefinitionerne i navigationsruden).
10. Klik på enhed nummer to, **Messer**, og klik på ikonet **Indsæt rapporteringsenhed**.
11. Dobbeltklik på enhedskolonnen i den tomme række, og vælg **USMF**.
12. Skriv **Marketing** i kolonne B og C.
13. Klik på enhed nummer fem, **Servicehandlinger**, og højreklik. **Vælg Indsæt rapporteringsenhed**.
14. Gentag trin 11.
15. Skriv **Operationer** i kolonne B og C.
16. Klik på enhed nummer 12, **Outlet**, og højreklik. Vælg **Indsæt rapporteringsenhed**.
17. Gentag trin 11.
18. Skriv **Detail** i kolonne B og C. Bemærk, at Marketing, Operationer og Detail-enheder vises på samme niveau som de aktuelle akkumulerede enheder. De nye enheder organiseres dernæst. Rapporteringsenheder organiseres gennem højrekliksindstillingerne: hæve og sænke eller ved at trække og slippe.
19. Kontroller, at enhed tre **Messer**, er aktiv, og højreklik.
20. Vælg **Sænk rapporteringsenhed**. Bemærk, at enheden nu vises underordnet til **Marketing**.
21. Klik på enhed fire, **Marketing** **Kampagne**, og højreklik.
22. Vælg **Sænk rapporteringsenhed**.
23. Klik på **Servicehandlinger** i den grafiske oversigt. Tryk på og hold venstre museknap nede, mens du trækker enheden op til **Operationer**. Slip venstre museknap for at slippe enheden i opdateringen til Operationer. Gentag dette for **produktion, kvalitetskontrol, logistik, indkøb og administration**.
24. Gøre **Outlet**, **Super**, **Indkøbscenter** og **Online** til underordnet til **Detail** ved at sænke dem eller trække og slippe dem.
25. Gemme den resulterende nye organisation. Nu hvor vi har oprettet og organiseret rapporteringstræet, kan det føjes til rapportdefinitionen.
26. I menuen **Vindue** skal du vælge **Resultatopgørelse – standard** for at åbne rapportdefinitionen.
27. Klik på rullelisten **Trætype**, og vælg **Rapporteringstræ**.
28. Klik på rullelisten Træ, og vælg **Bærere efter division**.
29. Ret basisåret til **2012**, **Gem** ændringerne, og **generer** rapporten. Når rapporten færdiggøres, oprettes og åbnes, kan du gennemse rapporten.
30. Vælg rullelisten **Rapporteringstræ** for at få vist rapporteringsenhederne. Alternativt kan du rulle ned på en række i rapporten for at se alle saldi for alle enheder af rapporteringstræet.
31. Luk **Resultatopgørelse – standard**.
32. Luk **Report Designer**.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>Øvelse 4: Opret en konsolideret rapport ved hjælp af et organisationshierarki
I denne øvelse skal du redigere en eksisterende standardrapport. Du vil tilføje et organisationshierarki i rapportdefinitionen for at oprette en konsolideret resultatopgørelse og balancen. Når opdateringerne er fuldført, skal du oprette den konsoliderede rapport og udforske den ved hjælp af rapporteringstræet. Vi starter fra listen over økonomiske rapporter.

1.  Gå til **Økonomirapporter** under Forespørgsler og rapporter i Finans.
2.  Vælg rækken for rapporten med navnet **Balancen og resultatopgørelsen side om side – standard**
3.  Vælg **Rediger**. **Balancen og resultatopgørelsen side om side – standard** åbnes i Report Desinger.
4.  Vælg **Filer** &gt; **Gem som** og giv rapporten navnet **Konsolideret balance og resultatopgørelse side om side**.
5.  Ret basisåret til 2012.
6.  Klik på rullelisten Træ og vælg **Organisationshierarkier**.
7.  Klik på rullelisten Træ, og vælg **Contoso Holdings**.
8.  Gem ændringerne, og generer rapporten. Hvis du bliver bedt om det, kan du vælge alle rapporteringsenheder. Når rapporten færdiggøres, oprettes og åbnes, kan du gennemse rapporten.
9.  Vælg **Rapportindstillinger**.
10. Vælg **Tilføj et dimensionsfilter** , og vælg **Afdeling**.
11. Skriv **022** i feltet, og vælg **OK**.
12. Luk den filtrerede rapport.
13. Vælg rullelisten **Rapporteringstræ** for at få vist rapporteringsenhederne. Alternativt kan du rulle ned på en række i rapporten for at se alle saldi for alle enheder af rapporteringstræet.
14. Luk **Konsolideret balance og resultatopgørelse side om side**.
15. Luk **Report Designer**.

## <a name="exercise-5-create-a-sidebyside-departmental-report"></a>Øvelse 5: Opret en side om side-afdelingsrapport
I denne øvelse skal du oprette en ny rapport. Rapporten er en afdelings resultatopgørelse side om side. Du skal bruge en eksisterende rækkedefinition, men du kan oprette en ny rapportdefinition, og en ny kolonnedefinition, der bruger dimensionsfiltre. Vi starter fra listen over økonomiske rapporter.

1.  Gå til **Økonomirapporter** under Forespørgsler og rapporter i Finans.
2.  Vælg **Ny**. Report Designer åbnes med en tom rapportdefinition, der er åben. Din første opgave skal være at oprette kolonnedefinitionen.
3.  Oprette en ny kolonnedefinition af ved at klikke på **Filer**, derefter **Ny** og derefter **Kolonnedefinition**.
4.  I **Kolonne A** skal du vælge **DESC** for kolonnetypen.
5.  I **Kolonne B** skal du vælge **FD** for kolonnetypen.
6.  Dobbeltklik på feltet **Dimensionsfilter**.
7.  I vinduet **Dimension** skal du dobbeltklikke på kolonnen **Afdeling**.
8.  I området med enkeltvist eller interval i dialogboksen skal du klikke på **ellipsen** for feltet **Fra** for at få vist en liste over afdelinger.
9.  Vælg afdeling **022**, **Salg og marketing**, og klik derefter på **OK**.
10. Gentag trin 5 til 8 for afdelingerne 23-25.
11. I rækken **Overskrift 2** til hver FD-kolonne skal du skrive følgende afdelingsbeskrivelser:
    -   Kolonne B - Salgs- og marketing
    -   Kolonne C – Operationer
    -   Kolonne D - Finans
    -   Kolonne E - It

12. Gem kolonnedefinitionen som afdelinger ved siden af hinanden. Da vi bruger en eksisterende rækkedefinition, kan rapportdefinitionen nu ændres, så den nyoprettede kolonnedefinitionen og eksisterende rækkedefinition kan bruges.
13. I menuen **Vindue** skal du vælge **Ny rapportdefinition** for at åbne rapportdefinitionen.
14. Vælg **Resultatopgørelse – standard** som rækkedefinition og **Afdelinger ved siden af hinanden** som kolonnedefinition.
15. Gem rapportdefinitionen som **Afdelingsresultatopgørelse side om side**.
16. Ret basisåret til **2012**.
17. Ret detaljeringsniveauet til **Finans, Konto og Transaktion**.
18. **Gem** dine ændringer og **generer**. Når rapporten færdiggøres, oprettes og åbnes, kan du gennemse rapporten.

## <a name="additional-resources"></a>Yderligere ressourcer
[Økonomirapportering](../../financials/general-ledger/financial-reporting-getting-started.md) 
[Vis økonomirapporter](../../financials/general-ledger/view-financial-reports.md) 
[Bloggen Dynamics Financial Reporting](http://blogs.msdn.com/b/dynamics_financial_reporting/)




