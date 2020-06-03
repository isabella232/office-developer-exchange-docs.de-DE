---
title: Token
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Token
api_type:
- schema
ms.assetid: 62b700e1-88c7-41ef-b431-d7af4a8b54a7
description: Das Token-Element enthält verschlüsselte Daten, die das Identifikations Token für die freigegebenen Daten darstellen.
ms.openlocfilehash: c2e80082f9b4ecb96defdca8c5f0223a945661ba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458908"
---
# <a name="token"></a><span data-ttu-id="042c3-103">Token</span><span class="sxs-lookup"><span data-stu-id="042c3-103">Token</span></span>

<span data-ttu-id="042c3-104">Das **Token** -Element enthält verschlüsselte Daten, die das Identifikations Token für die freigegebenen Daten darstellen.</span><span class="sxs-lookup"><span data-stu-id="042c3-104">The **Token** element contains encrypted data that represents the identification token for the shared data.</span></span> 
  
```xml
<Token/>
```

 <span data-ttu-id="042c3-105">**EncryptedDataContainerType**</span><span class="sxs-lookup"><span data-stu-id="042c3-105">**EncryptedDataContainerType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="042c3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="042c3-106">Attributes and elements</span></span>

<span data-ttu-id="042c3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="042c3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="042c3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="042c3-108">Attributes</span></span>

<span data-ttu-id="042c3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="042c3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="042c3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="042c3-110">Child elements</span></span>

<span data-ttu-id="042c3-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="042c3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="042c3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="042c3-112">Parent elements</span></span>

|<span data-ttu-id="042c3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="042c3-113">**Element**</span></span>|<span data-ttu-id="042c3-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="042c3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="042c3-115">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="042c3-115">EncryptedSharedFolderData</span></span>](encryptedsharedfolderdata.md) <br/> |<span data-ttu-id="042c3-116">Enthält die verschlüsselten Daten, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="042c3-116">Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="042c3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="042c3-117">Remarks</span></span>

<span data-ttu-id="042c3-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="042c3-118">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="042c3-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="042c3-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="042c3-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="042c3-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="042c3-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="042c3-121">Schema Name</span></span>  <br/> |<span data-ttu-id="042c3-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="042c3-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="042c3-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="042c3-123">Validation File</span></span>  <br/> |<span data-ttu-id="042c3-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="042c3-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="042c3-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="042c3-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="042c3-126">False</span><span class="sxs-lookup"><span data-stu-id="042c3-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="042c3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="042c3-127">See also</span></span>



[<span data-ttu-id="042c3-128">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="042c3-128">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="042c3-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="042c3-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

