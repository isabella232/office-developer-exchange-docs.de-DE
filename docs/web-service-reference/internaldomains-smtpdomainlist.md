---
title: InternalDomains (SmtpDomainList)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternalDomains
api_type:
- schema
ms.assetid: 0f2cbb05-338d-4302-8871-a06e78b33f98
description: Das InternalDomains-Element gibt die Liste der internen SMTP-Domänen der Organisation an.
ms.openlocfilehash: ec7ef2d72ae922c751f8f50b72ff7d6b31b212ca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459966"
---
# <a name="internaldomains-smtpdomainlist"></a><span data-ttu-id="6f099-103">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="6f099-103">InternalDomains (SmtpDomainList)</span></span>

<span data-ttu-id="6f099-104">Das **InternalDomains** -Element gibt die Liste der internen SMTP-Domänen der Organisation an.</span><span class="sxs-lookup"><span data-stu-id="6f099-104">The **InternalDomains** element identifies the list of internal SMTP domains of the organization.</span></span> 
  
```XML
<InternalDomains>
   <Domain/>
</InternalDomains>
```

 <span data-ttu-id="6f099-105">**SmtpDomainList**</span><span class="sxs-lookup"><span data-stu-id="6f099-105">**SmtpDomainList**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f099-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6f099-106">Attributes and elements</span></span>

<span data-ttu-id="6f099-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6f099-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f099-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6f099-108">Attributes</span></span>

<span data-ttu-id="6f099-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6f099-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f099-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6f099-110">Child elements</span></span>

|<span data-ttu-id="6f099-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6f099-111">**Element**</span></span>|<span data-ttu-id="6f099-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f099-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f099-113">Domäne</span><span class="sxs-lookup"><span data-stu-id="6f099-113">Domain</span></span>](domain.md) <br/> |<span data-ttu-id="6f099-114">Identifiziert eine einzelne SMTP-Domäne.</span><span class="sxs-lookup"><span data-stu-id="6f099-114">Identifies a single SMTP domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6f099-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6f099-115">Parent elements</span></span>

|<span data-ttu-id="6f099-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="6f099-116">**Element**</span></span>|<span data-ttu-id="6f099-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f099-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f099-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="6f099-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="6f099-119">Enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst.</span><span class="sxs-lookup"><span data-stu-id="6f099-119">Contains service configuration information for the mail tips service.</span></span>  <br/> |
|[<span data-ttu-id="6f099-120">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f099-120">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="6f099-121">Enthält Dienstkonfigurationsinformationen für den Schutz Regeldienst.</span><span class="sxs-lookup"><span data-stu-id="6f099-121">Contains service configuration information for the protection rules service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6f099-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="6f099-122">Text value</span></span>

<span data-ttu-id="6f099-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="6f099-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f099-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f099-124">Remarks</span></span>

<span data-ttu-id="6f099-125">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f099-125">This element is required.</span></span> 
  
<span data-ttu-id="6f099-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6f099-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f099-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6f099-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f099-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f099-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f099-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6f099-129">Schema Name</span></span>  <br/> |<span data-ttu-id="6f099-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6f099-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="6f099-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6f099-131">Validation File</span></span>  <br/> |<span data-ttu-id="6f099-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6f099-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f099-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6f099-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f099-134">False</span><span class="sxs-lookup"><span data-stu-id="6f099-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f099-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f099-135">See also</span></span>



- [<span data-ttu-id="6f099-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6f099-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

