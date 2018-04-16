### <a name="adonet-now-attempts-to-automatically-reconnect-broken-sql-connections"></a><span data-ttu-id="3c9ce-101">Теперь пытается автоматически подключиться прерванных соединений SQL ADO.NET</span><span class="sxs-lookup"><span data-stu-id="3c9ce-101">ADO.NET now attempts to automatically reconnect broken SQL connections</span></span>

|   |   |
|---|---|
|<span data-ttu-id="3c9ce-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="3c9ce-102">Details</span></span>|<span data-ttu-id="3c9ce-103">Начиная с .NET Framework 4.5.1, .NET Framework будет пытаться автоматически переподключаться прерванных соединений SQL.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-103">Beginning in the .NET Framework 4.5.1, the .NET Framework will attempt to automatically reconnect broken SQL connections.</span></span> <span data-ttu-id="3c9ce-104">Несмотря на то, что обычно станет приложений более надежным, существуют крайние случаи, в которых приложение должно быть известно, что соединение было потеряно, что может занять какое-либо действие после восстановления подключения.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-104">Although this will typically make apps more reliable, there are edge cases in which an app needs to know that the connection was lost so that it can take some action upon reconnection.</span></span>|
|<span data-ttu-id="3c9ce-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="3c9ce-105">Suggestion</span></span>|<span data-ttu-id="3c9ce-106">Если эта функция нежелательно из-за проблем совместимости, его можно отключить, задав <xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=name> свойстве строки соединения (или <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=name>) значение 0.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-106">If this feature is undesirable due to compatibility concerns, it can be disabled by setting the <xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=name> property of a connection string (or <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=name>) to 0.</span></span>|
|<span data-ttu-id="3c9ce-107">Область</span><span class="sxs-lookup"><span data-stu-id="3c9ce-107">Scope</span></span>|<span data-ttu-id="3c9ce-108">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="3c9ce-108">Edge</span></span>|
|<span data-ttu-id="3c9ce-109">Версия</span><span class="sxs-lookup"><span data-stu-id="3c9ce-109">Version</span></span>|<span data-ttu-id="3c9ce-110">4.5.1</span><span class="sxs-lookup"><span data-stu-id="3c9ce-110">4.5.1</span></span>|
|<span data-ttu-id="3c9ce-111">Тип</span><span class="sxs-lookup"><span data-stu-id="3c9ce-111">Type</span></span>|<span data-ttu-id="3c9ce-112">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="3c9ce-112">Runtime</span></span>|
|<span data-ttu-id="3c9ce-113">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="3c9ce-113">Affected APIs</span></span>|<ul><li><xref:System.Data.IDbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Configuration.ConnectionStringSettings.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor(System.Boolean)?displayProperty=nameWithType></li></ul>|
