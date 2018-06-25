---
title: Überprüfen der Ergebnisse eines Aufrufs EWS oder EWS Managed API
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78a1741c-1bbe-4cb4-9331-9d6d3171fc11
description: Erfahren Sie, wie die Ergebnisse der EWS oder EWS Managed API Anrufe zu überprüfen.
ms.openlocfilehash: 077dd923710a1a7f5cad4c822cbbd58ab3603661
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757135"
---
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a><span data-ttu-id="93a0c-103">Überprüfen der Ergebnisse eines Aufrufs EWS oder EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="93a0c-103">Verifying the results of an EWS or EWS Managed API call</span></span>

<span data-ttu-id="93a0c-104">Erfahren Sie, wie die Ergebnisse der EWS oder EWS Managed API Anrufe zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-104">Learn how to verify the results of your EWS or EWS Managed API calls.</span></span>
  
<span data-ttu-id="93a0c-105">Wenn Dinge nicht ordnungsgemäß funktionieren, sollten sie finden Sie unter Was passiert, durch die SOAP-Anforderungen, die über das Netzwerk und die Antworten, die der Server wieder sendet, sendet die Anwendung untersuchen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-105">When things aren't working correctly, it helps to see what's going on by examining the SOAP requests that your application is sending over the network and the responses that the server is sending back.</span></span> <span data-ttu-id="93a0c-106">[Tools und Ressourcen für die Problembehandlung EWS-Applikationen](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) Artikel enthält Links zu Tools, mit denen erfassen und diese SOAP-Anforderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-106">The [tools and resources for troubleshooting EWS applications](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) article includes links to tools to help capture and view those SOAP requests.</span></span> <span data-ttu-id="93a0c-107">Nachdem Sie die Anforderungen und die Antworten haben, wie überprüfen Sie, ob die Anforderung an den Server gesendeten ordnungsgemäß verarbeitet wurde?</span><span class="sxs-lookup"><span data-stu-id="93a0c-107">After you've got the requests and the responses, how do you verify that the request you sent to the server was processed correctly?</span></span> <span data-ttu-id="93a0c-108">Lesen Sie weiter unten finden Sie.</span><span class="sxs-lookup"><span data-stu-id="93a0c-108">Read on to find out.</span></span> 
  
<span data-ttu-id="93a0c-109">Wenn Sie EWS-Anforderungen senden, können Sie ihm Ihre Überprüfung starten, indem Sie das **ResponseClass** -Attribut für jede Antwortnachricht in der Antwort überprüfen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-109">If you're sending EWS requests, you're going to start your verification by checking the **ResponseClass** attribute for each response message in the response.</span></span> <span data-ttu-id="93a0c-110">Die erfahren Sie, ob der Vorgang für jedes Element erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-110">That will tell you whether the operation completed successfully on each item.</span></span> 
  
<span data-ttu-id="93a0c-111">Je nach dem Objekt anfordert, dass Ihre Methode aufruft, wenn Sie zum Senden die EWS Managed API verwenden, Sie einige Überprüfung mithilfe der Antwortobjekte machen können.</span><span class="sxs-lookup"><span data-stu-id="93a0c-111">Depending on the object that your method is calling, if you're using the EWS Managed API to send requests, you can do some verification using the response objects.</span></span> <span data-ttu-id="93a0c-112">Aber, da die SOAP-Antwort eine Obermenge enthält von was in die EWS Managed API-Antwort-Objekte enthalten ist, möglicherweise möchten Sie die SOAP-Antwort betrachten.</span><span class="sxs-lookup"><span data-stu-id="93a0c-112">But because the SOAP response contains a superset of what's included in the EWS Managed API response objects, you might want to look at the SOAP response as well.</span></span> <span data-ttu-id="93a0c-113">Da die SOAP-Antwort oft mehr Informationen als die EWS Managed API-Antwort-Objekte enthalten kann, starten Sie die Überprüfung mit der SOAP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="93a0c-113">Because the SOAP response can often contain more information than the EWS Managed API response objects, start your verification with the SOAP response.</span></span>
  
## <a name="verifying-the-results-of-a-soap-response"></a><span data-ttu-id="93a0c-114">Überprüfen der Ergebnisse einer SOAP-Antwort</span><span class="sxs-lookup"><span data-stu-id="93a0c-114">Verifying the results of a SOAP response</span></span>
<span data-ttu-id="93a0c-115"><a name="bk_verifysoap"> </a></span><span class="sxs-lookup"><span data-stu-id="93a0c-115"></span></span>

<span data-ttu-id="93a0c-116">Wenn Sie die SOAP-Antwort erhalten, wird als erstes betrachten das **ResponseClass** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="93a0c-116">When you receive a SOAP response, the first thing to look at is the **ResponseClass** attribute.</span></span> <span data-ttu-id="93a0c-117">Dieses Attribut ist in jeder Instanz **ResponseMessageType** im [ResponseMessages](http://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) -Element enthalten, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="93a0c-117">This attribute is included in each **ResponseMessageType** instance in the [ResponseMessages](http://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) element, as shown in the following example.</span></span> 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

<span data-ttu-id="93a0c-118">Da SOAP-Antwort möglicherweise mehrere Antwortnachrichten in einer einzelnen SOAP-Antwort enthält, ist es wichtig, um jede Antwortnachricht einzeln zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-118">Because a SOAP response might contain multiple response messages in a single SOAP response, it's important to check each response message individually.</span></span>
  
<span data-ttu-id="93a0c-119">Wenn Sie mit einem Vorgang arbeiten, die als Teil der Antwort auf einen Vorgang, wie im folgenden eine **ResponseClass** enthält möglicherweise versucht, nur die **ResponseClass** des Vorgangs überprüfen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-119">If you're working with an operation that includes a **ResponseClass** as part of the operation response, like the following, you might be tempted to only check the **ResponseClass** of the operation.</span></span> 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

<span data-ttu-id="93a0c-120">Jedoch gibt der Ausführungsstatus nur gibt die Form der Antwort auf oberster Ebene und nicht den Status der einzelnen Nachricht-Antworten entspricht.</span><span class="sxs-lookup"><span data-stu-id="93a0c-120">However, the operation status only reflects the shape of the top-level response and does not reflect the status of all the individual message responses.</span></span> <span data-ttu-id="93a0c-121">Im folgenden Beispiel die [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) -Operation besteht aus einem **ResponseClass** des **Erfolgs**, aber das zugrunde liegende [DelegateUserResponseMessageType](http://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) -Element hat den Wert **ResponseClass** **Fehler**.</span><span class="sxs-lookup"><span data-stu-id="93a0c-121">In the following example, the [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) operation has a **ResponseClass** of **Success**, but the underlying [DelegateUserResponseMessageType](http://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) element has a **ResponseClass** value of **Error**.</span></span>
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="93a0c-122">So für SOAP-EWS-Antworten Sie auf die **ResponseClass** des Vorgangs verlassen können nicht - müssen Sie sehen Sie sich die **ResponseClass** jeder Nachricht Antwort, um festzustellen, ob der Vorgang Verarbeitung der Elemente Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="93a0c-122">So for SOAP EWS responses, you can't rely on the **ResponseClass** of the operation - you have to look at the **ResponseClass** of each response message to determine whether the operation encountered any errors processing the items.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="93a0c-123">Überprüfen des Erfolgs des Updates</span><span class="sxs-lookup"><span data-stu-id="93a0c-123">Verifying success</span></span>

<span data-ttu-id="93a0c-124">Wenn jedes **ResponseClass** -Attribut für jedes **ResponseMessage** -Attribut auf **Erfolg**, der Vorgang erfolgreich abgeschlossen auf alle Elemente festgelegt ist, und Sie können auf die nächste Aufgabe verschieben.</span><span class="sxs-lookup"><span data-stu-id="93a0c-124">If each **ResponseClass** attribute for each **ResponseMessage** attribute is set to **Success**, the operation completed successfully on all the items, and you can move on to your next task.</span></span>
  
<span data-ttu-id="93a0c-125">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -Vorgang, um ein einzelnes Element abzurufen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-125">The following example shows a successful response to a [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation request to retrieve a single item.</span></span> <span data-ttu-id="93a0c-126">Beachten Sie, dass bei **Erfolg**der **ResponseClass** festgelegt ist, die zugeordneten [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) immer **NoError**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="93a0c-126">Note that when the **ResponseClass** is set to **Success**, the associated [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) is always set to **NoError**.</span></span>
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="93a0c-127">Im folgenden finden eine erfolgreiche Antwort auf eine Anforderung **GetItem** -Vorgang, um mehrere Elemente abzurufen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-127">The following is a successful response to a **GetItem** operation request to retrieve multiple items.</span></span> <span data-ttu-id="93a0c-128">Jedes Element [GetItemResponseMessage](http://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) verfügt über eine **ResponseClass** des **Erfolgs**.</span><span class="sxs-lookup"><span data-stu-id="93a0c-128">Each of the [GetItemResponseMessage](http://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) elements has a **ResponseClass** of **Success**.</span></span>
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="handling-errors-and-warnings"></a><span data-ttu-id="93a0c-129">Behandlung von Fehlern und Warnungen</span><span class="sxs-lookup"><span data-stu-id="93a0c-129">Handling errors and warnings</span></span>

<span data-ttu-id="93a0c-130">Wenn Sie eine Antwort erhalten, und das Attribut **ResponseClass** auf **Fehler**festgelegt ist, wurde die Operation auf ein oder mehrere Elemente nicht erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-130">When you receive a response and the **ResponseClass** attribute is set to **Error**, the operation did not complete successfully on one or more items.</span></span> <span data-ttu-id="93a0c-131">Korrigieren Sie das Problem, und wiederholen Sie die Anforderung oder der Teil der erfolgreichen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="93a0c-131">Correct the issue and retry your request, or the part of your request that failed.</span></span> <span data-ttu-id="93a0c-132">Ein Attributwert **ResponseClass** **Warnung** Wert wird nur von der Operation [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) zurückgegeben, und gibt an, dass die Entität nicht in eine eindeutige Identität aufgelöst werden konnte.</span><span class="sxs-lookup"><span data-stu-id="93a0c-132">A **ResponseClass** attribute value of **Warning** value is only returned by the [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation, and indicates that the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="93a0c-133">Sie können für alle anderen Vorgänge ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="93a0c-133">You can ignore it for all other operations.</span></span> 
  
<span data-ttu-id="93a0c-134">In der folgenden Antwort hat das **ResponseClass** -Attribut den Wert des **Fehlers**.</span><span class="sxs-lookup"><span data-stu-id="93a0c-134">In the following response, the **ResponseClass** attribute has a value of **Error**.</span></span>
  
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

<span data-ttu-id="93a0c-135">In diesem Beispiel bietet EWS Hinweise, um das Problem zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-135">In this example, EWS provides clues to debug the issue.</span></span> <span data-ttu-id="93a0c-136">Wenn das **ResponseClass** -Attribut den Wert **Fehler**hat, werden die folgenden zusätzlichen Elemente in der Antwort ggf. enthalten:</span><span class="sxs-lookup"><span data-stu-id="93a0c-136">When the **ResponseClass** attribute has a value of **Error**, the following additional elements are included in the response when applicable:</span></span>
  
- <span data-ttu-id="93a0c-137">[MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) – den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="93a0c-137">[MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="93a0c-138">[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) – enthält den Fehlercode, die verwendet werden kann, zusätzliche Ressourcen zur Problembehandlung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93a0c-138">[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="93a0c-139">[MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) – identifiziert die Elemente, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="93a0c-139">[MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) — Identifies the elements that caused the error.</span></span> 
    
- <span data-ttu-id="93a0c-140">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) – nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="93a0c-140">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) — Unused.</span></span> 
    
<span data-ttu-id="93a0c-141">Die Informationen in dieser Elemente können Sie um Ihr Problem zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-141">You can use the information provided in these elements to investigate your issue.</span></span> <span data-ttu-id="93a0c-142">Im vorherigen Beispiel gibt die **MessageText** , dass die Eigenschaft nicht für den Objekttyp gültig ist.</span><span class="sxs-lookup"><span data-stu-id="93a0c-142">In the previous example, the **MessageText** indicates that the property isn't valid for the object type.</span></span> <span data-ttu-id="93a0c-143">Die Anforderung war zu eine e-Mail-Nachricht erhalten möchten, aber Eigenschaftensatzes enthalten die **AssociatedCalendarItemId**, das nur für Terminelemente gültig ist.</span><span class="sxs-lookup"><span data-stu-id="93a0c-143">The request was to get an email message, but the property set included the **AssociatedCalendarItemId**, which is only valid for appointment items.</span></span>
  
<span data-ttu-id="93a0c-144">Das folgende Beispiel zeigt einen Fehler, der als Teil eines Vorgangs im Batchmodus abzurufenden mehrere e-Mail-Elemente empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="93a0c-144">The following example shows an error that was received as part of a batched operation to get multiple email items.</span></span> <span data-ttu-id="93a0c-145">Das erste Element erfolgreich abgerufen wurde, und die **ResponseClass** auf **Erfolg**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="93a0c-145">The first item was retrieved successfully and the **ResponseClass** is set to **Success**.</span></span> <span data-ttu-id="93a0c-146">Das zweite Element konnte nicht gefunden werden, und die **ResponseClass** auf **Fehler**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="93a0c-146">The second item could not be found, and the **ResponseClass** is set to **Error**.</span></span>
  
```XML
<m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="93a0c-147">Wenn ein oder mehrere Elemente in einer Anforderung im Batch nicht verarbeitet werden können, wie angefordert, für jedes Element, das nicht erfolgreich ist ein Fehler zurückgegeben, und die restlichen Elemente in den Batch verarbeitet wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="93a0c-147">When one or more items in a batched request can't be processed as requested, an error is returned for each item that failed, and the rest of the items in the batch are processed as expected.</span></span> <span data-ttu-id="93a0c-148">Fehler im Batch-Verarbeitung können auftreten, wenn das Element wurde gelöscht, und daher nicht gesendet, abgerufen, oder aktualisiert werden, oder wenn das Element in einem anderen Ordner verschoben, und daher eine neues Element-ID. hat</span><span class="sxs-lookup"><span data-stu-id="93a0c-148">Failures in batch processing can occur if the item was deleted, and therefore can't be sent, retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID.</span></span> <span data-ttu-id="93a0c-149">Da die Operation für einige Elemente beendet und kein Fehler zurückgegeben, wenn ein oder mehrere Elemente nicht verarbeitet werden können, ist es wichtig, um jedes **ResponseClass** -Attribut zu überprüfen, bevor Sie den nächsten Vorgang fortfahren.</span><span class="sxs-lookup"><span data-stu-id="93a0c-149">Because the operation will complete for some items and not return an error when one or more items can't be processed, it's important to check each **ResponseClass** attribute before you move on to your next operation.</span></span> 
  
<span data-ttu-id="93a0c-150">Wenn die Metriken aufgelistet, die Antwortelemente nicht Ihnen helfen, korrigieren Ihre Anforderung oder Entsperren Sie andernfalls, finden Sie unter [Nächste Schritte](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="93a0c-150">If the information provided by the response elements doesn't help you correct your request or otherwise unblock you, see [Next steps](#bk_nextsteps).</span></span>
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a><span data-ttu-id="93a0c-151">Überprüfen der Ergebnisse eines Methodenaufrufs EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="93a0c-151">Verifying the results of an EWS Managed API method call</span></span>
<span data-ttu-id="93a0c-152"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="93a0c-152"></span></span>

<span data-ttu-id="93a0c-153">Wenn Sie die EWS Managed API und eine Methode für ein Objekt [ExchangeService](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) aufrufen, wird die Methode wahrscheinlich eine [ServiceResponseCollection](http://msdn.microsoft.com/EN-US/library/dd633715%28v=exchg.80%29.aspx) -Objekt zurück, das enthält eine Auflistung von [ServiceResponse](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) -Objekten, oder eine Auflistung von Objekte aus der **ServiceResponse** Objekte abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="93a0c-153">If you're using the EWS Managed API and calling a method on an [ExchangeService](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, your method will likely return a [ServiceResponseCollection](http://msdn.microsoft.com/EN-US/library/dd633715%28v=exchg.80%29.aspx) object, which contains a collection of [ServiceResponse](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) objects, or a collection of objects derived from the **ServiceResponse** objects.</span></span> <span data-ttu-id="93a0c-154">Die **ServiceResponseCollection** und enthalten **ServiceResponse** -Objekte enthalten Informationen über das Ergebnis des Methodenaufrufs, die Sie verwenden können, um Ihre Ergebnisse zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-154">The **ServiceResponseCollection** and included **ServiceResponse** objects contain information about the result of the method call, which you can use to verify your results.</span></span> 
  
<span data-ttu-id="93a0c-155">Wenn Sie die EWS Managed API und Aufrufen einer Methode für ein [Element](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) -Objekt oder eines der abgeleitete Objekte, die wahrscheinlich-Methode nicht zurück Response-Objekt für den Erfolg zu überprüfen, sondern löst eine [Ausnahme](http://msdn.microsoft.com/EN-US/library/c18k6c59) aus, wenn die Methode nicht abgeschlossen wurde erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="93a0c-155">If you're using the EWS Managed API and calling a method on an [Item](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object, or one of the derived objects, the method likely does not return a response object to check for success, but does throw an [Exception](http://msdn.microsoft.com/EN-US/library/c18k6c59) if the method does not complete successfully.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="93a0c-156">Überprüfen des Erfolgs des Updates</span><span class="sxs-lookup"><span data-stu-id="93a0c-156">Verifying success</span></span>

<span data-ttu-id="93a0c-157">Ein Vorteil die EWS Managed API ist, dass beim Umgang mit mehreren Elementen in eine Antwort ein Gesamtstatus bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="93a0c-157">One benefit of using the EWS Managed API is that it provides an overall status when dealing with multiple items in one response.</span></span> <span data-ttu-id="93a0c-158">Wenn eine **ServiceResponseCollection**von die aufgerufenen Methode zurückgegeben wird, können Sie also überprüfen, dass die [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) -Eigenschaft der **ServiceResponseCollection** [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)gleich ist.</span><span class="sxs-lookup"><span data-stu-id="93a0c-158">So if the method you called returns a **ServiceResponseCollection**, you can check that the [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) property of the **ServiceResponseCollection** is equal to [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="93a0c-159">In diesem Fall wurden alle Elemente in der im Batchmodus Vorgang erfolgreich abgeschlossen wurde; Sie müssen nicht jedes Objekt **ServiceResponse** einzeln zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-159">If so, all the items in the batched process were completed successfully; you don't have to check each **ServiceResponse** object individually.</span></span> <span data-ttu-id="93a0c-160">Wenn die **OverallResult** -Eigenschaft nicht auf **ServiceResult.Success**festgelegt ist, müssen Sie [die Fehlermeldung oder einer Warnung zu behandeln](#bk_ewsmaerrors).</span><span class="sxs-lookup"><span data-stu-id="93a0c-160">If the **OverallResult** property is not set to **ServiceResult.Success**, you have to [handle the error or warning](#bk_ewsmaerrors).</span></span>
  
<span data-ttu-id="93a0c-161">Wenn die-Methode, die Sie Aufrufen einer **ServiceResponseCollection**gibt keine zurück, jedoch ein **ServiceResponse** -Objekt zurückgibt, müssen Sie den Wert der **Result** -Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-161">If the method you're calling does not return a **ServiceResponseCollection**, but does return a **ServiceResponse** object, you have to check the value of the **Result** property.</span></span> <span data-ttu-id="93a0c-162">Wenn der Wert **Ergebnis** **Erfolg**festgelegt ist, wissen Sie die Methode erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="93a0c-162">If the **Result** value is set to **Success**, you know the method completed successfully.</span></span>
  
<span data-ttu-id="93a0c-163">Wenn die Methode, die Sie aufrufen keinen Rückgabewert hat, ist es wirklich nicht möglich, überprüfen Sie für den Erfolg über die EWS Managed-API.</span><span class="sxs-lookup"><span data-stu-id="93a0c-163">If the method you're calling has no return value, there's really no way to check for success via the EWS Managed API.</span></span> <span data-ttu-id="93a0c-164">Solange keine Ausnahme ausgelöst wird, können Sie die Methode erfolgreich abgeschlossen wurde davon ausgehen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-164">As long as an exception is not thrown, you can assume the method completed successfully.</span></span> <span data-ttu-id="93a0c-165">Für zusätzliche Validierung können Sie auch [Überprüfen Sie die SOAP-Antwort, um die Ergebnisse zu überprüfen](#bk_verifysoap).</span><span class="sxs-lookup"><span data-stu-id="93a0c-165">For additional validation, you can also [check the SOAP response to verify the results](#bk_verifysoap).</span></span>
  
### <a name="handling-errors-warnings-and-exceptions"></a><span data-ttu-id="93a0c-166">Behandlung von Fehlern, Warnungen und Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="93a0c-166">Handling errors, warnings, and exceptions</span></span>
<span data-ttu-id="93a0c-167"><a name="bk_ewsmaerrors"> </a></span><span class="sxs-lookup"><span data-stu-id="93a0c-167"></span></span>

<span data-ttu-id="93a0c-168">Wenn EWS Managed API Code eine **Ausnahme**auslöst, können Sie den Wert [Exception.Message](http://msdn.microsoft.com/EN-US/library/9btwf6wk) , um die Ursache des Fehlers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-168">If your EWS Managed API code throws an **Exception**, you can use the [Exception.Message](http://msdn.microsoft.com/EN-US/library/9btwf6wk) value to determine the source of the error.</span></span> <span data-ttu-id="93a0c-169">Die **Message** -Eigenschaft enthält den Inhalt des [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) -Elements in der zugrunde liegenden SOAP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="93a0c-169">The **Message** property contains the contents of the [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) element in the underlying SOAP response.</span></span> <span data-ttu-id="93a0c-170">Darüber hinaus ist die Ausnahme vom Typ [ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) -Objekts, der am häufigsten verwendeten Ausnahmen, können Sie auch die [ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) in das zugrunde liegende SOAP- [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element und die [Antwort](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) enthaltenen abrufen Diese Eigenschaft das zugeordnete [ServiceResponse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) -Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="93a0c-170">In addition, if the exception is of type [ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) object, one of the most common exceptions, you can also retrieve the [ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) contained in the underlying SOAP [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element, and the [Response](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) property that identifies the associated [ServiceResponse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="93a0c-171">Der folgende Code zeigt, wie abgefangen und den Inhalt einer **ServiceResponseException**anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-171">The following code shows how to catch and display the contents of a **ServiceResponseException**.</span></span> 
  
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

<span data-ttu-id="93a0c-172">Wenn die aufgerufenen Methode eine **ServiceResponseCollection gibt**und der Wert der Eigenschaft **OverallResult** **Warnung** oder **Fehler**gleich ist, müssen Sie jedes Objekt in der **ServiceResponseCollection** zu durchlaufen Suchen Sie nach dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="93a0c-172">If the method you called returns a **ServiceResponseCollection**, and the value of the **OverallResult** property is equal to **Warning** or **Error**, you'll have to loop through each object in the **ServiceResponseCollection** to find the error.</span></span> <span data-ttu-id="93a0c-173">Die **OverallResult** -Eigenschaft wird auf **Warnung** festgelegt, wenn mindestens eine Antwort **Ergebnis** Wert auf **Warnung** festgelegt wurde und alle anderen Antworten ihren Werten **Ergebnis** **Erfolg**haben.</span><span class="sxs-lookup"><span data-stu-id="93a0c-173">The **OverallResult** property is set to **Warning** if at least one response has its **Result** value set to **Warning** and all other responses have their **Result** values set to **Success**.</span></span> <span data-ttu-id="93a0c-174">Die **OverallResult** -Eigenschaft wird auf **Fehler** festgelegt, wenn mindestens eine Antwort **Ergebnis** Wert auf **Fehler**festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="93a0c-174">The **OverallResult** property is set to **Error** if at least one response has its **Result** value set to **Error**.</span></span> <span data-ttu-id="93a0c-175">Wenn die **OverallResult** auf **Warnung** oder **Fehler**festgelegt ist, werden die folgenden Eigenschaften für die Objekte **ServiceResponse** entsprechend festgelegt:</span><span class="sxs-lookup"><span data-stu-id="93a0c-175">When the **OverallResult** is set to **Warning** or **Error**, the following properties are set on the **ServiceResponse** objects as appropriate:</span></span> 
  
- <span data-ttu-id="93a0c-176">[ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) – enthält den Fehlercode, die verwendet werden kann, zusätzliche Ressourcen zur Problembehandlung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93a0c-176">[ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="93a0c-177">[ErrorDetails](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) – enthält Details zu dem Fehler für einige **ErrorCodes**.</span><span class="sxs-lookup"><span data-stu-id="93a0c-177">[ErrorDetails](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) — Contains details about the error for some **ErrorCodes**.</span></span> <span data-ttu-id="93a0c-178">Beispielsweise bei der Fehlercode **ErrorRecurrenceHasNoOccurrence**ist, wird die **ErrorDetails** Schlüssel für **EffectiveStartDate** und **EffectiveEndDate**enthalten.</span><span class="sxs-lookup"><span data-stu-id="93a0c-178">For example, when the error code is **ErrorRecurrenceHasNoOccurrence**, the **ErrorDetails** will contain keys for **EffectiveStartDate** and **EffectiveEndDate**.</span></span> 
    
- <span data-ttu-id="93a0c-179">[ErrorMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) – den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="93a0c-179">[ErrorMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="93a0c-180">[ErrorProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) – sofern verfügbar, identifiziert die Eigenschaften, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="93a0c-180">[ErrorProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) — If available, identifies the properties that caused the error.</span></span> <span data-ttu-id="93a0c-181">Wenn der Fehlercode **ErrorInvalidPropertyForOperation**ist, enthält **ErrorProperties** beispielsweise die Definition der Eigenschaft, die für die Anforderung ungültig war.</span><span class="sxs-lookup"><span data-stu-id="93a0c-181">For example, when the error code is **ErrorInvalidPropertyForOperation**, **ErrorProperties** contains the definition of the property that was invalid for the request.</span></span> 
    
- <span data-ttu-id="93a0c-182">[Ergebnis](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) – enthält **Fehler** oder einer **Warnung** , wenn ein Problem aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="93a0c-182">[Result](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) — Contains **Error** or **Warning** when an issue is encountered.</span></span> 
    
<span data-ttu-id="93a0c-183">Wenn die Informationen von den Eigenschaften **ServiceResponse** bereitgestellt nicht genügend Informationen, um Ihre Methodenaufruf korrigieren oder Aufheben der Blockierung Sie, finden Sie unter [Nächste Schritte](#bk_nextsteps) , um weitere Informationen zu Werten **ErrorCode** einsteigen.</span><span class="sxs-lookup"><span data-stu-id="93a0c-183">If the information provided by the **ServiceResponse** properties doesn't provide enough information to correct your method call or unblock you, see [Next steps](#bk_nextsteps) to dig up more information on **ErrorCode** values.</span></span> 
  
## 
<span data-ttu-id="93a0c-184"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="93a0c-184"></span></span>

<span data-ttu-id="93a0c-185">Sie können zusätzliche Informationen zur Problembehandlung in den folgenden Themen suchen:</span><span class="sxs-lookup"><span data-stu-id="93a0c-185">You can look up additional troubleshooting information in the following topics:</span></span>
  
- <span data-ttu-id="93a0c-186">[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -element</span><span class="sxs-lookup"><span data-stu-id="93a0c-186">[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element</span></span> 
    
- <span data-ttu-id="93a0c-187">[ServiceError](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) -Aufzählung</span><span class="sxs-lookup"><span data-stu-id="93a0c-187">[ServiceError](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) enumeration</span></span> 
    
- [<span data-ttu-id="93a0c-188">EWS-Eigenschaft-bezogene Fehler</span><span class="sxs-lookup"><span data-stu-id="93a0c-188">EWS property-related errors</span></span>](ews-property-related-errors.md)
    
<span data-ttu-id="93a0c-189">Darüber hinaus je nachdem, was Sie in Ihrer Anforderung erreichen gerade, möglicherweise zusätzliche hilfreich finden Sie Informationen zu den Fehlercode in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="93a0c-189">In addition, depending on what you're trying to accomplish in your request, you might find additional helpful information about the error code in the following topics:</span></span>
  
- [<span data-ttu-id="93a0c-190">Behandeln von AutoErmittlungs-Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="93a0c-190">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
- [<span data-ttu-id="93a0c-191">Fehlerbehandlung Benachrichtigung-bezogene in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="93a0c-191">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="93a0c-192">Fehlerbehandlung Synchronisierung-bezogene in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="93a0c-192">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="93a0c-193">Fehlerbehandlung Löschung-bezogene in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="93a0c-193">Handling deletion-related errors in EWS in Exchange</span></span>](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="93a0c-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93a0c-194">See also</span></span>


- [<span data-ttu-id="93a0c-195">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="93a0c-195">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="93a0c-196">Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange</span><span class="sxs-lookup"><span data-stu-id="93a0c-196">Tools and resources for troubleshooting EWS applications for Exchange</span></span>](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

