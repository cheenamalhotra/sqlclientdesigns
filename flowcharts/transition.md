# Package/Class/API transition from MDS (.NET Core) to SqlClientX class design

| Package Name | Class Name | Method / API | New Package | New Class Name | New Method / API |
| --- | --- | --- | --- | --- | --- |
| Microsoft.Data.SqlClient.SNI | ConcurrentQueueSemaphore | * | <span style="color:green">Microsoft.Data.SqlClientX.Net.Types</span> | ConcurrentQueueSemaphore | * |
| Microsoft.Data.SqlClient.SNI | LocalDb (Windows) | * |  |  | * |
| Microsoft.Data.SqlClient.SNI | SNICommon | SNIAsyncCallback | <span style="color:green">Microsoft.Data.SqlClientX.Net.Helpers</span> | <span style="color:green">Common</span> | <span style="color:green">TdsAsyncCallback</span> |
| Microsoft.Data.SqlClient.SNI | SNICommon.SNIProviders | * | <span style="color:green">Microsoft.Data.SqlClientX.Net.Types</span> | <span style="color:green">Providers</span> | * |
| Microsoft.Data.SqlClient.SNI | SNICommon.SNISMUXHeader | * | <span style="color:green">Microsoft.Data.SqlClientX.Net.Types</span> | <span style="color:green">SmuxHeader</span> | * |
| Microsoft.Data.SqlClient.SNI | SNICommon.SNISMUXFlags | * | <span style="color:green">Microsoft.Data.SqlClientX.Net.Types</span> | <span style="color:green">SmuxFlags</span> | * |
| Microsoft.Data.SqlClient.SNI | SNICommon | ValidateSslServerCertificate | <span style="color:green">Microsoft.Data.SqlClientX.Net.Helpers</span> | <span style="color:green">Util</span> | ValidateSslServerCertificate |
|  |  | GetDnsIpAddresses | <span style="color:green">Microsoft.Data.SqlClientX.Net.Helpers</span> | <span style="color:green">Util</span> | GetDnsIpAddressesAsync <span style="color:red">*</span> |
|  |  | ReportSNIError | <span style="color:green">Microsoft.Data.SqlClientX.Net.Helpers</span> | <span style="color:green">Util</span> | ReportSNIError |
| Microsoft.Data.SqlClient.SNI | SNIProxy | CreateConnectionHandle | <span style="color:green">Microsoft.Data.SqlClientX.Net.Helpers</span> | <span style="color:green">Util</span> | <span style="color:green">CreateMessenger</span> |
|  |  | GetLastError | <span style="color:green">Microsoft.Data.SqlClientX.Net.Helpers</span> | <span style="color:green">Util</span> | GetLastError |
| Microsoft.Data.SqlClient.SNI | SNIError | * | <span style="color:green">Microsoft.Data.SqlClientX.Net.Types</span> | <span style="color:green">SqlNetworkError</span> | * |
| Microsoft.Data.SqlClient.SNI | SNIPacket | * | <span style="color:green">Microsoft.Data.SqlClientX.Net.Types</span> | <span style="color:green">Packet</span> | * |
| Microsoft.Data.SqlClient.SNI | SNIHandle | AuthenticateAsClientAsync | <span style="color:green">Microsoft.Data.SqlClientX.Net</span> | <span style="color:green">AuthenticateAsClientAsync</span> | * |
|  |  | Dispose | <span style="color:green">Microsoft.Data.SqlClientX.Net</span> | <span style="color:green">Packet</span> | * |
