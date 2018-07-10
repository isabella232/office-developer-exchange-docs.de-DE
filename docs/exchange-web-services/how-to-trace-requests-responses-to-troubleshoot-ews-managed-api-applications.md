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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756999"
---
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a><span data-ttu-id="d86cb-103">TRACE-Anfragen und Antworten für die Problembehandlung bei EWS Managed API-apps</span><span class="sxs-lookup"><span data-stu-id="d86cb-103">Trace requests and responses to troubleshoot EWS Managed API apps</span></span>

<span data-ttu-id="d86cb-104">Erfahren Sie, wie Sie EWS-Anforderungen und Antworten zum Beheben von Fehlern in die EWS Managed API-Anwendung zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="d86cb-104">Find out how to trace EWS requests and responses to troubleshoot errors in your EWS Managed API application.</span></span>
  
<span data-ttu-id="d86cb-105">Debuggen einer Web Service-basierte Anwendung kann schwierig sein, da ein Teil der Verarbeitung auf einem Remotecomputer ausgeführt wird, die möglicherweise nicht auf.</span><span class="sxs-lookup"><span data-stu-id="d86cb-105">Debugging a web service-based application can be difficult because part of the processing is performed on a remote computer that you might not have access to.</span></span> <span data-ttu-id="d86cb-106">Da Sie den Code auf dem Server schrittweise ist nicht möglich, kann es hilfreich sein, finden in der XML-Anforderungen und Antworten, die zwischen dem Client und dem Server, um zu bestimmen, welcher Teil der Anwendung einen Fehler verursacht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d86cb-106">Because you cannot step through the code on the server, it can be helpful to see the XML requests and responses that are sent between the client and the server to determine which part of the application is causing an error.</span></span> 
  
<span data-ttu-id="d86cb-107">Wenn Sie Exchange-Webdienste verwenden, verfügen Sie bereits über Zugriff auf die XML-Anfrage und-Antwort; Sie können einen Haltepunkt in Ihrem Code zum Überprüfen des Servers als Antwort auf Ihre Anforderung, um ein Problem zu behandeln ablegen.</span><span class="sxs-lookup"><span data-stu-id="d86cb-107">If you are using EWS, you already have access to the XML request and response; you can put a break point in your code to review the server's response to your request in order to troubleshoot an issue.</span></span> <span data-ttu-id="d86cb-108">Wenn Sie die EWS Managed API verwenden, haben Sie nicht direkten Zugriff auf die EWS-Anforderung und Antwort.</span><span class="sxs-lookup"><span data-stu-id="d86cb-108">If you're using the EWS Managed API, you don't have direct access to the EWS request and response.</span></span> <span data-ttu-id="d86cb-109">Jedoch können Tracing-Methoden für das Objekt [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) Sie die XML-Anfrage und-Antwort erfassen, und klicken Sie dann können den XML-Code um zu ermitteln, warum Ihr Code nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d86cb-109">However, you can use tracing methods on the [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object to capture the XML request and response, and you can then use the XML to determine why your code is not working.</span></span> 

<span data-ttu-id="d86cb-110">Wenn Sie eine Eigenschaft nicht richtig festgelegt haben, erhalten Sie möglicherweise eine unerwartete Antwort ein, und Sie können die Ablaufverfolgungsausgaben betrachten Sie die XML-Anforderung und Antwort zur Identifikation des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="d86cb-110">For example, if you did not set a property correctly, you might get an unexpected response, and you can use the trace output to look at the XML request and response to identify the error.</span></span> <span data-ttu-id="d86cb-111">Die Trace-Ausgabe aus der EWS Managed API können auch die XML-Anfrage zum Erstellen einer Anwendung EWS manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="d86cb-111">The trace output from the EWS Managed API can also help you manually build the XML request to create your EWS application.</span></span> <span data-ttu-id="d86cb-112">Wenn Sie Exchange-Webdienste verwenden, können Sie eine kleine Anwendung mithilfe von EWS Managed API erstellen, verfolgen sie und klicken Sie dann die XML-Anforderungsinformationen verwenden, um beim Erstellen von Ihrer EWS-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d86cb-112">If you are using EWS, you can create a small application by using EWS Managed API, trace it, and then use the XML request information to help you build your EWS request.</span></span> 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a><span data-ttu-id="d86cb-113">Aktivieren der Ablaufverfolgung auf dem ExchangeService-Objekt</span><span class="sxs-lookup"><span data-stu-id="d86cb-113">Enabling tracing on the ExchangeService object</span></span>
<span data-ttu-id="d86cb-114"><a name="bk_EnableTracing"> </a></span><span class="sxs-lookup"><span data-stu-id="d86cb-114"></span></span>

<span data-ttu-id="d86cb-115">Um Sie zu aktivieren, erstellen Sie ein [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für die Anwendung, und legen Sie die Verfolgung Eigenschaften, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d86cb-115">To enable tracing, create an [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for your application, and set the tracing properties as shown in the following example.</span></span> 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

<span data-ttu-id="d86cb-116">Nachdem Sie die [TraceEnabled](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) -Eigenschaft auf **true**festgelegt, werden alle Anfragen, die die Ablaufverfolgungsflags entsprechen dem angegebenen Trace-Listener versendet.</span><span class="sxs-lookup"><span data-stu-id="d86cb-116">After you set the [TraceEnabled](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true**, all requests that match the trace flags will be sent to the specified trace listener.</span></span> <span data-ttu-id="d86cb-117">Können Sie ein einzelnes Ablaufverfolgungsflag angeben, oder Sie können mehrere Ablaufverfolgungsflags durch Kombinieren mit ein logisches **OR**angeben.</span><span class="sxs-lookup"><span data-stu-id="d86cb-117">You can specify a single trace flag, or you can specify multiple trace flags by combining them with a logical **OR**.</span></span> <span data-ttu-id="d86cb-118">Die [TraceFlags-Enumeration](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) können Sie Werte für EWS und für die AutoErmittlung-Anforderungen und-Antworten angeben.</span><span class="sxs-lookup"><span data-stu-id="d86cb-118">You can use the [TraceFlags enumeration](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) to specify values for EWS and for Autodiscover requests and responses.</span></span> 
  
## <a name="implementing-a-tracelistener-object"></a><span data-ttu-id="d86cb-119">Implementieren eines TraceListener-Objekts</span><span class="sxs-lookup"><span data-stu-id="d86cb-119">Implementing a TraceListener object</span></span>
<span data-ttu-id="d86cb-120"><a name="bk_traceListener"> </a></span><span class="sxs-lookup"><span data-stu-id="d86cb-120"></span></span>

<span data-ttu-id="d86cb-121">Sie können die [TraceEnabled](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) -Eigenschaft auf **true fest,** um die XML-Anforderungen und Antworten auf die Anwendung aus, wie einem Konsolenfenster auszugeben festlegen.</span><span class="sxs-lookup"><span data-stu-id="d86cb-121">You can set the [TraceEnabled](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true** to output the XML requests and responses to your application, such as a console window.</span></span> <span data-ttu-id="d86cb-122">Wenn Sie die Trace-Ausgabe zu steuern und in einer Datei speichern möchten, wird empfohlen, dass Sie ein Objekt [TraceListener-Klasse](http://msdn.microsoft.com/de-de/library/system.diagnostics.tracelistener.aspx) implementieren.</span><span class="sxs-lookup"><span data-stu-id="d86cb-122">If you want to control the trace output and save it to a file, we recommend that you implement a [TraceListener class](http://msdn.microsoft.com/de-de/library/system.diagnostics.tracelistener.aspx) object.</span></span> <span data-ttu-id="d86cb-123">Das folgende Codebeispiel zeigt ein einfaches-Objekt, das die [ITraceListener](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) -Schnittstelle implementiert und speichert die verfolgten Anforderungen und Antworten in XML oder Textdateien.</span><span class="sxs-lookup"><span data-stu-id="d86cb-123">The following code example shows a simple object that implements the [ITraceListener](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) interface and stores the traced requests and responses in XML or text files.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="d86cb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d86cb-124">See also</span></span>

- [<span data-ttu-id="d86cb-125">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="d86cb-125">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
- [<span data-ttu-id="d86cb-126">Behandeln von AutoErmittlungs-Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="d86cb-126">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)    
- [<span data-ttu-id="d86cb-127">Verweisen auf die Assembly EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="d86cb-127">Reference the EWS Managed API assembly</span></span>](how-to-reference-the-ews-managed-api-assembly.md)    
- [<span data-ttu-id="d86cb-128">Kommunizieren Sie mit Exchange-Webdienste mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="d86cb-128">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

