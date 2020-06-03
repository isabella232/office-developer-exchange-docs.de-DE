---
title: GetInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRules
api_type:
- schema
ms.assetid: 7a54992d-03a6-4afc-a2e4-dcdc9ce54194
description: Das GetInboxRules -Element definiert eine Anforderung zum Abrufen der Posteingangsregeln für ein Postfach im Serverspeicher.
ms.openlocfilehash: 890592fd3f87fc5592a618a2febf28e4daf0dbe4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457928"
---
# <a name="getinboxrules"></a><span data-ttu-id="6f890-103">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="6f890-103">GetInboxRules</span></span>

<span data-ttu-id="6f890-104">Das **GetInboxRules** -Element definiert eine Anforderung zum Abrufen der Posteingangsregeln für ein Postfach im Serverspeicher.</span><span class="sxs-lookup"><span data-stu-id="6f890-104">The **GetInboxRules** element defines a request to get the Inbox rules on a mailbox in the server store.</span></span> 
  
```XML
<GetInboxRules>
   <MailboxSmtpAddress/>
</GetInboxRules>
```

 <span data-ttu-id="6f890-105">**GetInboxRulesRequestType**</span><span class="sxs-lookup"><span data-stu-id="6f890-105">**GetInboxRulesRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f890-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6f890-106">Attributes and elements</span></span>

<span data-ttu-id="6f890-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6f890-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f890-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6f890-108">Attributes</span></span>

<span data-ttu-id="6f890-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6f890-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f890-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6f890-110">Child elements</span></span>

|<span data-ttu-id="6f890-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6f890-111">**Element**</span></span>|<span data-ttu-id="6f890-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f890-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f890-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="6f890-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="6f890-114">Stellt die SMTP-Adresse des Benutzers, dessen Posteingangsregeln abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6f890-114">Represents the SMTP address of the user whose Inbox rules are to be retrieved.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6f890-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6f890-115">Parent elements</span></span>

<span data-ttu-id="6f890-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="6f890-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f890-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f890-117">Remarks</span></span>

<span data-ttu-id="6f890-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6f890-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f890-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6f890-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f890-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f890-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6f890-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6f890-121">Schema Name</span></span>  <br/> |<span data-ttu-id="6f890-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6f890-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6f890-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6f890-123">Validation File</span></span>  <br/> |<span data-ttu-id="6f890-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6f890-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6f890-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6f890-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f890-126">True</span><span class="sxs-lookup"><span data-stu-id="6f890-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f890-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f890-127">See also</span></span>



[<span data-ttu-id="6f890-128">GetInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6f890-128">GetInboxRules operation</span></span>](getinboxrules-operation.md)

