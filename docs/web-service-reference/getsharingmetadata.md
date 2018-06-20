---
title: GetSharingMetadata
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: b609ee26-6d28-4559-81b6-b8e8d4759a23
description: Das GetSharingMetadata-Element definiert eine Anforderung an ein undurchsichtiger Authentifizierungstoken erhalten möchten, die die Einladung zur Freigabe identifiziert. Dieses Element ist das Basiselement für den Vorgang GetSharingMetadata.
ms.openlocfilehash: 5283d35e11350ef10ed8cc01527e787ef54be927
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829677"
---
# <a name="getsharingmetadata"></a><span data-ttu-id="d0863-104">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="d0863-104">GetSharingMetadata</span></span>

<span data-ttu-id="d0863-105">Das **GetSharingMetadata** -Element definiert eine Anforderung an ein undurchsichtiger Authentifizierungstoken erhalten möchten, die die Einladung zur Freigabe identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d0863-105">The **GetSharingMetadata** element defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span> <span data-ttu-id="d0863-106">Dieses Element ist das Basiselement für den [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md).</span><span class="sxs-lookup"><span data-stu-id="d0863-106">This element is the base element for the [GetSharingMetadata operation](getsharingmetadata-operation.md).</span></span>
  
```XML
<GetSharingMetadata>
   <IdOfFolderToShare/>
   <SenderSmtpAddress/>
   <Recipients/>
</GetSharingMetadata>
```

 <span data-ttu-id="d0863-107">**GetSharingMetadataType**</span><span class="sxs-lookup"><span data-stu-id="d0863-107">**GetSharingMetadataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0863-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d0863-108">Attributes and elements</span></span>

<span data-ttu-id="d0863-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d0863-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0863-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d0863-110">Attributes</span></span>

<span data-ttu-id="d0863-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0863-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0863-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0863-112">Child elements</span></span>

|<span data-ttu-id="d0863-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0863-113">**Element**</span></span>|<span data-ttu-id="d0863-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0863-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0863-115">IdOfFolderToShare</span><span class="sxs-lookup"><span data-stu-id="d0863-115">IdOfFolderToShare</span></span>](idoffoldertoshare.md) <br/> |<span data-ttu-id="d0863-116">Stellt den Bezeichner des Ordners auf dem Server, der freigegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d0863-116">Represents the identifier of the folder on the server that will be shared.</span></span> <span data-ttu-id="d0863-117">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d0863-117">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="d0863-118">SenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="d0863-118">SenderSmtpAddress</span></span>](sendersmtpaddress.md) <br/> |<span data-ttu-id="d0863-119">Stellt die SMTP-e-Mail-Adresse, die entspricht an das Postfach, das den Ordner enthält, der durch das [IdOfFolderToShare](idoffoldertoshare.md) -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d0863-119">Represents the SMTP email address that corresponds to the mailbox that contains the folder that is identified by the [IdOfFolderToShare](idoffoldertoshare.md) element.</span></span> <span data-ttu-id="d0863-120">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d0863-120">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="d0863-121">Empfänger (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="d0863-121">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="d0863-122">Stellt die SMTP-e-Mail-Adressen eine oder mehrere Entitäten, die Zugriff auf die Daten in den Ordner erteilt werden, die durch das [IdOfFolderToShare](idoffoldertoshare.md) -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d0863-122">Represents the SMTP email addresses of one or more entities that will be granted access to the data in the folder that is identified by the [IdOfFolderToShare](idoffoldertoshare.md) element.</span></span> <span data-ttu-id="d0863-123">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d0863-123">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d0863-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0863-124">Parent elements</span></span>

<span data-ttu-id="d0863-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0863-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0863-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d0863-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0863-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0863-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d0863-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d0863-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d0863-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d0863-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d0863-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d0863-130">Validation File</span></span>  <br/> |<span data-ttu-id="d0863-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d0863-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d0863-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d0863-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0863-133">False</span><span class="sxs-lookup"><span data-stu-id="d0863-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0863-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0863-134">See also</span></span>



[<span data-ttu-id="d0863-135">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d0863-135">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="d0863-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d0863-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

