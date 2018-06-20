---
title: Überprüfen eines Zertifikats für die EWS Managed API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1fe0b215-8340-4bc8-a6ce-4f591ca9e353
description: Informationen Sie zum Erstellen und verweisen auf ein Zertifikat Validierung Rückrufmethode, damit Sie EWS Managed API-Anforderungen für einen Exchange-Server machen können.
ms.openlocfilehash: 13d7c51e55308b9e9997697a075c8a9e6b4f10d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757009"
---
# <a name="validate-a-server-certificate-for-the-ews-managed-api"></a>Überprüfen eines Zertifikats für die EWS Managed API

Informationen Sie zum Erstellen und verweisen auf ein Zertifikat Validierung Rückrufmethode, damit Sie EWS Managed API-Anforderungen für einen Exchange-Server machen können.
  
Standardmäßig verwendet Exchange beginnend mit Exchange 2007 SP1-Versionen selbstsignierten X509 Zertifikate, um Anrufe von EWS zu authentifizieren. Wenn Sie die EWS Managed API verwenden, müssen Sie eine Rückrufmethode des Zertifikat-Validierung erstellen. Andernfalls werden EWS Managed API Anforderungen fehl. Wenn Sie den AutoErmittlungsdienst verwenden, wird der Anruf an die EWS Managed API AutoErmittlung-Methode ein **AutodiscoverLocalException** Fehler auftreten. Wenn Sie einen Web generierte Webdienstproxy verwenden, Sie auch möglicherweise erstellen eine Rückrufmethode Validierung abhängig davon, wie der Proxy erstellt wird. 
  
## <a name="prerequisites-for-creating-a-validation-callback-method"></a>Voraussetzungen für das Erstellen einer Rückrufmethode Validierung
<a name="bk_prereq"> </a>

Zum Einrichten ein Serverzertifikats überprüfen, stellen Sie sicher, dass Folgendes zutrifft: 
  
- Der Exchange-Server ist ein selbstsigniertes Zertifikat für EWS geeignet. Wenn der Administrator ein gültiges Zertifikat, das aufzeichnet, ein Stammzertifikat installiert hat, müssen Sie keine Rückrufmethode Validierung erstellen. 
    
- Sie erstellen eine verwaltete Anwendung, die einen Verweis auf die folgenden erforderlichen .NET Framework-Namespaces enthält: 
    
  - **System.Net**
  - **System.Net.Security**  
  - **System.Security.Cryptography.X509Certificates**
    
## <a name="example-callback-method-to-validate-a-server-certificate-for-the-ews-managed-api"></a>Beispiel: Rückrufmethode zum Überprüfen eines Serverzertifikats für die EWS Managed API
<a name="bk_example"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie ein X509 erstellen Validierung Rückrufmethode für die EWS Managed API-Zertifikats. Diese Methode wird ein X509 überprüfen Zertifikat und nur true zurück, wenn eine der folgenden Kriterien erfüllt sind: 
  
- Das Zertifikat ist gültig und wieder zu einem gültigen Stammzertifikat verfolgt.    
- Das Zertifikat ist gültig und selbstsigniert vom Server, der es zurückgegeben. 
    
> [!IMPORTANT]
> Die Zertifikat Überprüfung Rückrufmethode in diesem Beispiel bietet ausreichend Sicherheit für entwickeln und Testen von EWS Managed API-Anwendungen. Jedoch könnte es bietet keine ausreichende Sicherheit für die Anwendung bereitgestellt. Sie sollten sicherstellen, dass die Rückrufmethode Zertifikat Überprüfung, mit denen Sie die Sicherheit Ihrer Organisation erfüllt. 
  
```cs
      private static bool CertificateValidationCallBack(
         object sender,
         System.Security.Cryptography.X509Certificates.X509Certificate certificate,
         System.Security.Cryptography.X509Certificates.X509Chain chain,
         System.Net.Security.SslPolicyErrors sslPolicyErrors)
    {
      // If the certificate is a valid, signed certificate, return true.
      if (sslPolicyErrors == System.Net.Security.SslPolicyErrors.None)
      {
        return true;
      }
      // If there are errors in the certificate chain, look at each error to determine the cause.
      if ((sslPolicyErrors &amp; System.Net.Security.SslPolicyErrors.RemoteCertificateChainErrors) != 0)
      {
        if (chain != null &amp;&amp; chain.ChainStatus != null)
        {
          foreach (System.Security.Cryptography.X509Certificates.X509ChainStatus status in chain.ChainStatus)
          {
            if ((certificate.Subject == certificate.Issuer) &amp;&amp;
               (status.Status == System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.UntrustedRoot))
            {
              // Self-signed certificates with an untrusted root are valid. 
              continue;
            }
            else
            {
              if (status.Status != System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.NoError)
              {
                // If there are any other errors in the certificate chain, the certificate is invalid,
             // so the method returns false.
                return false;
              }
            }
          }
        }
        // When processing reaches this line, the only errors in the certificate chain are 
    // untrusted root errors for self-signed certificates. These certificates are valid
    // for default Exchange server installations, so return true.
        return true;
      }
      else
      {
     // In all other cases, return false.
        return false;
      }
    }

```

Verwenden Sie die **ServicePointManager** -Klasse in .NET **System.Net** -Namespace, verknüpfen Sie eine Rückrufmethode Überprüfung durch Festlegen der **ServerCertificateValidationCallback** -Eigenschaft. Ähnlichen Code wie im folgenden Codebeispiel können Sie die **ServerCertificateValidationCallback** -Eigenschaft festgelegt. 
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## <a name="next-steps"></a>Nächste Schritte
<a name="bk_example"> </a>

Nachdem Sie die Validation-Rückrufmethode für die EWS Managed API erstellt haben, können Sie den AutoErmittlungsdienst verwenden, Verbindungspunkte sowie Benutzer- und domäneneinstellungen aus einem Exchange-Server abgerufen. Weitere Informationen finden Sie unter den folgenden Artikeln:
  
- [Mithilfe von AutoErmittlung Verbindungspunkte suchen](how-to-use-autodiscover-to-find-connection-points.md)
    
- [Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [Abrufen von domäneneinstellungen aus einem Exchange-server](how-to-get-domain-settings-from-an-exchange-server.md)
    
## <a name="see-also"></a>Siehe auch

- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)  
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    

