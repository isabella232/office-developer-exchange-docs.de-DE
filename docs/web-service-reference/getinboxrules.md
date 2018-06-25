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
ms.openlocfilehash: 3c3ee682dd009e5c4bec940637a7dfa3c11f8402
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758702"
---
# <a name="getinboxrules"></a><span data-ttu-id="36cf7-103">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="36cf7-103">GetInboxRules</span></span>

<span data-ttu-id="36cf7-104">Das **GetInboxRules** -Element definiert eine Anforderung zum Abrufen der Posteingangsregeln für ein Postfach im Serverspeicher.</span><span class="sxs-lookup"><span data-stu-id="36cf7-104">The **GetInboxRules** element defines a request to get the Inbox rules on a mailbox in the server store.</span></span> 
  
```XML
<GetInboxRules>
   <MailboxSmtpAddress/>
</GetInboxRules>
```

 <span data-ttu-id="36cf7-105">**GetInboxRulesRequestType**</span><span class="sxs-lookup"><span data-stu-id="36cf7-105">**GetInboxRulesRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36cf7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="36cf7-106">Attributes and elements</span></span>

<span data-ttu-id="36cf7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="36cf7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36cf7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="36cf7-108">Attributes</span></span>

<span data-ttu-id="36cf7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="36cf7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36cf7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36cf7-110">Child elements</span></span>

|<span data-ttu-id="36cf7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="36cf7-111">**Element**</span></span>|<span data-ttu-id="36cf7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="36cf7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36cf7-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="36cf7-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="36cf7-114">Stellt die SMTP-Adresse des Benutzers, dessen Posteingangsregeln abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="36cf7-114">Represents the SMTP address of the user whose Inbox rules are to be retrieved.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="36cf7-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36cf7-115">Parent elements</span></span>

<span data-ttu-id="36cf7-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="36cf7-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36cf7-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="36cf7-117">Remarks</span></span>

<span data-ttu-id="36cf7-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="36cf7-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="36cf7-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="36cf7-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36cf7-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="36cf7-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="36cf7-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="36cf7-121">Schema Name</span></span>  <br/> |<span data-ttu-id="36cf7-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="36cf7-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="36cf7-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="36cf7-123">Validation File</span></span>  <br/> |<span data-ttu-id="36cf7-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="36cf7-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="36cf7-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="36cf7-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="36cf7-126">True</span><span class="sxs-lookup"><span data-stu-id="36cf7-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36cf7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36cf7-127">See also</span></span>



[<span data-ttu-id="36cf7-128">GetInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="36cf7-128">GetInboxRules operation</span></span>](getinboxrules-operation.md)

