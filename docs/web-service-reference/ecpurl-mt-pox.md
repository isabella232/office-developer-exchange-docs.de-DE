---
title: EcpUrl-MT (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: Das EcpUrl-MT-Element gibt eine partielle URL an, die mit dem Wert des EcpUrl (POX)-Elements kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf e-Mail-Nachrichtenverfolgungseinstellungen für einen e-Mail-aktivierten Benutzer verwendet werden kann.
ms.openlocfilehash: 097811add5635bca14c659814652bca244a1398d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458712"
---
# <a name="ecpurl-mt-pox"></a><span data-ttu-id="2b05d-103">EcpUrl-MT (POX)</span><span class="sxs-lookup"><span data-stu-id="2b05d-103">EcpUrl-mt (POX)</span></span>

<span data-ttu-id="2b05d-104">Das **EcpUrl-MT-** Element gibt eine partielle URL an, die mit dem Wert des [EcpUrl (POX)](ecpurl-pox.md) -Elements kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf e-Mail-Nachrichtenverfolgungseinstellungen für einen e-Mail-aktivierten Benutzer verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b05d-104">The **EcpUrl-mt** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email message tracking settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="2b05d-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="2b05d-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="2b05d-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="2b05d-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="2b05d-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="2b05d-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="2b05d-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="2b05d-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="2b05d-109">EcpUrl-MT (POX)</span><span class="sxs-lookup"><span data-stu-id="2b05d-109">EcpUrl-mt (POX)</span></span>](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="2b05d-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2b05d-110">Attributes and elements</span></span>

<span data-ttu-id="2b05d-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2b05d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b05d-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="2b05d-112">Attributes</span></span>

<span data-ttu-id="2b05d-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="2b05d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b05d-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b05d-114">Child elements</span></span>

<span data-ttu-id="2b05d-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="2b05d-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2b05d-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b05d-116">Parent elements</span></span>

|<span data-ttu-id="2b05d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b05d-117">**Element**</span></span>|<span data-ttu-id="2b05d-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b05d-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b05d-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="2b05d-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="2b05d-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2b05d-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2b05d-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="2b05d-121">Text value</span></span>

<span data-ttu-id="2b05d-122">Der Textwert stellt eine partielle URL dar, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf e-Mail-Tracking-Einstellungen für den Benutzer verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b05d-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email tracking settings for the user.</span></span> <span data-ttu-id="2b05d-123">Der Wert des **EcpUrl-MT-** Elements enthält Parameter, die in "<"-und ">"-Zeichen enthalten sind, die durch den Client ersetzt werden, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2b05d-123">The value of the **EcpUrl-mt** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="2b05d-124">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="2b05d-124">**Parameter**</span></span>|<span data-ttu-id="2b05d-125">**Ersetzen durch**</span><span class="sxs-lookup"><span data-stu-id="2b05d-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2b05d-126">_IsOwa_</span><span class="sxs-lookup"><span data-stu-id="2b05d-126">_IsOwa_</span></span> <br/> |<span data-ttu-id="2b05d-127">n</span><span class="sxs-lookup"><span data-stu-id="2b05d-127">n</span></span>  <br/> |
| <span data-ttu-id="2b05d-128">_MsgID_</span><span class="sxs-lookup"><span data-stu-id="2b05d-128">_MsgID_</span></span> <br/> |<span data-ttu-id="2b05d-129">Internet Nachrichten-ID der Nachricht, die nachverfolgt werden soll, wie im Message-ID-Header angegeben.</span><span class="sxs-lookup"><span data-stu-id="2b05d-129">Internet message identifier of the message to be tracked as specified by the Message-ID header.</span></span>  <br/> |
| <span data-ttu-id="2b05d-130">_MBX_</span><span class="sxs-lookup"><span data-stu-id="2b05d-130">_Mbx_</span></span> <br/> |<span data-ttu-id="2b05d-131">Die SMTP-Adresse des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="2b05d-131">The SMTP address of the mailbox owner.</span></span>  <br/> |
| <span data-ttu-id="2b05d-132">_Sender_</span><span class="sxs-lookup"><span data-stu-id="2b05d-132">_Sender_</span></span> <br/> |<span data-ttu-id="2b05d-133">Die SMTP-Adresse des Absenders der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2b05d-133">The SMTP address of the message's sender.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b05d-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b05d-134">Remarks</span></span>

<span data-ttu-id="2b05d-135">Das **EcpUrl-MT-** Element ist ein optionales untergeordnetes Element des **Protocol** -Elements.</span><span class="sxs-lookup"><span data-stu-id="2b05d-135">The **EcpUrl-mt** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b05d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b05d-136">See also</span></span>



[<span data-ttu-id="2b05d-137">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="2b05d-137">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

