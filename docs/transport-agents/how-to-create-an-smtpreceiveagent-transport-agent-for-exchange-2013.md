---
title: Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: Erfahren Sie, wie Sie einen benutzerdefinierten SmtpReceiveAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
ms.openlocfilehash: 5ba021d02849ffc7e125029f0fd18ebf14c3f8da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459139"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="8538b-103">Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8538b-103">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="8538b-104">Erfahren Sie, wie Sie einen benutzerdefinierten SmtpReceiveAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.</span><span class="sxs-lookup"><span data-stu-id="8538b-104">Find out how to create a custom SmtpReceiveAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="8538b-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="8538b-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="8538b-106">Zugehörige Codeausschnitte und Beispiel-apps:</span><span class="sxs-lookup"><span data-stu-id="8538b-106">Related code snippets and sample apps:</span></span>

- [<span data-ttu-id="8538b-107">Exchange 2013: Erstellen eines Transport-Agents für die Text Konvertierung</span><span class="sxs-lookup"><span data-stu-id="8538b-107">Exchange 2013: Build a body conversion transport agent</span></span>](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
<span data-ttu-id="8538b-108">Mit der [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) -und der [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) -Klasse können Sie das Verhalten des Front-End-Transportdiensts auf einem Client Zugriffsserver oder dem Transportdienst auf einem Postfachserver erweitern.</span><span class="sxs-lookup"><span data-stu-id="8538b-108">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes enable you to extend the behavior of the Front End Transport service on a Client Access Server or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="8538b-109">Sie können diese Klassen verwenden, um Transport-Agents zu implementieren, die darauf ausgelegt sind, auf Nachrichten zu reagieren, wenn Sie in Ihrer Organisation eingehen.</span><span class="sxs-lookup"><span data-stu-id="8538b-109">You can use these classes to implement transport agents that are designed to respond to messages as they come into your organization.</span></span> 
  
<span data-ttu-id="8538b-110">Die [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) -und [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) -Klassen umfassen die in der folgenden Tabelle aufgeführten Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="8538b-110">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes include the events listed in the following table.</span></span> 
  
<span data-ttu-id="8538b-111">**Tabelle 1. Ereignisse der SmtpReceiveAgent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8538b-111">**Table 1. SmtpReceiveAgent class events**</span></span>

|<span data-ttu-id="8538b-112">**Event**</span><span class="sxs-lookup"><span data-stu-id="8538b-112">**Event**</span></span>|<span data-ttu-id="8538b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8538b-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8538b-114">OnAuthCommand</span><span class="sxs-lookup"><span data-stu-id="8538b-114">OnAuthCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |<span data-ttu-id="8538b-115">Verwenden Sie diese Methode, wenn Ihr Agent Informationen benötigt, die nur im SMTP- **Authentifizierungs** Befehl bereitgestellt werden, beispielsweise ein Agent, der versucht, eine Nachricht basierend auf dem Typ der verwendeten Authentifizierungsmethode zu übertragen oder abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="8538b-115">Use when your agent requires information that is provided only in the SMTP **AUTH** command, such as an agent that accepts or rejects attempts to deliver a message based on the type of authentication method used.</span></span>  <br/> |
|[<span data-ttu-id="8538b-116">OnConnect</span><span class="sxs-lookup"><span data-stu-id="8538b-116">OnConnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |<span data-ttu-id="8538b-117">Wird verwendet, wenn Ihr Agent Informationen benötigt, die nur beim Öffnen einer Verbindung über SMTP für den Front-End-Transport-Dienst bereitgestellt werden, beispielsweise ein Agent, der eine Aktion basierend auf der Adresse oder Domäne des SMTP-Remoteservers ausführt.</span><span class="sxs-lookup"><span data-stu-id="8538b-117">Use when your agent requires information that is provided only when a connection is opened via SMTP to the Front End Transport service, such as an agent that performs an action based on the address or domain of the remote SMTP server.</span></span>  <br/> |
|[<span data-ttu-id="8538b-118">OnDataCommand</span><span class="sxs-lookup"><span data-stu-id="8538b-118">OnDataCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |<span data-ttu-id="8538b-119">Verwenden Sie dieses Ereignis, wenn Ihr Agent Informationen benötigt, die im SMTP-Befehl **Data** bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8538b-119">Use this event when your agent requires information that is provided in the SMTP **DATA** command.</span></span>  <br/> |
|[<span data-ttu-id="8538b-120">OnDisconnect</span><span class="sxs-lookup"><span data-stu-id="8538b-120">OnDisconnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |<span data-ttu-id="8538b-121">Verwenden Sie diese Aktion, wenn Ihr Agent Informationen benötigt, die zum Zeitpunkt der Verbindungstrennung zur Verfügung stehen, beispielsweise das aktuelle Datum und die Uhrzeit, um Zeitberechnungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8538b-121">Use when your agent requires information that is available at the time of disconnection, such as the current date and time, in order to perform time calculations.</span></span>  <br/> |
|[<span data-ttu-id="8538b-122">OnEhloCommand</span><span class="sxs-lookup"><span data-stu-id="8538b-122">OnEhloCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |<span data-ttu-id="8538b-123">Verwenden Sie diese Funktion, wenn Ihr Agent Informationen benötigt, die im SMTP-Befehl **EHLO** bereitgestellt werden. Wenn Ihr Agent beispielsweise Nachrichten annimmt oder ablehnt, basierend auf der im Befehl **EHLO** angegebenen Identität.</span><span class="sxs-lookup"><span data-stu-id="8538b-123">Use when your agent requires information that is provided in the SMTP **EHLO** command; for example, if your agent accepts or rejects messages based on the identity provided in the **EHLO** command.</span></span>  <br/> |
|[<span data-ttu-id="8538b-124">OnEndOfAuthentication</span><span class="sxs-lookup"><span data-stu-id="8538b-124">OnEndOfAuthentication</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |<span data-ttu-id="8538b-125">Verwenden Sie dieses Verfahren, wenn Ihr Agent Informationen benötigt, die nach Abschluss des Authentifizierungsprozesses durch den Remoteserver verfügbar sind. beispielsweise für einen Agent, der eine Aktion für eine Nachricht basierend auf den vom Remote-SMTP-Server oder-Client bereitgestellten Authentifizierungsinformationen ausführt.</span><span class="sxs-lookup"><span data-stu-id="8538b-125">Use when your agent requires information that is available after the remote server completes the authentication process; for example, for an agent that performs an action on a message based on the authentication information provided by the remote SMTP server or client.</span></span>  <br/> |
|[<span data-ttu-id="8538b-126">OnEndOfData</span><span class="sxs-lookup"><span data-stu-id="8538b-126">OnEndOfData</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |<span data-ttu-id="8538b-127">Wird verwendet, wenn Ihr Agent eine Aktion basierend auf Daten ausführen muss, die in der Nachricht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="8538b-127">Use when your agent must perform an action based on data that is available in the message.</span></span> <span data-ttu-id="8538b-128">Dieses Ereignis wird nicht für den Front-End-Transport-Dienst ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8538b-128">This event will not fire on the Front End Transport service.</span></span> <span data-ttu-id="8538b-129">Wenn Ihr Transport-Agent dieses Ereignis verwenden muss, müssen Sie es auf einem Postfachserver installieren.</span><span class="sxs-lookup"><span data-stu-id="8538b-129">If your transport agent has to use this event, you have to install it on a Mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="8538b-130">OnEndOfHeaders</span><span class="sxs-lookup"><span data-stu-id="8538b-130">OnEndOfHeaders</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |<span data-ttu-id="8538b-131">Wird verwendet, wenn Ihr Agent eine Aktion basierend auf Informationen ausführen muss, die in den Kopfzeilen der übermittelten Nachricht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8538b-131">Use when your agent must perform an action based on information that is available in the headers of the submitted message.</span></span>  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a><span data-ttu-id="8538b-132">Erstellen eines benutzerdefinierten SmtpReceiveAgent-Transport-Agents</span><span class="sxs-lookup"><span data-stu-id="8538b-132">Creating a custom SmtpReceiveAgent transport agent</span></span>

<span data-ttu-id="8538b-133">Im folgenden Verfahren wird beschrieben, wie ein benutzerdefinierter SmtpReceiveAgent-Transport-Agent erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8538b-133">The following procedure describes how to create a custom SmtpReceiveAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="8538b-134">So erstellen Sie den Transport-Agent</span><span class="sxs-lookup"><span data-stu-id="8538b-134">To create the transport agent</span></span>

1. <span data-ttu-id="8538b-135">Fügen Sie Verweise auf die Namespaces hinzu.</span><span class="sxs-lookup"><span data-stu-id="8538b-135">Add references to the namespaces.</span></span>
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   <span data-ttu-id="8538b-136">Sie können diese Namespaces auf Ihrem Exchange 2013 Server finden.</span><span class="sxs-lookup"><span data-stu-id="8538b-136">You can find these namespaces on your Exchange 2013 server.</span></span> <span data-ttu-id="8538b-137">Wenn Sie einen Verweis auf diese Namespaces hinzufügen, haben Sie Zugriff auf die [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) -Member sowie auf andere Klassen, die im [Exchange 2013: Beispiel zum Erstellen eines Body Conversion Transport-Agents](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8538b-137">When you add a reference to these namespaces, you will have access to the [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a body conversion transport agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) sample.</span></span> 
    
2. <span data-ttu-id="8538b-138">Implementieren Sie die abgeleitete Klasse für die [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="8538b-138">Implement the derived class for the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) class.</span></span> 
    
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

   <span data-ttu-id="8538b-139">Mit diesem Code wird die abgeleitete Klasse instanziiert und die **createagent** -Methode überschrieben, um eine Instanz des neuen benutzerdefinierten Agents zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8538b-139">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> 
    
3. <span data-ttu-id="8538b-140">Definieren Sie Ihren Agent.</span><span class="sxs-lookup"><span data-stu-id="8538b-140">Define your agent.</span></span>
    
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

   <span data-ttu-id="8538b-141">Nachdem Sie die agentklasse definiert haben, können Sie Ihre benutzerdefinierte Funktionalität hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8538b-141">After you define your agent class, you can add your custom functionality.</span></span> <span data-ttu-id="8538b-142">In diesem Beispiel wird das [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) -Ereignis an Ihren benutzerdefinierten Ereignishandler umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8538b-142">In this example, the [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) event is redirected to your custom event handler.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8538b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8538b-143">See also</span></span>

- [<span data-ttu-id="8538b-144">Transport-Agent-Konzepte in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8538b-144">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="8538b-145">Transport-Agent-Referenz für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8538b-145">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="8538b-146">SmtpReceiveAgentFactory</span><span class="sxs-lookup"><span data-stu-id="8538b-146">SmtpReceiveAgentFactory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [<span data-ttu-id="8538b-147">SmtpReceiveAgent</span><span class="sxs-lookup"><span data-stu-id="8538b-147">SmtpReceiveAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

