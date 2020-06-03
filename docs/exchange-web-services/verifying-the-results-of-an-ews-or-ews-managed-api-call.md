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
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a>Überprüfen der Ergebnisse eines EWS- oder verwalteten EWS-API-Aufrufs

Erfahren Sie, wie Sie die Ergebnisse ihrer EWS-oder verwaltete EWS-API-Anrufe überprüfen können.
  
Wenn die Dinge nicht ordnungsgemäß funktionieren, können Sie sehen, was passiert, indem Sie die SOAP-Anforderungen untersuchen, die Ihre Anwendung über das Netzwerk sendet, und die Antworten, die der Server zurücksendet. Der Artikel [Tools und Ressourcen für die Problembehandlung für EWS-Anwendungen](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) enthält Links zu Tools, mit denen Sie diese SOAP-Anforderungen erfassen und anzeigen können. Wie stellen Sie sicher, dass die an den Server gesendete Anforderung ordnungsgemäß verarbeitet wurde, nachdem Sie die Anforderungen und Antworten erhalten haben? Lesen Sie weiter, um es herauszufinden. 
  
Wenn Sie EWS-Anforderungen senden, werden Sie mit der Überprüfung beginnen, indem Sie das **ResponseClass** -Attribut für jede Antwortnachricht in der Antwort überprüfen. Dadurch erfahren Sie, ob der Vorgang für jedes Element erfolgreich abgeschlossen wurde. 
  
Abhängig vom Objekt, das von der Methode aufgerufen wird, können Sie, wenn Sie die verwaltete EWS-API zum Senden von Anforderungen verwenden, einige Überprüfungen mithilfe der Response-Objekte durchführen. Da die SOAP-Antwort jedoch eine Obermenge dessen enthält, was in den verwaltete EWS-API-Antwort Objekten enthalten ist, sollten Sie sich auch die SOAP-Antwort ansehen. Da die SOAP-Antwort häufig mehr Informationen als die verwaltete EWS-API-Antwortobjekte enthalten kann, starten Sie die Überprüfung mit der SOAP-Antwort.
  
## <a name="verifying-the-results-of-a-soap-response"></a>Überprüfen der Ergebnisse einer SOAP-Antwort
<a name="bk_verifysoap"> </a>

Wenn Sie eine SOAP-Antwort erhalten, ist das **ResponseClass** -Attribut das erste, was Sie beachten sollten. Dieses Attribut ist in jeder **ResponseMessageType** -Instanz im [ResponseMessages](https://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) -Element enthalten, wie im folgenden Beispiel dargestellt. 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

Da eine SOAP-Antwort möglicherweise mehrere Antwortnachrichten in einer einzigen SOAP-Antwort enthalten kann, ist es wichtig, jede Antwortnachricht einzeln zu überprüfen.
  
Wenn Sie mit einer Operation arbeiten, die ein **ResponseClass** -Element als Teil der Vorgangs Antwort enthält, wie im folgenden Beispiel, könnten Sie versucht sein, die **ResponseClass** des Vorgangs nur zu überprüfen. 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

Der Vorgangsstatus gibt jedoch nur die Form der Antwort auf oberster Ebene wieder und gibt nicht den Status aller einzelnen Nachrichten Antworten an. Im folgenden Beispiel weist der [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) -Vorgang ein **ResponseClass** **auf, aber**das zugrunde liegende [DelegateUserResponseMessageType](https://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) -Element weist den **ResponseClass** -Wert **Error**auf.
  
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

Für SOAP-EWS-Antworten können Sie sich also nicht auf den **ResponseClass** des Vorgangs verlassen – Sie müssen sich die **ResponseClass** jeder Antwortnachricht ansehen, um zu bestimmen, ob der Vorgang Fehler bei der Verarbeitung der Elemente aufgetreten ist. 
  
### <a name="verifying-success"></a>Überprüfen des Erfolgs

Wenn jedes **ResponseClass** -Attribut für jedes **ResponseMessage** -Attribut auf " **erfolgreich**" festgelegt ist, wurde der Vorgang für alle Elemente erfolgreich abgeschlossen, und Sie können mit der nächsten Aufgabe fortfahren.
  
Im folgenden Beispiel wird eine erfolgreiche Antwort auf eine [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -Vorgangsanforderung zum Abrufen eines einzelnen Elements gezeigt. Beachten Sie, dass beim Festlegen von **ResponseClass** auf " **Success**" die zugeordnete [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) immer auf " **noError**" festgelegt ist.
  
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

Im folgenden finden Sie eine erfolgreiche Antwort auf eine **GetItem** -Vorgangsanforderung zum Abrufen mehrerer Elemente. Jedes der [GetItemResponseMessage](https://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) -Elemente hat einen **ResponseClass** **Erfolg**.
  
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

### <a name="handling-errors-and-warnings"></a>Behandeln von Fehlern und Warnungen

Wenn Sie eine Antwort erhalten und das **ResponseClass** -Attribut auf **Error**festgelegt ist, wurde der Vorgang für mindestens ein Element nicht erfolgreich abgeschlossen. Beheben Sie das Problem, und wiederholen Sie Ihre Anforderung oder den Teil Ihrer Anforderung, der fehlgeschlagen ist. Ein **ResponseClass** -Attributwert des **Warning** -Werts wird nur von der [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) -Operation zurückgegeben und gibt an, dass die Entität nicht in eine eindeutige Identität aufgelöst werden konnte. Sie können Sie für alle anderen Vorgänge ignorieren. 
  
In der folgenden Antwort hat das **ResponseClass** -Attribut den Wert **Error**.
  
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

In diesem Beispiel bietet EWS Anhaltspunkte zum Debuggen des Problems. Wenn das **ResponseClass** -Attribut den Wert **Error**aufweist, sind die folgenden zusätzlichen Elemente in der Antwort enthalten, wenn zutreffend:
  
- [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) – beschreibt den Fehler. 
    
- [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) – enthält den Fehlercode, der zum Auffinden zusätzlicher Ressourcen zur Problembehandlung verwendet werden kann. 
    
- [Messagexml verwendet](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) – gibt die Elemente an, die den Fehler verursacht haben. 
    
- [DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) – nicht verwendet. 
    
Sie können die in diesen Elementen bereitgestellten Informationen verwenden, um Ihr Problem zu untersuchen. Im vorherigen Beispiel gibt die **MessageText** an, dass die Eigenschaft nicht für den Objekttyp gültig ist. Die Anforderung bestand darin, eine e-Mail-Nachricht zu erhalten, aber der Eigenschaftensatz enthielt die **AssociatedCalendarItemId**, die nur für Termin Elemente gültig ist.
  
Das folgende Beispiel zeigt einen Fehler, der als Teil eines Batchvorgangs empfangen wurde, um mehrere e-Mail-Elemente abzurufen. Das erste Element wurde erfolgreich abgerufen, und die **ResponseClass** **ist auf "erfolgreich"** festgelegt. Das zweite Element konnte nicht gefunden werden, und die **ResponseClass** ist auf **Error**festgelegt.
  
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

Wenn ein oder mehrere Elemente in einer Batchanforderung nicht wie angefordert verarbeitet werden können, wird für jedes fehlgeschlagene Element ein Fehler zurückgegeben, und die restlichen Elemente im Batch werden wie erwartet verarbeitet. Fehler in der Batchverarbeitung können auftreten, wenn das Element gelöscht wurde und daher nicht gesendet, abgerufen oder aktualisiert werden kann oder wenn das Element in einen anderen Ordner verschoben wurde und daher über eine neue Element-ID verfügt. Da der Vorgang für einige Elemente abgeschlossen wird und kein Fehler zurückgegeben wird, wenn ein oder mehrere Elemente nicht verarbeitet werden können, ist es wichtig, jedes **ResponseClass** -Attribut zu überprüfen, bevor Sie mit dem nächsten Vorgang fortfahren. 
  
Wenn die von den Antwortelementen bereitgestellten Informationen Ihnen nicht helfen, Ihre Anforderung zu korrigieren oder Sie anderweitig aufzuheben, lesen Sie die [nächsten Schritte](#bk_nextsteps).
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a>Überprüfen der Ergebnisse eines verwaltete EWS-API-Methodenaufrufs
<a name="bk_successful"> </a>

Wenn Sie die verwaltete EWS-API verwenden und eine Methode für ein [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt aufrufen, gibt die Methode wahrscheinlich ein [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) -Objekt zurück, das eine Auflistung von [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) -Objekten enthält, oder eine Sammlung von Objekten, die von den **ServiceResponse** -Objekten abgeleitet sind. Die **ServiceResponseCollection** -und die include- **ServiceResponse** -Objekte enthalten Informationen über das Ergebnis des Methodenaufrufs, den Sie zum Überprüfen der Ergebnisse verwenden können. 
  
Wenn Sie die verwaltete EWS-API verwenden und eine Methode für ein [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) -Objekt oder eines der abgeleiteten Objekte aufrufen, gibt die Methode wahrscheinlich kein Response-Objekt zurück, um den Erfolg zu überprüfen, löst jedoch eine [Ausnahme](https://msdn.microsoft.com/library/c18k6c59) aus, wenn die Methode nicht erfolgreich abgeschlossen wird. 
  
### <a name="verifying-success"></a>Überprüfen des Erfolgs

Ein Vorteil der Verwendung der verwaltete EWS-API besteht darin, dass Sie einen allgemeinen Status bereitstellt, wenn Sie mit mehreren Elementen in einer Antwort umgehen. Wenn also die aufgerufene Methode ein **ServiceResponseCollection**-Objekt zurückgibt, können Sie überprüfen, ob die [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) -Eigenschaft des **ServiceResponseCollection** gleich [ServiceResult. Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)ist. Wenn dies der Fall ist, wurden alle Elemente im Batchprozess erfolgreich abgeschlossen; Sie müssen nicht jedes **ServiceResponse** -Objekt einzeln überprüfen. Wenn die **OverallResult** -Eigenschaft nicht auf **ServiceResult. Success**festgelegt ist, müssen Sie [den Fehler oder die Warnung behandeln](#bk_ewsmaerrors).
  
Wenn die aufgerufene Methode keinen **ServiceResponseCollection**zurückgibt, aber ein **ServiceResponse** -Objekt zurückgibt, müssen Sie den Wert der **Result** -Eigenschaft überprüfen. Wenn der **Ergebnis** Wert auf " **Success**" festgelegt ist, wissen Sie, dass die Methode erfolgreich abgeschlossen wurde.
  
Wenn die Methode, die Sie aufrufen, keinen Rückgabewert hat, gibt es wirklich keine Möglichkeit, über den verwaltete EWS-API auf Erfolg zu überprüfen. Solange keine Ausnahme ausgelöst wird, können Sie davon ausgehen, dass die Methode erfolgreich abgeschlossen wurde. Zur weiteren Überprüfung können Sie auch [die SOAP-Antwort überprüfen, um die Ergebnisse zu über](#bk_verifysoap)prüfen.
  
### <a name="handling-errors-warnings-and-exceptions"></a>Behandeln von Fehlern, Warnungen und Ausnahmen
<a name="bk_ewsmaerrors"> </a>

Wenn Ihr verwaltete EWS-API Code eine **Ausnahme**auslöst, können Sie den [Exception. Message](https://msdn.microsoft.com/library/9btwf6wk) -Wert verwenden, um die Ursache des Fehlers zu ermitteln. Die **Message** -Eigenschaft enthält den Inhalt des [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) -Elements in der zugrunde liegenden SOAP-Antwort. Darüber hinaus können Sie, wenn die Ausnahme vom Typ [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) -Objekt ist, eine der häufigsten Ausnahmen, auch den im zugrunde liegenden SOAP- [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element enthaltenen [errorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) und die [Response](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) -Eigenschaft, die das zugeordnete [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) -Objekt identifiziert, abrufen. Im folgenden Code wird gezeigt, wie der Inhalt eines **ServiceResponseException**abgefangen und angezeigt wird. 
  
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

Wenn die aufgerufene Methode ein **ServiceResponseCollection**-Objekt zurückgibt und der Wert der **OverallResult** -Eigenschaft gleich **Warning** oder **Error**ist, müssen Sie alle Objekte in der **ServiceResponseCollection** durchlaufen, um den Fehler zu finden. Die **OverallResult** -Eigenschaft ist auf **Warning** festgelegt, wenn mindestens eine Antwort den **Ergebnis** Wert auf **Warning** festgelegt hat und alle anderen Antworten ihre **Ergebnis** Werte auf " **erfolgreich**" festgelegt haben. Die **OverallResult** -Eigenschaft ist auf **Error** festgelegt, wenn mindestens eine Antwort den **Ergebnis** Wert auf **Error**festgelegt hat. Wenn **OverallResult** auf **Warning** oder **Error**festgelegt ist, werden die folgenden Eigenschaften für die **ServiceResponse** -Objekte entsprechend festgelegt: 
  
- [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) – enthält den Fehlercode, der zum Auffinden zusätzlicher Ressourcen zur Problembehandlung verwendet werden kann. 
    
- [ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) – enthält Details zum Fehler für einige **errorCodes**. Wenn der Fehlercode beispielsweise **ErrorRecurrenceHasNoOccurrence**lautet, enthält der **ErrorDetails** Schlüssel für **EffectiveStartDate** und **EffectiveEndDate**. 
    
- [ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) – beschreibt den Fehler. 
    
- [ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) – sofern verfügbar, werden die Eigenschaften identifiziert, die den Fehler verursacht haben. Wenn der Fehlercode beispielsweise **ErrorInvalidPropertyForOperation**lautet, enthält **ErrorProperties** die Definition der Eigenschaft, die für die Anforderung ungültig war. 
    
- [Ergebnis](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) – enthält **Fehler** oder **Warnungen** , wenn ein Problem auftritt. 
    
Wenn die von den **ServiceResponse** -Eigenschaften bereitgestellten Informationen nicht genügend Informationen zur Korrektur des Methodenaufrufs oder zum Aufheben der Blockierung bereitstellen, finden Sie weitere Informationen zu **errorCode** -Werten in den [nächsten Schritten](#bk_nextsteps) . 
  
## 
<a name="bk_nextsteps"> </a>

Weitere Informationen zur Problembehandlung finden Sie in den folgenden Themen:
  
- [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element 
    
- [Service Error](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) -Aufzählung 
    
- [Mit der EWS-Eigenschaft zusammenhängende Fehler](ews-property-related-errors.md)
    
Je nachdem, was Sie in Ihrer Anforderung erreichen möchten, finden Sie darüber hinaus möglicherweise weitere hilfreiche Informationen zum Fehlercode in den folgenden Themen:
  
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)
    
- [Umgang von Fehlern im Zusammenhang mit Benachrichtigungen in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Umgang mit Fehlern in Exchange im Zusammenhang mit Löschungen in EWS](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

