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
description: Das InternalDomains-Element identifiziert in der Liste von internen SMTP-Domänen der Organisation.
ms.openlocfilehash: f37a31f4348a7eb0024656489f249dec349bc67b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829953"
---
# <a name="internaldomains-smtpdomainlist"></a><span data-ttu-id="1ec70-103">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="1ec70-103">InternalDomains (SmtpDomainList)</span></span>

<span data-ttu-id="1ec70-104">Das **InternalDomains** -Element identifiziert in der Liste von internen SMTP-Domänen der Organisation.</span><span class="sxs-lookup"><span data-stu-id="1ec70-104">The **InternalDomains** element identifies the list of internal SMTP domains of the organization.</span></span> 
  
```XML
<InternalDomains>
   <Domain/>
</InternalDomains>
```

 <span data-ttu-id="1ec70-105">**SmtpDomainList**</span><span class="sxs-lookup"><span data-stu-id="1ec70-105">**SmtpDomainList**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ec70-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1ec70-106">Attributes and elements</span></span>

<span data-ttu-id="1ec70-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1ec70-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ec70-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1ec70-108">Attributes</span></span>

<span data-ttu-id="1ec70-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ec70-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ec70-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ec70-110">Child elements</span></span>

|<span data-ttu-id="1ec70-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ec70-111">**Element**</span></span>|<span data-ttu-id="1ec70-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ec70-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ec70-113">Domain</span><span class="sxs-lookup"><span data-stu-id="1ec70-113">Domain</span></span>](domain.md) <br/> |<span data-ttu-id="1ec70-114">Gibt eine einzelne SMTP-Domäne.</span><span class="sxs-lookup"><span data-stu-id="1ec70-114">Identifies a single SMTP domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1ec70-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ec70-115">Parent elements</span></span>

|<span data-ttu-id="1ec70-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ec70-116">**Element**</span></span>|<span data-ttu-id="1ec70-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ec70-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ec70-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="1ec70-118">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="1ec70-119">Enthält Konfigurationsinformationen für den e-Mail-Dienst Tipps Service.</span><span class="sxs-lookup"><span data-stu-id="1ec70-119">Contains service configuration information for the mail tips service.</span></span>  <br/> |
|[<span data-ttu-id="1ec70-120">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ec70-120">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="1ec70-121">Enthält Konfigurationsinformationen für den Schutz Regeln Dienst Service.</span><span class="sxs-lookup"><span data-stu-id="1ec70-121">Contains service configuration information for the protection rules service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1ec70-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="1ec70-122">Text value</span></span>

<span data-ttu-id="1ec70-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ec70-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ec70-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ec70-124">Remarks</span></span>

<span data-ttu-id="1ec70-125">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ec70-125">This element is required.</span></span> 
  
<span data-ttu-id="1ec70-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1ec70-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ec70-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1ec70-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ec70-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ec70-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1ec70-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1ec70-129">Schema Name</span></span>  <br/> |<span data-ttu-id="1ec70-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1ec70-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="1ec70-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1ec70-131">Validation File</span></span>  <br/> |<span data-ttu-id="1ec70-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1ec70-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1ec70-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1ec70-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ec70-134">False</span><span class="sxs-lookup"><span data-stu-id="1ec70-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ec70-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ec70-135">See also</span></span>



- [<span data-ttu-id="1ec70-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1ec70-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

