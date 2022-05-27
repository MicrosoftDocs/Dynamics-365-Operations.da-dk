---
title: Definere revisionspolitikker for kildedokumenter
description: Dette emne viser, hvordan du kan konfigurere og køre regler for overvågningspolitik.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8698dd2c14321498d23efe1d01be274c56d5721
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713776"
---
# <a name="define-audit-policies-for-source-documents"></a>Definere revisionspolitikker for kildedokumenter

[!include [banner](../../includes/banner.md)]

Dette emne viser, hvordan du kan konfigurere og køre regler for overvågningspolitik. I eksemplet bruges udgiftsrapporter med udgiftstypen hotel. Denne procedure bruger demofirmaet USMF. Rollen revisor indeholder de korrekte tilladelser til at kunne udføre disse opgaver.

1. Gå i navigationsruden til **Moduler > Revisionspanel > Opsætning > Regeltype**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Regelnavn**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Vælg **Udgiftsrapportlinje** i feltet **Forespørgselsnavn**.
6. Vælg **Aggreger** i Feltet **Forespørgselstype**.
7. Vælg **Juridisk enhed** i feltet **Juridisk enhed**.
8. Vælg **Dato og klokkeslæt for ændring** i feltet **Dokumentdatohenvisning**.
9. Vælg **Gem**.
10. Gå i navigationsruden til **Moduler > Revisionspanel > Opsætning > Overvågningspolitikker**.
11. Vælg **Ny**.
12. Skriv en værdi i feltet **Navn**.
13. Udvid sektionen **Regelstyrede organisationer**.
14. Vælg **Contoso Entertainment System USA** i træet, og vælg derefter **Tilføj**.
15. Vælg **Contoso Consulting USA** i træet, og vælg derefter **Tilføj**.
16. Vælg **Contoso Retail USA** i træet, og vælg derefter **Tilføj**.
17. Skjul sektionen **Regelstyrede organisationer**.
18. Udvid sektionen **Regler**.
19. Find og vælg den Politikregel, som blev oprettet tidligere, på listen.
20. Vælg **Opret politikregel**.
21. Angiv en dato og et klokkeslæt i feltet **Ikrafttrædelsesdato**.
22. Vælg **Filter**.
23. Vælg rækken for **Udgiftsart** på listen, og angiv detaljerne til **Hotel**.
24. Indtast eller vælg en værdi i feltet **Kriterier**.
25. Vælg fanen **Aggregering**.
26. Vælg **Tilføj**.
27. Vælg feltværdien **Transaktionsbeløb** på listen.
28. Indtast eller vælg en værdi i feltet **Felt**.
29. Vælg **Sum** i feltet **Aggregeringsfunktion**.
30. Vælg fanen **Sammenlæg pr.**
31. Vælg **Tilføj**.
32. Vælg værdien af **Medarbejder** på listen.
33. Vælg **Tilføj**.
34. Vælg værdien af **Udgiftsart** på listen.
35. Indtast eller vælg en værdi i feltet **Felt**.
36. Vælg fanen **Har**.
37. Vælg **Tilføj**.
38. Vælg **Transaktionsbeløb**.
39. Indtast eller vælg en værdi i feltet **Felt**.
40. Vælg **Sum** i feltet **Aggregeringsfunktion**.
41. Skriv `>2000` i feltet **Kriterier**.
42. Vælg **OK**.
43. Vælg **Test**.
44. Angiv en dato og klokkeslæt i feltet **Startdato for dokumentudvælgelse**.
45. Angiv en dato og klokkeslæt i feltet **Slutdato for dokumentudvælgelse**.
46. Vælg **Kør test**.
47. Vælg **Overvågningspolitik** i handlingsruden.
48. Vælge **Flere indstillinger**.
49. Angiv en dato og et klokkeslæt i feltet **Startdato**.
50. Angiv en dato og et klokkeslæt i feltet **Slutdato**.
51. Vælg **Batch**.
52. Udvid sektionen **Kør i baggrunden**.
53. Vælg **Ja** i feltet **Batchbehandling**.
54. Vælg **OK**.
55. Gå i navigationsruden til **Moduler > Revisionspanel > Overvåg sager**.
56. Find og vælg den ønskede post på listen.
57. Udvid sektionen **Tilknytninger**.
58. Find og vælg den ønskede post på listen.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
