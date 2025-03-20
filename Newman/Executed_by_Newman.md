Microsoft Windows [Version 10.0.22000.2538]
(c) Microsoft Corporation. All rights reserved.

C:\WINDOWS\system32>cd C:\Users\Szabo\Desktop\Postman_testof

C:\Users\Szabo\Desktop\Postman_testof>newman run MP3FilesinGoogleDrive.postman_collection.json -e workspace.postman_globals.json
(node:28040) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
(Use `node --trace-deprecation ...` to show where the warning was created)
newman

MP3 Files in Google Drive

→ Get-Token
  GET https://www.googleapis.com/drive/v3/files [403 Forbidden, 628B, 300ms]
  1. Response status code is 200
  2. Response has the required fields
  3. Validate the files array and its elements
  4. Mimetype is in a valid format
  5. Name field in the files array is a non-empty string
  6. Response time is less than 200ms
  7. Response body schema validation
  8. Response status code is 200
  9. Response time is less than 200ms
 10. Response body schema validation
 11. Response status code is 200

→ Simple-upload-file-binary
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=media [401 Unauthorized, 1.28kB, 2.8s]
  √  Response Content-Type is application/json
 12. Kind field exists in the response
 13. Id field in the response should exist
 14. Name field in the response should exist
 15. MIME type field exists and is not empty
 16. Response status code is 200
 17. Response time is less than 500ms
 18. Response schema validation for kind, id, name, and mimeType

→ Simple-upload-file-formdata
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=media  (node:28040) [DEP0044] DeprecationWarning: The `util.isArray` API is deprecated. Please use `Array.isArray()` instead.
[401 Unauthorized, 1.28kB, 2.4s]
 19. Response status code is 200
  √  Response Content-Type is application/json
 20. Response has the required fields
 21. Id must be a non-empty string
 22. MimeType is a valid MIME type

→ Multipart-upload-file-JSON
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=multipart [401 Unauthorized, 1.28kB, 163ms]
 23. Response status code is 200
 24. Response has the required fields - kind, id, name, and mimeType
 25. Id is a non-empty string
  √  Content-Type header is set to application/json
 26. Name should be a non-empty string

→ Multipart-upload-file-formdataJS-withoutMP3
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=multipart [401 Unauthorized, 1.28kB, 196ms]
 27. Response status code is 200
  √  Response content type is application/json
 28. Response has the required fields - kind, id, name, and mimeType
 29. Id is a non-empty string
 30. Name is a non-empty string

→ Multipart-upload-file-formdataJS-withMP3
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=multipart [401 Unauthorized, 1.28kB, 2.1s]
 31. Response status code is 200
  √  Response content type is application/json
 32. Response has the required fields
 33. ID is a non-empty string
 34. MimeType is a valid MIME type

→ Resumable-JSON
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=resumable [401 Unauthorized, 1.31kB, 228ms]
 35. Response status code is 200
  √  Response time is within an acceptable range
 36. Validate the schema of the response body

→ Resumable-upload-file-binary
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=resumable&access_token=ya29.a0AXooCgsaq_DSfSF4ZOWhDMyTFIKNbB4a6nrylYRU2H1AVthwZAyNNA4rfUCdW9Z7yiytrD1DTztGwKL2oA-PElwAoO0J40SXG-4g_Q4n-FIOxSGtOAjjx-GZNCXugUj4L30HXqmoEzMaPXmWNxR5nKuRyugX5P6q4FEaCgYKATsSARISFQHGX2MiE1D3JwV944YPO5LtlY9RjA0170&upload_id=ABPtcPof5Cqt6eDFeoiNSFVGV7P5agGjsBf1xPvsY8mledlknrje0Yt3tGHRXpaZi9LI_8ujdn_B-ZI7iOxjCmiaM4fVrRHHmqonVYy9ykeGhXqG2Q&session_crd=AHSoBRVk92lehdkkoivRMvaBd8gh9D4m3r-UnjD6vmvINnKlCywD3XBBFf-KDfy5w8mVRdAZKyFZR_l8QAI [200 OK, 741B, 2.1s]
  √  Response status code is 200
  √  Response has the required fields - kind, id, name, and mimeType
  √  ID is a non-empty string
  √  Name is a non-empty string
  √  MimeType is a valid MIME type format

→ Delete-file
  DELETE https://www.googleapis.com/drive/v3/files/1hlkMh-EQ_iQOxozgNZoHgwrcZ3L54abH [401 Unauthorized, 1.23kB, 149ms]

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
│              assertions │                  47 │                  36 │
├─────────────────────────┴─────────────────────┴─────────────────────┤
│ total run duration: 11.5s                                           │
├─────────────────────────────────────────────────────────────────────┤
│ total data received: 6.21kB (approx)                                │
├─────────────────────────────────────────────────────────────────────┤
│ average response time: 1185ms [min: 149ms, max: 2.8s, s.d.: 1108ms] │
└─────────────────────────────────────────────────────────────────────┘

   #  failure                   detail

 01.  AssertionError            Response status code is 200
                                expected 403 to equal 200
                                at assertion:0 in test-script
                                inside "Get-Token"

 02.  AssertionError            Response has the required fields
                                expected { error: { code: 403, …(3) } } to have property 'nextPageToken'
                                at assertion:1 in test-script
                                inside "Get-Token"

 03.  AssertionError            Validate the files array and its elements
                                expected undefined to be an array
                                at assertion:2 in test-script
                                inside "Get-Token"

 04.  AssertionError            Mimetype is in a valid format
                                expected undefined to be an array
                                at assertion:3 in test-script
                                inside "Get-Token"

 05.  AssertionError            Name field in the files array is a non-empty string
                                expected undefined to be an array
                                at assertion:4 in test-script
                                inside "Get-Token"

 06.  AssertionError            Response time is less than 200ms
                                expected 300 to be below 200
                                at assertion:5 in test-script
                                inside "Get-Token"

 07.  AssertionError            Response body schema validation
                                expected { error: { code: 403, …(3) } } to have property 'nextPageToken'
                                at assertion:6 in test-script
                                inside "Get-Token"

 08.  AssertionError            Response status code is 200
                                expected response to have status code 200 but got 403
                                at assertion:7 in test-script
                                inside "Get-Token"

 09.  AssertionError            Response time is less than 200ms
                                expected 300 to be below 200
                                at assertion:8 in test-script
                                inside "Get-Token"

 10.  AssertionError            Response body schema validation
                                expected { error: { code: 403, …(3) } } to have property 'nextPageToken'
                                at assertion:9 in test-script
                                inside "Get-Token"

 11.  AssertionError            Response status code is 200
                                expected 403 to equal 200
                                at assertion:10 in test-script
                                inside "Get-Token"

 12.  AssertionError            Kind field exists in the response
                                expected undefined to exist
                                at assertion:1 in test-script
                                inside "Simple-upload-file-binary"

 13.  AssertionError            Id field in the response should exist
                                expected undefined to exist
                                at assertion:2 in test-script
                                inside "Simple-upload-file-binary"

 14.  AssertionError            Name field in the response should exist
                                expected undefined to exist
                                at assertion:3 in test-script
                                inside "Simple-upload-file-binary"

 15.  AssertionError            MIME type field exists and is not empty
                                expected undefined to exist
                                at assertion:4 in test-script
                                inside "Simple-upload-file-binary"

 16.  AssertionError            Response status code is 200
                                expected 401 to equal 200
                                at assertion:5 in test-script
                                inside "Simple-upload-file-binary"

 17.  AssertionError            Response time is less than 500ms
                                expected 2835 to be below 500
                                at assertion:6 in test-script
                                inside "Simple-upload-file-binary"

 18.  AssertionError            Response schema validation for kind, id, name, and mimeType
                                expected { error: { code: 401, …(4) } } to have property 'kind'
                                at assertion:7 in test-script
                                inside "Simple-upload-file-binary"

 19.  AssertionError            Response status code is 200
                                expected 401 to equal 200
                                at assertion:0 in test-script
                                inside "Simple-upload-file-formdata"

 20.  AssertionError            Response has the required fields
                                expected { error: { code: 401, …(4) } } to have property 'kind'
                                at assertion:2 in test-script
                                inside "Simple-upload-file-formdata"

 21.  AssertionError            Id must be a non-empty string
                                expected undefined to be a string
                                at assertion:3 in test-script
                                inside "Simple-upload-file-formdata"

 22.  AssertionError            MimeType is a valid MIME type
                                expected undefined to match /^[-\w]+\/[-\w\+]+$/
                                at assertion:4 in test-script
                                inside "Simple-upload-file-formdata"

 23.  AssertionError            Response status code is 200
                                expected 401 to equal 200
                                at assertion:0 in test-script
                                inside "Multipart-upload-file-JSON"

 24.  AssertionError            Response has the required fields - kind, id, name, and mimeType
                                expected { error: { code: 401, …(4) } } to have property 'kind'
                                at assertion:1 in test-script
                                inside "Multipart-upload-file-JSON"

 25.  AssertionError            Id is a non-empty string
                                expected undefined to be a string
                                at assertion:2 in test-script
                                inside "Multipart-upload-file-JSON"

 26.  AssertionError            Name should be a non-empty string
                                expected undefined to be a string
                                at assertion:4 in test-script
                                inside "Multipart-upload-file-JSON"

 27.  AssertionError            Response status code is 200
                                expected response to have status code 200 but got 401
                                at assertion:0 in test-script
                                inside "Multipart-upload-file-formdataJS-withoutMP3"

 28.  AssertionError            Response has the required fields - kind, id, name, and mimeType
                                expected { error: { code: 401, …(4) } } to contain keys 'kind', 'id', 'name', and 'mimeType'
                                at assertion:2 in test-script
                                inside "Multipart-upload-file-formdataJS-withoutMP3"

 29.  AssertionError            Id is a non-empty string
                                expected undefined to be a string
                                at assertion:3 in test-script
                                inside "Multipart-upload-file-formdataJS-withoutMP3"

 30.  AssertionError            Name is a non-empty string
                                expected undefined to be a string
                                at assertion:4 in test-script
                                inside "Multipart-upload-file-formdataJS-withoutMP3"

 31.  AssertionError            Response status code is 200
                                expected 401 to equal 200
                                at assertion:0 in test-script
                                inside "Multipart-upload-file-formdataJS-withMP3"

 32.  AssertionError            Response has the required fields
                                expected { error: { code: 401, …(4) } } to have property 'kind'
                                at assertion:2 in test-script
                                inside "Multipart-upload-file-formdataJS-withMP3"

 33.  AssertionError            ID is a non-empty string
                                expected undefined to be a string
                                at assertion:3 in test-script
                                inside "Multipart-upload-file-formdataJS-withMP3"

 34.  AssertionError            MimeType is a valid MIME type
                                Invalid MIME type: expected undefined to match /^[a-z]+\/[a-z0-9\-\.\+]+$/i
                                at assertion:4 in test-script
                                inside "Multipart-upload-file-formdataJS-withMP3"

 35.  AssertionError            Response status code is 200
                                expected response to have status code 200 but got 401
                                at assertion:0 in test-script
                                inside "Resumable-JSON"

 36.  AssertionError            Validate the schema of the response body
                                expected { error: { code: 401, …(4) } } to have property 'id'
                                at assertion:2 in test-script
                                inside "Resumable-JSON"


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


C:\Users\Szabo\Desktop\Postman_testof>newman run DOCXFilesinGoogleDrive.postman_collection.json
(node:32328) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
(Use `node --trace-deprecation ...` to show where the warning was created)
newman

DOCX Files in Google Drive

→ Get-Token
  GET https://www.googleapis.com/drive/v3/files [403 Forbidden, 628B, 277ms]
  1. Response status code is 200
  2. Response has the required fields
  3. Files array should exist and be an array
  4. Each file in the files array has the required fields
  √  Content-Type is application/json

→ Simple-upload-file-binary
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=media [401 Unauthorized, 1.28kB, 381ms]
  5. Response status code is 200
  √  Content type is application/json
  6. Response has the required fields - kind, id, name, and mimeType
  7. Id is a non-empty string
  8. Name is a non-empty string

→ Simple-upload-file-formdata
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=media  (node:32328) [DEP0044] DeprecationWarning: The `util.isArray` API is deprecated. Please use `Array.isArray()` instead.
[401 Unauthorized, 1.28kB, 227ms]
  9. Response status code is 200
 10. Response has the required fields
 11. Id is a non-empty string
 12. Name must be a non-empty string
 13. MimeType is in a valid format
 14. Response status code is 200
  √  Content-Type header is application/json
 15. Response has the required fields
  √  ID is in a valid format
 16. Name is a non-empty string

→ Multipart-upload-file-JSON
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=multipart [401 Unauthorized, 1.28kB, 171ms]
 17. Response status code is 200
 18. Response has the required fields - kind, id, name, and mimeType
 19. Id is a non-empty string
 20. Name is a non-empty string
 21. Mimetype is a non-empty string
 22. Response status code is 200
 23. Response has the required fields - kind, id, name, and mimeType
 24. Id is a non-empty string
  √  Content-Type header is application/json
 25. Name is a non-empty string

→ Multipart-upload-file-formdataJS-withoutDOCX
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=multipart [401 Unauthorized, 1.28kB, 197ms]
 26. Response status code is 200
 27. Content-Type header is application/json
 28. Response has the required fields - kind, id, name, and mimeType
 29. Id is a non-empty string
 30. Name is a non-empty string
 31. Response status code is 200
 32. Response has the required fields - kind, id, name, and mimeType
 33. Id is a non-empty string
 34. Name is a non-empty string
 35. Mimetype should be a non-empty string

→ Multipart-upload-file-formdataJS-withDOCX
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=multipart [401 Unauthorized, 1.28kB, 243ms]
  √  Response Content-Type is application/json
 36. Response has the required fields
 37. Id is a non-empty string
 38. Name is a non-empty string
 39. MimeType is a non-empty string
 40. Response status code is 200
  √  Content-Type header is application/json
 41. Response has the required fields - kind, id, name, and mimeType
 42. Id is a non-empty string
 43. Name should be a non-empty string

→ Resumable-JSON
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=resumable [401 Unauthorized, 1.31kB, 183ms]

→ Resumable-upload-file-binary
  POST https://www.googleapis.com/upload/drive/v3/files?uploadType=resumable&access_token=ya29.a0AXooCgvoEYYilc2Cgp6eStJSgpATO_jcRF6ZKGavj25bVgo-Ocl6-_ro0Co3uXr1KGJPxQQxuiw-UNO99oxUjba-XzF0JMxKudlOlAwHpxZXu1wnovPaTGy4NcmkG-xWenwsxGDqDeZfm3T2qBmb9vF33gY3L6yokyV4EiYgaCgYKAVQSARISFQHGX2MiCGpf9My65YP4WXy7-8lpsQ0175&upload_id=ABPtcPoqzSh-3jhaRvrk4oUlVe_DL7AO-p4cyIFqFCbivDWMmF7-DpSEl5dNghiCIvJJN7OxEkp_z5cJhI8OML_AQCyJT4bDB-QY87YNcXWArZ0Gmw&session_crd=AHSoBRUg0caNpbxdO_5nJnAI35-c3_sPIpEiVHumQR8u0lxZgxkdm8xWaSyls_At99ckCGWyFmGfAg0cPgc [200 OK, 786B, 1187ms]
  √  Response has the required fields
  √  ID is a non-empty string
  √  Name is in a valid format
  √  MimeType is a non-empty string
  √  Response Content-Type header is application/json

→ Delete-file
  DELETE https://www.googleapis.com/drive/v3/files/1hlkMh-EQ_iQOxozgNZoHgwrcZ3L54abH [401 Unauthorized, 1.23kB, 144ms]

┌─────────────────────────┬─────────────────────┬─────────────────────┐
│                         │            executed │              failed │
├─────────────────────────┼─────────────────────┼─────────────────────┤
│              iterations │                   1 │                   0 │
├─────────────────────────┼─────────────────────┼─────────────────────┤
│                requests │                   9 │                   0 │
├─────────────────────────┼─────────────────────┼─────────────────────┤
│            test-scripts │                   7 │                   0 │
├─────────────────────────┼─────────────────────┼─────────────────────┤
│      prerequest-scripts │                   0 │                   0 │
├─────────────────────────┼─────────────────────┼─────────────────────┤
│              assertions │                  55 │                  43 │
├─────────────────────────┴─────────────────────┴─────────────────────┤
│ total run duration: 3.8s                                            │
├─────────────────────────────────────────────────────────────────────┤
│ total data received: 6.25kB (approx)                                │
├─────────────────────────────────────────────────────────────────────┤
│ average response time: 334ms [min: 144ms, max: 1187ms, s.d.: 308ms] │
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
                             expected 401 to equal 200
                             at assertion:0 in test-script
                             inside "Simple-upload-file-binary"

 06.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:2 in test-script
                             inside "Simple-upload-file-binary"

 07.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:3 in test-script
                             inside "Simple-upload-file-binary"

 08.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:4 in test-script
                             inside "Simple-upload-file-binary"

 09.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:0 in test-script
                             inside "Simple-upload-file-formdata"

 10.  AssertionError         Response has the required fields
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:1 in test-script
                             inside "Simple-upload-file-formdata"

 11.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:2 in test-script
                             inside "Simple-upload-file-formdata"

 12.  AssertionError         Name must be a non-empty string
                             expected undefined to be a string
                             at assertion:3 in test-script
                             inside "Simple-upload-file-formdata"

 13.  AssertionError         MimeType is in a valid format
                             expected undefined to be a string
                             at assertion:4 in test-script
                             inside "Simple-upload-file-formdata"

 14.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:5 in test-script
                             inside "Simple-upload-file-formdata"

 15.  AssertionError         Response has the required fields
                             expected { error: { code: 401, …(4) } } to contain keys 'kind', 'id', 'name', and
                             'mimeType'
                             at assertion:7 in test-script
                             inside "Simple-upload-file-formdata"

 16.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:9 in test-script
                             inside "Simple-upload-file-formdata"

 17.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:0 in test-script
                             inside "Multipart-upload-file-JSON"

 18.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected { error: { code: 401, …(4) } } to contain keys 'kind', 'id', 'name', and
                             'mimeType'
                             at assertion:1 in test-script
                             inside "Multipart-upload-file-JSON"

 19.  AssertionError         Id is a non-empty string
                             expected { error: { code: 401, …(4) } } to have property 'id'
                             at assertion:2 in test-script
                             inside "Multipart-upload-file-JSON"

 20.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:3 in test-script
                             inside "Multipart-upload-file-JSON"

 21.  AssertionError         Mimetype is a non-empty string
                             expected undefined to be a string
                             at assertion:4 in test-script
                             inside "Multipart-upload-file-JSON"

 22.  AssertionError         Response status code is 200
                             expected 401 to equal 200
                             at assertion:5 in test-script
                             inside "Multipart-upload-file-JSON"

 23.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:6 in test-script
                             inside "Multipart-upload-file-JSON"

 24.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:7 in test-script
                             inside "Multipart-upload-file-JSON"

 25.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:9 in test-script
                             inside "Multipart-upload-file-JSON"

 26.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:0 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutDOCX"

 27.  AssertionError         Content-Type header is application/json
                             expected 'application/json; charset=UTF-8' to equal 'application/json'
                             at assertion:1 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutDOCX"

 28.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected undefined to exist
                             at assertion:2 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutDOCX"

 29.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:3 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutDOCX"

 30.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:4 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutDOCX"

 31.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:5 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutDOCX"

 32.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:6 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutDOCX"

 33.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:7 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutDOCX"

 34.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:8 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutDOCX"

 35.  AssertionError         Mimetype should be a non-empty string
                             expected undefined to be a string
                             at assertion:9 in test-script
                             inside "Multipart-upload-file-formdataJS-withoutDOCX"

 36.  AssertionError         Response has the required fields
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:1 in test-script
                             inside "Multipart-upload-file-formdataJS-withDOCX"

 37.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:2 in test-script
                             inside "Multipart-upload-file-formdataJS-withDOCX"

 38.  AssertionError         Name is a non-empty string
                             expected undefined to be a string
                             at assertion:3 in test-script
                             inside "Multipart-upload-file-formdataJS-withDOCX"

 39.  AssertionError         MimeType is a non-empty string
                             expected undefined to be a string
                             at assertion:4 in test-script
                             inside "Multipart-upload-file-formdataJS-withDOCX"

 40.  AssertionError         Response status code is 200
                             expected response to have status code 200 but got 401
                             at assertion:5 in test-script
                             inside "Multipart-upload-file-formdataJS-withDOCX"

 41.  AssertionError         Response has the required fields - kind, id, name, and mimeType
                             expected { error: { code: 401, …(4) } } to have property 'kind'
                             at assertion:7 in test-script
                             inside "Multipart-upload-file-formdataJS-withDOCX"

 42.  AssertionError         Id is a non-empty string
                             expected undefined to be a string
                             at assertion:8 in test-script
                             inside "Multipart-upload-file-formdataJS-withDOCX"

 43.  AssertionError         Name should be a non-empty string
                             expected undefined to be a string
                             at assertion:9 in test-script
                             inside "Multipart-upload-file-formdataJS-withDOCX"
