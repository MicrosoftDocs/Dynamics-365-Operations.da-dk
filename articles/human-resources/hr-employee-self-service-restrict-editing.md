---
title: Begrænse redigering af personlige oplysninger
description: Begrænse medarbejdere i at redigere kontaktoplysninger i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e43b9127b247fa618558b725837d12bf290662f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052019"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="700e2-103">Begrænse redigering af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="700e2-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="700e2-104">Dette emne beskriver, hvordan du begrænser medarbejdernes mulighed for at redigere kontaktoplysninger i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="700e2-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="700e2-105">Du kan f.eks. forhindre medarbejdere i at redigere bestemte kontaktoplysninger, f.eks. deres firmaadresse eller mailadresse.</span><span class="sxs-lookup"><span data-stu-id="700e2-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="700e2-106">Hvis du vil bruge denne funktion, skal du først aktivere **(Forhåndsversion) Begrænse medarbejdere i at tilføje eller redigere adresse- og kontaktoplysninger til udvalgte formål** i Funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="700e2-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="700e2-107">Du kan finde flere oplysninger om aktivering af prøveversionsfunktioner i [Administrere funktioner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="700e2-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="700e2-108">![Aktivér visningsfunktion](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="700e2-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="700e2-109">Vælge de oplysninger, som en medarbejder kan tilføje eller redigere</span><span class="sxs-lookup"><span data-stu-id="700e2-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="700e2-110">I Human Resources skal du vælge **Personalestyring**, vælge **Links** og derefter vælge **Human Resources-parametre**.</span><span class="sxs-lookup"><span data-stu-id="700e2-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Gå til Personaleparametre](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="700e2-112">Vælg fanen **Medarbejderselvbetjening** på siden **Personaleparametre**.</span><span class="sxs-lookup"><span data-stu-id="700e2-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Medarbejderselvbetjening](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="700e2-114">Under fanen **Medarbejderselvbetjening** skal du fjerne markeringen af alle oplysninger i afsnittet **Adresse- og kontaktoplysninger**, som du ikke ønsker, at medarbejdere skal tilføje eller redigere.</span><span class="sxs-lookup"><span data-stu-id="700e2-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="700e2-115">I dette eksempel har vi ikke markeret **Forretningskontaktoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="700e2-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![Begrænse redigeringen af forretningskontaktoplysninger](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="700e2-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="700e2-117">Select **Save**.</span></span>

   ![Gem ændringer](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="700e2-119">Medarbejdererfaring</span><span class="sxs-lookup"><span data-stu-id="700e2-119">Employee experience</span></span>

<span data-ttu-id="700e2-120">Når du har begrænset medarbejdernes adgang til at tilføje eller redigere kontaktoplysninger, kan de se oplysningerne, men de kan ikke ændre dem.</span><span class="sxs-lookup"><span data-stu-id="700e2-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="700e2-121">I dette eksempel, hvor medarbejdere ikke kan redigere **forretningskontaktoplysninger**, kan de stadig se oplysningerne i Medarbejderselvbetjening:</span><span class="sxs-lookup"><span data-stu-id="700e2-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![Se forretningskontaktoplysninger](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="700e2-123">Men når de vælger forretningskontaktoplysninger, vises ruden **Rediger adresse** som skrivebeskyttet, og de kan ikke ændre nogen af felterne.</span><span class="sxs-lookup"><span data-stu-id="700e2-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![Forretningskontaktoplysninger vises som skrivebeskyttede](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="700e2-125">Hvis de vælger **Tilføj** for at tilføje en ny adresse, kan de heller ikke vælge **Forretning** på rullelisten **Formål**.</span><span class="sxs-lookup"><span data-stu-id="700e2-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Medarbejderen kan ikke tilføje en forretningsadresse](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="700e2-127">Medarbejdere får samme erfaring, når de vælger **Kontaktoplysninger** på siden **Personlige oplysninger** og tilføjer en ny adresse.</span><span class="sxs-lookup"><span data-stu-id="700e2-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="700e2-128">På rullelisten **Formål** vises kun de typer oplysninger, de kan tilføje.</span><span class="sxs-lookup"><span data-stu-id="700e2-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Medarbejderen kan ikke vælge Forretning på rullelisten Formål](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="700e2-130">**Kontaktoplysninger** viser nu **Formål** i gitteret.</span><span class="sxs-lookup"><span data-stu-id="700e2-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![Formål vises i gitteret Kontaktoplysninger](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="700e2-132">Se også</span><span class="sxs-lookup"><span data-stu-id="700e2-132">See also</span></span>

[<span data-ttu-id="700e2-133">Oversigt over medarbejder- og lederselvbetjening</span><span class="sxs-lookup"><span data-stu-id="700e2-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="700e2-134">Konfigurere Human Resources-parametre</span><span class="sxs-lookup"><span data-stu-id="700e2-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="700e2-135">Rediger personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="700e2-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)