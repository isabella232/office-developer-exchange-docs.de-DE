---
title: CreateItem-Vorgang (Aufgabe)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 12c5da4d-290c-4a8a-a965-0bf5d55c7978
description: Der CreateItem-Vorgang erstellt Aufgabenelemente in der Exchange-Informationsspeicher.
ms.openlocfilehash: 502108843193e7ed8377b0fade9e106ef3d1976c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457102"
---
# <a name="createitem-operation-task"></a><span data-ttu-id="51eb4-103">CreateItem-Vorgang (Aufgabe)</span><span class="sxs-lookup"><span data-stu-id="51eb4-103">CreateItem operation (task)</span></span>

<span data-ttu-id="51eb4-104">Der CreateItem-Vorgang erstellt Aufgabenelemente in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="51eb4-104">The CreateItem operation creates task items in the Exchange store.</span></span>
  
## <a name="task-createitem-request"></a><span data-ttu-id="51eb4-105">Aufgaben-CreateItem-Anforderung</span><span class="sxs-lookup"><span data-stu-id="51eb4-105">Task CreateItem Request</span></span>

### <a name="description"></a><span data-ttu-id="51eb4-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51eb4-106">Description</span></span>

<span data-ttu-id="51eb4-107">Im folgenden Beispiel einer CreateItem-Anforderung wird gezeigt, wie ein Aufgabenelement in einem Postfach erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="51eb4-107">The following example of a CreateItem request shows how to create a task item in a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="51eb4-108">Code</span><span class="sxs-lookup"><span data-stu-id="51eb4-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                MessageDisposition="SaveOnly">
      <Items>
        <t:Task>
          <t:Subject>My task</t:Subject>
          <t:DueDate>2006-10-26T21:32:52</t:DueDate>
          <t:Status>NotStarted</t:Status>
        </t:Task>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="51eb4-109">Comments</span><span class="sxs-lookup"><span data-stu-id="51eb4-109">Comments</span></span>

<span data-ttu-id="51eb4-110">Anforderungen für wiederkehrende Aufgaben werden geändert, wenn Sie von dem Computer empfangen werden, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="51eb4-110">Requests for recurring tasks are altered when they are received by the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span> <span data-ttu-id="51eb4-111">Die folgenden Änderungen treten auf:</span><span class="sxs-lookup"><span data-stu-id="51eb4-111">The following changes occur:</span></span>
  
- <span data-ttu-id="51eb4-112">Nur das Datum wird für die StartDate-Eigenschaft [(Serie)](startdate-recurrence.md) des Serien Bereichs des Vorgangs gespeichert.</span><span class="sxs-lookup"><span data-stu-id="51eb4-112">Only the date is saved for the [StartDate (Recurrence)](startdate-recurrence.md) property of the recurrence range of the task.</span></span> <span data-ttu-id="51eb4-113">Der Zeitbereich wird abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="51eb4-113">The time part is truncated.</span></span> 
    
- <span data-ttu-id="51eb4-114">Die [StartDate-Eigenschaft (Serie)](startdate-recurrence.md) kann abhängig vom Serienmuster angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="51eb4-114">The [StartDate (Recurrence)](startdate-recurrence.md) property may be adjusted, depending on the recurrence pattern.</span></span> <span data-ttu-id="51eb4-115">Wenn beispielsweise das Serienmuster jeden Montag angegeben wird und das Startwert auf den 26. Oktober 2006 festgelegt ist, was ein Donnerstag ist, wird StartDate auf den 30. Oktober 2006 eingestellt, was der nächste Montag ist.</span><span class="sxs-lookup"><span data-stu-id="51eb4-115">For example, if the recurrence pattern is specified as every Monday and the StartDate is set to October 26, 2006, which is a Thursday, StartDate is adjusted to October 30, 2006, which is the next Monday.</span></span> 
    
- <span data-ttu-id="51eb4-116">Wenn die [StartDate](startdate.md) -Eigenschaft des Vorgangs festgelegt ist, wird Sie entsprechend der [StartDate (Serie)](startdate-recurrence.md) des Serien Bereichs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="51eb4-116">If the [StartDate](startdate.md) property of the task is set, it is updated to match the [StartDate (Recurrence)](startdate-recurrence.md) of the recurrence range.</span></span> <span data-ttu-id="51eb4-117">Die [DueDate](duedate.md) -Eigenschaft des Tasks wird auch basierend auf dem neuen [StartDate](startdate.md)aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="51eb4-117">The [DueDate](duedate.md) property of the task is also updated based on the new [StartDate](startdate.md).</span></span>
    
- <span data-ttu-id="51eb4-118">Wenn das [Startwert nicht](startdate.md) festgelegt ist, wird nur die [DueDate](duedate.md) -Eigenschaft so aktualisiert, dass Sie der [StartDate (Serie)](startdate-recurrence.md) des Serien Bereichs entspricht.</span><span class="sxs-lookup"><span data-stu-id="51eb4-118">If the [StartDate](startdate.md) is not set, only the [DueDate](duedate.md) property is updated to match the [StartDate (Recurrence)](startdate-recurrence.md) of the recurrence range.</span></span> 
    
<span data-ttu-id="51eb4-119">In der folgenden Tabelle sind die Änderungen aufgeführt, die der Client Zugriffsserver für eine wiederkehrende Aufgabe vornimmt, die ein Task. Serie. Pattern jedes montags aufweist.</span><span class="sxs-lookup"><span data-stu-id="51eb4-119">The following table shows the changes that the Client Access server makes to a recurring task that has a Task.Recurrence.Pattern of every Monday.</span></span>
  
<span data-ttu-id="51eb4-120">**Änderungen an einer wiederkehrenden Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="51eb4-120">**Changes to a recurring task**</span></span>

|<span data-ttu-id="51eb4-121">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="51eb4-121">**Property**</span></span>|<span data-ttu-id="51eb4-122">**Ursprünglicher Wert**</span><span class="sxs-lookup"><span data-stu-id="51eb4-122">**Original Value**</span></span>|<span data-ttu-id="51eb4-123">**Aktualisierter Wert**</span><span class="sxs-lookup"><span data-stu-id="51eb4-123">**Updated Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="51eb4-124">Task. StartDate</span><span class="sxs-lookup"><span data-stu-id="51eb4-124">Task.StartDate</span></span>  <br/> |<span data-ttu-id="51eb4-125">1. Januar 2006</span><span class="sxs-lookup"><span data-stu-id="51eb4-125">January 1, 2006</span></span>  <br/> |<span data-ttu-id="51eb4-126">30. Oktober 2006</span><span class="sxs-lookup"><span data-stu-id="51eb4-126">October 30, 2006</span></span>  <br/> |
|<span data-ttu-id="51eb4-127">Task. DueDate</span><span class="sxs-lookup"><span data-stu-id="51eb4-127">Task.DueDate</span></span>  <br/> |<span data-ttu-id="51eb4-128">3. Januar 2006</span><span class="sxs-lookup"><span data-stu-id="51eb4-128">January 3, 2006</span></span>  <br/> |<span data-ttu-id="51eb4-129">1. November 2006</span><span class="sxs-lookup"><span data-stu-id="51eb4-129">November 1, 2006</span></span>  <br/> |
|<span data-ttu-id="51eb4-130">Task. Serie. Range. StartDate</span><span class="sxs-lookup"><span data-stu-id="51eb4-130">Task.Recurrence.Range.StartDate</span></span>  <br/> |<span data-ttu-id="51eb4-131">26. Oktober 2006</span><span class="sxs-lookup"><span data-stu-id="51eb4-131">October 26, 2006</span></span>  <br/> |<span data-ttu-id="51eb4-132">30. Oktober 2006</span><span class="sxs-lookup"><span data-stu-id="51eb4-132">October 30, 2006</span></span>  <br/> |
   
<span data-ttu-id="51eb4-133">Wenn ein Zielordner nicht angegeben ist, werden die Aufgabenelemente standardmäßig im Ordner Aufgaben erstellt.</span><span class="sxs-lookup"><span data-stu-id="51eb4-133">By default, if a destination folder is not specified, task items are created in the Tasks folder.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="51eb4-134">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="51eb4-134">Request elements</span></span>

<span data-ttu-id="51eb4-135">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="51eb4-135">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="51eb4-136">CreateItem</span><span class="sxs-lookup"><span data-stu-id="51eb4-136">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="51eb4-137">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="51eb4-137">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="51eb4-138">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="51eb4-138">Task</span></span>](task.md)
    
- [<span data-ttu-id="51eb4-139">Betreff</span><span class="sxs-lookup"><span data-stu-id="51eb4-139">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="51eb4-140">DueDate</span><span class="sxs-lookup"><span data-stu-id="51eb4-140">DueDate</span></span>](duedate.md)
    
- [<span data-ttu-id="51eb4-141">Status</span><span class="sxs-lookup"><span data-stu-id="51eb4-141">Status</span></span>](status.md)
    
## <a name="successful-task-createitem-response"></a><span data-ttu-id="51eb4-142">Erfolgreiche Aufgabe CreateItem-Antwort</span><span class="sxs-lookup"><span data-stu-id="51eb4-142">Successful Task CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="51eb4-143">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51eb4-143">Description</span></span>

<span data-ttu-id="51eb4-144">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="51eb4-144">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="51eb4-145">Code</span><span class="sxs-lookup"><span data-stu-id="51eb4-145">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Task>
              <t:ItemId Id="AAAtAE=" ChangeKey="EwAAABYA"/>
            </t:Task>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="51eb4-146">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="51eb4-146">Successful response elements</span></span>

<span data-ttu-id="51eb4-147">Die Antwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="51eb4-147">The following elements are included in the response:</span></span>
  
- [<span data-ttu-id="51eb4-148">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="51eb4-148">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="51eb4-149">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="51eb4-149">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="51eb4-150">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="51eb4-150">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="51eb4-151">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="51eb4-151">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="51eb4-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="51eb4-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="51eb4-153">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="51eb4-153">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="51eb4-154">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="51eb4-154">Task</span></span>](task.md)
    
- [<span data-ttu-id="51eb4-155">ItemId</span><span class="sxs-lookup"><span data-stu-id="51eb4-155">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="51eb4-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51eb4-156">See also</span></span>



[<span data-ttu-id="51eb4-157">CreateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="51eb4-157">CreateItem operation</span></span>](createitem-operation.md)


[<span data-ttu-id="51eb4-158">Erstellen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="51eb4-158">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="51eb4-159">Aktualisieren von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="51eb4-159">Updating Tasks</span></span>](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[<span data-ttu-id="51eb4-160">Deleting Tasks</span><span class="sxs-lookup"><span data-stu-id="51eb4-160">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

