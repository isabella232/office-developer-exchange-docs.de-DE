---
title: Erstellen eines SmtpReceiveAgent Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: Erfahren Sie, wie Sie einen benutzerdefinierten SmtpReceiveAgent Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
ms.openlocfilehash: a74d5baae6334c5e17acb6335206964b48f320e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757299"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="80da1-103">Erstellen eines SmtpReceiveAgent Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="80da1-103">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="80da1-104">Erfahren Sie, wie Sie einen benutzerdefinierten SmtpReceiveAgent Transport-Agent für die Verwendung mit Exchange 2013 erstellen.</span><span class="sxs-lookup"><span data-stu-id="80da1-104">Find out how to create a custom SmtpReceiveAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="80da1-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="80da1-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="80da1-106">Verwandte Codeabschnitte und Beispiel-apps:</span><span class="sxs-lookup"><span data-stu-id="80da1-106">Related code snippets and sample apps:</span></span>

- [<span data-ttu-id="80da1-107">Exchange 2013: Erstellen eines Stelle Konvertierung Transport-Agents</span><span class="sxs-lookup"><span data-stu-id="80da1-107">Exchange 2013: Build a body conversion transport agent</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
<span data-ttu-id="80da1-108">Die Klassen [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) und [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) können Sie das Verhalten der Front-End-Transportdienst auf einem Client Access Server oder den Transportdienst auf einem Postfachserver zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="80da1-108">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes enable you to extend the behavior of the Front End Transport service on a Client Access Server or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="80da1-109">Diese Klassen können Sie um Transport-Agents zu implementieren, mit denen auf Nachrichten antworten, wie sie in Ihrer Organisation stammen.</span><span class="sxs-lookup"><span data-stu-id="80da1-109">You can use these classes to implement transport agents that are designed to respond to messages as they come into your organization.</span></span> 
  
<span data-ttu-id="80da1-110">Die Klassen [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) und [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) enthalten, die in der folgenden Tabelle aufgeführten Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="80da1-110">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes include the events listed in the following table.</span></span> 
  
<span data-ttu-id="80da1-111">**In Tabelle 1. SmtpReceiveAgent-Klassenereignisse**</span><span class="sxs-lookup"><span data-stu-id="80da1-111">**Table 1. SmtpReceiveAgent class events**</span></span>

|<span data-ttu-id="80da1-112">Document.SelectionChanged **-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="80da1-112">**Event**</span></span>|<span data-ttu-id="80da1-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80da1-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80da1-114">OnAuthCommand</span><span class="sxs-lookup"><span data-stu-id="80da1-114">OnAuthCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |<span data-ttu-id="80da1-115">Wird verwendet, wenn der Agent Informationen, die nur in den Befehl SMTP- **AUTH** bereitgestellt wird, erfordert wie ein Agent, der annimmt oder ablehnt versucht, eine Nachricht basierend auf den Typ der Authentifizierungsmethode übermitteln.</span><span class="sxs-lookup"><span data-stu-id="80da1-115">Use when your agent requires information that is provided only in the SMTP **AUTH** command, such as an agent that accepts or rejects attempts to deliver a message based on the type of authentication method used.</span></span>  <br/> |
|[<span data-ttu-id="80da1-116">OnConnect</span><span class="sxs-lookup"><span data-stu-id="80da1-116">OnConnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |<span data-ttu-id="80da1-117">Wird verwendet, wenn der Agent Informationen erforderlich, die bereitgestellt wird sind, nur, wenn eine Verbindung über SMTP auf den Front-End-Transport-Dienst, wie ein Agent geöffnet wird, das eine Aktion basierend auf dem Adresse oder die Domäne des SMTP-Remoteserver verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="80da1-117">Use when your agent requires information that is provided only when a connection is opened via SMTP to the Front End Transport service, such as an agent that performs an action based on the address or domain of the remote SMTP server.</span></span>  <br/> |
|[<span data-ttu-id="80da1-118">OnDataCommand</span><span class="sxs-lookup"><span data-stu-id="80da1-118">OnDataCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |<span data-ttu-id="80da1-119">Verwenden Sie dieses Ereignis, wenn der Agent Informationen erforderlich sind, die im SMTP- **DATA** -Befehl bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="80da1-119">Use this event when your agent requires information that is provided in the SMTP **DATA** command.</span></span>  <br/> |
|[<span data-ttu-id="80da1-120">OnDisconnect</span><span class="sxs-lookup"><span data-stu-id="80da1-120">OnDisconnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |<span data-ttu-id="80da1-121">Wird verwendet, wenn der Agent Informationen erforderlich, verfügbar zum Zeitpunkt der Trennung, wie etwa das aktuelle Datum und Uhrzeit sind, um Berechnungen Zeit ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="80da1-121">Use when your agent requires information that is available at the time of disconnection, such as the current date and time, in order to perform time calculations.</span></span>  <br/> |
|[<span data-ttu-id="80da1-122">OnEhloCommand</span><span class="sxs-lookup"><span data-stu-id="80da1-122">OnEhloCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |<span data-ttu-id="80da1-123">Wird verwendet, wenn der Agent Informationen erforderlich sind, die in den SMTP- **EHLO** -Befehl bereitgestellt wird; Wenn beispielsweise der Agent akzeptiert oder lehnt Nachrichten auf Grundlage der Identität in den **EHLO** -Befehl bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="80da1-123">Use when your agent requires information that is provided in the SMTP **EHLO** command; for example, if your agent accepts or rejects messages based on the identity provided in the **EHLO** command.</span></span>  <br/> |
|[<span data-ttu-id="80da1-124">OnEndOfAuthentication</span><span class="sxs-lookup"><span data-stu-id="80da1-124">OnEndOfAuthentication</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |<span data-ttu-id="80da1-125">Wird verwendet, wenn der Agent Informationen erforderlich, die sind nach der Remoteserver den Authentifizierungsprozess abgeschlossen ist; zum Beispiel für ein Agent, der eine Aktion für eine Nachricht basierend auf die von der remote-SMTP-Server oder Client bereitgestellten Authentifizierungsinformationen ausführt.</span><span class="sxs-lookup"><span data-stu-id="80da1-125">Use when your agent requires information that is available after the remote server completes the authentication process; for example, for an agent that performs an action on a message based on the authentication information provided by the remote SMTP server or client.</span></span>  <br/> |
|[<span data-ttu-id="80da1-126">"OnEndofData"</span><span class="sxs-lookup"><span data-stu-id="80da1-126">OnEndOfData</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |<span data-ttu-id="80da1-127">Wird verwendet, wenn der Agent ausführen muss, eine Aktion basierend auf Daten, die in der Nachricht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="80da1-127">Use when your agent must perform an action based on data that is available in the message.</span></span> <span data-ttu-id="80da1-128">Dieses Ereignis wird nicht ausgelöst, auf den Front-End-Transport-Dienst.</span><span class="sxs-lookup"><span data-stu-id="80da1-128">This event will not fire on the Front End Transport service.</span></span> <span data-ttu-id="80da1-129">Wenn Ihre Transport-Agent muss dieses Ereignis verwendet werden, müssen Sie ihn auf einem Postfachserver zu installieren.</span><span class="sxs-lookup"><span data-stu-id="80da1-129">If your transport agent has to use this event, you have to install it on a Mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="80da1-130">"OnEndOfHeaders"</span><span class="sxs-lookup"><span data-stu-id="80da1-130">OnEndOfHeaders</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |<span data-ttu-id="80da1-131">Wird verwendet, wenn der Agent ausführen muss, eine Aktion basierend auf Informationen, die in den Kopfzeilen der gesendete Nachricht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="80da1-131">Use when your agent must perform an action based on information that is available in the headers of the submitted message.</span></span>  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a><span data-ttu-id="80da1-132">Erstellen eines benutzerdefinierten SmtpReceiveAgent Transport-Agents</span><span class="sxs-lookup"><span data-stu-id="80da1-132">Creating a custom SmtpReceiveAgent transport agent</span></span>

<span data-ttu-id="80da1-133">Das folgende Verfahren beschreibt, wie Sie einen benutzerdefinierten SmtpReceiveAgent Transport-Agent zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="80da1-133">The following procedure describes how to create a custom SmtpReceiveAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="80da1-134">So erstellen Sie den Transport-agent</span><span class="sxs-lookup"><span data-stu-id="80da1-134">To create the transport agent</span></span>

1. <span data-ttu-id="80da1-135">Fügen Sie Verweise auf die Namespaces hinzu.</span><span class="sxs-lookup"><span data-stu-id="80da1-135">Add references to the namespaces.</span></span>
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   <span data-ttu-id="80da1-136">Diese Namespaces finden Sie auf Ihrem Exchange 2013-Server.</span><span class="sxs-lookup"><span data-stu-id="80da1-136">You can find these namespaces on your Exchange 2013 server.</span></span> <span data-ttu-id="80da1-137">Wenn Sie einen Verweis auf die Namespaces hinzufügen, haben Sie Zugriff auf die Member [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) sowie andere Klassen in der [Exchange 2013: Erstellen Sie einen Textkörper Konvertierung Transport-Agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) Beispiel.</span><span class="sxs-lookup"><span data-stu-id="80da1-137">When you add a reference to these namespaces, you will have access to the [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a body conversion transport agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) sample.</span></span> 
    
2. <span data-ttu-id="80da1-138">Implementieren Sie die für die [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) -Klasse abgeleitete Klasse.</span><span class="sxs-lookup"><span data-stu-id="80da1-138">Implement the derived class for the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) class.</span></span> 
    
   ```cs
      public class BodyConversionFactory : SmtpReceiveAgentFactory
      {
          /// <summary>
          /// Create a new BodyConversion
          /// </summary>
          /// <param name="server">Exchange server</param>
          /// <returns>A new BodyConversion</returns>
          public override SmtpReceiveAgent CreateAgent(SmtpServer server)
          {
              return new BodyConversion();
          }
      }
  
   ```

   <span data-ttu-id="80da1-139">Dieser Code abgeleitete Klasse instanziieren und überschreiben Sie die **Hilfe von CreateAgent** -Methode zum Erstellen einer Instanz des neuen benutzerdefinierten Agents.</span><span class="sxs-lookup"><span data-stu-id="80da1-139">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> 
    
3. <span data-ttu-id="80da1-140">Definieren des Agents.</span><span class="sxs-lookup"><span data-stu-id="80da1-140">Define your agent.</span></span>
    
   ```cs
     public class BodyConversion : SmtpReceiveAgent
      {
          // Your custom code goes here
          /// <summary>
          /// The constructor registers an end of data event handler.
          /// </summary>
          public BodyConversion()
          {
              Debug.WriteLine("[BodyConversion] Agent constructor");
              this.OnEndOfData += new EndOfDataEventHandler(this.OnEndOfDataHandler);
          }
      }
  
   ```

   <span data-ttu-id="80da1-141">Nachdem Sie Ihre Agent-Klasse definiert haben, können Sie Ihre benutzerdefinierten Funktionalität hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="80da1-141">After you define your agent class, you can add your custom functionality.</span></span> <span data-ttu-id="80da1-142">In diesem Beispiel wird das Ereignis ["OnEndofData"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) an den benutzerdefinierten Ereignishandler umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="80da1-142">In this example, the [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) event is redirected to your custom event handler.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="80da1-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80da1-143">See also</span></span>

- [<span data-ttu-id="80da1-144">Transport-Agent Konzepte in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="80da1-144">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="80da1-145">Transport-Agent-Referenz für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="80da1-145">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="80da1-146">SmtpReceiveAgentFactory</span><span class="sxs-lookup"><span data-stu-id="80da1-146">SmtpReceiveAgentFactory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [<span data-ttu-id="80da1-147">SmtpReceiveAgent</span><span class="sxs-lookup"><span data-stu-id="80da1-147">SmtpReceiveAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

