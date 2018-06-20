---
title: EcpUrl-Mt (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: Das EcpUrl Mt-Element gibt eine partielle URL, die mit dem EcpUrl (POX) Elementwert generiert eine URL, die verwendet werden können, für den e-Mail-Nachricht Nachverfolgen der Einstellungen für einen e-Mail-aktivierten Benutzer Zugriff auf kombiniert werden kann.
ms.openlocfilehash: 13954a4dab8e81f4ba75b3578e6ba7f67f4b8b96
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758118"
---
# <a name="ecpurl-mt-pox"></a><span data-ttu-id="265ab-103">EcpUrl-Mt (POX)</span><span class="sxs-lookup"><span data-stu-id="265ab-103">EcpUrl-mt (POX)</span></span>

<span data-ttu-id="265ab-104">Das **EcpUrl Mt** -Element gibt eine partielle URL, die mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die verwendet werden können, für den e-Mail-Nachricht Nachverfolgen der Einstellungen für einen e-Mail-aktivierten Benutzer Zugriff auf kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="265ab-104">The **EcpUrl-mt** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email message tracking settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="265ab-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="265ab-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="265ab-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="265ab-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="265ab-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="265ab-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="265ab-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="265ab-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="265ab-109">EcpUrl-Mt (POX)</span><span class="sxs-lookup"><span data-stu-id="265ab-109">EcpUrl-mt (POX)</span></span>](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="265ab-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="265ab-110">Attributes and elements</span></span>

<span data-ttu-id="265ab-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="265ab-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="265ab-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="265ab-112">Attributes</span></span>

<span data-ttu-id="265ab-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="265ab-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="265ab-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="265ab-114">Child elements</span></span>

<span data-ttu-id="265ab-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="265ab-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="265ab-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="265ab-116">Parent elements</span></span>

|<span data-ttu-id="265ab-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="265ab-117">**Element**</span></span>|<span data-ttu-id="265ab-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="265ab-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="265ab-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="265ab-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="265ab-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="265ab-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="265ab-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="265ab-121">Text value</span></span>

<span data-ttu-id="265ab-122">Der Textwert stellt eine partielle URL, die kombiniert werden kann, mit der [EcpUrl (POX)](ecpurl-pox.md) Element Wert generiert eine URL, die Zugriff auf e-Mails Nachverfolgen der Einstellungen für den Benutzer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="265ab-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email tracking settings for the user.</span></span> <span data-ttu-id="265ab-123">Der Wert des Elements **EcpUrl Mt** enthält Parameter enthaltenen ' <' und ' >' Zeichen, die vom Client ersetzt werden, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="265ab-123">The value of the **EcpUrl-mt** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="265ab-124">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="265ab-124">**Parameter**</span></span>|<span data-ttu-id="265ab-125">**Ersetzen durch**</span><span class="sxs-lookup"><span data-stu-id="265ab-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="265ab-126">_IsOwa_</span><span class="sxs-lookup"><span data-stu-id="265ab-126">_IsOwa_</span></span> <br/> |<span data-ttu-id="265ab-127">n</span><span class="sxs-lookup"><span data-stu-id="265ab-127">n</span></span>  <br/> |
| <span data-ttu-id="265ab-128">_MsgID_</span><span class="sxs-lookup"><span data-stu-id="265ab-128">_MsgID_</span></span> <br/> |<span data-ttu-id="265ab-129">Internetnachricht-ID der Nachricht nachverfolgt werden durch die Kopfzeile Nachrichten-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="265ab-129">Internet message identifier of the message to be tracked as specified by the Message-ID header.</span></span>  <br/> |
| <span data-ttu-id="265ab-130">_MBX_</span><span class="sxs-lookup"><span data-stu-id="265ab-130">_Mbx_</span></span> <br/> |<span data-ttu-id="265ab-131">Die SMTP-Adresse des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="265ab-131">The SMTP address of the mailbox owner.</span></span>  <br/> |
| <span data-ttu-id="265ab-132">_Absender_</span><span class="sxs-lookup"><span data-stu-id="265ab-132">_Sender_</span></span> <br/> |<span data-ttu-id="265ab-133">Die SMTP-Adresse des Absenders der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="265ab-133">The SMTP address of the message's sender.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="265ab-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="265ab-134">Remarks</span></span>

<span data-ttu-id="265ab-135">Das **EcpUrl Mt** -Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements.</span><span class="sxs-lookup"><span data-stu-id="265ab-135">The **EcpUrl-mt** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="265ab-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="265ab-136">See also</span></span>



[<span data-ttu-id="265ab-137">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="265ab-137">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

