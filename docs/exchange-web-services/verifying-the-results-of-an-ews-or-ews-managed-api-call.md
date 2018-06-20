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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757135"
---
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a>Überprüfen der Ergebnisse eines Aufrufs EWS oder EWS Managed API

Erfahren Sie, wie die Ergebnisse der EWS oder EWS Managed API Anrufe zu überprüfen.
  
Wenn Dinge nicht ordnungsgemäß funktionieren, sollten sie finden Sie unter Was passiert, durch die SOAP-Anforderungen, die über das Netzwerk und die Antworten, die der Server wieder sendet, sendet die Anwendung untersuchen. [Tools und Ressourcen für die Problembehandlung EWS-Applikationen](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) Artikel enthält Links zu Tools, mit denen erfassen und diese SOAP-Anforderungen anzuzeigen. Nachdem Sie die Anforderungen und die Antworten haben, wie überprüfen Sie, ob die Anforderung an den Server gesendeten ordnungsgemäß verarbeitet wurde? Lesen Sie weiter unten finden Sie. 
  
Wenn Sie EWS-Anforderungen senden, können Sie ihm Ihre Überprüfung starten, indem Sie das **ResponseClass** -Attribut für jede Antwortnachricht in der Antwort überprüfen. Die erfahren Sie, ob der Vorgang für jedes Element erfolgreich abgeschlossen. 
  
Je nach dem Objekt anfordert, dass Ihre Methode aufruft, wenn Sie zum Senden die EWS Managed API verwenden, Sie einige Überprüfung mithilfe der Antwortobjekte machen können. Aber, da die SOAP-Antwort eine Obermenge enthält von was in die EWS Managed API-Antwort-Objekte enthalten ist, möglicherweise möchten Sie die SOAP-Antwort betrachten. Da die SOAP-Antwort oft mehr Informationen als die EWS Managed API-Antwort-Objekte enthalten kann, starten Sie die Überprüfung mit der SOAP-Antwort.
  
## <a name="verifying-the-results-of-a-soap-response"></a>Überprüfen der Ergebnisse einer SOAP-Antwort
<a name="bk_verifysoap"> </a>

Wenn Sie die SOAP-Antwort erhalten, wird als erstes betrachten das **ResponseClass** -Attribut. Dieses Attribut ist in jeder Instanz **ResponseMessageType** im [ResponseMessages](http://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) -Element enthalten, wie im folgenden Beispiel dargestellt. 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

Da SOAP-Antwort möglicherweise mehrere Antwortnachrichten in einer einzelnen SOAP-Antwort enthält, ist es wichtig, um jede Antwortnachricht einzeln zu überprüfen.
  
Wenn Sie mit einem Vorgang arbeiten, die als Teil der Antwort auf einen Vorgang, wie im folgenden eine **ResponseClass** enthält möglicherweise versucht, nur die **ResponseClass** des Vorgangs überprüfen. 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

Jedoch gibt der Ausführungsstatus nur gibt die Form der Antwort auf oberster Ebene und nicht den Status der einzelnen Nachricht-Antworten entspricht. Im folgenden Beispiel die [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) -Operation besteht aus einem **ResponseClass** des **Erfolgs**, aber das zugrunde liegende [DelegateUserResponseMessageType](http://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) -Element hat den Wert **ResponseClass** **Fehler**.
  
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

So für SOAP-EWS-Antworten Sie auf die **ResponseClass** des Vorgangs verlassen können nicht - müssen Sie sehen Sie sich die **ResponseClass** jeder Nachricht Antwort, um festzustellen, ob der Vorgang Verarbeitung der Elemente Fehler aufgetreten. 
  
### <a name="verifying-success"></a>Überprüfen des Erfolgs des Updates

Wenn jedes **ResponseClass** -Attribut für jedes **ResponseMessage** -Attribut auf **Erfolg**, der Vorgang erfolgreich abgeschlossen auf alle Elemente festgelegt ist, und Sie können auf die nächste Aufgabe verschieben.
  
Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -Vorgang, um ein einzelnes Element abzurufen. Beachten Sie, dass bei **Erfolg**der **ResponseClass** festgelegt ist, die zugeordneten [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) immer **NoError**festgelegt ist.
  
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

Im folgenden finden eine erfolgreiche Antwort auf eine Anforderung **GetItem** -Vorgang, um mehrere Elemente abzurufen. Jedes Element [GetItemResponseMessage](http://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) verfügt über eine **ResponseClass** des **Erfolgs**.
  
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

### <a name="handling-errors-and-warnings"></a>Behandlung von Fehlern und Warnungen

Wenn Sie eine Antwort erhalten, und das Attribut **ResponseClass** auf **Fehler**festgelegt ist, wurde die Operation auf ein oder mehrere Elemente nicht erfolgreich abgeschlossen. Korrigieren Sie das Problem, und wiederholen Sie die Anforderung oder der Teil der erfolgreichen Anforderung. Ein Attributwert **ResponseClass** **Warnung** Wert wird nur von der Operation [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) zurückgegeben, und gibt an, dass die Entität nicht in eine eindeutige Identität aufgelöst werden konnte. Sie können für alle anderen Vorgänge ignoriert wird. 
  
In der folgenden Antwort hat das **ResponseClass** -Attribut den Wert des **Fehlers**.
  
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

In diesem Beispiel bietet EWS Hinweise, um das Problem zu debuggen. Wenn das **ResponseClass** -Attribut den Wert **Fehler**hat, werden die folgenden zusätzlichen Elemente in der Antwort ggf. enthalten:
  
- [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) – den Fehler beschreibt. 
    
- [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) – enthält den Fehlercode, die verwendet werden kann, zusätzliche Ressourcen zur Problembehandlung zu erhalten. 
    
- [MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) – identifiziert die Elemente, die den Fehler verursacht hat. 
    
- [DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) – nicht verwendet. 
    
Die Informationen in dieser Elemente können Sie um Ihr Problem zu untersuchen. Im vorherigen Beispiel gibt die **MessageText** , dass die Eigenschaft nicht für den Objekttyp gültig ist. Die Anforderung war zu eine e-Mail-Nachricht erhalten möchten, aber Eigenschaftensatzes enthalten die **AssociatedCalendarItemId**, das nur für Terminelemente gültig ist.
  
Das folgende Beispiel zeigt einen Fehler, der als Teil eines Vorgangs im Batchmodus abzurufenden mehrere e-Mail-Elemente empfangen wurde. Das erste Element erfolgreich abgerufen wurde, und die **ResponseClass** auf **Erfolg**festgelegt ist. Das zweite Element konnte nicht gefunden werden, und die **ResponseClass** auf **Fehler**festgelegt ist.
  
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

Wenn ein oder mehrere Elemente in einer Anforderung im Batch nicht verarbeitet werden können, wie angefordert, für jedes Element, das nicht erfolgreich ist ein Fehler zurückgegeben, und die restlichen Elemente in den Batch verarbeitet wie erwartet. Fehler im Batch-Verarbeitung können auftreten, wenn das Element wurde gelöscht, und daher nicht gesendet, abgerufen, oder aktualisiert werden, oder wenn das Element in einem anderen Ordner verschoben, und daher eine neues Element-ID. hat Da die Operation für einige Elemente beendet und kein Fehler zurückgegeben, wenn ein oder mehrere Elemente nicht verarbeitet werden können, ist es wichtig, um jedes **ResponseClass** -Attribut zu überprüfen, bevor Sie den nächsten Vorgang fortfahren. 
  
Wenn die Metriken aufgelistet, die Antwortelemente nicht Ihnen helfen, korrigieren Ihre Anforderung oder Entsperren Sie andernfalls, finden Sie unter [Nächste Schritte](#bk_nextsteps).
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a>Überprüfen der Ergebnisse eines Methodenaufrufs EWS Managed API
<a name="bk_successful"> </a>

Wenn Sie die EWS Managed API und eine Methode für ein Objekt [ExchangeService](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) aufrufen, wird die Methode wahrscheinlich eine [ServiceResponseCollection](http://msdn.microsoft.com/EN-US/library/dd633715%28v=exchg.80%29.aspx) -Objekt zurück, das enthält eine Auflistung von [ServiceResponse](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) -Objekten, oder eine Auflistung von Objekte aus der **ServiceResponse** Objekte abgeleitet. Die **ServiceResponseCollection** und enthalten **ServiceResponse** -Objekte enthalten Informationen über das Ergebnis des Methodenaufrufs, die Sie verwenden können, um Ihre Ergebnisse zu überprüfen. 
  
Wenn Sie die EWS Managed API und Aufrufen einer Methode für ein [Element](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) -Objekt oder eines der abgeleitete Objekte, die wahrscheinlich-Methode nicht zurück Response-Objekt für den Erfolg zu überprüfen, sondern löst eine [Ausnahme](http://msdn.microsoft.com/EN-US/library/c18k6c59) aus, wenn die Methode nicht abgeschlossen wurde erfolgreich. 
  
### <a name="verifying-success"></a>Überprüfen des Erfolgs des Updates

Ein Vorteil die EWS Managed API ist, dass beim Umgang mit mehreren Elementen in eine Antwort ein Gesamtstatus bereitgestellt. Wenn eine **ServiceResponseCollection**von die aufgerufenen Methode zurückgegeben wird, können Sie also überprüfen, dass die [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) -Eigenschaft der **ServiceResponseCollection** [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)gleich ist. In diesem Fall wurden alle Elemente in der im Batchmodus Vorgang erfolgreich abgeschlossen wurde; Sie müssen nicht jedes Objekt **ServiceResponse** einzeln zu prüfen. Wenn die **OverallResult** -Eigenschaft nicht auf **ServiceResult.Success**festgelegt ist, müssen Sie [die Fehlermeldung oder einer Warnung zu behandeln](#bk_ewsmaerrors).
  
Wenn die-Methode, die Sie Aufrufen einer **ServiceResponseCollection**gibt keine zurück, jedoch ein **ServiceResponse** -Objekt zurückgibt, müssen Sie den Wert der **Result** -Eigenschaft überprüfen. Wenn der Wert **Ergebnis** **Erfolg**festgelegt ist, wissen Sie die Methode erfolgreich abgeschlossen wurde.
  
Wenn die Methode, die Sie aufrufen keinen Rückgabewert hat, ist es wirklich nicht möglich, überprüfen Sie für den Erfolg über die EWS Managed-API. Solange keine Ausnahme ausgelöst wird, können Sie die Methode erfolgreich abgeschlossen wurde davon ausgehen. Für zusätzliche Validierung können Sie auch [Überprüfen Sie die SOAP-Antwort, um die Ergebnisse zu überprüfen](#bk_verifysoap).
  
### <a name="handling-errors-warnings-and-exceptions"></a>Behandlung von Fehlern, Warnungen und Ausnahmen
<a name="bk_ewsmaerrors"> </a>

Wenn EWS Managed API Code eine **Ausnahme**auslöst, können Sie den Wert [Exception.Message](http://msdn.microsoft.com/EN-US/library/9btwf6wk) , um die Ursache des Fehlers zu bestimmen. Die **Message** -Eigenschaft enthält den Inhalt des [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) -Elements in der zugrunde liegenden SOAP-Antwort. Darüber hinaus ist die Ausnahme vom Typ [ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) -Objekts, der am häufigsten verwendeten Ausnahmen, können Sie auch die [ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) in das zugrunde liegende SOAP- [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element und die [Antwort](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) enthaltenen abrufen Diese Eigenschaft das zugeordnete [ServiceResponse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) -Objekt identifiziert. Der folgende Code zeigt, wie abgefangen und den Inhalt einer **ServiceResponseException**anzuzeigen. 
  
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

Wenn die aufgerufenen Methode eine **ServiceResponseCollection gibt**und der Wert der Eigenschaft **OverallResult** **Warnung** oder **Fehler**gleich ist, müssen Sie jedes Objekt in der **ServiceResponseCollection** zu durchlaufen Suchen Sie nach dem Fehler. Die **OverallResult** -Eigenschaft wird auf **Warnung** festgelegt, wenn mindestens eine Antwort **Ergebnis** Wert auf **Warnung** festgelegt wurde und alle anderen Antworten ihren Werten **Ergebnis** **Erfolg**haben. Die **OverallResult** -Eigenschaft wird auf **Fehler** festgelegt, wenn mindestens eine Antwort **Ergebnis** Wert auf **Fehler**festgelegt wurde. Wenn die **OverallResult** auf **Warnung** oder **Fehler**festgelegt ist, werden die folgenden Eigenschaften für die Objekte **ServiceResponse** entsprechend festgelegt: 
  
- [ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) – enthält den Fehlercode, die verwendet werden kann, zusätzliche Ressourcen zur Problembehandlung zu erhalten. 
    
- [ErrorDetails](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) – enthält Details zu dem Fehler für einige **ErrorCodes**. Beispielsweise bei der Fehlercode **ErrorRecurrenceHasNoOccurrence**ist, wird die **ErrorDetails** Schlüssel für **EffectiveStartDate** und **EffectiveEndDate**enthalten. 
    
- [ErrorMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) – den Fehler beschreibt. 
    
- [ErrorProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) – sofern verfügbar, identifiziert die Eigenschaften, die den Fehler verursacht hat. Wenn der Fehlercode **ErrorInvalidPropertyForOperation**ist, enthält **ErrorProperties** beispielsweise die Definition der Eigenschaft, die für die Anforderung ungültig war. 
    
- [Ergebnis](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) – enthält **Fehler** oder einer **Warnung** , wenn ein Problem aufgetreten ist. 
    
Wenn die Informationen von den Eigenschaften **ServiceResponse** bereitgestellt nicht genügend Informationen, um Ihre Methodenaufruf korrigieren oder Aufheben der Blockierung Sie, finden Sie unter [Nächste Schritte](#bk_nextsteps) , um weitere Informationen zu Werten **ErrorCode** einsteigen. 
  
## 
<a name="bk_nextsteps"> </a>

Sie können zusätzliche Informationen zur Problembehandlung in den folgenden Themen suchen:
  
- [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -element 
    
- [ServiceError](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) -Aufzählung 
    
- [EWS-Eigenschaft-bezogene Fehler](ews-property-related-errors.md)
    
Darüber hinaus je nachdem, was Sie in Ihrer Anforderung erreichen gerade, möglicherweise zusätzliche hilfreich finden Sie Informationen zu den Fehlercode in den folgenden Themen:
  
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)
    
- [Fehlerbehandlung Benachrichtigung-bezogene in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Fehlerbehandlung Synchronisierung-bezogene in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Fehlerbehandlung Löschung-bezogene in EWS in Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

