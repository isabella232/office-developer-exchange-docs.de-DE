---
title: TRACE-Anfragen und Antworten für die Problembehandlung bei EWS Managed API-apps
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 186c1d1d-b8dc-4914-b3cd-6fada7ecd877
description: Erfahren Sie, wie Sie EWS-Anforderungen und Antworten zum Beheben von Fehlern in die EWS Managed API-Anwendung zu verfolgen.
ms.openlocfilehash: 056a1f84c4172b0404975d6fc35f9ecd7395ecdb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756999"
---
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a>TRACE-Anfragen und Antworten für die Problembehandlung bei EWS Managed API-apps

Erfahren Sie, wie Sie EWS-Anforderungen und Antworten zum Beheben von Fehlern in die EWS Managed API-Anwendung zu verfolgen.
  
Debuggen einer Web Service-basierte Anwendung kann schwierig sein, da ein Teil der Verarbeitung auf einem Remotecomputer ausgeführt wird, die möglicherweise nicht auf. Da Sie den Code auf dem Server schrittweise ist nicht möglich, kann es hilfreich sein, finden in der XML-Anforderungen und Antworten, die zwischen dem Client und dem Server, um zu bestimmen, welcher Teil der Anwendung einen Fehler verursacht gesendet werden. 
  
Wenn Sie Exchange-Webdienste verwenden, verfügen Sie bereits über Zugriff auf die XML-Anfrage und-Antwort; Sie können einen Haltepunkt in Ihrem Code zum Überprüfen des Servers als Antwort auf Ihre Anforderung, um ein Problem zu behandeln ablegen. Wenn Sie die EWS Managed API verwenden, haben Sie nicht direkten Zugriff auf die EWS-Anforderung und Antwort. Jedoch können Tracing-Methoden für das Objekt [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) Sie die XML-Anfrage und-Antwort erfassen, und klicken Sie dann können den XML-Code um zu ermitteln, warum Ihr Code nicht funktioniert. 

Wenn Sie eine Eigenschaft nicht richtig festgelegt haben, erhalten Sie möglicherweise eine unerwartete Antwort ein, und Sie können die Ablaufverfolgungsausgaben betrachten Sie die XML-Anforderung und Antwort zur Identifikation des Fehlers. Die Trace-Ausgabe aus der EWS Managed API können auch die XML-Anfrage zum Erstellen einer Anwendung EWS manuell erstellen. Wenn Sie Exchange-Webdienste verwenden, können Sie eine kleine Anwendung mithilfe von EWS Managed API erstellen, verfolgen sie und klicken Sie dann die XML-Anforderungsinformationen verwenden, um beim Erstellen von Ihrer EWS-Anforderung. 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a>Aktivieren der Ablaufverfolgung auf dem ExchangeService-Objekt
<a name="bk_EnableTracing"> </a>

Um Sie zu aktivieren, erstellen Sie ein [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für die Anwendung, und legen Sie die Verfolgung Eigenschaften, wie im folgenden Beispiel dargestellt. 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

Nachdem Sie die [TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) -Eigenschaft auf **true**festgelegt, werden alle Anfragen, die die Ablaufverfolgungsflags entsprechen dem angegebenen Trace-Listener versendet. Können Sie ein einzelnes Ablaufverfolgungsflag angeben, oder Sie können mehrere Ablaufverfolgungsflags durch Kombinieren mit ein logisches **OR**angeben. Die [TraceFlags-Enumeration](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) können Sie Werte für EWS und für die AutoErmittlung-Anforderungen und-Antworten angeben. 
  
## <a name="implementing-a-tracelistener-object"></a>Implementieren eines TraceListener-Objekts
<a name="bk_traceListener"> </a>

Sie können die [TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) -Eigenschaft auf **true fest,** um die XML-Anforderungen und Antworten auf die Anwendung aus, wie einem Konsolenfenster auszugeben festlegen. Wenn Sie die Trace-Ausgabe zu steuern und in einer Datei speichern möchten, wird empfohlen, dass Sie ein Objekt [TraceListener-Klasse](http://msdn.microsoft.com/en-us/library/system.diagnostics.tracelistener.aspx) implementieren. Das folgende Codebeispiel zeigt ein einfaches-Objekt, das die [ITraceListener](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) -Schnittstelle implementiert und speichert die verfolgten Anforderungen und Antworten in XML oder Textdateien. 
  
```cs
class TraceListener : ITraceListener
{
    #region ITraceListener Members
    public void Trace(string traceType, string traceMessage)
    {
      CreateXMLTextFile(traceType, traceMessage.ToString());
    }
    #endregion
    private void CreateXMLTextFile(string fileName, string traceContent)
    {
      // Create a new XML file for the trace information.
      try
      {
        // If the trace data is valid XML, create an XmlDocument object and save.
        XmlDocument xmlDoc = new XmlDocument();
        xmlDoc.Load(traceContent);
        xmlDoc.Save(fileName + ".xml");
      }
      catch
      {
        // If the trace data is not valid XML, save it as a text document.
        System.IO.File.WriteAllText(fileName + ".txt", traceContent);
      }
    }
}

```

## <a name="see-also"></a>Siehe auch

- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)    
- [Verweisen auf die Assembly EWS Managed API](how-to-reference-the-ews-managed-api-assembly.md)    
- [Kommunizieren Sie mit Exchange-Webdienste mithilfe der EWS Managed API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

