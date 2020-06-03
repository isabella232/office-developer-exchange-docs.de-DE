---
title: Überprüfen der Ergebnisse eines EWS- oder verwalteten EWS-API-Aufrufs
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: 78a1741c-1bbe-4cb4-9331-9d6d3171fc11
description: Erfahren Sie, wie Sie die Ergebnisse ihrer EWS-oder verwaltete EWS-API-Anrufe überprüfen können.
localization_priority: Priority
ms.openlocfilehash: be8e76898dd111a6dec33d4a57d9d50a2a935390
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457396"
---
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a><span data-ttu-id="4f304-103">Überprüfen der Ergebnisse eines EWS- oder verwalteten EWS-API-Aufrufs</span><span class="sxs-lookup"><span data-stu-id="4f304-103">Verifying the results of an EWS or EWS Managed API call</span></span>

<span data-ttu-id="4f304-104">Erfahren Sie, wie Sie die Ergebnisse ihrer EWS-oder verwaltete EWS-API-Anrufe überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="4f304-104">Learn how to verify the results of your EWS or EWS Managed API calls.</span></span>
  
<span data-ttu-id="4f304-105">Wenn die Dinge nicht ordnungsgemäß funktionieren, können Sie sehen, was passiert, indem Sie die SOAP-Anforderungen untersuchen, die Ihre Anwendung über das Netzwerk sendet, und die Antworten, die der Server zurücksendet.</span><span class="sxs-lookup"><span data-stu-id="4f304-105">When things aren't working correctly, it helps to see what's going on by examining the SOAP requests that your application is sending over the network and the responses that the server is sending back.</span></span> <span data-ttu-id="4f304-106">Der Artikel [Tools und Ressourcen für die Problembehandlung für EWS-Anwendungen](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) enthält Links zu Tools, mit denen Sie diese SOAP-Anforderungen erfassen und anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="4f304-106">The [tools and resources for troubleshooting EWS applications](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) article includes links to tools to help capture and view those SOAP requests.</span></span> <span data-ttu-id="4f304-107">Wie stellen Sie sicher, dass die an den Server gesendete Anforderung ordnungsgemäß verarbeitet wurde, nachdem Sie die Anforderungen und Antworten erhalten haben?</span><span class="sxs-lookup"><span data-stu-id="4f304-107">After you've got the requests and the responses, how do you verify that the request you sent to the server was processed correctly?</span></span> <span data-ttu-id="4f304-108">Lesen Sie weiter, um es herauszufinden.</span><span class="sxs-lookup"><span data-stu-id="4f304-108">Read on to find out.</span></span> 
  
<span data-ttu-id="4f304-109">Wenn Sie EWS-Anforderungen senden, werden Sie mit der Überprüfung beginnen, indem Sie das **ResponseClass** -Attribut für jede Antwortnachricht in der Antwort überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4f304-109">If you're sending EWS requests, you're going to start your verification by checking the **ResponseClass** attribute for each response message in the response.</span></span> <span data-ttu-id="4f304-110">Dadurch erfahren Sie, ob der Vorgang für jedes Element erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4f304-110">That will tell you whether the operation completed successfully on each item.</span></span> 
  
<span data-ttu-id="4f304-111">Abhängig vom Objekt, das von der Methode aufgerufen wird, können Sie, wenn Sie die verwaltete EWS-API zum Senden von Anforderungen verwenden, einige Überprüfungen mithilfe der Response-Objekte durchführen.</span><span class="sxs-lookup"><span data-stu-id="4f304-111">Depending on the object that your method is calling, if you're using the EWS Managed API to send requests, you can do some verification using the response objects.</span></span> <span data-ttu-id="4f304-112">Da die SOAP-Antwort jedoch eine Obermenge dessen enthält, was in den verwaltete EWS-API-Antwort Objekten enthalten ist, sollten Sie sich auch die SOAP-Antwort ansehen.</span><span class="sxs-lookup"><span data-stu-id="4f304-112">But because the SOAP response contains a superset of what's included in the EWS Managed API response objects, you might want to look at the SOAP response as well.</span></span> <span data-ttu-id="4f304-113">Da die SOAP-Antwort häufig mehr Informationen als die verwaltete EWS-API-Antwortobjekte enthalten kann, starten Sie die Überprüfung mit der SOAP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="4f304-113">Because the SOAP response can often contain more information than the EWS Managed API response objects, start your verification with the SOAP response.</span></span>
  
## <a name="verifying-the-results-of-a-soap-response"></a><span data-ttu-id="4f304-114">Überprüfen der Ergebnisse einer SOAP-Antwort</span><span class="sxs-lookup"><span data-stu-id="4f304-114">Verifying the results of a SOAP response</span></span>
<span data-ttu-id="4f304-115"><a name="bk_verifysoap"> </a></span><span class="sxs-lookup"><span data-stu-id="4f304-115"><a name="bk_verifysoap"> </a></span></span>

<span data-ttu-id="4f304-116">Wenn Sie eine SOAP-Antwort erhalten, ist das **ResponseClass** -Attribut das erste, was Sie beachten sollten.</span><span class="sxs-lookup"><span data-stu-id="4f304-116">When you receive a SOAP response, the first thing to look at is the **ResponseClass** attribute.</span></span> <span data-ttu-id="4f304-117">Dieses Attribut ist in jeder **ResponseMessageType** -Instanz im [ResponseMessages](https://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) -Element enthalten, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4f304-117">This attribute is included in each **ResponseMessageType** instance in the [ResponseMessages](https://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) element, as shown in the following example.</span></span> 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

<span data-ttu-id="4f304-118">Da eine SOAP-Antwort möglicherweise mehrere Antwortnachrichten in einer einzigen SOAP-Antwort enthalten kann, ist es wichtig, jede Antwortnachricht einzeln zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4f304-118">Because a SOAP response might contain multiple response messages in a single SOAP response, it's important to check each response message individually.</span></span>
  
<span data-ttu-id="4f304-119">Wenn Sie mit einer Operation arbeiten, die ein **ResponseClass** -Element als Teil der Vorgangs Antwort enthält, wie im folgenden Beispiel, könnten Sie versucht sein, die **ResponseClass** des Vorgangs nur zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4f304-119">If you're working with an operation that includes a **ResponseClass** as part of the operation response, like the following, you might be tempted to only check the **ResponseClass** of the operation.</span></span> 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

<span data-ttu-id="4f304-120">Der Vorgangsstatus gibt jedoch nur die Form der Antwort auf oberster Ebene wieder und gibt nicht den Status aller einzelnen Nachrichten Antworten an.</span><span class="sxs-lookup"><span data-stu-id="4f304-120">However, the operation status only reflects the shape of the top-level response and does not reflect the status of all the individual message responses.</span></span> <span data-ttu-id="4f304-121">Im folgenden Beispiel weist der [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) -Vorgang ein **ResponseClass** **auf, aber**das zugrunde liegende [DelegateUserResponseMessageType](https://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) -Element weist den **ResponseClass** -Wert **Error**auf.</span><span class="sxs-lookup"><span data-stu-id="4f304-121">In the following example, the [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) operation has a **ResponseClass** of **Success**, but the underlying [DelegateUserResponseMessageType](https://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) element has a **ResponseClass** value of **Error**.</span></span>
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
    <m:ResponseCode>NoError</m:ResponseCode>
    <m:ResponseMessages>
      <m:DelegateUserResponseMessageType ResponseClass="Error">
        <m:MessageText>The user is already a delegate for the mailbox.</m:MessageText>
        <m:ResponseCode>ErrorDelegateAlreadyExists</m:ResponseCode>
        <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
      </m:DelegateUserResponseMessageType>
    </m:ResponseMessages>
  </m:AddDelegateResponse>
</soap:Body>
```

<span data-ttu-id="4f304-122">Für SOAP-EWS-Antworten können Sie sich also nicht auf den **ResponseClass** des Vorgangs verlassen – Sie müssen sich die **ResponseClass** jeder Antwortnachricht ansehen, um zu bestimmen, ob der Vorgang Fehler bei der Verarbeitung der Elemente aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4f304-122">So for SOAP EWS responses, you can't rely on the **ResponseClass** of the operation - you have to look at the **ResponseClass** of each response message to determine whether the operation encountered any errors processing the items.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="4f304-123">Überprüfen des Erfolgs</span><span class="sxs-lookup"><span data-stu-id="4f304-123">Verifying success</span></span>

<span data-ttu-id="4f304-124">Wenn jedes **ResponseClass** -Attribut für jedes **ResponseMessage** -Attribut auf " **erfolgreich**" festgelegt ist, wurde der Vorgang für alle Elemente erfolgreich abgeschlossen, und Sie können mit der nächsten Aufgabe fortfahren.</span><span class="sxs-lookup"><span data-stu-id="4f304-124">If each **ResponseClass** attribute for each **ResponseMessage** attribute is set to **Success**, the operation completed successfully on all the items, and you can move on to your next task.</span></span>
  
<span data-ttu-id="4f304-125">Im folgenden Beispiel wird eine erfolgreiche Antwort auf eine [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -Vorgangsanforderung zum Abrufen eines einzelnen Elements gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4f304-125">The following example shows a successful response to a [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation request to retrieve a single item.</span></span> <span data-ttu-id="4f304-126">Beachten Sie, dass beim Festlegen von **ResponseClass** auf " **Success**" die zugeordnete [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) immer auf " **noError**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4f304-126">Note that when the **ResponseClass** is set to **Success**, the associated [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) is always set to **NoError**.</span></span>
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
            <m:ResponseCode>NoError</m:ResponseCode>
            <m:Items>
              <t:Message>
                <t:ItemId Id="Er5bAAA=" 
                          ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAhE0/M" />
                <t:Subject>Dinner Party</t:Subject>
              </t:Message>
            </m:Items>
          </m:GetItemResponseMessage>
        </m:ResponseMessages>
      </m:GetItemResponse>
    </s:Body>
```

<span data-ttu-id="4f304-127">Im folgenden finden Sie eine erfolgreiche Antwort auf eine **GetItem** -Vorgangsanforderung zum Abrufen mehrerer Elemente.</span><span class="sxs-lookup"><span data-stu-id="4f304-127">The following is a successful response to a **GetItem** operation request to retrieve multiple items.</span></span> <span data-ttu-id="4f304-128">Jedes der [GetItemResponseMessage](https://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) -Elemente hat einen **ResponseClass** **Erfolg**.</span><span class="sxs-lookup"><span data-stu-id="4f304-128">Each of the [GetItemResponseMessage](https://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) elements has a **ResponseClass** of **Success**.</span></span>
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
    <m:ResponseMessages>
      <m:GetItemResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Items>
          <t:Message>
            <t:ItemId Id="Er5bAAA=" 
                      ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAhE0/M" /
            <t:Subject>Dinner Party</t:Subject>
          </t:Message>
        </m:Items>
      </m:GetItemResponseMessage>
      <m:GetItemResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Items>
          <t:Message>
            <t:ItemId Id="3c66AAA="
                      ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAc3kqm" />
            <t:Subject>Company Soccer Team</t:Subject>
          </t:Message>
        </m:Items>
      </m:GetItemResponseMessage>
    </m:ResponseMessages>
  </m:GetItemResponse>
</s:Body>
```

### <a name="handling-errors-and-warnings"></a><span data-ttu-id="4f304-129">Behandeln von Fehlern und Warnungen</span><span class="sxs-lookup"><span data-stu-id="4f304-129">Handling errors and warnings</span></span>

<span data-ttu-id="4f304-130">Wenn Sie eine Antwort erhalten und das **ResponseClass** -Attribut auf **Error**festgelegt ist, wurde der Vorgang für mindestens ein Element nicht erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4f304-130">When you receive a response and the **ResponseClass** attribute is set to **Error**, the operation did not complete successfully on one or more items.</span></span> <span data-ttu-id="4f304-131">Beheben Sie das Problem, und wiederholen Sie Ihre Anforderung oder den Teil Ihrer Anforderung, der fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="4f304-131">Correct the issue and retry your request, or the part of your request that failed.</span></span> <span data-ttu-id="4f304-132">Ein **ResponseClass** -Attributwert des **Warning** -Werts wird nur von der [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) -Operation zurückgegeben und gibt an, dass die Entität nicht in eine eindeutige Identität aufgelöst werden konnte.</span><span class="sxs-lookup"><span data-stu-id="4f304-132">A **ResponseClass** attribute value of **Warning** value is only returned by the [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation, and indicates that the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="4f304-133">Sie können Sie für alle anderen Vorgänge ignorieren.</span><span class="sxs-lookup"><span data-stu-id="4f304-133">You can ignore it for all other operations.</span></span> 
  
<span data-ttu-id="4f304-134">In der folgenden Antwort hat das **ResponseClass** -Attribut den Wert **Error**.</span><span class="sxs-lookup"><span data-stu-id="4f304-134">In the following response, the **ResponseClass** attribute has a value of **Error**.</span></span>
  
```XML
<m:GetItemResponseMessage ResponseClass="Error">
  <m:MessageText>Property is not valid for this object type.</m:MessageText>
  <m:ResponseCode>ErrorInvalidPropertyRequest</m:ResponseCode>
  <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
  <m:MessageXml>
    <t:FieldURI FieldURI="meeting:AssociatedCalendarItemId" />
  </m:MessageXml>
  <m:Items />
</m:GetItemResponseMessage>
```

<span data-ttu-id="4f304-135">In diesem Beispiel bietet EWS Anhaltspunkte zum Debuggen des Problems.</span><span class="sxs-lookup"><span data-stu-id="4f304-135">In this example, EWS provides clues to debug the issue.</span></span> <span data-ttu-id="4f304-136">Wenn das **ResponseClass** -Attribut den Wert **Error**aufweist, sind die folgenden zusätzlichen Elemente in der Antwort enthalten, wenn zutreffend:</span><span class="sxs-lookup"><span data-stu-id="4f304-136">When the **ResponseClass** attribute has a value of **Error**, the following additional elements are included in the response when applicable:</span></span>
  
- <span data-ttu-id="4f304-137">[MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) – beschreibt den Fehler.</span><span class="sxs-lookup"><span data-stu-id="4f304-137">[MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="4f304-138">[Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) – enthält den Fehlercode, der zum Auffinden zusätzlicher Ressourcen zur Problembehandlung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4f304-138">[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="4f304-139">[Messagexml verwendet](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) – gibt die Elemente an, die den Fehler verursacht haben.</span><span class="sxs-lookup"><span data-stu-id="4f304-139">[MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) — Identifies the elements that caused the error.</span></span> 
    
- <span data-ttu-id="4f304-140">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) – nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f304-140">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) — Unused.</span></span> 
    
<span data-ttu-id="4f304-141">Sie können die in diesen Elementen bereitgestellten Informationen verwenden, um Ihr Problem zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="4f304-141">You can use the information provided in these elements to investigate your issue.</span></span> <span data-ttu-id="4f304-142">Im vorherigen Beispiel gibt die **MessageText** an, dass die Eigenschaft nicht für den Objekttyp gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4f304-142">In the previous example, the **MessageText** indicates that the property isn't valid for the object type.</span></span> <span data-ttu-id="4f304-143">Die Anforderung bestand darin, eine e-Mail-Nachricht zu erhalten, aber der Eigenschaftensatz enthielt die **AssociatedCalendarItemId**, die nur für Termin Elemente gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4f304-143">The request was to get an email message, but the property set included the **AssociatedCalendarItemId**, which is only valid for appointment items.</span></span>
  
<span data-ttu-id="4f304-144">Das folgende Beispiel zeigt einen Fehler, der als Teil eines Batchvorgangs empfangen wurde, um mehrere e-Mail-Elemente abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4f304-144">The following example shows an error that was received as part of a batched operation to get multiple email items.</span></span> <span data-ttu-id="4f304-145">Das erste Element wurde erfolgreich abgerufen, und die **ResponseClass** **ist auf "erfolgreich"** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4f304-145">The first item was retrieved successfully and the **ResponseClass** is set to **Success**.</span></span> <span data-ttu-id="4f304-146">Das zweite Element konnte nicht gefunden werden, und die **ResponseClass** ist auf **Error**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4f304-146">The second item could not be found, and the **ResponseClass** is set to **Error**.</span></span>
  
```XML
<m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <m:ResponseMessages>
    <m:GetItemResponseMessage ResponseClass="Success">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:Items>
        <t:Message>
          <t:ItemId Id="Er5cAAA="
                    ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAhE0/O" />
          <t:Subject>Business plans</t:Subject>
        </t:Message>
      </m:Items>
    </m:GetItemResponseMessage>
    <m:GetItemResponseMessage ResponseClass="Error">
      <m:MessageText>The specified object was not found in the store.</m:MessageText>
      <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
      <m:Items />
    </m:GetItemResponseMessage>
  </m:ResponseMessages>
</m:GetItemResponse>
```

<span data-ttu-id="4f304-147">Wenn ein oder mehrere Elemente in einer Batchanforderung nicht wie angefordert verarbeitet werden können, wird für jedes fehlgeschlagene Element ein Fehler zurückgegeben, und die restlichen Elemente im Batch werden wie erwartet verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="4f304-147">When one or more items in a batched request can't be processed as requested, an error is returned for each item that failed, and the rest of the items in the batch are processed as expected.</span></span> <span data-ttu-id="4f304-148">Fehler in der Batchverarbeitung können auftreten, wenn das Element gelöscht wurde und daher nicht gesendet, abgerufen oder aktualisiert werden kann oder wenn das Element in einen anderen Ordner verschoben wurde und daher über eine neue Element-ID verfügt.</span><span class="sxs-lookup"><span data-stu-id="4f304-148">Failures in batch processing can occur if the item was deleted, and therefore can't be sent, retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID.</span></span> <span data-ttu-id="4f304-149">Da der Vorgang für einige Elemente abgeschlossen wird und kein Fehler zurückgegeben wird, wenn ein oder mehrere Elemente nicht verarbeitet werden können, ist es wichtig, jedes **ResponseClass** -Attribut zu überprüfen, bevor Sie mit dem nächsten Vorgang fortfahren.</span><span class="sxs-lookup"><span data-stu-id="4f304-149">Because the operation will complete for some items and not return an error when one or more items can't be processed, it's important to check each **ResponseClass** attribute before you move on to your next operation.</span></span> 
  
<span data-ttu-id="4f304-150">Wenn die von den Antwortelementen bereitgestellten Informationen Ihnen nicht helfen, Ihre Anforderung zu korrigieren oder Sie anderweitig aufzuheben, lesen Sie die [nächsten Schritte](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="4f304-150">If the information provided by the response elements doesn't help you correct your request or otherwise unblock you, see [Next steps](#bk_nextsteps).</span></span>
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a><span data-ttu-id="4f304-151">Überprüfen der Ergebnisse eines verwaltete EWS-API-Methodenaufrufs</span><span class="sxs-lookup"><span data-stu-id="4f304-151">Verifying the results of an EWS Managed API method call</span></span>
<span data-ttu-id="4f304-152"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="4f304-152"><a name="bk_successful"> </a></span></span>

<span data-ttu-id="4f304-153">Wenn Sie die verwaltete EWS-API verwenden und eine Methode für ein [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt aufrufen, gibt die Methode wahrscheinlich ein [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) -Objekt zurück, das eine Auflistung von [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) -Objekten enthält, oder eine Sammlung von Objekten, die von den **ServiceResponse** -Objekten abgeleitet sind.</span><span class="sxs-lookup"><span data-stu-id="4f304-153">If you're using the EWS Managed API and calling a method on an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, your method will likely return a [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) object, which contains a collection of [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) objects, or a collection of objects derived from the **ServiceResponse** objects.</span></span> <span data-ttu-id="4f304-154">Die **ServiceResponseCollection** -und die include- **ServiceResponse** -Objekte enthalten Informationen über das Ergebnis des Methodenaufrufs, den Sie zum Überprüfen der Ergebnisse verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4f304-154">The **ServiceResponseCollection** and included **ServiceResponse** objects contain information about the result of the method call, which you can use to verify your results.</span></span> 
  
<span data-ttu-id="4f304-155">Wenn Sie die verwaltete EWS-API verwenden und eine Methode für ein [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) -Objekt oder eines der abgeleiteten Objekte aufrufen, gibt die Methode wahrscheinlich kein Response-Objekt zurück, um den Erfolg zu überprüfen, löst jedoch eine [Ausnahme](https://msdn.microsoft.com/library/c18k6c59) aus, wenn die Methode nicht erfolgreich abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4f304-155">If you're using the EWS Managed API and calling a method on an [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object, or one of the derived objects, the method likely does not return a response object to check for success, but does throw an [Exception](https://msdn.microsoft.com/library/c18k6c59) if the method does not complete successfully.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="4f304-156">Überprüfen des Erfolgs</span><span class="sxs-lookup"><span data-stu-id="4f304-156">Verifying success</span></span>

<span data-ttu-id="4f304-157">Ein Vorteil der Verwendung der verwaltete EWS-API besteht darin, dass Sie einen allgemeinen Status bereitstellt, wenn Sie mit mehreren Elementen in einer Antwort umgehen.</span><span class="sxs-lookup"><span data-stu-id="4f304-157">One benefit of using the EWS Managed API is that it provides an overall status when dealing with multiple items in one response.</span></span> <span data-ttu-id="4f304-158">Wenn also die aufgerufene Methode ein **ServiceResponseCollection**-Objekt zurückgibt, können Sie überprüfen, ob die [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) -Eigenschaft des **ServiceResponseCollection** gleich [ServiceResult. Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)ist.</span><span class="sxs-lookup"><span data-stu-id="4f304-158">So if the method you called returns a **ServiceResponseCollection**, you can check that the [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) property of the **ServiceResponseCollection** is equal to [ServiceResult.Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="4f304-159">Wenn dies der Fall ist, wurden alle Elemente im Batchprozess erfolgreich abgeschlossen; Sie müssen nicht jedes **ServiceResponse** -Objekt einzeln überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4f304-159">If so, all the items in the batched process were completed successfully; you don't have to check each **ServiceResponse** object individually.</span></span> <span data-ttu-id="4f304-160">Wenn die **OverallResult** -Eigenschaft nicht auf **ServiceResult. Success**festgelegt ist, müssen Sie [den Fehler oder die Warnung behandeln](#bk_ewsmaerrors).</span><span class="sxs-lookup"><span data-stu-id="4f304-160">If the **OverallResult** property is not set to **ServiceResult.Success**, you have to [handle the error or warning](#bk_ewsmaerrors).</span></span>
  
<span data-ttu-id="4f304-161">Wenn die aufgerufene Methode keinen **ServiceResponseCollection**zurückgibt, aber ein **ServiceResponse** -Objekt zurückgibt, müssen Sie den Wert der **Result** -Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4f304-161">If the method you're calling does not return a **ServiceResponseCollection**, but does return a **ServiceResponse** object, you have to check the value of the **Result** property.</span></span> <span data-ttu-id="4f304-162">Wenn der **Ergebnis** Wert auf " **Success**" festgelegt ist, wissen Sie, dass die Methode erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4f304-162">If the **Result** value is set to **Success**, you know the method completed successfully.</span></span>
  
<span data-ttu-id="4f304-163">Wenn die Methode, die Sie aufrufen, keinen Rückgabewert hat, gibt es wirklich keine Möglichkeit, über den verwaltete EWS-API auf Erfolg zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4f304-163">If the method you're calling has no return value, there's really no way to check for success via the EWS Managed API.</span></span> <span data-ttu-id="4f304-164">Solange keine Ausnahme ausgelöst wird, können Sie davon ausgehen, dass die Methode erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4f304-164">As long as an exception is not thrown, you can assume the method completed successfully.</span></span> <span data-ttu-id="4f304-165">Zur weiteren Überprüfung können Sie auch [die SOAP-Antwort überprüfen, um die Ergebnisse zu über](#bk_verifysoap)prüfen.</span><span class="sxs-lookup"><span data-stu-id="4f304-165">For additional validation, you can also [check the SOAP response to verify the results](#bk_verifysoap).</span></span>
  
### <a name="handling-errors-warnings-and-exceptions"></a><span data-ttu-id="4f304-166">Behandeln von Fehlern, Warnungen und Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="4f304-166">Handling errors, warnings, and exceptions</span></span>
<span data-ttu-id="4f304-167"><a name="bk_ewsmaerrors"> </a></span><span class="sxs-lookup"><span data-stu-id="4f304-167"><a name="bk_ewsmaerrors"> </a></span></span>

<span data-ttu-id="4f304-168">Wenn Ihr verwaltete EWS-API Code eine **Ausnahme**auslöst, können Sie den [Exception. Message](https://msdn.microsoft.com/library/9btwf6wk) -Wert verwenden, um die Ursache des Fehlers zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="4f304-168">If your EWS Managed API code throws an **Exception**, you can use the [Exception.Message](https://msdn.microsoft.com/library/9btwf6wk) value to determine the source of the error.</span></span> <span data-ttu-id="4f304-169">Die **Message** -Eigenschaft enthält den Inhalt des [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) -Elements in der zugrunde liegenden SOAP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="4f304-169">The **Message** property contains the contents of the [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) element in the underlying SOAP response.</span></span> <span data-ttu-id="4f304-170">Darüber hinaus können Sie, wenn die Ausnahme vom Typ [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) -Objekt ist, eine der häufigsten Ausnahmen, auch den im zugrunde liegenden SOAP- [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element enthaltenen [errorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) und die [Response](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) -Eigenschaft, die das zugeordnete [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) -Objekt identifiziert, abrufen.</span><span class="sxs-lookup"><span data-stu-id="4f304-170">In addition, if the exception is of type [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) object, one of the most common exceptions, you can also retrieve the [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) contained in the underlying SOAP [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element, and the [Response](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) property that identifies the associated [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="4f304-171">Im folgenden Code wird gezeigt, wie der Inhalt eines **ServiceResponseException**abgefangen und angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4f304-171">The following code shows how to catch and display the contents of a **ServiceResponseException**.</span></span> 
  
```cs
try
    {
         …
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error code: " + ex.ErrorCode);
        Console.WriteLine("Error message: " + ex.Message);
        Console.WriteLine("Response: " + ex.Response);
    }
```

<span data-ttu-id="4f304-172">Wenn die aufgerufene Methode ein **ServiceResponseCollection**-Objekt zurückgibt und der Wert der **OverallResult** -Eigenschaft gleich **Warning** oder **Error**ist, müssen Sie alle Objekte in der **ServiceResponseCollection** durchlaufen, um den Fehler zu finden.</span><span class="sxs-lookup"><span data-stu-id="4f304-172">If the method you called returns a **ServiceResponseCollection**, and the value of the **OverallResult** property is equal to **Warning** or **Error**, you'll have to loop through each object in the **ServiceResponseCollection** to find the error.</span></span> <span data-ttu-id="4f304-173">Die **OverallResult** -Eigenschaft ist auf **Warning** festgelegt, wenn mindestens eine Antwort den **Ergebnis** Wert auf **Warning** festgelegt hat und alle anderen Antworten ihre **Ergebnis** Werte auf " **erfolgreich**" festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="4f304-173">The **OverallResult** property is set to **Warning** if at least one response has its **Result** value set to **Warning** and all other responses have their **Result** values set to **Success**.</span></span> <span data-ttu-id="4f304-174">Die **OverallResult** -Eigenschaft ist auf **Error** festgelegt, wenn mindestens eine Antwort den **Ergebnis** Wert auf **Error**festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="4f304-174">The **OverallResult** property is set to **Error** if at least one response has its **Result** value set to **Error**.</span></span> <span data-ttu-id="4f304-175">Wenn **OverallResult** auf **Warning** oder **Error**festgelegt ist, werden die folgenden Eigenschaften für die **ServiceResponse** -Objekte entsprechend festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4f304-175">When the **OverallResult** is set to **Warning** or **Error**, the following properties are set on the **ServiceResponse** objects as appropriate:</span></span> 
  
- <span data-ttu-id="4f304-176">[ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) – enthält den Fehlercode, der zum Auffinden zusätzlicher Ressourcen zur Problembehandlung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4f304-176">[ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="4f304-177">[ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) – enthält Details zum Fehler für einige **errorCodes**.</span><span class="sxs-lookup"><span data-stu-id="4f304-177">[ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) — Contains details about the error for some **ErrorCodes**.</span></span> <span data-ttu-id="4f304-178">Wenn der Fehlercode beispielsweise **ErrorRecurrenceHasNoOccurrence**lautet, enthält der **ErrorDetails** Schlüssel für **EffectiveStartDate** und **EffectiveEndDate**.</span><span class="sxs-lookup"><span data-stu-id="4f304-178">For example, when the error code is **ErrorRecurrenceHasNoOccurrence**, the **ErrorDetails** will contain keys for **EffectiveStartDate** and **EffectiveEndDate**.</span></span> 
    
- <span data-ttu-id="4f304-179">[ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) – beschreibt den Fehler.</span><span class="sxs-lookup"><span data-stu-id="4f304-179">[ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="4f304-180">[ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) – sofern verfügbar, werden die Eigenschaften identifiziert, die den Fehler verursacht haben.</span><span class="sxs-lookup"><span data-stu-id="4f304-180">[ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) — If available, identifies the properties that caused the error.</span></span> <span data-ttu-id="4f304-181">Wenn der Fehlercode beispielsweise **ErrorInvalidPropertyForOperation**lautet, enthält **ErrorProperties** die Definition der Eigenschaft, die für die Anforderung ungültig war.</span><span class="sxs-lookup"><span data-stu-id="4f304-181">For example, when the error code is **ErrorInvalidPropertyForOperation**, **ErrorProperties** contains the definition of the property that was invalid for the request.</span></span> 
    
- <span data-ttu-id="4f304-182">[Ergebnis](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) – enthält **Fehler** oder **Warnungen** , wenn ein Problem auftritt.</span><span class="sxs-lookup"><span data-stu-id="4f304-182">[Result](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) — Contains **Error** or **Warning** when an issue is encountered.</span></span> 
    
<span data-ttu-id="4f304-183">Wenn die von den **ServiceResponse** -Eigenschaften bereitgestellten Informationen nicht genügend Informationen zur Korrektur des Methodenaufrufs oder zum Aufheben der Blockierung bereitstellen, finden Sie weitere Informationen zu **errorCode** -Werten in den [nächsten Schritten](#bk_nextsteps) .</span><span class="sxs-lookup"><span data-stu-id="4f304-183">If the information provided by the **ServiceResponse** properties doesn't provide enough information to correct your method call or unblock you, see [Next steps](#bk_nextsteps) to dig up more information on **ErrorCode** values.</span></span> 
  
## 
<span data-ttu-id="4f304-184"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="4f304-184"><a name="bk_nextsteps"> </a></span></span>

<span data-ttu-id="4f304-185">Weitere Informationen zur Problembehandlung finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4f304-185">You can look up additional troubleshooting information in the following topics:</span></span>
  
- <span data-ttu-id="4f304-186">[Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element</span><span class="sxs-lookup"><span data-stu-id="4f304-186">[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element</span></span> 
    
- <span data-ttu-id="4f304-187">[Service Error](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) -Aufzählung</span><span class="sxs-lookup"><span data-stu-id="4f304-187">[ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) enumeration</span></span> 
    
- [<span data-ttu-id="4f304-188">Mit der EWS-Eigenschaft zusammenhängende Fehler</span><span class="sxs-lookup"><span data-stu-id="4f304-188">EWS property-related errors</span></span>](ews-property-related-errors.md)
    
<span data-ttu-id="4f304-189">Je nachdem, was Sie in Ihrer Anforderung erreichen möchten, finden Sie darüber hinaus möglicherweise weitere hilfreiche Informationen zum Fehlercode in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4f304-189">In addition, depending on what you're trying to accomplish in your request, you might find additional helpful information about the error code in the following topics:</span></span>
  
- [<span data-ttu-id="4f304-190">Behandeln von AutoErmittlungs-Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="4f304-190">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
- [<span data-ttu-id="4f304-191">Umgang von Fehlern im Zusammenhang mit Benachrichtigungen in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="4f304-191">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="4f304-192">Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="4f304-192">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="4f304-193">Umgang mit Fehlern in Exchange im Zusammenhang mit Löschungen in EWS</span><span class="sxs-lookup"><span data-stu-id="4f304-193">Handling deletion-related errors in EWS in Exchange</span></span>](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="4f304-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f304-194">See also</span></span>


- [<span data-ttu-id="4f304-195">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="4f304-195">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="4f304-196">Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange</span><span class="sxs-lookup"><span data-stu-id="4f304-196">Tools and resources for troubleshooting EWS applications for Exchange</span></span>](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

