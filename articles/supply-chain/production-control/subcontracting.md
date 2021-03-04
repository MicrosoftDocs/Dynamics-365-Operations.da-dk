---
title: Underleverandørarbejde
description: Med dette emne kan du opbygge en gennemgang af underleverandørarbejde i produktion i Dynamics 365 Supply Chain Management.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1cc1040393d843f39ca8c741a7c51435c7169c00
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424364"
---
# <a name="subcontracting"></a>Underleverandørarbejde

[!include [banner](../includes/banner.md)]

Med dette emne kan du opbygge en gennemgang af underleverandørarbejde i produktion i Microsoft Dynamics 365 Supply Chain Management. Den første del af dette emne beskriver opsætningen af dataene. Den anden del fører dig gennem trinnene i gennemgangen.

## <a name="target-audience"></a>Målgruppe

I dette emne lærer du, hvordan du konfigurerer underleverandørarbejde i produktion. Du skal bruge eksisterende data i den juridiske enhed HQUS til at foretage grundlæggende opsætning af et aktivitetsflow for underleverandørarbejde. Demodataene i den juridiske enhed HQUS omfatter opsætningsparametre, der er forudindstillet til at understøtte trinnene i gennemgangen. Selvom gennemgangen omhandler vigtige smertepunkter og udfordringer for forskellige roller, kan den fuldføres af systemadministratoren.

## <a name="demo-scenario"></a>Demoscenarie

Højttalere af høj kvalitet produceres i den juridiske enhed HQUS. Under fremstillingsprocessen gennemgår højttalerne følgende tre operationer.

- **Formontering** – Højttalerens kabinet samles. Materialet til kabinettet plukkes på materialelagerstedet, før operationen startes.
- **Belægning** – Når højttalerkabinettet er samlet, skal det belægges. Denne handling udføres af en leverandør (underleverandør). Det formonterede højttalerkabinet leveres til underleverandøren af belægning sammen med to materialer.
- **Finish** – Efter det formonterede højttalerkabinet er blevet belagt af underleverandøren, returneres det til den juridiske enhed HQUS, så den endelige montage af højttaleren kan fuldføres.

I følgende illustration vises de tre operationer og de materialer, de forbruger.

![Operationerne Formontering, Belægning og Finish og de materialer, de forbruger](./media/subcontract01_operations-materials.png)

## <a name="setup"></a>Konfiguration

Før du begynder denne gennemgang, skal du konfigurere dataene.

### <a name="set-up-the-finished-product"></a>Konfigurer det færdige produkt

Denne procedure der fører dig gennem opsætningen af det frigivne produkt D8100, "Belagt kabinet".

1. Vælg **Administration af produktoplysninger \> Produkter \> Frigivne produkter** for at åbne siden **Frigivne produktdetaljer**.
2. Angiv **D8100** i Quick filter-feltet for at finde det eksisterende frigivne produkt.

    ![Filtrering for frigivet produkt D8100 på siden Frigivne produktdetaljer](./media/subcontract02_filtering-released-products.png)

3. I handlingsruden skal du under fanen **Opret** vælge **Rute** for at åbne siden **Rute**.

    På siden **Rute** vises de otte ruteversioner for det frigivne produkt D8100. De otte ruteversioner er opdelt i fire ruter på sted 1 og sted 5. Rute 000400 anvendes til efterkalkulation, rute 00041 bruges, når operationen Belægning er en intern handling, og rute 00042 bruges, når operationen Belægning er en ekstern operation.

    ![Otte ruteversioner på siden Rute](./media/subcontract03_route-page.png)

4. I den øverste rude i **Versioner**-gitteret skal du vælge ruteversion **00042** for sted **5**.
5. I den nederste rude under fanen **Oversigt** skal du vælge operationen **20** (**Cbnt CtSc**) i gitteret.

    ![Operation 20 for ruteversion 00042 for sted 5 er valgt](./media/subcontract04_route-version-operation.png)

6. Vælg fanen **Generelt**.

    Bemærk, at feltet **Rutetype** er angivet til **Leverandør**. Denne værdi angiver, at operation 20 (Cbnt CtSc) er en operation, der er udført af underleverandør.

    ![Feltet Rutetype angivet til Leverandør under fanen Generelt](./media/subcontract05_general-tab.png)

7. Vælg fanen **Ressourcebehov**.

    Egenskaber skal bruges til at finde en passende ressource i produktionsplanlægningen. For operation 20 (Cbnt CtSc) skal du bemærke, at en ressource, der har to egenskaber, **Belægning** og **Belagte kabinetter**, er påkrævet.

    ![Belægning og Belagte kabinetter som egenskaber under fanen Ressourcebehov](./media/subcontract06_resource-requirements-tab.png)

8. Vælg **Disponible ressourcer** for at åbne **Disponible ressourcer**-dialogboksen.

    Der findes tre ressourcer, der opfylder ressourcebehovet til operationen. Bemærk, at ressourcerne 8851 og 8852 er af typen **Leverandør**.

    ![Tre disponible ressourcer i dialogboksen Disponible ressourcer](./media/subcontract07_applicable-resources-dialog.png)

9. Vælg **OK** at lukke **Disponible ressourcer**-dialogboksen, og vend tilbage til siden **Rute**.
10. Luk siden **Rute** for at vende tilbage til siden **Frigivne produktdetaljer**.

    ![Siden Frigivne produktdetaljer](./media/subcontract08_released-product-details-page.png)

11. I handlingsruden skal du under fanen **Opret** vælge **Styklisteversioner** for at åbne siden **Styklisteversioner**.

    Siden **Styklisteversioner** viser de fire styklisteversioner for det frigivne produkt D8100. Styklisten 000040 anvendes til efterkalkulation og planlægning, styklisten 000041 bruges, hvis handlingen Belægning udføres internt, og styklisterne 000042 og 000043 bruges, hvis handlingen Belægning udføres af underleverandør.

    Bemærk, at vare S8050 er et produkt af **Service**-varetypen. Varen repræsenterer det arbejde, der udføres af underleverandør.

    ![Fire styklisteversioner på siden Styklisteversioner](./media/subcontract09_bom-versions-page.png)

12. Brug oversigtspanelet **Styklistelinjer** til at vælge **Rediger** for at åbne **Rediger styklistelinje**-dialogboksen.

    Når en produktionsordre er oprettet og forkalkuleret for det frigivne produkt D8100, genereres en indkøbsordre automatisk for vare S8050. Denne indkøbsordre bliver knyttet til produktionsordren. For indkøbsordrer, der skal genereres automatisk, skal feltet **Linjetype** være angivet til **Leverandør**, og kreditorkontoen for underleverandøren skal være valgt. I dette tilfælde er kreditorkontoen US-801.

    Bemærk, at styklistelinjen er tilknyttet operationen Belægning via operationsnummeret (i dette tilfælde 20).

    ![Dialogboksen Rediger styklistelinje](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a>Opret en adgangskode til lagermedarbejdere

Du skal definere en adgangskode for de lagermedarbejdere, der bruger en håndholdt enhed.

1. Vælg **Lagerstedsstyring \> Konfiguration \> Arbejder** for at åbne siden **Arbejdsbrugere**.
2. I oversigtspanelet **Brugere** skal du vælge rækken for bruger **51**.

    ![Siden Arbejdsbrugere](./media/subcontract11_work-users-page.png)

3. Vælg **Nulstil adgangskode**.
4. I felterne **Adgangskode** og **Bekræft adgangskode** skal du angive **1**.
5. Vælg **Angiv adgangskode**.

## <a name="step-by-step-walkthrough"></a>Trinvis gennemgang

**Scenario og baggrund**

Der oprettes en produktionsordre på 10 styk for produkt D8100, "Belagt kabinet". Belægningen af kabinetterne er en underleverandøroperation, der udføres hos leverandør US-801, Perfect Coating Solutions. Produktionsordren består af tre operationer. I den første operation er kabinettet formonteret som en intern operation. Materialet til formonteringen frigives til pluk på råvarelageret. Når formonteringen er fuldført, sendes det formonterede kabinet til Perfect Coating Solutions sammen med to materialer, der kræves til operationen Belægning. Når det belagte kabinet modtages fra leverandøren, gennemgår det en endelig montage, før det færdigmeldes.

1. Vælg **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer** for at åbne siden **Alle produktionsordrer**.
2. I handlingsruden skal du vælge **Ny produktionsordre** for at åbne dialogboksen **Oprettelse af produktionsordre**.

    ![Dialogboksen Oprettelse af produktionsordre](./media/subcontract12_create-production-order-dialog.png)

3. Vælg **D8100** i feltet **Varenummer**.
4. Når du har valgt varenummeret, vises felter for lagerdimensioner. Vælg **Krom** i feltet **Farve**.

    Der vises en meddelelse, hvor du bliver spurgt, om de aktive versioner for styklisten og ruten skal indsættes.

    ![Meddelelsesboks](./media/subcontract13_message-box.png)

5. Vælg **Ja**. 

    I **Opret produktionsordre**-dialogboksen er de aktive versioner af styklisten og ruten for produkt D8100 automatisk valgt i felterne **Styklistenummer** og **Rutenummer**. I dette tilfælde er stykliste **000040** og rute **000040** valgt.
    
    > [!NOTE]
    > Version 000040 bruges til efterkalkulation og planlægning for både styklisten og ruten.

6. Vælg **5** i feltet **Sted**.
7. Vælg **51** i feltet **Lagersted**.
8. I felterne **Styklistenummer** og **Rutenummer** skal du ændre den værdi, der automatisk er valgt, til **000042**.

    > [!NOTE]
    > Version 000042 bruges til at give i underentreprise belægningen af kabinettet til leverandør US-801 for både styklisten og ruten.

    ![Værdier i dialogboksen Opret produktionsordre](./media/subcontract14_create-production-order-dialog-set.png)

9. Vælg **Opret** for at oprette produktionsordren og vende tilbage til siden **Alle produktionsordrer**.

    ![Ny produktionsordre på siden Alle produktionsordrer](./media/subcontract15_new-production-order.png)

10. I handlingsruden skal du under fanen **Produktionsordre** vælge **Estimat** for at åbne **Estimat**-dialogboksen.

    ![Dialogboksen Estimat](./media/subcontract16_estimate-dialog.png)

11. Vælg **OK** for at bekræfte estimatet og vende tilbage til siden **Alle produktionsordrer**.

    > [!NOTE]
    > Når produktionsordren er estimeret, genereres indkøbsordren for servicevare S8050 for leverandør US-801.

12. I handlingsruden skal du under fanen **Produktionsordre** vælge **Stykliste** for at åbne siden **Stykliste**, hvor du kan få vist styklistelinjer for produktionsordren.

    For servicevare S8050 skal du bemærke, at der er en reference til den indkøbsordre, der blev genereret, da produktionsordren blev estimeret.

    ![Produktionsordrens styklistelinjer på siden Stykliste](./media/subcontract17_production-order-bom-lines.png)

13. Luk siden **Stykliste** for at vende tilbage til siden **Alle produktionsordrer**.
14. I handlingsruden skal du under fanen **Tidsplan** vælge **Finplanlægge** for at åbne **Finplanlægning**-dialogboksen.
15. Angiv følgende værdier:

    - Vælg **Fremad fra i morgen** i feltet **Planlægningsvej**.
    - Angiv **Kapacitetsbegrænsning** til **Ja**.

    ![Dialogboksen Finplanlægning](./media/subcontract18_job-scheduling-dialog.png)

16. Vælg **OK** for at lukke **Finplanlægning**-dialogboksen og vende tilbage til siden **Alle produktionsordrer**.
17. I handlingsruden skal du under fanen **Tidsplan** vælge **Gantt** for at åbne siden **Gantt-diagram - ressourcevisning**.

    Gantt-diagrammet indeholder en visuel oversigt over, hvordan produktionsjob planlægges på ressourcer. Bemærk, at den eksterne belægningsoperation består af tre job: et procesjob, et transportjob og et køtidsjob.

    ![Gantt-diagram på Gantt-diagram - siden Ressourcevisning](./media/subcontract19_gantt-chart.png)

18. Luk siden **Gantt-diagram - ressourcevisning** for at vende tilbage til siden **Alle produktionsordrer**.
19. I handlingsruden skal du under fanen **Produktionsordre** vælge **Frigivelse** for at åbne **Frigivelse**-dialogboksen.

    ![Dialogboksen Frigivelse](./media/subcontract20_release-dialog.png)

20. Vælg **OK** for at lukke dialogboksen **Frigivelse**.
21. Vælg **Produktionsstyring \> Periodiske opgaver \> Frigiv til lagersted \> Automatisk frigivelse af stykliste- og formellinjer** for at åbne dialogboksen **Automatisk frigivelse af stykliste- og formellinjer**.

    ![Dialogboksen Automatisk frigivelse af stykliste- og formellinjer](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. Vælg **OK** for at køre automatisk frigivelse af stykliste- og formellinjejob.

    Dette job frigiver plukarbejde for råmaterialer til lagerstedet.

23. Vælg **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer** for at åbne siden **Alle produktionsordrer**.
24. Du kan bruge feltet Quick filter til at vælge den produktionsordre, du har arbejdet på.
25. I handlingsruden skal du under fanen **Lagersted** vælge **Arbejdsdetaljer** for at åbne siden **Arbejde**.

    Bemærk, at siden viser to sæt af arbejde til pluk af råmateriale. Det første arbejde er for materialerne M8100 og M8101. Disse materialer forbruges af operation 10. Det andet arbejde er for materialerne M8202 og M8250. Materialerne forbruges af operation 20, som er operationen hos underleverandøren.

    ![To sæt af arbejde til pluk af råmateriale på siden Arbejde](./media/subcontract22_work-page.png)

26. Start lagerstedsappen for at behandle lagerstedets arbejde for operation 10.

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. Vælg **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer** for at åbne siden **Alle produktionsordrer**.
28. Du kan bruge feltet Quick filter til at vælge den produktionsordre, du har arbejdet på.
29. I handlingsruden skal du under fanen **Produktionsordre** vælge **Start** for at åbne **Start**-dialogboksen.
30. Angiv følgende værdier under fanen **Generelt**:

    - I feltet **Fra opr.nr.** skal du vælge **10**.
    - I feltet **Til opr.nr.** skal du vælge **10**.

    ![Værdier, der er angivet under fanen Generelt](./media/subcontract23_start-dialog.png)

31. Vælg **OK** for at lukke **Start**-dialogboksen og vende tilbage til siden **Alle produktionsordrer**.

    Bemærk, at status for produktionsordren nu er **Startet**. Materialerne til operation 10 forbruges af en automatisk bogføring af pluklistekladden. Tidsforbruget for operation 10 er medtaget i en automatisk bogføring af en rutekortskladde.

32. Start lagerstedsappen for at behandle lagerstedets arbejde for operation 20.

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. I handlingsruden skal du under fanen **Produktionsordre** vælge **Start** for at åbne **Start**-dialogboksen.
34. Angiv følgende værdier under fanen **Generelt**:

    - I feltet **Fra opr.nr.** skal du vælge **20**.
    - I feltet **Til opr.nr.** skal du vælge **20**.
    - Angiv **10** i feltet **Antal**.
    - Vælg **Nej** i feltet **Bogfør plukliste nu**.

    ![Værdier, der er angivet under fanen Generelt](./media/subcontract24_general-tab.png)

35. Vælg **OK** for at lukke **Start**-dialogboksen og vende tilbage til siden **Alle produktionsordrer**.

    Der oprettes en plukliste for de materialer, der bruges til operationen Belægning og til servicevaren. Servicevaren repræsenterer omkostningerne for operationen hos underleverandøren.

36. I handlingsruden skal du under fanen **Vis** vælge **Plukliste** for at åbne siden **Plukliste**.
37. Vælg pluklisten, der ikke er bogført, og vælg derefter kladdenummeret for at få vist kladdelinjerne.

    ![Kladdelinjer på siden Plukliste](./media/subcontract25_picking-list.png)

38. I handlingsruden skal du vælge **Udskriv** \> **Plukliste (rapport)** for at åbne dialogboksen **Plukliste (rapport)**.
39. Angiv indstillingen **Brug følgeseddellayout** til **Ja**.

    ![Dialogboksen Plukliste (rapport)](./media/subcontract26_picking-list-report-dialog.png)

40. Vælg **OK** for at generere en **Plukliste**-rapport.

    I dette tilfælde udskrives en leverandørfølgeseddel fra pluklistekladden for produktionen. Følgeseddelen angiver de materialer, der leveres til den leverandør, der udfører belægningsoperationen.

    ![Plukliste (rapport)](./media/subcontract27_picking-list-report.png)

41. Luk **Plukliste**-rapporten for at vende tilbage til siden **Plukliste**.
42. I handlingsruden skal du vælge **Bogfør** for at åbne **Bogfør kladde**-dialogboksen.

    ![Dialogboksen Bogfør kladde](./media/subcontract28_post-journal-dialog.png)

43. Vælg **OK** for at lukke dialogboksen **Bogfør kladde**.
44. Åbn indkøbsordren

    ![Siden Indkøbsordre](./media/subcontract29_purchase-order-page.png)

45. I handlingsruden under fanen **Indkøb** skal du vælge **Bekræft**.
46. Vælg **Bogfør** for at åbne dialogboksen **Bogfør kladde**.
47. Vælg **OK** for at lukke **Bogfør kladde**-dialogboksen og vende tilbage til siden **Indkøbsordre**.
48. Skift enhedspris fra **33** til **40**.

    ![Enhedspris, der er ændret på siden Indkøbsordre](./media/subcontract30_unit-price.png)

49. Bekræft indkøbsordren igen.
50. Produktkvittering.

    ![Dialogboksen Konterer produktkvittering](./media/subcontract31_posting-product-receipt-dialog.png)

51. Indkøbsfaktura.
52. Opdater status for sammenholdelse.

    ![Siden Kreditorfaktura](./media/subcontract32_vendor-invoice-page.png)

53. Færdigmelding.

    ![Dialogboksen Færdigmelding](./media/subcontract33_report-as-finished-dialog.png)

54. Slut.

    ![Dialogboksen Slut](./media/subcontract34_end-dialog.png)

55. Omkostningssammenligning.

    ![Sammenligningsdiagrammer for omkostning](./media/subcontract35_cost-comparison-charts.png)

Manglende opsætning i data.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]