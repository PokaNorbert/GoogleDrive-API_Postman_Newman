Microsoft Windows [Version 10.0.22000.2538]
(c) Microsoft Corporation. All rights reserved.

C:\WINDOWS\system32>cd C:\Users\Szabo\Desktop\Postman_testof

C:\Users\Szabo\Desktop\Postman_testof>run newman JPGFilesinGoogleDrive.postman_collection.json
'run' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Szabo\Desktop\Postman_testof>newman run JPGFilesinGoogleDrive.postman_collection.json
(node:24536) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
(Use `node --trace-deprecation ...` to show where the warning was created)
newman

JPGFilesinGoogleDrive

→ Get-Token
  GET https://www.googleapis.com/drive/v3/files [403 Forbidden, 628B, 305ms]
  1. Response status code is 200
  2. Response has the required fields
  3. Files array should exist and be an array
  4. Each file in the files array has the required fields
  √  Content-Type is application/json
  √  Response time is less than 500ms
  5. Response status code is 200
  6. Validate response schema
  7. NextPageToken, Kind, and IncompleteSearch are present in the response
  8. Each file in the 'files' array has the required fields

→ Simple-upload-file-binary
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=media [401 Unauthorized, 1.28kB, 310ms]
  9. Response status code is 200
  √  Content type is application/json
 10. Response has the required fields - kind, id, name, and mimeType
 11. Id is a non-empty string
 12. Name is a non-empty string
 13. Response time is less than 200ms
 14. Response status code is 200
 15. Validate the schema of the response
 16. Kind is a non-empty string
 17. MimeType is a non-empty string
 18. Response time is less than 200ms
 19. Response status code is 200
 20. Validate the schema of the response
 21. Kind is a non-empty string
 22. Mimetype is a non-empty string

→ Simple-upload-file-formdata
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=media  (node:24536) [DEP0044] DeprecationWarning: The `util.isArray` API is deprecated. Please use `Array.isArray()` instead.
[401 Unauthorized, 1.28kB, 703ms]
 23. Response status code is 200
 24. Response has the required fields
 25. Id is a non-empty string
 26. Name must be a non-empty string
 27. MimeType is in a valid format
 28. Response status code is 200
  √  Content-Type header is application/json
 29. Response has the required fields
  √  ID is in a valid format
 30. Name is a non-empty string

→ Multipart-upload-file-JSON
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=multipart [401 Unauthorized, 1.28kB, 187ms]
 31. Response status code is 200
 32. Response has the required fields - kind, id, name, and mimeType
 33. Id is a non-empty string
 34. Name is a non-empty string
 35. Mimetype is a non-empty string
 36. Response status code is 200
 37. Response has the required fields - kind, id, name, and mimeType
 38. Id is a non-empty string
  √  Content-Type header is application/json
 39. Name is a non-empty string
  √  Response time is less than 200ms
 40. Response status code is 200
 41. Validate the response schema for required fields
 42. Kind is a non-empty string
 43. MimeType is a non-empty string

→ Multipart-upload-file-formdataJS-withoutPNG
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=multipart [401 Unauthorized, 1.28kB, 200ms]
 44. Response status code is 200
 45. Content-Type header is application/json
 46. Response has the required fields - kind, id, name, and mimeType
 47. Id is a non-empty string
 48. Name is a non-empty string
 49. Response status code is 200
 50. Response has the required fields - kind, id, name, and mimeType
 51. Id is a non-empty string
 52. Name is a non-empty string
 53. Mimetype should be a non-empty string

→ Multipart-upload-file-formdataJS-withPNG
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=multipart [401 Unauthorized, 1.28kB, 261ms]
  √  Response Content-Type is application/json
 54. Response has the required fields
 55. Id is a non-empty string
 56. Name is a non-empty string
 57. MimeType is a non-empty string
 58. Response status code is 200
  √  Content-Type header is application/json
 59. Response has the required fields - kind, id, name, and mimeType
 60. Id is a non-empty string
 61. Name should be a non-empty string
 62. Response status code is 200
  √  Response Content-Type is application/json
 63. Response has the required fields
 64. Id is a non-empty string
 65. Name is a non-empty string

→ Resumable-JSON
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=resumable [401 Unauthorized, 1.31kB, 169ms]
 66. Response status code is 200
 67. Validate the schema of the response
  √  Response time is less than 200ms

→ Resumable-upload-file-binary
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=resumable&access_token=ya29.a0AXooCgs2tS9Hz0rggTjnb9PrliXdqOuCz7NM-6264CUD5QtFgBTLlQJY_IGV8u-yi7aUyArdgHcTq4Rin7l9di9449SYMo-2OoEl3DRuF4KWRAWTwiIqFx4U_tuo5U0hcMAtpiCdZlt1pr6ZE9BgdbbVm5EtIxwwsagWlbXvaCgYKAQ8SARISFQHGX2MicEaQIqRdTmp3PPfX8IbUSg0175&upload_id=ABPtcPp2EoD9L5aSqAxP4GWUwKmQrJ6Jg4erArV6iADiuALS174e07s_hHLV5MS2ET3yQfntMcTXKoQ0ZD1dTT-A0wSSFvjQqC5gX6sH0nRiLoAhhg&session_crd=AHSoBRXeb0I_5ckuZ0H7TTCibJpUf8MwRQ4pKAswTI_o24d7sRkCC1WQeTvK0R8h4oyR37tpzHVNO8LOgUI [200 OK, 732B, 1880ms]
  √  Response has the required fields
  √  ID is a non-empty string
  √  Name is in a valid format
  √  MimeType is a non-empty string
  √  Response Content-Type header is application/json

→ Delete-file
  DELETE https://www.googleapis.com/drive/v3/files/1vK_7iAUNbzFf4ReDoW9yJI7ZDo_hv4oq [401 Unauthorized, 1.23kB, 172ms]

┌─────────────────────────┬─────────────────────┬─────────────────────┐
│                         │            executed │              failed │
├─────────────────────────┼─────────────────────┼─────────────────────┤
│              iterations │                   1 │                   0 │
├─────────────────────────┼─────────────────────┼─────────────────────┤
│                requests │                   9 │                   0 │
├─────────────────────────┼─────────────────────┼─────────────────────┤
│            test-scripts │                   8 │                   0 │
├─────────────────────────┼─────────────────────┼─────────────────────┤
│      prerequest-scripts │                   0 │                   0 │
├─────────────────────────┼─────────────────────┼─────────────────────┤
│              assertions │                  83 │                  67 │
├─────────────────────────┴─────────────────────┴─────────────────────┤
│ total run duration: 5s                                              │
├─────────────────────────────────────────────────────────────────────┤
│ total data received: 6.2kB (approx)                                 │
├─────────────────────────────────────────────────────────────────────┤
│ average response time: 465ms [min: 169ms, max: 1880ms, s.d.: 523ms] │
└─────────────────────────────────────────────────────────────────────┘

   #  failure                detail

 01.  AssertionError         Response status code is 200
                             expected 403 to equal 200
                             at assertion:0 in test-script
                             inside "Get-Token"

 02.  AssertionError         Response has the required fields
                             expected { error: { code: 403, …(3) } } to have property 'nextPageToken'
                             at assertion:1 in test-script
                             inside "Get-Token"

 03.  AssertionError         Files array should exist and be an array
                             expected undefined to exist
                             at assertion:2 in test-script
                             inside "Get-Token"

 04.  AssertionError         Each file in the files array has the required fields
                             expected undefined to be an array
                             at assertion:3 in test-script
                             inside "Get-Token"

 05.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 403
                             at assertion:6 in test-script
                             inside "Get-Token"

 06.  AssertionError         Validate response schema
                             expected { error: { code: 403, …(3) } } to have property 'nextPageToken'
                             at assertion:7 in test-script
                             inside "Get-Token"

 07.  AssertionError         NextPageToken, Kind, and IncompleteSearch are present in the response
                             expected { error: { code: 403, …(3) } } to contain keys 'nextPageToken', 'kind', and
                             'incompleteSearch'
                             at assertion:8 in test-script
                             inside "Get-Token"

 08.  AssertionError         Each file in the 'files' array has the required fields
                             expected undefined to be an array
                             at assertion:9 in test-script
                             inside "Get-Token"

 09.  AssertionError         Response status code is 200
                             expected 401 to equal 200
                             at assertion:0 in test-script
                             inside "Simple-upload-file-binary"

 10.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:2 in test-script
                             inside "Simple-upload-file-binary"

 11.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:3 in test-script
                             inside "Simple-upload-file-binary"

 12.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:4 in test-script
                             inside "Simple-upload-file-binary"

 13.  AssertionError         Response time is less than 200ms
                             expected 310 to be below 200
                             at assertion:5 in test-script
                             inside "Simple-upload-file-binary"

 14.  AssertionError         Response status code is 200
                             expected 401 to equal 200
                             at assertion:6 in test-script
                             inside "Simple-upload-file-binary"

 15.  AssertionError         Validate the schema of the response
                             expected undefined to be a string
                             at assertion:7 in test-script
                             inside "Simple-upload-file-binary"

 16.  AssertionError         Kind is a non-empty string
                             expected undefined to be a string
                             at assertion:8 in test-script
                             inside "Simple-upload-file-binary"

 17.  AssertionError         MimeType is a non-empty string
                             expected undefined to be a string
                             at assertion:9 in test-script
                             inside "Simple-upload-file-binary"

 18.  AssertionError         Response time is less than 200ms
                             expected 310 to be below 200
                             at assertion:10 in test-script
                             inside "Simple-upload-file-binary"

 19.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:11 in test-script
                             inside "Simple-upload-file-binary"

 20.  AssertionError         Validate the schema of the response
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:12 in test-script
                             inside "Simple-upload-file-binary"

 21.  AssertionError         Kind is a non-empty string
                             expected undefined to be a string
                             at assertion:13 in test-script
                             inside "Simple-upload-file-binary"

 22.  AssertionError         Mimetype is a non-empty string
                             expected undefined to be a string
                             at assertion:14 in test-script
                             inside "Simple-upload-file-binary"

 23.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:0 in test-script
                             inside "Simple-upload-file-formdata"

 24.  AssertionError         Response has the required fields
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:1 in test-script
                             inside "Simple-upload-file-formdata"

 25.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:2 in test-script
                             inside "Simple-upload-file-formdata"

 26.  AssertionError         Name must be a non-empty string
                             expected undefined to be a string
                             at assertion:3 in test-script
                             inside "Simple-upload-file-formdata"

 27.  AssertionError         MimeType is in a valid format
                             expected undefined to be a string
                             at assertion:4 in test-script
                             inside "Simple-upload-file-formdata"

 28.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:5 in test-script
                             inside "Simple-upload-file-formdata"

 29.  AssertionError         Response has the required fields
                             expected { error: { code: 401, …(4) } } to contain keys 'kind', 'id', 'name', and
                             'mimeType'
                             at assertion:7 in test-script
                             inside "Simple-upload-file-formdata"

 30.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:9 in test-script
                             inside "Simple-upload-file-formdata"

 31.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:0 in test-script
                             inside "Multipart-upload-file-JSON"

 32.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected { error: { code: 401, …(4) } } to contain keys 'kind', 'id', 'name', and
                             'mimeType'
                             at assertion:1 in test-script
                             inside "Multipart-upload-file-JSON"

 33.  AssertionError         Id is a non-empty string
                             expected { error: { code: 401, …(4) } } to have property 'id'
                             at assertion:2 in test-script
                             inside "Multipart-upload-file-JSON"

 34.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:3 in test-script
                             inside "Multipart-upload-file-JSON"

 35.  AssertionError         Mimetype is a non-empty string
                             expected undefined to be a string
                             at assertion:4 in test-script
                             inside "Multipart-upload-file-JSON"

 36.  AssertionError         Response status code is 200
                             expected 401 to equal 200
                             at assertion:5 in test-script
                             inside "Multipart-upload-file-JSON"

 37.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:6 in test-script
                             inside "Multipart-upload-file-JSON"

 38.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:7 in test-script
                             inside "Multipart-upload-file-JSON"

 39.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:9 in test-script
                             inside "Multipart-upload-file-JSON"

 40.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:11 in test-script
                             inside "Multipart-upload-file-JSON"

 41.  AssertionError         Validate the response schema for required fields
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:12 in test-script
                             inside "Multipart-upload-file-JSON"

 42.  AssertionError         Kind is a non-empty string
                             expected undefined to be a string
                             at assertion:13 in test-script
                             inside "Multipart-upload-file-JSON"

 43.  AssertionError         MimeType is a non-empty string
                             expected undefined to be a string
                             at assertion:14 in test-script
                             inside "Multipart-upload-file-JSON"

 44.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:0 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutPNG"

 45.  AssertionError         Content-Type header is application/json
                             expected 'application/json; charset=UTF-8' to equal 'application/json'
                             at assertion:1 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutPNG"

 46.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected undefined to exist
                             at assertion:2 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutPNG"

 47.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:3 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutPNG"

 48.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:4 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutPNG"

 49.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:5 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutPNG"

 50.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:6 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutPNG"

 51.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:7 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutPNG"

 52.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:8 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutPNG"

 53.  AssertionError         Mimetype should be a non-empty string
                             expected undefined to be a string
                             at assertion:9 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutPNG"

 54.  AssertionError         Response has the required fields
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:1 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 55.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:2 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 56.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:3 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 57.  AssertionError         MimeType is a non-empty string
                             expected undefined to be a string
                             at assertion:4 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 58.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:5 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 59.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:7 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 60.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:8 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 61.  AssertionError         Name should be a non-empty string
                             expected undefined to be a string
                             at assertion:9 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 62.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:10 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 63.  AssertionError         Response has the required fields
                             expected { error: { code: 401, …(4) } } to contain keys 'kind', 'id', 'name', and
                             'mimeType'
                             at assertion:12 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 64.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:13 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 65.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:14 in test-script
                             inside "Multipart-upload-file-formdataJS-withPNG"

 66.  AssertionError         Response status code is 200
                             expected 401 to equal 200
                             at assertion:0 in test-script
                             inside "Resumable-JSON"

 67.  AssertionError         Validate the schema of the response
                             expected { error: { code: 401, …(4) } } to have property 'fileId'
                             at assertion:1 in test-script
                             inside "Resumable-JSON"
