---
title: UpdateItem-Vorgang (Vorgang)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: Der UpdateItem-Vorgang wird zum Aktualisieren von Aufgabenelementeigenschaften in der Exchange-Informationsspeicher verwendet.
ms.openlocfilehash: 0041af114d11fd9577037dd154e40b84e8483c35
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459805"
---
# <a name="updateitem-operation-task"></a><span data-ttu-id="30231-103">UpdateItem-Vorgang (Vorgang)</span><span class="sxs-lookup"><span data-stu-id="30231-103">UpdateItem operation (task)</span></span>

<span data-ttu-id="30231-104">Der UpdateItem-Vorgang wird zum Aktualisieren von Aufgabenelementeigenschaften in der Exchange-Informationsspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="30231-104">The UpdateItem operation is used to update task item properties in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30231-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30231-105">Remarks</span></span>

<span data-ttu-id="30231-106">Sie können keine Aufgabenanforderungen mithilfe von Exchange Webdienste senden.</span><span class="sxs-lookup"><span data-stu-id="30231-106">You cannot use Exchange Web Services to send task requests.</span></span> <span data-ttu-id="30231-107">Exchange Webdienste kann Aufgabenanforderungen zurückgeben, die von MicrosoftOfficeOutlook erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="30231-107">Exchange Web Services can return task requests that are created by MicrosoftOfficeOutlook.</span></span> <span data-ttu-id="30231-108">Wenn bereits eine Aufgabenanfrage gesendet wurde, gibt eine Anforderung zum Aktualisieren der Aufgabe einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="30231-108">If a task request has already been sent, a request to update the task will return an error.</span></span>
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a><span data-ttu-id="30231-109">Aktualisieren des aktuellen Vorkommens einer wiederkehrenden Aufgabe</span><span class="sxs-lookup"><span data-stu-id="30231-109">Updating the Current Occurrence of a Recurring Task</span></span>

<span data-ttu-id="30231-110">Das Ergebnis einer UpdateItem-Operation bei wiederkehrenden Vorgängen unterscheidet sich vom Ergebnis des UpdateItem-Vorgangs für einen einzelnen, nicht wiederkehrenden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="30231-110">The result of an UpdateItem operation on recurring tasks differs from the result of the UpdateItem operation on a single, nonrecurring task.</span></span> <span data-ttu-id="30231-111">Änderungen an einem Vorkommen einer wiederkehrenden Aufgabe führen dazu, dass einmalige Vorgänge generiert werden, wenn die folgenden Updates vorgenommen werden:</span><span class="sxs-lookup"><span data-stu-id="30231-111">Changes to an occurrence of a recurring task cause one-off tasks to be generated when the following updates are made:</span></span>
  
1. <span data-ttu-id="30231-112">Die Status-Eigenschaft eines regenerierenden oder nonregenerating wiederkehrenden Tasks wird auf **Completed**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="30231-112">The status property of a regenerating or nonregenerating recurrent task is set to **Completed**.</span></span>
    
2. <span data-ttu-id="30231-113">Das Startdatum oder das Enddatum eines wiederkehrenden nonregenerating-Vorgangs wird geändert.</span><span class="sxs-lookup"><span data-stu-id="30231-113">The start date or end date of a nonregenerating recurrent task is changed.</span></span>
    
<span data-ttu-id="30231-114">Wenn beispielsweise eine **UpdateItem** -Anforderung den completed-Wert einer wiederkehrenden Aufgabe auf **true**festgelegt wird, enthält die **UpdateItemResponse** eine neue ID und ChangeKey, die eine neu erstellte einmalige Aufgabe darstellen.</span><span class="sxs-lookup"><span data-stu-id="30231-114">For example, if an **UpdateItem** request sets the Completed value of a recurring task to **true**, the **UpdateItemResponse** will include a new Id and ChangeKey that represent a newly created one-off task.</span></span> <span data-ttu-id="30231-115">Die in der Anforderung enthaltene ID ist weiterhin gültig, und die wiederkehrende Aufgabe, die durch diese ID dargestellt wird, wurde aktualisiert und stellt das nächste Vorkommen dar.</span><span class="sxs-lookup"><span data-stu-id="30231-115">The Id that was included in the request is still valid and the recurring task that is represented by that Id has been updated to represent the next occurrence.</span></span> <span data-ttu-id="30231-116">Die in der Anforderung enthaltene ChangeKey ist nicht mehr gültig, da die wiederkehrende Aufgabe aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="30231-116">The ChangeKey that was included in the request is no longer valid because the recurring task has been updated.</span></span> 
  
<span data-ttu-id="30231-117">Sie können den [GetItem-Vorgang](getitem-operation.md) verwenden, um die neuesten **ChangeKey** für den wiederkehrenden Vorgang abzurufen.</span><span class="sxs-lookup"><span data-stu-id="30231-117">You can use the [GetItem operation](getitem-operation.md) to get the latest **ChangeKey** for the recurring task.</span></span> 
  
<span data-ttu-id="30231-118">Bei nicht wiederkehrenden Vorgängen oder beim letzten Auftreten einer wiederkehrenden Aufgabe gibt die UpdateItem-Antwort dieselbe **ID** zurück, die an Sie übergeben wurde, und gibt die zugeordnete aktualisierte **ChangeKey**zurück.</span><span class="sxs-lookup"><span data-stu-id="30231-118">For nonrecurring tasks or for the last occurrence of a recurring task, the UpdateItem response returns the same **Id** that was passed to it and returns the associated updated **ChangeKey**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30231-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30231-119">See also</span></span>



[<span data-ttu-id="30231-120">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="30231-120">UpdateItem operation</span></span>](updateitem-operation.md)

