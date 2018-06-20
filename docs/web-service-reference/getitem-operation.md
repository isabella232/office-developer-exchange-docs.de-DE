---
title: GetItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: Hier finden Sie Informationen zu den GetItem-EWS Vorgang.
ms.openlocfilehash: 9b63032b2eaa3bf26027a42e38bfa06bedcbac86
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758718"
---
# <a name="getitem-operation"></a><span data-ttu-id="c1b73-103">GetItem Operation</span><span class="sxs-lookup"><span data-stu-id="c1b73-103">GetItem operation</span></span>

<span data-ttu-id="c1b73-104">Hier finden Sie Informationen zu den **GetItem** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c1b73-104">Find information about the **GetItem** EWS operation.</span></span> 
  
<span data-ttu-id="c1b73-105">Die **GetItem** Operation ruft Elemente aus dem Exchange-Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="c1b73-105">The **GetItem** operation gets items from the Exchange store.</span></span> 
  
## <a name="using-the-getitem-operation"></a><span data-ttu-id="c1b73-106">Verwenden des GetItem-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="c1b73-106">Using the GetItem operation</span></span>

<span data-ttu-id="c1b73-107">Die **GetItem** Operation gibt viele Elementeigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="c1b73-107">The **GetItem** operation returns many item properties.</span></span> <span data-ttu-id="c1b73-108">Die Eigenschaften, die in einer Antwort **GetItem** zurückgegeben werden hängen die angeforderte Form angeforderte zusätzliche Eigenschaften und den Typ des Elements zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c1b73-108">The properties that are returned in a **GetItem** response vary based on the requested shape, requested additional properties, and the type of item returned.</span></span> 
  
<span data-ttu-id="c1b73-109">[Nachrichtenelemente](message-ex15websvcsotherref.md) darstellen, e-Mail-Nachrichten und andere Elemente, die vom Exchange-Webdienste (EWS) Schema nicht stark typisiert sind.</span><span class="sxs-lookup"><span data-stu-id="c1b73-109">[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="c1b73-110">Elemente wie IPM.Sharing- und IPM.InfoPath-Elemente werden als [Message](message-ex15websvcsotherref.md)-Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c1b73-110">Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements.</span></span> <span data-ttu-id="c1b73-111">Exchange gibt das [Element](item.md)-Basiselement nicht in Antworten zurück.</span><span class="sxs-lookup"><span data-stu-id="c1b73-111">Exchange does not return the base [Item](item.md) element in responses.</span></span> 
  
<span data-ttu-id="c1b73-112">Die **GetItem** Operation gibt keine Anlagen zurück.</span><span class="sxs-lookup"><span data-stu-id="c1b73-112">The **GetItem** operation does not return attachments.</span></span> <span data-ttu-id="c1b73-113">Es gibt Metadaten zu einem angefügte Element oder eine Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="c1b73-113">It does return metadata about an attached item or file.</span></span> <span data-ttu-id="c1b73-114">Wenn eine Anlage zurückgeben möchten, verwenden Sie die [-Vorgangs GetAttachment](getattachment-operation.md).</span><span class="sxs-lookup"><span data-stu-id="c1b73-114">To return an attachment, use the [GetAttachment operation](getattachment-operation.md).</span></span>
  
## <a name="getitem-operation-soap-headers"></a><span data-ttu-id="c1b73-115">GetItem Operation SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="c1b73-115">GetItem operation SOAP headers</span></span>

<span data-ttu-id="c1b73-116">Die **GetItem** Operation können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="c1b73-116">The **GetItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c1b73-117">Kopfzeile \*\*\*</span><span class="sxs-lookup"><span data-stu-id="c1b73-117">****Header****</span></span>|<span data-ttu-id="c1b73-118">****Element****</span><span class="sxs-lookup"><span data-stu-id="c1b73-118">****Element****</span></span>|<span data-ttu-id="c1b73-119">****Beschreibung****</span><span class="sxs-lookup"><span data-stu-id="c1b73-119">****Description****</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1b73-120">**DateTimePrecision**</span><span class="sxs-lookup"><span data-stu-id="c1b73-120">**DateTimePrecision**</span></span> <br/> |[<span data-ttu-id="c1b73-121">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="c1b73-121">DateTimePrecision</span></span>](datetimeprecision.md) <br/> |<span data-ttu-id="c1b73-122">Gibt die Auflösung der Daten-/Uhrzeitwerte in Antworten vom Server an, entweder in Sekunden oder in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="c1b73-122">Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds.</span></span>  <br/> |
|<span data-ttu-id="c1b73-123">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="c1b73-123">**Impersonation**</span></span> <br/> |[<span data-ttu-id="c1b73-124">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="c1b73-124">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c1b73-125">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="c1b73-125">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="c1b73-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="c1b73-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="c1b73-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c1b73-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c1b73-128">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1b73-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="c1b73-129">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c1b73-129">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c1b73-130">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c1b73-130">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c1b73-131">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="c1b73-131">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="c1b73-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="c1b73-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="c1b73-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c1b73-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c1b73-134">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="c1b73-134">Identifies the version of the server that responded to the request.</span></span>  <br/> |
|<span data-ttu-id="c1b73-135">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="c1b73-135">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="c1b73-136">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="c1b73-136">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="c1b73-137">Gibt die Zeitzone für alle Antworten vom Server an.</span><span class="sxs-lookup"><span data-stu-id="c1b73-137">Identifies the time zone to be used for all responses from the server.</span></span>  <br/> |
   
## <a name="in-this-section"></a><span data-ttu-id="c1b73-138">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="c1b73-138">In This Section</span></span>

[<span data-ttu-id="c1b73-139">GetItem-Vorgang (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="c1b73-139">GetItem operation (email message)</span></span>](getitem-operation-email-message.md)
  
[<span data-ttu-id="c1b73-140">GetItem-Vorgang (Kalenderelement)</span><span class="sxs-lookup"><span data-stu-id="c1b73-140">GetItem operation (calendar item)</span></span>](getitem-operation-calendar-item.md)
  
[<span data-ttu-id="c1b73-141">GetItem-Vorgang (Aufgabe)</span><span class="sxs-lookup"><span data-stu-id="c1b73-141">GetItem operation (task)</span></span>](getitem-operation-task.md)
  
[<span data-ttu-id="c1b73-142">GetItem-Vorgang (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="c1b73-142">GetItem operation (contact)</span></span>](getitem-operation-contact.md)
  
## <a name="see-also"></a><span data-ttu-id="c1b73-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1b73-143">See also</span></span>



[<span data-ttu-id="c1b73-144">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="c1b73-144">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

