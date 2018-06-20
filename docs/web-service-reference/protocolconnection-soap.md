---
title: ProtocolConnection (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6eef2188-6194-48f1-ad7e-46104aecdf56
description: Das Element ProtocolConnection stellt die Protokoll Verbindung des Webclients Server dar.
ms.openlocfilehash: 8b5396821cd959e41d24fcf7a94c519f9c634a1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830915"
---
# <a name="protocolconnection-soap"></a><span data-ttu-id="1b145-103">ProtocolConnection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1b145-103">ProtocolConnection (SOAP)</span></span>

<span data-ttu-id="1b145-104">Das Element **ProtocolConnection** stellt die Protokoll Verbindung des Webclients Server dar.</span><span class="sxs-lookup"><span data-stu-id="1b145-104">The **ProtocolConnection** element represents the protocol connection of the server Web client.</span></span> 
  
```XML
<ProtocolConnection>
   <Hostname/>
   <Port/>
   <EncryptionMethod/>
</ProtocolConnection>
```

 <span data-ttu-id="1b145-105">**ProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="1b145-105">**ProtocolConnection**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b145-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1b145-106">Attributes and elements</span></span>

<span data-ttu-id="1b145-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1b145-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b145-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1b145-108">Attributes</span></span>

<span data-ttu-id="1b145-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1b145-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1b145-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b145-110">Child elements</span></span>

|<span data-ttu-id="1b145-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1b145-111">**Element**</span></span>|<span data-ttu-id="1b145-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1b145-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b145-113">Hostname (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1b145-113">Hostname (SOAP)</span></span>](hostname-soap.md) <br/> |<span data-ttu-id="1b145-114">Stellt die Hostnamenkomponente des den vollständigen Namen des Computers an.</span><span class="sxs-lookup"><span data-stu-id="1b145-114">Represents the host name portion of the full computer name of the computer.</span></span>  <br/> |
|[<span data-ttu-id="1b145-115">Port (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1b145-115">Port (SOAP)</span></span>](port-soap.md) <br/> |<span data-ttu-id="1b145-116">Stellt die Portnummer an, die für das Protokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b145-116">Represents the port number to use for the protocol.</span></span>  <br/> |
|[<span data-ttu-id="1b145-117">EncryptionMethod (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1b145-117">EncryptionMethod (SOAP)</span></span>](encryptionmethod-soap.md) <br/> |<span data-ttu-id="1b145-118">Stellt die kryptografische-Methode, die für die POP-, IMAP- und SMTP-Protokolle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b145-118">Represents the cryptographic method that is used for the POP, IMAP, and SMTP protocols.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1b145-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b145-119">Parent elements</span></span>

|<span data-ttu-id="1b145-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="1b145-120">**Element**</span></span>|<span data-ttu-id="1b145-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1b145-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b145-122">ProtocolConnections (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1b145-122">ProtocolConnections (SOAP)</span></span>](protocolconnections-soap.md) <br/> |<span data-ttu-id="1b145-123">Enthält null oder mehr Protocol-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="1b145-123">Contains zero or more protocol connections.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1b145-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="1b145-124">Text value</span></span>

<span data-ttu-id="1b145-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="1b145-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b145-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1b145-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b145-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b145-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="1b145-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1b145-128">Schema Name</span></span>  <br/> |<span data-ttu-id="1b145-129">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="1b145-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="1b145-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1b145-130">Validation File</span></span>  <br/> |<span data-ttu-id="1b145-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1b145-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1b145-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1b145-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="1b145-133">True</span><span class="sxs-lookup"><span data-stu-id="1b145-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b145-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b145-134">See also</span></span>



[<span data-ttu-id="1b145-135">ProtocolConnectionCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1b145-135">ProtocolConnectionCollectionSetting (SOAP)</span></span>](protocolconnectioncollectionsetting-soap.md)

