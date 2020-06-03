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
description: Das ProtocolConnection-Element stellt die Protokollverbindung des Server-Webclients dar.
ms.openlocfilehash: b9df3febe36db53d7c5bf0610ba857f13aa96abc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528860"
---
# <a name="protocolconnection-soap"></a><span data-ttu-id="31937-103">ProtocolConnection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="31937-103">ProtocolConnection (SOAP)</span></span>

<span data-ttu-id="31937-104">Das **ProtocolConnection** -Element stellt die Protokollverbindung des Server-Webclients dar.</span><span class="sxs-lookup"><span data-stu-id="31937-104">The **ProtocolConnection** element represents the protocol connection of the server Web client.</span></span> 
  
```XML
<ProtocolConnection>
   <Hostname/>
   <Port/>
   <EncryptionMethod/>
</ProtocolConnection>
```

 <span data-ttu-id="31937-105">**ProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="31937-105">**ProtocolConnection**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31937-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="31937-106">Attributes and elements</span></span>

<span data-ttu-id="31937-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="31937-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31937-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="31937-108">Attributes</span></span>

<span data-ttu-id="31937-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="31937-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31937-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31937-110">Child elements</span></span>

|<span data-ttu-id="31937-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="31937-111">**Element**</span></span>|<span data-ttu-id="31937-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31937-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31937-113">Hostname (SOAP)</span><span class="sxs-lookup"><span data-stu-id="31937-113">Hostname (SOAP)</span></span>](hostname-soap.md) <br/> |<span data-ttu-id="31937-114">Stellt den Hostnamensteil des vollständigen Computernamens des Computers dar.</span><span class="sxs-lookup"><span data-stu-id="31937-114">Represents the host name portion of the full computer name of the computer.</span></span>  <br/> |
|[<span data-ttu-id="31937-115">Port (SOAP)</span><span class="sxs-lookup"><span data-stu-id="31937-115">Port (SOAP)</span></span>](port-soap.md) <br/> |<span data-ttu-id="31937-116">Stellt die Portnummer dar, die für das Protokoll verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="31937-116">Represents the port number to use for the protocol.</span></span>  <br/> |
|[<span data-ttu-id="31937-117">EncryptionMethod (SOAP)</span><span class="sxs-lookup"><span data-stu-id="31937-117">EncryptionMethod (SOAP)</span></span>](encryptionmethod-soap.md) <br/> |<span data-ttu-id="31937-118">Stellt die kryptografische Methode dar, die für die Protokolle Pop, IMAP und SMTP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31937-118">Represents the cryptographic method that is used for the POP, IMAP, and SMTP protocols.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="31937-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31937-119">Parent elements</span></span>

|<span data-ttu-id="31937-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="31937-120">**Element**</span></span>|<span data-ttu-id="31937-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31937-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31937-122">ProtocolConnections (SOAP)</span><span class="sxs-lookup"><span data-stu-id="31937-122">ProtocolConnections (SOAP)</span></span>](protocolconnections-soap.md) <br/> |<span data-ttu-id="31937-123">Enthält NULL oder mehr Protokoll Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="31937-123">Contains zero or more protocol connections.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="31937-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="31937-124">Text value</span></span>

<span data-ttu-id="31937-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="31937-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31937-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="31937-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31937-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="31937-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="31937-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="31937-128">Schema Name</span></span>  <br/> |<span data-ttu-id="31937-129">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="31937-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="31937-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="31937-130">Validation File</span></span>  <br/> |<span data-ttu-id="31937-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="31937-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="31937-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="31937-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="31937-133">True</span><span class="sxs-lookup"><span data-stu-id="31937-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31937-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31937-134">See also</span></span>



[<span data-ttu-id="31937-135">ProtocolConnectionCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="31937-135">ProtocolConnectionCollectionSetting (SOAP)</span></span>](protocolconnectioncollectionsetting-soap.md)

