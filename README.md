# Fix root CA store
QGIS on windows suffers from non-loading of root CA certificates that are in the OS trust list, but not downloaded to the local computers certificate store yet.

Calling windows' curl.exe on the server triggers an import of the root CA certificate, if it is in the OS trust list.

## References ##

https://superuser.com/questions/1919651/why-is-a-ca-certificate-harica-tls-rsa-root-ca-2021-listed-in-ccadb-not-in-win
https://github.com/qgis/QGIS/issues/51722
https://github.com/qgis/QGIS/issues/62782
