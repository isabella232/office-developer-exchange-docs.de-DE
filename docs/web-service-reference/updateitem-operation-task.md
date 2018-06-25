---
title: UpdateItem-Vorgang (Aufgabe)
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
description: Der Vorgang UpdateItem wird verwendet, um Eigenschaften für Aufgabenelemente im Exchange-Speicher zu aktualisieren.
ms.openlocfilehash: d6f966fa663300b476383a136d30cf611d6bfb9b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839376"
---
# <a name="updateitem-operation-task"></a><span data-ttu-id="40ad2-103">UpdateItem-Vorgang (Aufgabe)</span><span class="sxs-lookup"><span data-stu-id="40ad2-103">UpdateItem operation (task)</span></span>

<span data-ttu-id="40ad2-104">Der Vorgang UpdateItem wird verwendet, um Eigenschaften für Aufgabenelemente im Exchange-Speicher zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="40ad2-104">The UpdateItem operation is used to update task item properties in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40ad2-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40ad2-105">Remarks</span></span>

<span data-ttu-id="40ad2-106">Sie können Exchange-Webdienste Aufgabenanfragen senden.</span><span class="sxs-lookup"><span data-stu-id="40ad2-106">You cannot use Exchange Web Services to send task requests.</span></span> <span data-ttu-id="40ad2-107">Exchange-Webdienste können Aufgabenanfragen zurückzugeben, die vom MicrosoftOfficeOutlook erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="40ad2-107">Exchange Web Services can return task requests that are created by MicrosoftOfficeOutlook.</span></span> <span data-ttu-id="40ad2-108">Wenn bereits eine Aufgabenanfrage gesendet wurde, wird eine Anforderung zum Aktualisieren der Aufgabe einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="40ad2-108">If a task request has already been sent, a request to update the task will return an error.</span></span>
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a><span data-ttu-id="40ad2-109">Aktualisieren das aktuelle Vorkommen einer wiederkehrenden Aufgabe</span><span class="sxs-lookup"><span data-stu-id="40ad2-109">Updating the Current Occurrence of a Recurring Task</span></span>

<span data-ttu-id="40ad2-110">Das Ergebnis einer UpdateItem Operation für wiederkehrende Aufgaben unterscheidet sich von das Ergebnis des Vorgangs UpdateItem für einen einzelnen, einer einmaligen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="40ad2-110">The result of an UpdateItem operation on recurring tasks differs from the result of the UpdateItem operation on a single, nonrecurring task.</span></span> <span data-ttu-id="40ad2-111">Änderungen an einem Vorkommen einer Aufgabenserie verursachen einmalige Aufgaben generiert werden soll, wenn die folgenden Updates vorgenommen werden:</span><span class="sxs-lookup"><span data-stu-id="40ad2-111">Changes to an occurrence of a recurring task cause one-off tasks to be generated when the following updates are made:</span></span>
  
1. <span data-ttu-id="40ad2-112">Die Statuseigenschaft des einer wiederkehrenden Aufgabe erzeugt oder nonregenerating wird auf **abgeschlossen**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="40ad2-112">The status property of a regenerating or nonregenerating recurrent task is set to **Completed**.</span></span>
    
2. <span data-ttu-id="40ad2-113">Das Start- oder Enddatum des einer nonregenerating wiederkehrenden Aufgabe geändert wird.</span><span class="sxs-lookup"><span data-stu-id="40ad2-113">The start date or end date of a nonregenerating recurrent task is changed.</span></span>
    
<span data-ttu-id="40ad2-114">Beispielsweise, wenn eine Anforderung **UpdateItem** den abgeschlossen-Wert, der einen sich wiederholenden Vorgang auf **true**festgelegt wird, muss die **UpdateItemResponse** enthalten, eine neue-Id und ChangeKey, die einen neu erstellten einmaligen Vorgang darstellen.</span><span class="sxs-lookup"><span data-stu-id="40ad2-114">For example, if an **UpdateItem** request sets the Completed value of a recurring task to **true**, the **UpdateItemResponse** will include a new Id and ChangeKey that represent a newly created one-off task.</span></span> <span data-ttu-id="40ad2-115">Die Id, die in der Anforderung enthalten war noch gültig ist, und die Aufgabenserie, die durch diese Id dargestellt ist wurde aktualisiert, um das nächste Vorkommen darstellen.</span><span class="sxs-lookup"><span data-stu-id="40ad2-115">The Id that was included in the request is still valid and the recurring task that is represented by that Id has been updated to represent the next occurrence.</span></span> <span data-ttu-id="40ad2-116">Die ChangeKey, die in der Anforderung enthalten war ist nicht mehr gültig, da sich wiederholenden Vorgang aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="40ad2-116">The ChangeKey that was included in the request is no longer valid because the recurring task has been updated.</span></span> 
  
<span data-ttu-id="40ad2-117">Die [GetItem-Vorgang](getitem-operation.md) können Sie um die neuesten **ChangeKey** für die sich wiederholenden Vorgang zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="40ad2-117">You can use the [GetItem operation](getitem-operation.md) to get the latest **ChangeKey** for the recurring task.</span></span> 
  
<span data-ttu-id="40ad2-118">Für einen einzelnen Aufgaben oder für das letzte Vorkommen einer Aufgabenserie, gibt die Antwort UpdateItem dieselbe **Id** , die es übergeben wurde, und gibt Sie zurück, dass der zugeordnete **ChangeKey**aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="40ad2-118">For nonrecurring tasks or for the last occurrence of a recurring task, the UpdateItem response returns the same **Id** that was passed to it and returns the associated updated **ChangeKey**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40ad2-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40ad2-119">See also</span></span>



[<span data-ttu-id="40ad2-120">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="40ad2-120">UpdateItem operation</span></span>](updateitem-operation.md)

