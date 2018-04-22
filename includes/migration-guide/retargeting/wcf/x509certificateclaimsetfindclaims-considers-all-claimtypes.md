### <a name="x509certificateclaimsetfindclaims-considers-all-claimtypes"></a>X509CertificateClaimSet.FindClaims учитывает все аргументы claimType

|   |   |
|---|---|
|Подробные сведения|Если в приложениях, предназначенных для .NET Framework 4.6.1, набор утверждений X509 инициализируется из сертификата, имеющего несколько записей DNS в поле SAN, метод <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> пытается сопоставить аргумент claimType со всеми записями DNS. В приложениях, предназначенных для предыдущих версий .NET Framework, метод <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> пытается сопоставить аргумент claimType только с последней записью DNS.|
|Предложение|Это изменение затрагивает только приложения, предназначенные для .NET Framework 4.6.1. Это изменение может быть отключено (или включено, если используются версии, предшествующие 4.6.1) с помощью параметра совместимости [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation).|
|Область|Дополнительный номер|
|Версия|4.6.1|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=nameWithType></li></ul>|

