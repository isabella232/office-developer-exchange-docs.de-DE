---
title: SenderSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SenderSmtpAddress
api_type:
- schema
ms.assetid: e39c7df7-4bfa-455f-b4bb-1f1d05398eec
description: Das SenderSmtpAddress-Element stellt die SMTP-e-Mail-Adresse dar, die dem Postfach entspricht, das den Ordner enthält, der freigegeben werden soll.
ms.openlocfilehash: 73047dcecfbccb55d74e373891c3154bc7baeeba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464896"
---
# <a name="sendersmtpaddress"></a><span data-ttu-id="128e7-103">SenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="128e7-103">SenderSmtpAddress</span></span>

<span data-ttu-id="128e7-104">Das **SenderSmtpAddress** -Element stellt die SMTP-e-Mail-Adresse dar, die dem Postfach entspricht, das den Ordner enthält, der freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="128e7-104">The **SenderSmtpAddress** element represents the SMTP e-mail address corresponding to the mailbox that contains the folder that will be shared.</span></span> 
  
```xml
<SenderSmtpAddress/>
```

 <span data-ttu-id="128e7-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="128e7-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="128e7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="128e7-106">Attributes and elements</span></span>

<span data-ttu-id="128e7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="128e7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="128e7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="128e7-108">Attributes</span></span>

<span data-ttu-id="128e7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="128e7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="128e7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="128e7-110">Child elements</span></span>

<span data-ttu-id="128e7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="128e7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="128e7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="128e7-112">Parent elements</span></span>

|<span data-ttu-id="128e7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="128e7-113">**Element**</span></span>|<span data-ttu-id="128e7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="128e7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="128e7-115">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="128e7-115">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="128e7-116">Definiert eine Anforderung zum Abrufen eines nicht transparenten Authentifizierungstokens, das die Freigabeeinladung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="128e7-116">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="128e7-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="128e7-117">Text value</span></span>

<span data-ttu-id="128e7-118">Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="128e7-118">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="128e7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="128e7-119">Remarks</span></span>

<span data-ttu-id="128e7-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="128e7-120">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="128e7-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="128e7-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="128e7-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="128e7-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="128e7-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="128e7-123">Schema Name</span></span>  <br/> |<span data-ttu-id="128e7-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="128e7-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="128e7-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="128e7-125">Validation File</span></span>  <br/> |<span data-ttu-id="128e7-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="128e7-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="128e7-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="128e7-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="128e7-128">False</span><span class="sxs-lookup"><span data-stu-id="128e7-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="128e7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="128e7-129">See also</span></span>



[<span data-ttu-id="128e7-130">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="128e7-130">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="128e7-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="128e7-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

