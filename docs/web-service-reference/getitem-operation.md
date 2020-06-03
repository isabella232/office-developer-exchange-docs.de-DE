---
title: GetItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: Hier finden Sie Informationen zum GetItem-EWS-Vorgang.
localization_priority: Priority
ms.openlocfilehash: 8871dde183974454fc27dbddda489e6b0a70f3aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463328"
---
# <a name="getitem-operation"></a><span data-ttu-id="a0bc9-103">GetItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a0bc9-103">GetItem operation</span></span>

<span data-ttu-id="a0bc9-104">Hier finden Sie Informationen zum **GetItem** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-104">Find information about the **GetItem** EWS operation.</span></span> 
  
<span data-ttu-id="a0bc9-105">Der **GetItem** -Vorgang ruft Elemente aus dem Exchange-Informationsspeicher ab.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-105">The **GetItem** operation gets items from the Exchange store.</span></span> 
  
## <a name="using-the-getitem-operation"></a><span data-ttu-id="a0bc9-106">Verwenden des GetItem-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="a0bc9-106">Using the GetItem operation</span></span>

<span data-ttu-id="a0bc9-107">Der **GetItem** -Vorgang gibt viele Elementeigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-107">The **GetItem** operation returns many item properties.</span></span> <span data-ttu-id="a0bc9-108">Die Eigenschaften, die in einer **GetItem** -Antwort zurückgegeben werden, variieren basierend auf der angeforderten Form, den angeforderten zusätzlichen Eigenschaften und dem Typ des zurückgegebenen Elements.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-108">The properties that are returned in a **GetItem** response vary based on the requested shape, requested additional properties, and the type of item returned.</span></span> 
  
<span data-ttu-id="a0bc9-109">[Nachrichten](message-ex15websvcsotherref.md) Elemente stellen e-Mail-Nachrichten und alle anderen Elemente dar, die nicht stark vom Exchange-Webdienste Schema eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-109">[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="a0bc9-110">Elemente wie IPM.Sharing- und IPM.InfoPath-Elemente werden als [Message](message-ex15websvcsotherref.md)-Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-110">Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements.</span></span> <span data-ttu-id="a0bc9-111">Exchange gibt das [Element](item.md)-Basiselement nicht in Antworten zurück.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-111">Exchange does not return the base [Item](item.md) element in responses.</span></span> 
  
<span data-ttu-id="a0bc9-112">Der **GetItem** -Vorgang gibt keine Anlagen zurück.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-112">The **GetItem** operation does not return attachments.</span></span> <span data-ttu-id="a0bc9-113">Es werden Metadaten zu einem angefügten Element oder einer Datei zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-113">It does return metadata about an attached item or file.</span></span> <span data-ttu-id="a0bc9-114">Verwenden Sie den [GetAttachment-Vorgang](getattachment-operation.md), um eine Anlage zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-114">To return an attachment, use the [GetAttachment operation](getattachment-operation.md).</span></span>
  
## <a name="getitem-operation-soap-headers"></a><span data-ttu-id="a0bc9-115">GetItem-Vorgangs-SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="a0bc9-115">GetItem operation SOAP headers</span></span>

<span data-ttu-id="a0bc9-116">Der **GetItem** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-116">The **GetItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="a0bc9-117">Kopfzeile \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a0bc9-117">\*\*\*\*Header\*\*\*\*</span></span>|<span data-ttu-id="a0bc9-118">\*\*\*\*Element\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a0bc9-118">\*\*\*\*Element\*\*\*\*</span></span>|<span data-ttu-id="a0bc9-119">\*\*\*\*Beschreibung\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a0bc9-119">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0bc9-120">**DateTimePrecision**</span><span class="sxs-lookup"><span data-stu-id="a0bc9-120">**DateTimePrecision**</span></span> <br/> |[<span data-ttu-id="a0bc9-121">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="a0bc9-121">DateTimePrecision</span></span>](datetimeprecision.md) <br/> |<span data-ttu-id="a0bc9-122">Gibt die Auflösung der Daten-/Uhrzeitwerte in Antworten vom Server an, entweder in Sekunden oder in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-122">Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds.</span></span>  <br/> |
|<span data-ttu-id="a0bc9-123">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="a0bc9-123">**Impersonation**</span></span> <br/> |[<span data-ttu-id="a0bc9-124">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="a0bc9-124">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="a0bc9-125">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-125">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="a0bc9-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="a0bc9-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="a0bc9-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="a0bc9-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="a0bc9-128">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="a0bc9-129">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="a0bc9-129">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="a0bc9-130">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="a0bc9-130">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="a0bc9-131">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-131">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="a0bc9-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="a0bc9-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="a0bc9-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a0bc9-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="a0bc9-134">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-134">Identifies the version of the server that responded to the request.</span></span>  <br/> |
|<span data-ttu-id="a0bc9-135">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="a0bc9-135">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="a0bc9-136">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="a0bc9-136">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="a0bc9-137">Gibt die Zeitzone für alle Antworten vom Server an.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-137">Identifies the time zone to be used for all responses from the server.</span></span>  <br/> |
   
## <a name="in-this-section"></a><span data-ttu-id="a0bc9-138">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a0bc9-138">In This Section</span></span>

[<span data-ttu-id="a0bc9-139">GetItem-Vorgang (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="a0bc9-139">GetItem operation (email message)</span></span>](getitem-operation-email-message.md)
  
[<span data-ttu-id="a0bc9-140">GetItem-Vorgang (Kalenderelement)</span><span class="sxs-lookup"><span data-stu-id="a0bc9-140">GetItem operation (calendar item)</span></span>](getitem-operation-calendar-item.md)
  
[<span data-ttu-id="a0bc9-141">GetItem-Vorgang (Aufgabe)</span><span class="sxs-lookup"><span data-stu-id="a0bc9-141">GetItem operation (task)</span></span>](getitem-operation-task.md)
  
[<span data-ttu-id="a0bc9-142">GetItem-Vorgang (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="a0bc9-142">GetItem operation (contact)</span></span>](getitem-operation-contact.md)
  
## <a name="see-also"></a><span data-ttu-id="a0bc9-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0bc9-143">See also</span></span>



[<span data-ttu-id="a0bc9-144">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="a0bc9-144">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

